---
title: Fontdirentry-Struktur
description: Enthält Informationen über eine einzelne Schriftart in einer Schriftart Ressourcengruppe. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: 0ada2afe-b299-4ef2-99b7-96da10ee218a
keywords:
- Fontdirentry-Struktur Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- FONTDIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1cee72a490fd2b94b1c810797f656d81418c0f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475771"
---
# <a name="fontdirentry-structure"></a><span data-ttu-id="547a9-105">Fontdirentry-Struktur</span><span class="sxs-lookup"><span data-stu-id="547a9-105">FONTDIRENTRY structure</span></span>

<span data-ttu-id="547a9-106">Enthält Informationen über eine einzelne Schriftart in einer Schriftart Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="547a9-106">Contains information about an individual font in a font resource group.</span></span> <span data-ttu-id="547a9-107">Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="547a9-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="547a9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="547a9-108">Syntax</span></span>


```C++
typedef struct {
  WORD  dfVersion;
  DWORD dfSize;
  CHAR  dfCopyright[60];
  WORD  dfType;
  WORD  dfPoints;
  WORD  dfVertRes;
  WORD  dfHorizRes;
  WORD  dfAscent;
  WORD  dfInternalLeading;
  WORD  dfExternalLeading;
  BYTE  dfItalic;
  BYTE  dfUnderline;
  BYTE  dfStrikeOut;
  WORD  dfWeight;
  BYTE  dfCharSet;
  WORD  dfPixWidth;
  WORD  dfPixHeight;
  BYTE  dfPitchAndFamily;
  WORD  dfAvgWidth;
  WORD  dfMaxWidth;
  BYTE  dfFirstChar;
  BYTE  dfLastChar;
  BYTE  dfDefaultChar;
  BYTE  dfBreakChar;
  WORD  dfWidthBytes;
  DWORD dfDevice;
  DWORD dfFace;
  DWORD dfReserved;
  CHAR  szDeviceName;
  CHAR  szFaceName;
} FONTDIRENTRY;
```



