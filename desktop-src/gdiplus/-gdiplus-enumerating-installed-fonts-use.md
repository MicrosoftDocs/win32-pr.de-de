---
description: Die InstalledFontCollection-Klasse erbt von der abstrakten Basisklasse FontCollection.
ms.assetid: 59598f66-4241-4766-a2f0-5de736de959e
title: Auflisten der installierten Schriftarten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f41242522c2575ffb08e53f7100380ac9a849d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215586"
---
# <a name="enumerating-installed-fonts"></a><span data-ttu-id="8a12c-103">Auflisten der installierten Schriftarten</span><span class="sxs-lookup"><span data-stu-id="8a12c-103">Enumerating Installed Fonts</span></span>

<span data-ttu-id="8a12c-104">Die [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection) -Klasse erbt von der abstrakten Basisklasse [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) .</span><span class="sxs-lookup"><span data-stu-id="8a12c-104">The [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection) class inherits from the [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) abstract base class.</span></span> <span data-ttu-id="8a12c-105">Sie können ein **InstalledFontCollection** -Objekt verwenden, um die auf dem Computer installierten Schriftarten aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="8a12c-105">You can use an **InstalledFontCollection** object to enumerate the fonts installed on the computer.</span></span> <span data-ttu-id="8a12c-106">Die [**FontCollection:: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) -Methode eines **InstalledFontCollection** -Objekts gibt ein Array von [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Objekten zurück.</span><span class="sxs-lookup"><span data-stu-id="8a12c-106">The [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) method of an **InstalledFontCollection** object returns an array of [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) objects.</span></span> <span data-ttu-id="8a12c-107">Bevor Sie **FontCollection:: GetFamilies** aufrufen, müssen Sie einen Puffer zuordnen, der groß genug ist, um das Array zu speichern.</span><span class="sxs-lookup"><span data-stu-id="8a12c-107">Before you call **FontCollection::GetFamilies**, you must allocate a buffer large enough to hold that array.</span></span> <span data-ttu-id="8a12c-108">Um die Größe des erforderlichen Puffers zu bestimmen, müssen Sie die [**FontCollection:: getfamilycount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) -Methode aufrufen und den Rückgabewert mit **sizeof**(**FontFamily**) multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="8a12c-108">To determine the size of the required buffer, call the [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) method and multiply the return value by **sizeof**(**FontFamily**).</span></span>

<span data-ttu-id="8a12c-109">Im folgenden Beispiel werden die Namen aller auf dem Computer installierten Schriftfamilien aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8a12c-109">The following example lists the names of all the font families installed on the computer.</span></span> <span data-ttu-id="8a12c-110">Der Code Ruft die Namen der Schriftfamilie durch Aufrufen der [**FontFamily:: getfamilyname**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getfamilyname) -Methode jedes [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Objekts in dem von [**FontCollection:: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies)zurückgegebenen Array ab.</span><span class="sxs-lookup"><span data-stu-id="8a12c-110">The code retrieves the font family names by calling the [**FontFamily::GetFamilyName**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getfamilyname) method of each [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object in the array returned by [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies).</span></span> <span data-ttu-id="8a12c-111">Wenn die Familiennamen abgerufen werden, werden Sie verkettet, um eine durch Trennzeichen getrennte Liste zu bilden.</span><span class="sxs-lookup"><span data-stu-id="8a12c-111">As the family names are retrieved, they are concatenated to form a comma-separated list.</span></span> <span data-ttu-id="8a12c-112">Anschließend zeichnet die [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) -Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse die durch Kommas getrennte Liste in einem Rechteck.</span><span class="sxs-lookup"><span data-stu-id="8a12c-112">Then the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class draws the comma-separated list in a rectangle.</span></span>


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



<span data-ttu-id="8a12c-113">Die folgende Abbildung zeigt eine mögliche Ausgabe des vorangehenden Codes.</span><span class="sxs-lookup"><span data-stu-id="8a12c-113">The following illustration shows a possible output of the preceding code.</span></span> <span data-ttu-id="8a12c-114">Wenn Sie den Code ausführen, kann die Ausgabe abhängig von den auf Ihrem Computer installierten Schriftarten abweichen.</span><span class="sxs-lookup"><span data-stu-id="8a12c-114">If you run the code, the output might be different, depending on the fonts installed on your computer.</span></span>

![Screenshot eines Fensters, das eine durch Trennzeichen getrennte Liste installierter Schriftart Familien enthält](images/fontstext6.png)

 

 



