---
title: Caretzeichen (MSAA-Benutzeroberflächen Element-Referenz)
description: Die Einfügemarke ist eine blinkende Linie, ein Block oder eine Bitmap im Client Bereich eines Fensters oder in einem Steuerelement, das Tastatureingaben annimmt.
ms.assetid: f2c48c36-1859-4e0a-8833-3ca90b4da323
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3855e4825c6c8b8498f0b4b278a099452baa9d
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "103857944"
---
# <a name="caret-msaa-ui-element-reference"></a><span data-ttu-id="79c78-103">Caretzeichen (MSAA-Benutzeroberflächen Element-Referenz)</span><span class="sxs-lookup"><span data-stu-id="79c78-103">Caret (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="79c78-104">In diesem Thema werden die Einfügevorgänge für die MSAA-Benutzeroberflächen Element Referenz beschrieben.</span><span class="sxs-lookup"><span data-stu-id="79c78-104">This topic describes carets for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="79c78-105">Die Verwendung von Caretzeichen in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="79c78-105">How to use carets in various UI frameworks is not described here.</span></span> <span data-ttu-id="79c78-106">Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.</span><span class="sxs-lookup"><span data-stu-id="79c78-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="79c78-107">Die Einfügemarke ist eine blinkende Linie, ein Block oder eine Bitmap im Client Bereich eines Fensters oder in einem Steuerelement, das Tastatureingaben annimmt.</span><span class="sxs-lookup"><span data-stu-id="79c78-107">The caret is a flashing line, block, or bitmap in the client area of a window or in a control that accepts keyboard input.</span></span> <span data-ttu-id="79c78-108">Gibt den Ort an, an dem Text oder Grafiken eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="79c78-108">It indicates the place at which text or graphics are inserted.</span></span> <span data-ttu-id="79c78-109">Da jeweils nur ein Fenster den Tastaturfokus besitzt, gibt es nur eine Einfügemarke im System.</span><span class="sxs-lookup"><span data-stu-id="79c78-109">Because only one window at a time has the keyboard focus, there is only one caret in the system.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="79c78-110">IAccessible-Methoden</span><span class="sxs-lookup"><span data-stu-id="79c78-110">IAccessible Methods</span></span>

<span data-ttu-id="79c78-111">Der Caretzeichen unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="79c78-111">The caret supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="79c78-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="79c78-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="79c78-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="79c78-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a><span data-ttu-id="79c78-114">IAccessible-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="79c78-114">IAccessible Properties</span></span>

<span data-ttu-id="79c78-115">Die Einfügemarke unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="79c78-115">The caret supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="79c78-116">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="79c78-116">Property</span></span></th>
<th><span data-ttu-id="79c78-117">Kommentare</span><span class="sxs-lookup"><span data-stu-id="79c78-117">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="79c78-118"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="79c78-118"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span></span></td>
<td><span data-ttu-id="79c78-119">Die <strong>childCount</strong> -Eigenschaft ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="79c78-119">The <strong>ChildCount</strong> property is zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79c78-120"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a></span><span class="sxs-lookup"><span data-stu-id="79c78-120"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a></span></span></td>
<td><span data-ttu-id="79c78-121">Die <strong>Name</strong> -Eigenschaft ist " &quot; Edit" &quot; .</span><span class="sxs-lookup"><span data-stu-id="79c78-121">The <strong>Name</strong> property is &quot;Edit&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="79c78-122"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a></span><span class="sxs-lookup"><span data-stu-id="79c78-122"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a></span></span></td>
<td><span data-ttu-id="79c78-123">Die <strong>Role</strong> -Eigenschaft ist <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>.</span><span class="sxs-lookup"><span data-stu-id="79c78-123">The <strong>Role</strong> property is <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79c78-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a></span><span class="sxs-lookup"><span data-stu-id="79c78-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a></span></span></td>
<td><span data-ttu-id="79c78-125">Mögliche Werte für die <strong>State</strong> -Eigenschaft sind:</span><span class="sxs-lookup"><span data-stu-id="79c78-125">Possible values for the <strong>State</strong> property include:</span></span>
<ul>
<li><span data-ttu-id="79c78-126">NULL, was bedeutet, dass die Einfügemarke sichtbar ist</span><span class="sxs-lookup"><span data-stu-id="79c78-126">Zero, which means the caret is visible</span></span></li>
<li><span data-ttu-id="79c78-127"><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></span><span class="sxs-lookup"><span data-stu-id="79c78-127"><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a><span data-ttu-id="79c78-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="79c78-128">Notes</span></span>

-   <span data-ttu-id="79c78-129">Anders als andere Elemente der Benutzeroberfläche verfügt das Caretzeichen über kein zugeordnetes Fenster handle.</span><span class="sxs-lookup"><span data-stu-id="79c78-129">Unlike other UI elements, the caret object does not have an associated window handle.</span></span> <span data-ttu-id="79c78-130">Um Zugriff auf das Caretzeichen-Objekt zu erhalten, müssen Clients ein [*wineventproc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) festlegen und auf das Generieren von Ereignissen durch das Caretzeichen warten.</span><span class="sxs-lookup"><span data-stu-id="79c78-130">To obtain access to the caret object, clients must set a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) and wait for the caret object to generate events.</span></span>
-   <span data-ttu-id="79c78-131">Das Caretzeichen-Objekt im Rich Edit-Steuerelement, das von Riched20.dll bereitgestellt wird (das in Text-Editoren wie Microsoft WordPad in Windows 98 verwendet wird), sendet keine [WinEvents](winevents-infrastructure.md) , wenn seine Position während der Textauswahl geändert wird.</span><span class="sxs-lookup"><span data-stu-id="79c78-131">The caret object in the rich edit control provided by Riched20.dll (which is used in text editors such as Microsoft WordPad in Windows 98) does not send any [WinEvents](winevents-infrastructure.md) when its position is changed during text selection.</span></span> <span data-ttu-id="79c78-132">Wenn Benutzer die UMSCHALTTASTE und die Pfeiltasten drücken, um Text auszuwählen, löst das Caretzeichen Objekt das [**Ereignis \_ Objekt \_ locationchange**](event-constants.md) WinEvent nicht aus.</span><span class="sxs-lookup"><span data-stu-id="79c78-132">When users press SHIFT and arrow keys to select text, the caret object does not trigger the [**EVENT\_OBJECT\_LOCATIONCHANGE**](event-constants.md) WinEvent.</span></span> <span data-ttu-id="79c78-133">Wenn die Auswahlprogramm gesteuert durch Rich-Edit-Meldungen festgelegt wird, sendet das Caretzeichen-Objekt auch keine Ereignisse, um die neue Position anzugeben.</span><span class="sxs-lookup"><span data-stu-id="79c78-133">Similarly, when the selection is set programmatically through rich edit messages, the caret object does not send any events to indicate its new position.</span></span>

    <span data-ttu-id="79c78-134">Alle Anwendungen, die Riched20.dll verwenden, weisen dieses Problem auf.</span><span class="sxs-lookup"><span data-stu-id="79c78-134">All applications that use Riched20.dll exhibit this problem.</span></span> <span data-ttu-id="79c78-135">Anwendungen, die frühere Versionen des Rich Edit-Steuer Elements verwenden, senden Ereignisse auf der Grundlage der Auswahl ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="79c78-135">Applications using earlier versions of the rich edit control correctly send events based on the selection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79c78-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="79c78-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79c78-137">IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="79c78-137">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




