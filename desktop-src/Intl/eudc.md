---
description: Der EUDC-Registrierungsschlüssel enthält mindestens einen Unterschlüssel, der Werte enthält, die die Schriftarten definieren, die endbenutzerdefinierten Zeichen (EUDCs) für eine bestimmte Codepage zugeordnet sind.
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: EUDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b583c7a0bfaa67684901e8d0a4a95ac5e45658
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120705"
---
# <a name="eudc"></a><span data-ttu-id="910be-103">EUDC</span><span class="sxs-lookup"><span data-stu-id="910be-103">EUDC</span></span>

<span data-ttu-id="910be-104">Der EUDC-Registrierungsschlüssel enthält mindestens einen Unterschlüssel, der Werte enthält, die die Schriftarten definieren, die endbenutzerdefinierten Zeichen [(EUDCs)](end-user-defined-characters.md) für eine bestimmte Codepage zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="910be-104">The EUDC registry key contains one or more subkeys containing values defining the fonts associated with [end-user-defined characters (EUDCs)](end-user-defined-characters.md) for a given code page.</span></span> <span data-ttu-id="910be-105">Sie verfügt über den folgenden Registrierungsspeicherort:</span><span class="sxs-lookup"><span data-stu-id="910be-105">It has the following registry location:</span></span>

<span data-ttu-id="910be-106">HKEY \_ CURRENT \_ USER \\ EUDC</span><span class="sxs-lookup"><span data-stu-id="910be-106">HKEY\_CURRENT\_USER\\EUDC</span></span>

<span data-ttu-id="910be-107">Das Format lautet:</span><span class="sxs-lookup"><span data-stu-id="910be-107">The format is:</span></span>

<span data-ttu-id="910be-108">EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName</span><span class="sxs-lookup"><span data-stu-id="910be-108">EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName</span></span>

<span data-ttu-id="910be-109">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="910be-109">where:</span></span>



| <span data-ttu-id="910be-110">Wert</span><span class="sxs-lookup"><span data-stu-id="910be-110">Value</span></span>                         | <span data-ttu-id="910be-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="910be-111">Description</span></span>                                                                                                                                         |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="910be-112">SystemDefaultEUDCFont</span><span class="sxs-lookup"><span data-stu-id="910be-112">SystemDefaultEUDCFont</span></span>    | <span data-ttu-id="910be-113">Vordefinierter Name, der zum Festlegen der Standardschriftart des Systems verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="910be-113">Predefined name used to set the system default font.</span></span> <span data-ttu-id="910be-114">Es gibt keine EUDC-Standardschriftart des Systems, es sei denn, dieser Eintrag ist explizit angegeben.</span><span class="sxs-lookup"><span data-stu-id="910be-114">There is no system default EUDC font unless this entry is explicitly specified.</span></span>     |
| <span data-ttu-id="910be-115">TrueTypeFontTypeface</span><span class="sxs-lookup"><span data-stu-id="910be-115">TrueTypeFontTypeface</span></span>     | <span data-ttu-id="910be-116">Benutzerdefinierter Name, der einer Nicht-EUDC TrueType-Schriftart zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="910be-116">User-defined name associated with a non-EUDC TrueType font.</span></span>                                                                              |
| <span data-ttu-id="910be-117">TrueTypeEUDCFontFileName</span><span class="sxs-lookup"><span data-stu-id="910be-117">TrueTypeEUDCFontFileName</span></span> | <span data-ttu-id="910be-118">Eine Zeichenfolge, die aus dem Dateinamen einer separaten EUDC-Schriftartdatei besteht.</span><span class="sxs-lookup"><span data-stu-id="910be-118">String consisting of the file name of a separate EUDC font file.</span></span> <span data-ttu-id="910be-119">Diese Datei identifiziert eine Schriftart, die TrueTypeFontTypeface zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="910be-119">This file identifies a font to be associated with TrueTypeFontTypeface.</span></span> |



 

<span data-ttu-id="910be-120">Das folgende Beispiel zeigt den EUDC-Schlüssel für Codepage 932.</span><span class="sxs-lookup"><span data-stu-id="910be-120">The following example shows the EUDC key for code page 932.</span></span>


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



<span data-ttu-id="910be-121">Im folgenden Beispiel wird die EUDC-Standardschriftart des Systems auf Eudc.ttf festgelegt, und die separaten EUDC-Schriftarten Mineudc.ttf und Goteudc.ttf werden den Schriftartnamen MS Mincho bzw. MS Solleezugetrennt.</span><span class="sxs-lookup"><span data-stu-id="910be-121">The following example sets the system default EUDC font to be Eudc.ttf and associates the separate EUDC fonts Mineudc.ttf and Goteudc.ttf with the font names MS Mincho and MS Gothic, respectively.</span></span>


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



<span data-ttu-id="910be-122">Wenn die Windows-Codepage (System ACP), die der Sprache für Nicht-Unicode-Programme zugeordnet ist, dem Unterschlüssel entspricht, sucht das GDI-Subsystem nach den Unterschlüssel-Wertpaaren, um Anzeigeinformationen zum Zeichen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="910be-122">When the Windows code page (system ACP) associated with the language for non-Unicode programs matches the subkey, the GDI subsystem looks to the subkey value pairs to obtain display information about the character.</span></span> <span data-ttu-id="910be-123">Zunächst wird nach einem Namen für die aktuelle Schriftart sucht.</span><span class="sxs-lookup"><span data-stu-id="910be-123">It first looks for a name matching the current font.</span></span> <span data-ttu-id="910be-124">Wenn keines der Fall ist, wird der SystemDefaultEUDCFont-Wert untersucht.</span><span class="sxs-lookup"><span data-stu-id="910be-124">If there is none, it examines the SystemDefaultEUDCFont value.</span></span> <span data-ttu-id="910be-125">Wenn kein Wert definiert ist, behandelt GDI das Zeichen als nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="910be-125">If no value is defined, GDI treats the character as undefined.</span></span>

<span data-ttu-id="910be-126">Beachten Sie, dass der Text selbst nicht in der Windows-Codepage enthalten sein muss.</span><span class="sxs-lookup"><span data-stu-id="910be-126">Note that the text itself does not have to be in the Windows code page.</span></span> <span data-ttu-id="910be-127">Angenommen, die Codepage hat den Bezeichner 1252, die Windows-Standardcodepage für Englisch.</span><span class="sxs-lookup"><span data-stu-id="910be-127">For example, assume that the code page has the identifier 1252, the default Windows code page for English.</span></span> <span data-ttu-id="910be-128">Eine Anwendung übergibt den einzelnen Unicode-Codepunkt U+E000 im privaten Unicode-Verwendungsbereich (PUA) an [**DrawText.**](/windows/win32/api/winuser/nf-winuser-drawtext)</span><span class="sxs-lookup"><span data-stu-id="910be-128">An application passes the single Unicode code point U+E000, in the Unicode private use area (PUA), to [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span></span> <span data-ttu-id="910be-129">In diesem Fall untersucht GDI die Registrierungswerte unter 1252, um die Schriftartinformationen für die Zeichenanzeigeeigenschaften zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="910be-129">In this case, GDI looks at the registry values under 1252 to obtain the font information for the character display properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="910be-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="910be-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="910be-131">EUDC-Registrierungseinträge</span><span class="sxs-lookup"><span data-stu-id="910be-131">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="910be-132">EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="910be-132">EUDCCodeRange</span></span>](eudccoderange.md)
</dt> </dl>

 

 
