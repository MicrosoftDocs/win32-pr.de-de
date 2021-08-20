---
description: Die PrivateFontCollection-Klasse erbt von der abstrakten FontCollection-Basisklasse. Sie können ein PrivateFontCollection-Objekt verwenden, um einen Satz von Schriftarten speziell für Ihre Anwendung zu verwalten.
ms.assetid: ae12afcf-12cc-4c84-9aba-de56fc39437b
title: Erstellen einer privaten Schriftartsammlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df673273611ed329e933c84e6540ed984088202590dc1d1c644ccdedca2c80c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977590"
---
# <a name="creating-a-private-font-collection"></a>Erstellen einer privaten Schriftartsammlung

Die [**PrivateFontCollection-Klasse erbt**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) von der abstrakten [**FontCollection-Basisklasse.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) Sie können ein **PrivateFontCollection-Objekt** verwenden, um einen Satz von Schriftarten speziell für Ihre Anwendung zu verwalten.

Eine private Schriftartsammlung kann installierte Systemschriftarten sowie Schriftarten enthalten, die nicht auf dem Computer installiert wurden. Um einer privaten Schriftartsammlung eine Schriftartdatei hinzuzufügen, rufen Sie die [**PrivateFontCollection::AddFontFile-Methode**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) eines [**PrivateFontCollection-Objekts**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) auf.

> [!Note]  
> Wenn Sie die GDI+-API verwenden, dürfen Sie niemals zulassen, dass Ihre Anwendung beliebige Schriftarten aus nicht vertrauenswürdigen Quellen herunterlädt. Das Betriebssystem erfordert erhöhte Rechte, um sicherzustellen, dass alle installierten Schriftarten vertrauenswürdig sind.

 

Die [**FontCollection::GetFamilies-Methode**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) eines [**PrivateFontCollection-Objekts**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) gibt ein Array von [**FontFamily-Objekten**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) zurück. Bevor Sie **FontCollection::GetFamilies** aufrufen, müssen Sie einen Puffer zuordnen, der groß genug ist, um dieses Array zu speichern. Um die Größe des erforderlichen Puffers zu bestimmen, rufen Sie die [**FontCollection::GetFamilyCount-Methode**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) auf, und multiplizieren Sie den Rückgabewert mit **sizeof**(**FontFamily**).

Die Anzahl der Schriftfamilien in einer privaten Schriftartauflistung ist nicht notwendigerweise mit der Anzahl der Schriftartdateien identisch, die der Auflistung hinzugefügt wurden. Angenommen, Sie fügen die Dateien ArialBd.tff, Times.tff und TimesBd.tff einer Sammlung hinzu. Es gibt drei Dateien, aber nur zwei Familien in der Sammlung, da Times.tff und TimesBd.tff zur gleichen Familie gehören.

Im folgenden Beispiel werden die folgenden drei Schriftartdateien einem [**PrivateFontCollection-Objekt**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) hinzugefügt:

-   C: \\ WINNT \\ Fonts \\ Arial.tff (Arial, regular)
-   C: \\ \\ WINNT-Schriftarten \\ –SchriftartenBI.tff (Courier New, bold kursiv)
-   C: \\ WINNT \\ Fonts \\ TimesBd.tff (Times New Roman, bold)

Der Code ruft die [**FontCollection::GetFamilyCount-Methode**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) des [**PrivateFontCollection-Objekts**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) auf, um die Anzahl der Familien in der privaten Auflistung zu bestimmen, und ruft dann [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) auf, um ein Array von [**FontFamily-Objekten**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) abzurufen.

Für jedes [**FontFamily-Objekt**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) in der Auflistung ruft der Code die [**FontFamily::IsStyleAvailable-Methode**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) auf, um zu bestimmen, ob verschiedene Stile (normal, fett, kursiv, fett kursiv, unterstrichen und durchstrichen) verfügbar sind. Die an die **FontFamily::IsStyleAvailable-Methode** übergebenen Argumente sind Member der [**FontStyle-Enumeration,**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) die in Gdiplusenums.h deklariert ist.

