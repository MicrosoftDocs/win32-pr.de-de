---
title: Flatscrollleiste
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die zum Steuern von flatscrollleisten verwendet werden.
ms.assetid: vs|controls|~\controls\flatsb\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e611e8d5755d119a8c24bdbccb9f10408d3d7d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855715"
---
# <a name="flat-scroll-bar"></a><span data-ttu-id="ca318-103">Flatscrollleiste</span><span class="sxs-lookup"><span data-stu-id="ca318-103">Flat Scroll Bar</span></span>

<span data-ttu-id="ca318-104">Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die zum Steuern von flatscrollleisten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca318-104">This section contains information about the programming elements used to control flat scroll bars.</span></span>

### <a name="overviews"></a><span data-ttu-id="ca318-105">Übersichten</span><span class="sxs-lookup"><span data-stu-id="ca318-105">Overviews</span></span>



| <span data-ttu-id="ca318-106">Thema</span><span class="sxs-lookup"><span data-stu-id="ca318-106">Topic</span></span>                                    | <span data-ttu-id="ca318-107">Inhalte</span><span class="sxs-lookup"><span data-stu-id="ca318-107">Contents</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca318-108">Flache Scrollleisten</span><span class="sxs-lookup"><span data-stu-id="ca318-108">Flat Scroll Bars</span></span>](flat-scroll-bars.md) | <span data-ttu-id="ca318-109">Microsoft Internet Explorer 4,0 führte eine neue visuelle Technologie mit dem Namen "flatscrollleisten" ein.</span><span class="sxs-lookup"><span data-stu-id="ca318-109">Microsoft Internet Explorer 4.0 introduced a new visual technology called flat scroll bars.</span></span> <span data-ttu-id="ca318-110">Funktionale, flache Schiebe leisten Verhalten sich genau wie Standard Scrollleisten.</span><span class="sxs-lookup"><span data-stu-id="ca318-110">Functionally, flat scroll bars behave just like standard scroll bars.</span></span> <span data-ttu-id="ca318-111">Der Unterschied besteht darin, dass Sie Ihre Darstellung in größerem Umfang als Standard Scrollleisten anpassen können.</span><span class="sxs-lookup"><span data-stu-id="ca318-111">The difference is that you can customize their appearance to a greater extent than standard scroll bars.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="ca318-112">Functions</span><span class="sxs-lookup"><span data-stu-id="ca318-112">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca318-113">Thema</span><span class="sxs-lookup"><span data-stu-id="ca318-113">Topic</span></span></th>
<th><span data-ttu-id="ca318-114">Inhalte</span><span class="sxs-lookup"><span data-stu-id="ca318-114">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ca318-115"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="ca318-115"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a></span></span></td>
<td><span data-ttu-id="ca318-116">Aktiviert oder deaktiviert eine oder beide Richtungs Schaltflächen der flatscrollleiste.</span><span class="sxs-lookup"><span data-stu-id="ca318-116">Enables or disables one or both flat scroll bar direction buttons.</span></span> <span data-ttu-id="ca318-117">Wenn für das Fenster keine flatscrollleisten initialisiert werden, ruft diese Funktion die Standardfunktion <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>enablescrollbar</strong></a> auf.</span><span class="sxs-lookup"><span data-stu-id="ca318-117">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca318-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="ca318-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a></span></span></td>
<td><span data-ttu-id="ca318-119">Ruft die Informationen für eine flatscrollleiste ab.</span><span class="sxs-lookup"><span data-stu-id="ca318-119">Gets the information for a flat scroll bar.</span></span> <span data-ttu-id="ca318-120">Wenn für das Fenster keine flatscrollleisten initialisiert werden, ruft diese Funktion die standardmäßige <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>getscrollinfo</strong></a> -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="ca318-120">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca318-121"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a></span><span class="sxs-lookup"><span data-stu-id="ca318-121"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a></span></span></td>
<td><span data-ttu-id="ca318-122">Ruft die Ziehpunkt Position in einer flachen Bild Lauf Leiste ab.</span><span class="sxs-lookup"><span data-stu-id="ca318-122">Gets the thumb position in a flat scroll bar.</span></span> <span data-ttu-id="ca318-123">Wenn für das Fenster keine flatscrollleisten initialisiert werden, ruft diese Funktion die standardmäßige <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>getscrollpos</strong></a> -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="ca318-123">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca318-124"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="ca318-124"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a></span></span></td>
<td><span data-ttu-id="ca318-125">Ruft die Eigenschaften für eine flatscrollleiste ab.</span><span class="sxs-lookup"><span data-stu-id="ca318-125">Gets the properties for a flat scroll bar.</span></span> <span data-ttu-id="ca318-126">Diese Funktion kann auch verwendet werden, um zu bestimmen, ob <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>initializeflatsb</strong></a> für dieses Fenster aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="ca318-126">This function can also be used to determine if <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> has been called for this window.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca318-127"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a></span><span class="sxs-lookup"><span data-stu-id="ca318-127"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a></span></span></td>
<td><span data-ttu-id="ca318-128">Ruft die Eigenschaften für eine flatscrollleiste ab.</span><span class="sxs-lookup"><span data-stu-id="ca318-128">Gets the properties for a flat scroll bar.</span></span> <span data-ttu-id="ca318-129">Diese Funktion kann auch verwendet werden, um zu bestimmen, ob <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>initializeflatsb</strong></a> für dieses Fenster aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="ca318-129">This function can also be used to determine if <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> has been called for this window.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="ca318-130">Dies ist mit <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>identisch.</span><span class="sxs-lookup"><span data-stu-id="ca318-130">This is identical to <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca318-131"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="ca318-131"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a></span></span></td>
<td><span data-ttu-id="ca318-132">Ruft den Bild Laufbereich für eine flatscrollleiste ab.</span><span class="sxs-lookup"><span data-stu-id="ca318-132">Gets the scroll range for a flat scroll bar.</span></span> <span data-ttu-id="ca318-133">Wenn für das Fenster keine flatscrollleisten initialisiert werden, ruft diese Funktion die standardmäßige <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>getscrollrange</strong></a> -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="ca318-133">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca318-134"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="ca318-134"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a></span></span></td>
<td><span data-ttu-id="ca318-135">Legt die Informationen für eine flache Bild Lauf Leiste fest.</span><span class="sxs-lookup"><span data-stu-id="ca318-135">Sets the information for a flat scroll bar.</span></span> <span data-ttu-id="ca318-136">Wenn für das Fenster keine flatscrollleisten initialisiert werden, ruft diese Funktion die Standardfunktion " <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>setScrollInfo</strong></a> " auf.</span><span class="sxs-lookup"><span data-stu-id="ca318-136">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca318-137"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a></span><span class="sxs-lookup"><span data-stu-id="ca318-137"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a></span></span></td>
<td><span data-ttu-id="ca318-138">Legt die aktuelle Position des Zieh Punkts auf einer flachen Bild Lauf Leiste fest.</span><span class="sxs-lookup"><span data-stu-id="ca318-138">Sets the current position of the thumb in a flat scroll bar.</span></span> <span data-ttu-id="ca318-139">Wenn für das Fenster keine flatscrollleisten initialisiert werden, ruft diese Funktion die Standardfunktion <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>setscrollpos</strong></a> auf.</span><span class="sxs-lookup"><span data-stu-id="ca318-139">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca318-140"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a></span><span class="sxs-lookup"><span data-stu-id="ca318-140"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a></span></span></td>
<td><span data-ttu-id="ca318-141">Legt die Eigenschaften für eine flache Bild Lauf Leiste fest.</span><span class="sxs-lookup"><span data-stu-id="ca318-141">Sets the properties for a flat scroll bar.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca318-142"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="ca318-142"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a></span></span></td>
<td><span data-ttu-id="ca318-143">Legt den scrollbereich einer flachen Bild Lauf Leiste fest.</span><span class="sxs-lookup"><span data-stu-id="ca318-143">Sets the scroll range of a flat scroll bar.</span></span> <span data-ttu-id="ca318-144">Wenn für das Fenster keine flatscrollleisten initialisiert werden, ruft diese Funktion die Standardfunktion <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>setscrollrange</strong></a> auf.</span><span class="sxs-lookup"><span data-stu-id="ca318-144">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca318-145"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="ca318-145"><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a></span></span></td>
<td><span data-ttu-id="ca318-146">Zeigt eine flache Schiebe Leiste an oder blendet sie aus.</span><span class="sxs-lookup"><span data-stu-id="ca318-146">Shows or hides a flat scroll bar.</span></span> <span data-ttu-id="ca318-147">Wenn für das Fenster keine flatscrollleisten initialisiert werden, ruft diese Funktion die Standardfunktion " <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollbar</strong></a> " auf.</span><span class="sxs-lookup"><span data-stu-id="ca318-147">If flat scroll bars are not initialized for the window, this function calls the standard <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca318-148"><a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>Initializeflatsb</strong></a></span><span class="sxs-lookup"><span data-stu-id="ca318-148"><a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a></span></span></td>
<td><span data-ttu-id="ca318-149">Initialisiert flatscrollleisten für ein bestimmtes Fenster.</span><span class="sxs-lookup"><span data-stu-id="ca318-149">Initializes flat scroll bars for a particular window.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca318-150"><a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>Uninitializeflatsb</strong></a></span><span class="sxs-lookup"><span data-stu-id="ca318-150"><a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a></span></span></td>
<td><span data-ttu-id="ca318-151">Hebt die Initialisierung der flatscrollleisten für ein bestimmtes Fenster auf.</span><span class="sxs-lookup"><span data-stu-id="ca318-151">Uninitializes flat scroll bars for a particular window.</span></span> <span data-ttu-id="ca318-152">Das angegebene Fenster wird auf Standard Scrollleisten zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="ca318-152">The specified window will revert to standard scroll bars.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

 

 





