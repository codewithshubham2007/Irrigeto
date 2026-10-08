# Irrigeto
A software who tracks the water level and irrigation timing of a field

#include <stdio.h>

int main()
{
    int moisture;
    int pump = 0;

    printf("=== Smart Irrigation System ===\n");

    printf("Enter soil moisture/water level (0-100%%): ");
    scanf("%d", &moisture);

    if (moisture < 30)
    {
        pump = 1;
        printf("\nField is DRY.\n");
        printf("Water pump: ON\n");
        printf("Irrigation started.\n");
    }
    else if (moisture >= 30 && moisture <= 70)
    {
        pump = 1;
        printf("\nMoisture level is LOW/MEDIUM.\n");
        printf("Water pump: ON\n");
        printf("Irrigation continuing.\n");
    }
    else
    {
        pump = 0;
        printf("\nSufficient water/moisture detected.\n");
        printf("Water pump: OFF\n");
        printf("Irrigation stopped.\n");
    }

    return 0;
}