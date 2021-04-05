---
title: So implementieren Sie mehrzeilige Quick Infos
description: Mehrzeilige Quick Infos ermöglichen das Anzeigen von Text in mehr als einer Zeile.
ms.assetid: 62B10B44-C1C2-4C86-8648-AE6B606BACBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d6f32d638b2d33ea6270aa5f8ce2c09f0f4174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708663"
---
# <a name="how-to-implement-multiline-tooltips"></a><span data-ttu-id="72eda-103">So implementieren Sie mehrzeilige Quick Infos</span><span class="sxs-lookup"><span data-stu-id="72eda-103">How to Implement Multiline Tooltips</span></span>

<span data-ttu-id="72eda-104">Mehrzeilige Quick Infos ermöglichen das Anzeigen von Text in mehr als einer Zeile.</span><span class="sxs-lookup"><span data-stu-id="72eda-104">Multiline tooltips allow text to be displayed on more than one line.</span></span>

<span data-ttu-id="72eda-105">Sie werden von [Version 4,70](common-control-versions.md) und höher der allgemeinen Steuerelemente unterstützt.</span><span class="sxs-lookup"><span data-stu-id="72eda-105">They are supported by [version 4.70](common-control-versions.md) and later of the common controls.</span></span> <span data-ttu-id="72eda-106">Die Anwendung erstellt eine mehrzeilige QuickInfo, indem eine [**TTM- \_ SetMaxTipWidth**](ttm-setmaxtipwidth.md) -Meldung gesendet wird, die die Breite des Anzeige Rechtecks angibt.</span><span class="sxs-lookup"><span data-stu-id="72eda-106">Your application creates a multiline tooltip by sending a [**TTM\_SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md) message, specifying the width of the display rectangle.</span></span> <span data-ttu-id="72eda-107">Text, der diese Breite überschreitet, wird in die nächste Zeile umschlossen, anstatt den Anzeigebereich zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="72eda-107">Text that exceeds this width wraps to the next line rather than widening the display region.</span></span> <span data-ttu-id="72eda-108">Die Rechtecks Höhe wird nach Bedarf erweitert, um den zusätzlichen Zeilen Rechnung zu tragen.</span><span class="sxs-lookup"><span data-stu-id="72eda-108">The rectangle height is increased as needed to accommodate the additional lines.</span></span> <span data-ttu-id="72eda-109">Das QuickInfo-Steuerelement umschließt die Linien automatisch, oder Sie können eine Kombination aus Wagen Rücklauf/Zeilenvorschub, \\ r \\ n, verwenden, um Zeilenumbrüche an bestimmten Positionen zu erzwingen</span><span class="sxs-lookup"><span data-stu-id="72eda-109">The tooltip control wraps the lines automatically, or you can use a carriage return/line feed combination, \\r\\n, to force line breaks at particular locations.</span></span>

<span data-ttu-id="72eda-110">Die resultierende Anzeige wird in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="72eda-110">The resulting display is shown in the following illustration.</span></span>

![Screenshot eines Dialog Felds mit einer QuickInfo, die Text wie einen mehrzeiligen Absatz enthält](images/tt-multiline.png)

> [!Note]  
> <span data-ttu-id="72eda-112">Der Text Puffer, der vom **szText** -Member der [**nmttdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) -Struktur angegeben wird, kann nur 80 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="72eda-112">The text buffer specified by the **szText** member of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure can accommodate only 80 characters.</span></span> <span data-ttu-id="72eda-113">Wenn Sie eine längere Zeichenfolge verwenden müssen, verweisen Sie auf den **lpszText** -Member von **nmttdispinfo** auf einen Puffer, der den gewünschten Text enthält.</span><span class="sxs-lookup"><span data-stu-id="72eda-113">If you need to use a longer string, point the **lpszText** member of **NMTTDISPINFO** to a buffer containing the desired text.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="72eda-114">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="72eda-114">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="72eda-115">Technologien</span><span class="sxs-lookup"><span data-stu-id="72eda-115">Technologies</span></span>

-   [<span data-ttu-id="72eda-116">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="72eda-116">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="72eda-117">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="72eda-117">Prerequisites</span></span>

-   <span data-ttu-id="72eda-118">C/C++</span><span class="sxs-lookup"><span data-stu-id="72eda-118">C/C++</span></span>
-   <span data-ttu-id="72eda-119">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="72eda-119">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="72eda-120">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="72eda-120">Instructions</span></span>

### <a name="implement-multiline-tooltips"></a><span data-ttu-id="72eda-121">Implementieren von mehrzeiligen Quick Infos</span><span class="sxs-lookup"><span data-stu-id="72eda-121">Implement Multiline Tooltips</span></span>

<span data-ttu-id="72eda-122">Das folgende Code Fragment ist ein Beispiel für einen einfachen [TTN \_ getdispinfo](ttn-getdispinfo.md) -Benachrichtigungs Handler.</span><span class="sxs-lookup"><span data-stu-id="72eda-122">The following code fragment is an example of a simple [TTN\_GETDISPINFO](ttn-getdispinfo.md) notification handler.</span></span> <span data-ttu-id="72eda-123">Dadurch wird eine mehrzeilige QuickInfo aktiviert, indem das Anzeige Rechteck auf 150 Pixel festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="72eda-123">It enables a multiline tooltip by setting the display rectangle to 150 pixels.</span></span> <span data-ttu-id="72eda-124">Ein manueller Zeilenumbruch wird nach dem ersten Wort eingefügt, um anzuzeigen, dass Zeilenumbrüche schwierig und weich sind.</span><span class="sxs-lookup"><span data-stu-id="72eda-124">A manual line break is inserted after the first word to show that line breaks can be hard as well as soft.</span></span>


```C++
    case WM_NOTIFY:
    {
        switch (((LPNMHDR)lParam)->code)
        {
        case TTN_GETDISPINFO:
            LPNMTTDISPINFO pInfo = (LPNMTTDISPINFO)lParam;
            SendMessage(pInfo->hdr.hwndFrom, TTM_SETMAXTIPWIDTH, 0, 150);
            wcscpy_s(pInfo->szText, ARRAYSIZE(pInfo->szText), 
                L"This\nis a very long text string " \
                L"that must be broken into several lines.");
            break;
        }
        break;
    }
```



## <a name="related-topics"></a><span data-ttu-id="72eda-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="72eda-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72eda-126">Verwenden von Quick Infos</span><span class="sxs-lookup"><span data-stu-id="72eda-126">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