## <a name="members"></a><span data-ttu-id="547a9-109">Member</span><span class="sxs-lookup"><span data-stu-id="547a9-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="547a9-110">**dfversion**</span><span class="sxs-lookup"><span data-stu-id="547a9-110">**dfVersion**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-111">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="547a9-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-112">Eine benutzerdefinierte Versionsnummer für die Ressourcen Daten, die Tools zum Lesen und Schreiben von Ressourcen Dateien verwenden können.</span><span class="sxs-lookup"><span data-stu-id="547a9-112">A user-defined version number for the resource data that tools can use to read and write resource files.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-113">**dfsize**</span><span class="sxs-lookup"><span data-stu-id="547a9-113">**dfSize**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-114">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="547a9-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-115">Die Größe der Datei (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="547a9-115">The size of the file, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-116">**dfcopyright \[ 60\]**</span><span class="sxs-lookup"><span data-stu-id="547a9-116">**dfCopyright\[60\]**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-117">Typ: **char**</span><span class="sxs-lookup"><span data-stu-id="547a9-117">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-118">Die Copyright Informationen des Schriftart Lieferanten.</span><span class="sxs-lookup"><span data-stu-id="547a9-118">The font supplier's copyright information.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-119">**dftype**</span><span class="sxs-lookup"><span data-stu-id="547a9-119">**dfType**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-120">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="547a9-120">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-121">Der Typ der Schriftart Datei.</span><span class="sxs-lookup"><span data-stu-id="547a9-121">The type of font file.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-122">**dfpoints**</span><span class="sxs-lookup"><span data-stu-id="547a9-122">**dfPoints**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-123">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="547a9-123">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-124">Die Punktgröße, bei der dieser Zeichensatz am besten aussieht.</span><span class="sxs-lookup"><span data-stu-id="547a9-124">The point size at which this character set looks best.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-125">**dfvertres**</span><span class="sxs-lookup"><span data-stu-id="547a9-125">**dfVertRes**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-126">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="547a9-126">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-127">Die vertikale Auflösung in Punkten pro Zoll, bei der dieser Zeichensatz digitalisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="547a9-127">The vertical resolution, in dots per inch, at which this character set was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-128">**dfHorizRes**</span><span class="sxs-lookup"><span data-stu-id="547a9-128">**dfHorizRes**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-129">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="547a9-129">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-130">Die horizontale Auflösung in Punkten pro Zoll, bei der dieser Zeichensatz digitalisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="547a9-130">The horizontal resolution, in dots per inch, at which this character set was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-131">**dfascent**</span><span class="sxs-lookup"><span data-stu-id="547a9-131">**dfAscent**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-132">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="547a9-132">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-133">Der Abstand zwischen dem oberen Rand einer Zeichen Definitions Zelle und der Baseline der typografischen Schriftart.</span><span class="sxs-lookup"><span data-stu-id="547a9-133">The distance from the top of a character definition cell to the baseline of the typographical font.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-134">**dfinternalleading**</span><span class="sxs-lookup"><span data-stu-id="547a9-134">**dfInternalLeading**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-135">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="547a9-135">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-136">Die Menge der führenden innerhalb der durch das **dfpixheight** -Member festgelegten Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="547a9-136">The amount of leading inside the bounds set by the **dfPixHeight** member.</span></span> <span data-ttu-id="547a9-137">In diesem Bereich können Akzente und andere diakritische Zeichen auftreten.</span><span class="sxs-lookup"><span data-stu-id="547a9-137">Accent marks and other diacritical characters can occur in this area.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-138">**dfexternalleading**</span><span class="sxs-lookup"><span data-stu-id="547a9-138">**dfExternalLeading**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-139">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="547a9-139">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-140">Die Menge der zusätzlichen führenden, die von der Anwendung zwischen Zeilen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="547a9-140">The amount of extra leading that the application adds between rows.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-141">**dsptalic**</span><span class="sxs-lookup"><span data-stu-id="547a9-141">**dfItalic**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-142">Type: **Byte**</span><span class="sxs-lookup"><span data-stu-id="547a9-142">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-143">Eine kursiv Schrift, wenn nicht gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="547a9-143">An italic font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-144">**dfunderline**</span><span class="sxs-lookup"><span data-stu-id="547a9-144">**dfUnderline**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-145">Type: **Byte**</span><span class="sxs-lookup"><span data-stu-id="547a9-145">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-146">Eine unterstrichene Schriftart, wenn ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="547a9-146">An underlined font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-147">**dfstrikeout**</span><span class="sxs-lookup"><span data-stu-id="547a9-147">**dfStrikeOut**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-148">Type: **Byte**</span><span class="sxs-lookup"><span data-stu-id="547a9-148">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-149">Eine ausstrich Schriftart, wenn nicht gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="547a9-149">A strikeout font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-150">**dfweight**</span><span class="sxs-lookup"><span data-stu-id="547a9-150">**dfWeight**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-151">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="547a9-151">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-152">Die Gewichtung der Schriftart im Bereich von 0 bis 1000.</span><span class="sxs-lookup"><span data-stu-id="547a9-152">The weight of the font in the range 0 through 1000.</span></span> <span data-ttu-id="547a9-153">400 ist z. b. Roman, und 700 ist fett formatiert.</span><span class="sxs-lookup"><span data-stu-id="547a9-153">For example, 400 is roman and 700 is bold.</span></span> <span data-ttu-id="547a9-154">Wenn dieser Wert 0 (null) ist, wird eine Standard Gewichtung verwendet.</span><span class="sxs-lookup"><span data-stu-id="547a9-154">If this value is zero, a default weight is used.</span></span> <span data-ttu-id="547a9-155">Weitere definierte Werte finden Sie in der Beschreibung der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="547a9-155">For additional defined values, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-156">**dfcharset**</span><span class="sxs-lookup"><span data-stu-id="547a9-156">**dfCharSet**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-157">Type: **Byte**</span><span class="sxs-lookup"><span data-stu-id="547a9-157">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-158">Der Zeichensatz der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="547a9-158">The character set of the font.</span></span> <span data-ttu-id="547a9-159">Informationen zu vordefinierten Werten finden Sie in der Beschreibung der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="547a9-159">For predefined values, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-160">**dfpixwidth**</span><span class="sxs-lookup"><span data-stu-id="547a9-160">**dfPixWidth**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-161">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="547a9-161">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-162">Die Breite des Rasters, in dem eine Vektor Schriftart digitalisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="547a9-162">The width of the grid on which a vector font was digitized.</span></span> <span data-ttu-id="547a9-163">Wenn das Element bei Raster Schriftarten nicht gleich 0 (null) ist, stellt es die Breite für alle Zeichen in der Bitmap dar.</span><span class="sxs-lookup"><span data-stu-id="547a9-163">For raster fonts, if the member is not equal to zero, it represents the width for all the characters in the bitmap.</span></span> <span data-ttu-id="547a9-164">Wenn der Member gleich 0 (null) ist, weist die Schriftart Zeichen variabler Breite auf.</span><span class="sxs-lookup"><span data-stu-id="547a9-164">If the member is equal to zero, the font has variable-width characters.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-165">**dfpixheight**</span><span class="sxs-lookup"><span data-stu-id="547a9-165">**dfPixHeight**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-166">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="547a9-166">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-167">Die Höhe der Zeichen Bitmap für Raster Schriftarten oder die Höhe des Rasters, in dem eine Vektor Schriftart digitalisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="547a9-167">The height of the character bitmap for raster fonts or the height of the grid on which a vector font was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-168">**dfpitchandfamily**</span><span class="sxs-lookup"><span data-stu-id="547a9-168">**dfPitchAndFamily**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-169">Type: **Byte**</span><span class="sxs-lookup"><span data-stu-id="547a9-169">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-170">Die Tonhöhe und die Familie der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="547a9-170">The pitch and the family of the font.</span></span> <span data-ttu-id="547a9-171">Weitere Informationen finden Sie in der Beschreibung der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="547a9-171">For additional information, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-172">**dfavgwidth**</span><span class="sxs-lookup"><span data-stu-id="547a9-172">**dfAvgWidth**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-173">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="547a9-173">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-174">Die durchschnittliche Breite der Zeichen in der Schriftart (im Allgemeinen als Breite des Buchstaben x definiert).</span><span class="sxs-lookup"><span data-stu-id="547a9-174">The average width of characters in the font (generally defined as the width of the letter x).</span></span> <span data-ttu-id="547a9-175">Dieser Wert enthält nicht den für Fett-oder kursiv Zeichen erforderlichen Überlauf.</span><span class="sxs-lookup"><span data-stu-id="547a9-175">This value does not include the overhang required for bold or italic characters.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-176">**dfmaxwidth**</span><span class="sxs-lookup"><span data-stu-id="547a9-176">**dfMaxWidth**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-177">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="547a9-177">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-178">Die Breite des breitesten Zeichens in der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="547a9-178">The width of the widest character in the font.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-179">**dffirstchar**</span><span class="sxs-lookup"><span data-stu-id="547a9-179">**dfFirstChar**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-180">Type: **Byte**</span><span class="sxs-lookup"><span data-stu-id="547a9-180">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-181">Der erste Zeichencode, der in der Schriftart definiert ist.</span><span class="sxs-lookup"><span data-stu-id="547a9-181">The first character code defined in the font.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-182">**dflastchar**</span><span class="sxs-lookup"><span data-stu-id="547a9-182">**dfLastChar**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-183">Type: **Byte**</span><span class="sxs-lookup"><span data-stu-id="547a9-183">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-184">Der letzte Zeichencode, der in der Schriftart definiert ist.</span><span class="sxs-lookup"><span data-stu-id="547a9-184">The last character code defined in the font.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-185">**dfdefaultchar**</span><span class="sxs-lookup"><span data-stu-id="547a9-185">**dfDefaultChar**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-186">Type: **Byte**</span><span class="sxs-lookup"><span data-stu-id="547a9-186">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-187">Das Zeichen, das nicht in der Schriftart, sondern in Zeichen ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="547a9-187">The character to substitute for characters not in the font.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-188">**dfbreakchar**</span><span class="sxs-lookup"><span data-stu-id="547a9-188">**dfBreakChar**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-189">Type: **Byte**</span><span class="sxs-lookup"><span data-stu-id="547a9-189">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-190">Das Zeichen, das zum Definieren von Wort Umbrüchen für die Textausrichtung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="547a9-190">The character that will be used to define word breaks for text justification.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-191">**dfwidthbytes**</span><span class="sxs-lookup"><span data-stu-id="547a9-191">**dfWidthBytes**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-192">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="547a9-192">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-193">Die Anzahl der Bytes in jeder Zeile der Bitmap.</span><span class="sxs-lookup"><span data-stu-id="547a9-193">The number of bytes in each row of the bitmap.</span></span> <span data-ttu-id="547a9-194">Dieser Wert ist immer, auch wenn die Zeilen an Wortgrenzen beginnen.</span><span class="sxs-lookup"><span data-stu-id="547a9-194">This value is always even so that the rows start on word boundaries.</span></span> <span data-ttu-id="547a9-195">Bei Vektor Schriftarten hat dieser Member keine Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="547a9-195">For vector fonts, this member has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-196">**dfdevice**</span><span class="sxs-lookup"><span data-stu-id="547a9-196">**dfDevice**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-197">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="547a9-197">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-198">Der Offset in der Datei mit einer auf NULL endenden Zeichenfolge, die einen Gerätenamen angibt.</span><span class="sxs-lookup"><span data-stu-id="547a9-198">The offset in the file to a null-terminated string that specifies a device name.</span></span> <span data-ttu-id="547a9-199">Bei einer generischen Schriftart ist dieser Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="547a9-199">For a generic font, this value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-200">**dfface**</span><span class="sxs-lookup"><span data-stu-id="547a9-200">**dfFace**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-201">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="547a9-201">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-202">Der Offset in der Datei mit einer auf NULL endenden Zeichenfolge, die die Schriftart benennt.</span><span class="sxs-lookup"><span data-stu-id="547a9-202">The offset in the file to a null-terminated string that names the typeface.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-203">**dfreserved**</span><span class="sxs-lookup"><span data-stu-id="547a9-203">**dfReserved**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-204">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="547a9-204">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-205">Dieser Member ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="547a9-205">This member is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-206">**szdevicename**</span><span class="sxs-lookup"><span data-stu-id="547a9-206">**szDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-207">Typ: **char**</span><span class="sxs-lookup"><span data-stu-id="547a9-207">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-208">Der Name des Geräts, wenn diese Schriftart Datei für ein bestimmtes Gerät bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="547a9-208">The name of the device if this font file is designated for a specific device.</span></span>

