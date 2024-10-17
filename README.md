#include <stdio.h>

int main() {
    char username[50];
    char email[100];
    char password[50];
    char first_name[50];
    char last_name[50];
    printf("Enter username: ");
    scanf("%s", username);
    printf("Enter email: ");
    scanf("%s", email);
    printf("Enter password: ");
    scanf("%s", password);
    printf("Enter first name: ");
    scanf("%s", first_name);

   printf("Enter last name: ");
    scanf("%s", last_name);

   FILE *file = fopen("user_data.txt", "a");
    if (file == NULL) {
        printf("Error opening file!\n");
        return 1; 
    }

   fprintf(file, "Username: %s\n", username);
   fprintf(file, "Email: %s\n", email);
    fprintf(file, "Password: %s\n", password);
    fprintf(file, "First Name: %s\n", first_name);
    fprintf(file, "Last Name: %s\n", last_name);
    fprintf(file, "------------------------\n");

   fclose(file);

   printf("User data stored successfully!\n");

  return 0;
}
