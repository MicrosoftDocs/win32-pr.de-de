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
# <a name="creating-a-private-font-collection"></a><span data-ttu-id="a6ba1-104">Erstellen einer privaten Schriftartsammlung</span><span class="sxs-lookup"><span data-stu-id="a6ba1-104">Creating a Private Font Collection</span></span>

<span data-ttu-id="a6ba1-105">Die [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) -Klasse erbt von der abstrakten Basisklasse [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) .</span><span class="sxs-lookup"><span data-stu-id="a6ba1-105">The [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) class inherits from the [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) abstract base class.</span></span> <span data-ttu-id="a6ba1-106">Sie können ein **PrivateFontCollection** -Objekt verwenden, um eine Reihe von Schriftarten speziell für Ihre Anwendung beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-106">You can use a **PrivateFontCollection** object to maintain a set of fonts specifically for your application.</span></span>

<span data-ttu-id="a6ba1-107">Eine private Schriftart Auflistung kann installierte System Schriftarten und Schriftarten enthalten, die nicht auf dem Computer installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-107">A private font collection can include installed system fonts as well as fonts that have not been installed on the computer.</span></span> <span data-ttu-id="a6ba1-108">Um einer privaten Schriftart Auflistung eine Schriftart Datei hinzuzufügen, nennen Sie die [**PrivateFontCollection:: AddFontFile**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) -Methode eines [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-108">To add a font file to a private font collection, call the [**PrivateFontCollection::AddFontFile**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) method of a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object.</span></span>

> [!Note]  
> <span data-ttu-id="a6ba1-109">Wenn Sie die GDI+-API verwenden, dürfen Sie niemals zulassen, dass Ihre Anwendung beliebige Schriftarten aus nicht vertrauenswürdigen Quellen herunterlädt.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-109">When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources.</span></span> <span data-ttu-id="a6ba1-110">Das Betriebssystem erfordert erhöhte Berechtigungen, um sicherzustellen, dass alle installierten Schriftarten vertrauenswürdig sind.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-110">The operating system requires elevated privileges to assure that all installed fonts are trusted.</span></span>

 

