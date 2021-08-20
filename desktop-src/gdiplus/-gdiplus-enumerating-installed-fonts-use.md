---
description: Die InstalledFontCollection-Klasse erbt von der abstrakten FontCollection-Basisklasse.
ms.assetid: 59598f66-4241-4766-a2f0-5de736de959e
title: Auflisten der installierten Schriftarten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa54298cb7d177708d609e2ee011dd4da7173c726445b59b07a9c8e60ce786cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118067351"
---
# <a name="enumerating-installed-fonts"></a>Auflisten der installierten Schriftarten

Die [**InstalledFontCollection-Klasse erbt**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection) von der abstrakten [**FontCollection-Basisklasse.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) Sie können ein **InstalledFontCollection-Objekt** verwenden, um die auf dem Computer installierten Schriftarten aufzuzählen. Die [**FontCollection::GetFamilies-Methode**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) eines **InstalledFontCollection-Objekts** gibt ein Array von [**FontFamily-Objekten**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) zurück. Bevor Sie **FontCollection::GetFamilies** aufrufen, müssen Sie einen Puffer zuordnen, der groß genug ist, um dieses Array zu speichern. Um die Größe des erforderlichen Puffers zu bestimmen, rufen Sie die [**FontCollection::GetFamilyCount-Methode**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) auf, und multiplizieren Sie den Rückgabewert mit **sizeof**(**FontFamily**).

Im folgenden Beispiel werden die Namen aller auf dem Computer installierten Schriftfamilien aufgelistet. Der Code ruft die Namen der Schriftfamilien ab, indem die [**FontFamily::GetFamilyName-Methode**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getfamilyname) jedes [**FontFamily-Objekts**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) im Array aufgerufen wird, das von [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies)zurückgegeben wird. Wenn die Namen der Familie abgerufen werden, werden sie verkettet, um eine durch Trennzeichen getrennte Liste zu bilden. Anschließend zeichnet die [DrawString-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) der [**Graphics-Klasse**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) die durch Trennzeichen getrennte Liste in einem Rechteck.


```
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 8, FontStyleRegular, UnitPoint);
RectF        rectF(10.0f, 10.0f, 500.0f, 500.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 0));

INT          count = 0;
INT          found = 0;
WCHAR        familyName[LF_FACESIZE];  // enough space for one family name
WCHAR*       familyList = NULL;
FontFamily*  pFontFamily = NULL;

InstalledFontCollection installedFontCollection;

// How many font families are installed?
count = installedFontCollection.GetFamilyCount();

// Allocate a buffer to hold the array of FontFamily
// objects returned by GetFamilies.
pFontFamily = new FontFamily[count];

// Get the array of FontFamily objects.
installedFontCollection.GetFamilies(count, pFontFamily, &found);

// The loop below creates a large string that is a comma-separated
// list of all font family names.
// Allocate a buffer large enough to hold that string.
familyList = new WCHAR[count*(sizeof(familyName)+ 3)];
StringCchCopy(familyList, 1, L"");

for(INT j = 0; j < count; ++j)
{
   pFontFamily[j].GetFamilyName(familyName);  
   StringCchCatW(familyList, count*(sizeof(familyName)+ 3), familyName);
   StringCchCatW(familyList, count*(sizeof(familyName)+ 3), L",  ");
}

// Draw the large string (list of all families) in a rectangle.
graphics.DrawString(
   familyList, -1, &font, rectF, NULL, &solidBrush);

delete [] pFontFamily;
delete [] familyList;
            
```



Die folgende Abbildung zeigt eine mögliche Ausgabe des vorangehenden Codes. Wenn Sie den Code ausführen, kann die Ausgabe abhängig von den auf Ihrem Computer installierten Schriftarten unterschiedlich sein.

![Screenshot eines Fensters mit einer durch Trennzeichen getrennten Liste installierter Schriftfamilien](images/fontstext6.png)

 

 