</dd> <dt>

<span data-ttu-id="547a9-209">**szfakename**</span><span class="sxs-lookup"><span data-stu-id="547a9-209">**szFaceName**</span></span>
</dt> <dd>

<span data-ttu-id="547a9-210">Typ: **char**</span><span class="sxs-lookup"><span data-stu-id="547a9-210">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="547a9-211">Der Schriftart Name der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="547a9-211">The typeface name of the font.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="547a9-212">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="547a9-212">Remarks</span></span>

<span data-ttu-id="547a9-213">Es gibt eine **fontdirentry** -Struktur für jede Schriftart in der RES-Datei.</span><span class="sxs-lookup"><span data-stu-id="547a9-213">There is one **FONTDIRENTRY** structure for every font in the .res file.</span></span> <span data-ttu-id="547a9-214">Anwendungen, die RES-Dateien mit Schriftart Ressourcen generieren, müssen der Datei auch eine **fontdirentry** -Struktur für jede Schriftart hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="547a9-214">Applications that generate .res files with font resources must also add to the file a **FONTDIRENTRY** structure for each font.</span></span>

<span data-ttu-id="547a9-215">Schriftart Deklarationen können mit anderen Ressourcen Deklarationen in gemischt werden. RC-Datei, da Schriftarten in der RES-Datei nicht zusammenhängend sein müssen.</span><span class="sxs-lookup"><span data-stu-id="547a9-215">Font declarations can be mixed with other resource declarations in the .RC file because fonts do not need to be contiguous in the .res file.</span></span>