<span data-ttu-id="a6ba1-111">Die [**FontCollection:: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) -Methode eines [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) -Objekts gibt ein Array von [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Objekten zurück.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-111">The [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) method of a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object returns an array of [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) objects.</span></span> <span data-ttu-id="a6ba1-112">Bevor Sie **FontCollection:: GetFamilies** aufrufen, müssen Sie einen Puffer zuordnen, der groß genug ist, um das Array zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-112">Before you call **FontCollection::GetFamilies**, you must allocate a buffer large enough to hold that array.</span></span> <span data-ttu-id="a6ba1-113">Um die Größe des erforderlichen Puffers zu bestimmen, müssen Sie die [**FontCollection:: getfamilycount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) -Methode aufrufen und den Rückgabewert mit **sizeof**(**FontFamily**) multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-113">To determine the size of the required buffer, call the [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) method and multiply the return value by **sizeof**(**FontFamily**).</span></span>

<span data-ttu-id="a6ba1-114">Die Anzahl der Schriftart Familien in einer privaten Schriftart Auflistung ist nicht notwendigerweise identisch mit der Anzahl der Schriftart Dateien, die der Sammlung hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-114">The number of font families in a private font collection is not necessarily the same as the number of font files that have been added to the collection.</span></span> <span data-ttu-id="a6ba1-115">Nehmen Sie beispielsweise an, dass Sie die Dateien ArialBd. tff, Times. tff und TimesBd. tff einer Auflistung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-115">For example, suppose you add the files ArialBd.tff, Times.tff, and TimesBd.tff to a collection.</span></span> <span data-ttu-id="a6ba1-116">Es gibt drei Dateien, aber nur zwei Familien in der Sammlung, da times. tff und TimesBd. tff derselben Familie angehören.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-116">There will be three files but only two families in the collection because Times.tff and TimesBd.tff belong to the same family.</span></span>

<span data-ttu-id="a6ba1-117">Im folgenden Beispiel werden die folgenden drei Schriftart Dateien einem [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) -Objekt hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="a6ba1-117">The following example adds the following three font files to a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object:</span></span>

-   <span data-ttu-id="a6ba1-118">C: \\ Winnt \\ Fonts \\ Arial. tff (Arial, Regular)</span><span class="sxs-lookup"><span data-stu-id="a6ba1-118">C:\\WINNT\\Fonts\\Arial.tff (Arial, regular)</span></span>
-   <span data-ttu-id="a6ba1-119">C: \\ Winnt \\ Fonts \\ courbi. tff (Courier New, Fett kursiv)</span><span class="sxs-lookup"><span data-stu-id="a6ba1-119">C:\\WINNT\\Fonts\\CourBI.tff (Courier New, bold italic)</span></span>
-   <span data-ttu-id="a6ba1-120">C: \\ Winnt \\ Fonts \\ TimesBd. tff (Times New Roman, Bold)</span><span class="sxs-lookup"><span data-stu-id="a6ba1-120">C:\\WINNT\\Fonts\\TimesBd.tff (Times New Roman, bold)</span></span>

<span data-ttu-id="a6ba1-121">Der Code Ruft die [**FontCollection:: getfamilycount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) -Methode des [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) -Objekts auf, um die Anzahl der Familien in der privaten Auflistung zu bestimmen, und ruft dann [**FontCollection:: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) auf, um ein Array von [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Objekten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-121">The code calls the [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) method of the [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object to determine the number of families in the private collection, and then calls [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) to retrieve an array of [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) objects.</span></span>

<span data-ttu-id="a6ba1-122">Der Code Ruft für jedes [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Objekt in der Auflistung die [**FontFamily:: IsStyleAvailable**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) -Methode auf, um zu bestimmen, ob verschiedene Stile (regulär, Fett, kursiv, Fett kursiv, unterstrichen und durchgestrichen) verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-122">For each [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object in the collection, the code calls the [**FontFamily::IsStyleAvailable**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) method to determine whether various styles (regular, bold, italic, bold italic, underline, and strikeout) are available.</span></span> <span data-ttu-id="a6ba1-123">Die an die **FontFamily:: IsStyleAvailable** -Methode über gebenden Argumente sind Member der [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) -Enumeration, die in "gdiplusenums. h" deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-123">The arguments passed to the **FontFamily::IsStyleAvailable** method are members of the [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) enumeration, which is declared in Gdiplusenums.h.</span></span>

<span data-ttu-id="a6ba1-124">Wenn eine bestimmte Kombination aus Familie und Stil verfügbar ist, wird ein [**Schriftart**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) Objekt mit dieser Familie und diesem Stil erstellt.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-124">If a particular family/style combination is available, a [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) object is constructed using that family and style.</span></span> <span data-ttu-id="a6ba1-125">Das erste Argument, das an den **Schriftart** -Konstruktor übergeben wird, ist der Schriftfamilien Name (kein [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) -Objekt wie bei anderen Variationen des **Schriftart** Konstruktors), und das letzte Argument ist die Adresse des [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-125">The first argument passed to the **Font** constructor is the font family name (not a [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object as is the case for other variations of the **Font** constructor), and the final argument is the address of the [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object.</span></span> <span data-ttu-id="a6ba1-126">Nachdem das **Schriftart** Objekt erstellt wurde, wird die Adresse an die [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) -Methode der [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse weitergegeben, um den Familiennamen zusammen mit dem Namen des Stils anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-126">After the **Font** object is constructed, its address is passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to display the family name along with the name of the style.</span></span>


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



<span data-ttu-id="a6ba1-127">Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-127">The following illustration shows the output of the preceding code.</span></span>

![Screenshot eines Fensters, das neun Schriftart Namen auflistet, von denen jede die benannte Schriftart veranschaulicht](images/fontstext7.png)

<span data-ttu-id="a6ba1-129">Arial. tff (der der privaten Schriftart Auflistung im vorangehenden Codebeispiel hinzugefügt wurde) ist die Schriftart Datei für den normalen Arial-Stil.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-129">Arial.tff (which was added to the private font collection in the preceding code example) is the font file for the Arial regular style.</span></span> <span data-ttu-id="a6ba1-130">Beachten Sie jedoch, dass die Programmausgabe für die Schriftart der Arial-Schriftart verschiedene andere andere Formate als regulär anzeigt.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-130">Note, however, that the program output shows several available styles other than regular for the Arial font family.</span></span> <span data-ttu-id="a6ba1-131">Dies liegt daran, dass Windows GDI+ die fetten, kursiv und Fetten kursiv formatierten Stile aus dem regulären Stil simulieren kann.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-131">That is because Windows GDI+ can simulate the bold, italic, and bold italic styles from the regular style.</span></span> <span data-ttu-id="a6ba1-132">GDI+ kann auch Unterstriche und Striche aus dem regulären Stil ergeben.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-132">GDI+ can also produce underlines and strikeouts from the regular style.</span></span>

<span data-ttu-id="a6ba1-133">Ebenso kann GDI+ den fett formatierten Stil entweder aus dem fett formatierten Stil oder dem kursiv formatierten Stil simulieren.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-133">Similarly, GDI+ can simulate the bold italic style from either the bold style or the italic style.</span></span> <span data-ttu-id="a6ba1-134">Die Programmausgabe zeigt, dass der Fett formatierte Stil für die Zeit Familie verfügbar ist, auch wenn TimesBd. tff (Times New Roman, Bold) die einzige Datei in der Sammlung ist.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-134">The program output shows that the bold italic style is available for the Times family even though TimesBd.tff (Times New Roman, bold) is the only Times file in the collection.</span></span>

<span data-ttu-id="a6ba1-135">Diese Tabelle gibt die nicht-System Schriftarten an, die von GDI+ unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a6ba1-135">This table specifies the non-system fonts that GDI+ supports.</span></span>



|                     | <span data-ttu-id="a6ba1-136">GDI</span><span class="sxs-lookup"><span data-stu-id="a6ba1-136">GDI</span></span> | <span data-ttu-id="a6ba1-137">GDI+ unter Windows 7</span><span class="sxs-lookup"><span data-stu-id="a6ba1-137">GDI+ on Windows 7</span></span> | <span data-ttu-id="a6ba1-138">GDI+ unter Windows 8</span><span class="sxs-lookup"><span data-stu-id="a6ba1-138">GDI+ on Windows 8</span></span> | <span data-ttu-id="a6ba1-139">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="a6ba1-139">DirectWrite</span></span> |
|---------------------|-----|-------------------|-------------------|-------------|
| <span data-ttu-id="a6ba1-140">. Geruchs</span><span class="sxs-lookup"><span data-stu-id="a6ba1-140">.FON</span></span>                | <span data-ttu-id="a6ba1-141">ja</span><span class="sxs-lookup"><span data-stu-id="a6ba1-141">yes</span></span> | <span data-ttu-id="a6ba1-142">nein</span><span class="sxs-lookup"><span data-stu-id="a6ba1-142">no</span></span>                | <span data-ttu-id="a6ba1-143">nein</span><span class="sxs-lookup"><span data-stu-id="a6ba1-143">no</span></span>                | <span data-ttu-id="a6ba1-144">nein</span><span class="sxs-lookup"><span data-stu-id="a6ba1-144">no</span></span>          |
| <span data-ttu-id="a6ba1-145">. Mit dem Namen</span><span class="sxs-lookup"><span data-stu-id="a6ba1-145">.FNT</span></span>                | <span data-ttu-id="a6ba1-146">ja</span><span class="sxs-lookup"><span data-stu-id="a6ba1-146">yes</span></span> | <span data-ttu-id="a6ba1-147">nein</span><span class="sxs-lookup"><span data-stu-id="a6ba1-147">no</span></span>                | <span data-ttu-id="a6ba1-148">nein</span><span class="sxs-lookup"><span data-stu-id="a6ba1-148">no</span></span>                | <span data-ttu-id="a6ba1-149">nein</span><span class="sxs-lookup"><span data-stu-id="a6ba1-149">no</span></span>          |
| <span data-ttu-id="a6ba1-150">. TTF</span><span class="sxs-lookup"><span data-stu-id="a6ba1-150">.TTF</span></span>                | <span data-ttu-id="a6ba1-151">ja</span><span class="sxs-lookup"><span data-stu-id="a6ba1-151">yes</span></span> | <span data-ttu-id="a6ba1-152">ja</span><span class="sxs-lookup"><span data-stu-id="a6ba1-152">yes</span></span>               | <span data-ttu-id="a6ba1-153">ja</span><span class="sxs-lookup"><span data-stu-id="a6ba1-153">yes</span></span>               | <span data-ttu-id="a6ba1-154">ja</span><span class="sxs-lookup"><span data-stu-id="a6ba1-154">yes</span></span>         |
| <span data-ttu-id="a6ba1-155">. OTF mit TrueType</span><span class="sxs-lookup"><span data-stu-id="a6ba1-155">.OTF with TrueType</span></span>  | <span data-ttu-id="a6ba1-156">ja</span><span class="sxs-lookup"><span data-stu-id="a6ba1-156">yes</span></span> | <span data-ttu-id="a6ba1-157">ja</span><span class="sxs-lookup"><span data-stu-id="a6ba1-157">yes</span></span>               | <span data-ttu-id="a6ba1-158">ja</span><span class="sxs-lookup"><span data-stu-id="a6ba1-158">yes</span></span>               | <span data-ttu-id="a6ba1-159">ja</span><span class="sxs-lookup"><span data-stu-id="a6ba1-159">yes</span></span>         |
| <span data-ttu-id="a6ba1-160">. OTF mit Adobe CFF</span><span class="sxs-lookup"><span data-stu-id="a6ba1-160">.OTF with Adobe CFF</span></span> | <span data-ttu-id="a6ba1-161">ja</span><span class="sxs-lookup"><span data-stu-id="a6ba1-161">yes</span></span> | <span data-ttu-id="a6ba1-162">nein</span><span class="sxs-lookup"><span data-stu-id="a6ba1-162">no</span></span>                | <span data-ttu-id="a6ba1-163">ja</span><span class="sxs-lookup"><span data-stu-id="a6ba1-163">yes</span></span>               | <span data-ttu-id="a6ba1-164">ja</span><span class="sxs-lookup"><span data-stu-id="a6ba1-164">yes</span></span>         |
| <span data-ttu-id="a6ba1-165">Adobe-Typ 1</span><span class="sxs-lookup"><span data-stu-id="a6ba1-165">Adobe Type 1</span></span>        | <span data-ttu-id="a6ba1-166">ja</span><span class="sxs-lookup"><span data-stu-id="a6ba1-166">yes</span></span> | <span data-ttu-id="a6ba1-167">nein</span><span class="sxs-lookup"><span data-stu-id="a6ba1-167">no</span></span>                | <span data-ttu-id="a6ba1-168">nein</span><span class="sxs-lookup"><span data-stu-id="a6ba1-168">no</span></span>                | <span data-ttu-id="a6ba1-169">nein</span><span class="sxs-lookup"><span data-stu-id="a6ba1-169">no</span></span>          |



 

 

 



