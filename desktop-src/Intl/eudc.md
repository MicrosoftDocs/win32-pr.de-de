---
description: Der EUDC-Registrierungsschlüssel enthält einen oder mehrere Unterschlüssel mit Werten, die die Schriftarten definieren, die Endbenutzer definierten Zeichen (eudcs) für eine bestimmte Codepage zugeordnet sind.
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: EUDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781f7c28460c2e56f4bcdb393277f509f88a0383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350872"
---
# <a name="eudc"></a><span data-ttu-id="49960-103">EUDC</span><span class="sxs-lookup"><span data-stu-id="49960-103">EUDC</span></span>

<span data-ttu-id="49960-104">Der EUDC-Registrierungsschlüssel enthält einen oder mehrere Unterschlüssel mit Werten, die die Schriftarten definieren, die [Endbenutzer definierten Zeichen (eudcs)](end-user-defined-characters.md) für eine bestimmte Codepage zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="49960-104">The EUDC registry key contains one or more subkeys containing values defining the fonts associated with [end-user-defined characters (EUDCs)](end-user-defined-characters.md) for a given code page.</span></span> <span data-ttu-id="49960-105">Es verfügt über den folgenden Registrierungs Speicherort:</span><span class="sxs-lookup"><span data-stu-id="49960-105">It has the following registry location:</span></span>

<span data-ttu-id="49960-106">HKEY \_ aktueller \_ Benutzer ( \\ EUDC)</span><span class="sxs-lookup"><span data-stu-id="49960-106">HKEY\_CURRENT\_USER\\EUDC</span></span>

<span data-ttu-id="49960-107">Das Format lautet:</span><span class="sxs-lookup"><span data-stu-id="49960-107">The format is:</span></span>

<span data-ttu-id="49960-108">EUDC systemdefaulteudcfont = truetyeteudcfontfilename truetyetfonttypeer = truetyeteudcfontfilename</span><span class="sxs-lookup"><span data-stu-id="49960-108">EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName</span></span>

<span data-ttu-id="49960-109">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="49960-109">where:</span></span>



|                          |                                                                                                                                          |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49960-110">Systemdefaulteudcfont</span><span class="sxs-lookup"><span data-stu-id="49960-110">SystemDefaultEUDCFont</span></span>    | <span data-ttu-id="49960-111">Der vordefinierte Name, der zum Festlegen der System Standard Schriftart verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="49960-111">Predefined name used to set the system default font.</span></span> <span data-ttu-id="49960-112">Es gibt keine System Standard-EUDC-Schriftart, es sei denn, dieser Eintrag ist explizit angegeben.</span><span class="sxs-lookup"><span data-stu-id="49960-112">There is no system default EUDC font unless this entry is explicitly specified.</span></span>     |
| <span data-ttu-id="49960-113">Truetyetfonttyetface</span><span class="sxs-lookup"><span data-stu-id="49960-113">TrueTypeFontTypeface</span></span>     | <span data-ttu-id="49960-114">Ein benutzerdefinierter Name, der mit einer nicht-EUDC TrueType-Schriftart verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="49960-114">User-defined name associated with a non-EUDC TrueType font.</span></span>                                                                              |
| <span data-ttu-id="49960-115">Truetyeteudcfontfilename</span><span class="sxs-lookup"><span data-stu-id="49960-115">TrueTypeEUDCFontFileName</span></span> | <span data-ttu-id="49960-116">Eine Zeichenfolge, die aus dem Dateinamen einer separaten EUDC-Schriftart Datei besteht.</span><span class="sxs-lookup"><span data-stu-id="49960-116">String consisting of the file name of a separate EUDC font file.</span></span> <span data-ttu-id="49960-117">Diese Datei identifiziert eine Schriftart, die truetyetfonttyetface zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="49960-117">This file identifies a font to be associated with TrueTypeFontTypeface.</span></span> |



 

<span data-ttu-id="49960-118">Das folgende Beispiel zeigt den EUDC-Schlüssel für die Codepage 932.</span><span class="sxs-lookup"><span data-stu-id="49960-118">The following example shows the EUDC key for code page 932.</span></span>


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



<span data-ttu-id="49960-119">Im folgenden Beispiel wird die Standard Schriftart des EUDC-Systems auf EUDC. ttf festgelegt, und die separaten EUDC-Schriftarten mineudc. ttf und goteudc. ttf werden den Schriftart Namen MS Mincho bzw. MS Gothic zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="49960-119">The following example sets the system default EUDC font to be Eudc.ttf and associates the separate EUDC fonts Mineudc.ttf and Goteudc.ttf with the font names MS Mincho and MS Gothic, respectively.</span></span>


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



<span data-ttu-id="49960-120">Wenn die Windows-Codepage (System ACP), die der Sprache für nicht-Unicode-Programme zugeordnet ist, mit dem Unterschlüssel übereinstimmt, sucht das GDI-Subsystem nach den Unterschlüssel-Wert-Paaren, um Anzeigeinformationen zum Zeichen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="49960-120">When the Windows code page (system ACP) associated with the language for non-Unicode programs matches the subkey, the GDI subsystem looks to the subkey value pairs to obtain display information about the character.</span></span> <span data-ttu-id="49960-121">Zuerst sucht er nach einem Namen, der mit der aktuellen Schriftart übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="49960-121">It first looks for a name matching the current font.</span></span> <span data-ttu-id="49960-122">Wenn keine vorhanden ist, wird der Wert systemdefaulteudcfont überprüft.</span><span class="sxs-lookup"><span data-stu-id="49960-122">If there is none, it examines the SystemDefaultEUDCFont value.</span></span> <span data-ttu-id="49960-123">Wenn kein Wert definiert ist, behandelt GDI das Zeichen als nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="49960-123">If no value is defined, GDI treats the character as undefined.</span></span>

<span data-ttu-id="49960-124">Beachten Sie, dass sich der Text selbst nicht auf der Windows-Codepage befinden muss.</span><span class="sxs-lookup"><span data-stu-id="49960-124">Note that the text itself does not have to be in the Windows code page.</span></span> <span data-ttu-id="49960-125">Nehmen Sie beispielsweise an, dass die Codepage den Bezeichner 1252 hat, die standardmäßige Windows-Codepage für Englisch.</span><span class="sxs-lookup"><span data-stu-id="49960-125">For example, assume that the code page has the identifier 1252, the default Windows code page for English.</span></span> <span data-ttu-id="49960-126">Eine Anwendung übergibt den einzelnen Unicode-Codepunkt U + E000 im privaten Unicode-Verwendungsbereich (Pua) an [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="49960-126">An application passes the single Unicode code point U+E000, in the Unicode private use area (PUA), to [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span></span> <span data-ttu-id="49960-127">In diesem Fall prüft GDI die Registrierungs Werte unter 1252, um die Schriftart Informationen für die Zeichen Anzeigeeigenschaften zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="49960-127">In this case, GDI looks at the registry values under 1252 to obtain the font information for the character display properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49960-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="49960-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49960-129">EUDC-Registrierungseinträge</span><span class="sxs-lookup"><span data-stu-id="49960-129">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="49960-130">Eudccoderange</span><span class="sxs-lookup"><span data-stu-id="49960-130">EUDCCodeRange</span></span>](eudccoderange.md)
</dt> </dl>

 

 
