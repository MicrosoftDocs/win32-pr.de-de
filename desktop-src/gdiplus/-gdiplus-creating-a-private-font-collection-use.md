---
description: Die PrivateFontCollection-Klasse erbt von der abstrakten Basisklasse FontCollection. Sie können ein PrivateFontCollection-Objekt verwenden, um eine Reihe von Schriftarten speziell für Ihre Anwendung beizubehalten.
ms.assetid: ae12afcf-12cc-4c84-9aba-de56fc39437b
title: Erstellen einer privaten Schriftartsammlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084e8a2d6f79f60e0719f04fbabb778b9483bd80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215591"
---
# <a name="creating-a-private-font-collection"></a>Erstellen einer privaten Schriftartsammlung

Die [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) -Klasse erbt von der abstrakten Basisklasse [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) . Sie können ein **PrivateFontCollection** -Objekt verwenden, um eine Reihe von Schriftarten speziell für Ihre Anwendung beizubehalten.

Eine private Schriftart Auflistung kann installierte System Schriftarten und Schriftarten enthalten, die nicht auf dem Computer installiert wurden. Um einer privaten Schriftart Auflistung eine Schriftart Datei hinzuzufügen, nennen Sie die [**PrivateFontCollection:: AddFontFile**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) -Methode eines [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) -Objekts.

> [!Note]  
> Wenn Sie die GDI+-API verwenden, dürfen Sie niemals zulassen, dass Ihre Anwendung beliebige Schriftarten aus nicht vertrauenswürdigen Quellen herunterlädt. Das Betriebssystem erfordert erhöhte Berechtigungen, um sicherzustellen, dass alle installierten Schriftarten vertrauenswürdig sind.

 

Die [**FontCollection:: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) -Methode eines [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) -Objekts gibt ein Array von [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Objekten zurück. Bevor Sie **FontCollection:: GetFamilies** aufrufen, müssen Sie einen Puffer zuordnen, der groß genug ist, um das Array zu speichern. Um die Größe des erforderlichen Puffers zu bestimmen, müssen Sie die [**FontCollection:: getfamilycount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) -Methode aufrufen und den Rückgabewert mit **sizeof**(**FontFamily**) multiplizieren.

Die Anzahl der Schriftart Familien in einer privaten Schriftart Auflistung ist nicht notwendigerweise identisch mit der Anzahl der Schriftart Dateien, die der Sammlung hinzugefügt wurden. Nehmen Sie beispielsweise an, dass Sie die Dateien ArialBd. tff, Times. tff und TimesBd. tff einer Auflistung hinzufügen. Es gibt drei Dateien, aber nur zwei Familien in der Sammlung, da times. tff und TimesBd. tff derselben Familie angehören.

Im folgenden Beispiel werden die folgenden drei Schriftart Dateien einem [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) -Objekt hinzugefügt:

-   C: \\ Winnt \\ Fonts \\ Arial. tff (Arial, Regular)
-   C: \\ Winnt \\ Fonts \\ courbi. tff (Courier New, Fett kursiv)
-   C: \\ Winnt \\ Fonts \\ TimesBd. tff (Times New Roman, Bold)

Der Code Ruft die [**FontCollection:: getfamilycount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) -Methode des [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) -Objekts auf, um die Anzahl der Familien in der privaten Auflistung zu bestimmen, und ruft dann [**FontCollection:: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) auf, um ein Array von [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Objekten abzurufen.

Der Code Ruft für jedes [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Objekt in der Auflistung die [**FontFamily:: IsStyleAvailable**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) -Methode auf, um zu bestimmen, ob verschiedene Stile (regulär, Fett, kursiv, Fett kursiv, unterstrichen und durchgestrichen) verfügbar sind. Die an die **FontFamily:: IsStyleAvailable** -Methode über gebenden Argumente sind Member der [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) -Enumeration, die in "gdiplusenums. h" deklariert wird.

Wenn eine bestimmte Kombination aus Familie und Stil verfügbar ist, wird ein [**Schriftart**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) Objekt mit dieser Familie und diesem Stil erstellt. Das erste Argument, das an den **Schriftart** -Konstruktor übergeben wird, ist der Schriftfamilien Name (kein [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Objekt wie bei anderen Variationen des **Schriftart** Konstruktors), und das letzte Argument ist die Adresse des [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) -Objekts. Nachdem das **Schriftart** Objekt erstellt wurde, wird die Adresse an die [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) -Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse weitergegeben, um den Familiennamen zusammen mit dem Namen des Stils anzuzeigen.


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

![Screenshot eines Fensters, das neun Schriftart Namen auflistet, von denen jede die benannte Schriftart veranschaulicht](images/fontstext7.png)

Arial. tff (der der privaten Schriftart Auflistung im vorangehenden Codebeispiel hinzugefügt wurde) ist die Schriftart Datei für den normalen Arial-Stil. Beachten Sie jedoch, dass die Programmausgabe für die Schriftart der Arial-Schriftart verschiedene andere andere Formate als regulär anzeigt. Dies liegt daran, dass Windows GDI+ die fetten, kursiv und Fetten kursiv formatierten Stile aus dem regulären Stil simulieren kann. GDI+ kann auch Unterstriche und Striche aus dem regulären Stil ergeben.

Ebenso kann GDI+ den fett formatierten Stil entweder aus dem fett formatierten Stil oder dem kursiv formatierten Stil simulieren. Die Programmausgabe zeigt, dass der Fett formatierte Stil für die Zeit Familie verfügbar ist, auch wenn TimesBd. tff (Times New Roman, Bold) die einzige Datei in der Sammlung ist.

Diese Tabelle gibt die nicht-System Schriftarten an, die von GDI+ unterstützt werden.



|                     | GDI | GDI+ unter Windows 7 | GDI+ unter Windows 8 | DirectWrite |
|---------------------|-----|-------------------|-------------------|-------------|
| . Geruchs                | ja | nein                | nein                | nein          |
| . Mit dem Namen                | ja | nein                | nein                | nein          |
| . TTF                | ja | ja               | ja               | ja         |
| . OTF mit TrueType  | ja | ja               | ja               | ja         |
| . OTF mit Adobe CFF | ja | nein                | ja               | ja         |
| Adobe-Typ 1        | ja | nein                | nein                | nein          |



 

 

 