## <a name="requirements"></a><span data-ttu-id="547a9-216">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="547a9-216">Requirements</span></span>



| <span data-ttu-id="547a9-217">Anforderung</span><span class="sxs-lookup"><span data-stu-id="547a9-217">Requirement</span></span> | <span data-ttu-id="547a9-218">Wert</span><span class="sxs-lookup"><span data-stu-id="547a9-218">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="547a9-219">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="547a9-219">Minimum supported client</span></span><br/> | <span data-ttu-id="547a9-220">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="547a9-220">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="547a9-221">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="547a9-221">Minimum supported server</span></span><br/> | <span data-ttu-id="547a9-222">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="547a9-222">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="547a9-223">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="547a9-223">See also</span></span>

<dl> <dt>

<span data-ttu-id="547a9-224">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="547a9-224">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="547a9-225">**Direntry**</span><span class="sxs-lookup"><span data-stu-id="547a9-225">**DIRENTRY**</span></span>](direntry.md)
</dt> <dt>

[<span data-ttu-id="547a9-226">**Fontgrouphdr**</span><span class="sxs-lookup"><span data-stu-id="547a9-226">**FONTGROUPHDR**</span></span>](fontgrouphdr.md)
</dt> <dt>

<span data-ttu-id="547a9-227">**Licher**</span><span class="sxs-lookup"><span data-stu-id="547a9-227">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="547a9-228">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="547a9-228">Resources</span></span>](resources.md)
</dt> <dt>

<span data-ttu-id="547a9-229">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="547a9-229">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="547a9-230">**"LogFont"**</span><span class="sxs-lookup"><span data-stu-id="547a9-230">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