Wenn eine bestimmte Kombination aus Familie und Stil verfügbar ist, wird ein [**Font-Objekt**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) mit dieser Familie und diesem Stil erstellt. Das erste Argument,  das an den Font-Konstruktor übergeben wird, ist der Name der Schriftfamilie (kein [**FontFamily-Objekt**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) wie bei anderen Varianten des Font-Konstruktors), und das letzte Argument ist die Adresse des  [**PrivateFontCollection-Objekts.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) Nachdem das **Font-Objekt** erstellt wurde, wird seine Adresse an die [DrawString-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) der [**Graphics-Klasse**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) übergeben, um den Familiennamen zusammen mit dem Namen des Stils anzuzeigen.


```
#define MAX_STYLE_SIZE 20
#define MAX_FACEANDSTYLE_SIZE (LF_FACESIZE + MAX_STYLE_SIZE + 2)

PointF      pointF(10.0f, 0.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 0));
INT                   count = 0;
INT                   found = 0;
WCHAR                 familyName[LF_FACESIZE];
WCHAR                 familyNameAndStyle[MAX_FACEANDSTYLE_SIZE]; 
FontFamily*           pFontFamily;
PrivateFontCollection privateFontCollection;

// Add three font files to the private collection.
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\Arial.ttf");
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\CourBI.ttf");
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\TimesBd.ttf");

// How many font families are in the private collection?
count = privateFontCollection.GetFamilyCount();

// Allocate a buffer to hold the array of FontFamily
// objects returned by GetFamilies.
pFontFamily = new FontFamily[count];

// Get the array of FontFamily objects.
privateFontCollection.GetFamilies(count, pFontFamily, &found);

// Display the name of each font family in the private collection
// along with the available styles for that font family.
for(INT j = 0; j < count; ++j)
{
   // Get the font family name.
   pFontFamily[j].GetFamilyName(familyName);
   
   // Is the regular style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleRegular))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Regular");

      Font* pFont = new Font(
         familyName, 16, FontStyleRegular, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);      
   }

   // Is the bold style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleBold))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Bold");

      Font* pFont = new Font(
         familyName, 16, FontStyleBold, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Is the italic style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleItalic))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Italic");

      Font* pFont = new Font(
         familyName, 16, FontStyleItalic, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Is the bold italic style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleBoldItalic))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" BoldItalic");

      Font* pFont = new Font(familyName, 16, 
         FontStyleBoldItalic, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
    }

   // Is the underline style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleUnderline))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Underline");

      Font* pFont = new Font(familyName, 16, 
         FontStyleUnderline, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0);
      delete(pFont);
   }
 
   // Is the strikeout style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleStrikeout))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Strikeout");

      Font* pFont = new Font(familyName, 16, 
         FontStyleStrikeout, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Separate the families with white space.
   pointF.Y += 10.0f;

} // for

delete pFontFamily;
            
```



Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.

![Screenshot eines Fensters, in dem neun Schriftartnamen aufgelistet sind, die jeweils die benannte Schriftart veranschaulichen](images/fontstext7.png)

Arial.tff (das im vorherigen Codebeispiel der privaten Schriftartsammlung hinzugefügt wurde) ist die Schriftartdatei für den regulären Arial-Stil. Beachten Sie jedoch, dass die Programmausgabe mehrere verfügbare Stile anzeigt, die für die Arial-Schriftfamilie nicht normal sind. Dies liegt daran, dass Windows GDI+ die kursiven Fett-, Kursiv- und Fettformatvorlagen aus dem regulären Stil simulieren können. GDI+ können auch Unterstreichungen und Striche im regulären Stil erzeugen.

Auf ähnliche Weise können GDI+ den kursiven Fettstil entweder aus dem fett formatiertem oder kursiv formatiertem Stil simulieren. Die Programmausgabe zeigt, dass der kursive Fettformatierstil für die Times-Familie verfügbar ist, obwohl TimesBd.tff (Times New Roman, bold) die einzige Times-Datei in der Sammlung ist.

Diese Tabelle gibt die Nicht-Systemschriftarten an, die GDI+ unterstützt.



|                     | GDI | GDI+ auf Windows 7 | GDI+ auf Windows 8 | DirectWrite |
|---------------------|-----|-------------------|-------------------|-------------|
| . Fon                | Ja | Nein                | Nein                | Nein          |
| . Fnt                | Ja | Nein                | Nein                | Nein          |
| . Ttf                | Ja | Ja               | Ja               | Ja         |
| . OTF mit TrueType  | Ja | Ja               | Ja               | Ja         |
| . OTF mit Adobe CFF | Ja | Nein                | Ja               | Ja         |
| Adobe Type 1        | Ja | Nein                | Nein                | Nein          |



 

 

 



