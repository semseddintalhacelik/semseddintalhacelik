```c
#include <stdio.h>
#include <stdbool.h>

typedef struct {
char name[30];
char title[40];
char department[50];
char skills[6][25];
bool isCurious;
bool lovesEmbedded;
bool drinksTea;
} Engineer;

int main() {
Engineer me = {"Şemseddin Talha Çelik", "Embedded Systems Developer", "Elektrik-Elektronik Mühendisliği",
{"C", "Arduino", "ESP32", "Raspberry Pi", "Gömülü Sistemler", "Otomasyon"},
true, true, true};

printf("👋 Merhaba, ben %s!\n", me.name);
printf("🏫 Bölüm: %s\n", me.department);
printf("🛠️ Unvan: %s\n\n", me.title);

printf("💻 Yetkinliklerim:\n");
for (int i = 0; i < 6; i++) {
printf(" - %s\n", me.skills[i]);
}

if (me.isCurious && me.lovesEmbedded) {
printf("🧠 Yeni teknolojilere meraklı, düşük seviyeli kod yazmayı seven biriyim.\n");
}

if (me.drinksTea) {
printf("🍵 Projeler çayla daha iyi gider.\n");
}

printf("📂 GitHub profilime göz at, kodları konuşalım!\n");

return 0;
}
