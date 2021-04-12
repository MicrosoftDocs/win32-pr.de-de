---
title: Titelleiste (MSAA UI-Element Referenz)
description: Die Titelleiste am oberen Rand eines Fensters zeigt ein Anwendungs definiertes Symbol und eine Textzeile an.
ms.assetid: f41ab777-6c94-4d8e-b743-c635e93df396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fee3642a67be85b27eac6a73ac7c452f2349d1
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104389788"
---
# <a name="title-bar-msaa-ui-element-reference"></a><span data-ttu-id="4cd29-103">Titelleiste (MSAA UI-Element Referenz)</span><span class="sxs-lookup"><span data-stu-id="4cd29-103">Title Bar (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="4cd29-104">In diesem Thema werden **Titel** leisten Objekte für den MSAA-Benutzeroberflächen-Element Verweis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4cd29-104">This topic describes **Title Bar** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="4cd29-105">Das Erstellen von **Titel** leisten Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4cd29-105">How to create **Title Bar** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="4cd29-106">Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.</span><span class="sxs-lookup"><span data-stu-id="4cd29-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="4cd29-107">Die Titelleiste am oberen Rand eines Fensters zeigt ein Anwendungs definiertes Symbol und eine Textzeile an.</span><span class="sxs-lookup"><span data-stu-id="4cd29-107">The title bar at the top of a window displays an application-defined icon and line of text.</span></span> <span data-ttu-id="4cd29-108">Der Text gibt den Namen der Anwendung an und gibt den Zweck des Fensters an.</span><span class="sxs-lookup"><span data-stu-id="4cd29-108">The text specifies the name of the application and indicates the purpose of the window.</span></span> <span data-ttu-id="4cd29-109">Die Titelleiste ermöglicht es dem Benutzer auch, das Fenster mit einer Maus oder einem anderen Zeigegerät zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="4cd29-109">The title bar also makes it possible for the user to move the window using a mouse or other pointing device.</span></span>

<span data-ttu-id="4cd29-110">Titelleisten enthalten mindestens drei kleine Schaltflächen zum minimieren, maximieren oder wiederherstellen und zum Schließen des Fensters, das mit der Titelleiste verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="4cd29-110">Title bars contain at least three small buttons that minimize, maximize or restore, and close the window associated with the title bar.</span></span> <span data-ttu-id="4cd29-111">Titelleisten enthalten außerdem eine kontextabhängige Hilfe Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="4cd29-111">Title bars also contain a context-sensitive Help button.</span></span> <span data-ttu-id="4cd29-112">Anwendungen, die in der Far-East Version des Windows-Betriebssystems ausgeführt werden, können auch Schaltflächen für Eingabemethoden-Editor (IME) enthalten.</span><span class="sxs-lookup"><span data-stu-id="4cd29-112">Applications running in the Far-East version of the Windows operating system may also contain Input Method Editor (IME) buttons.</span></span> <span data-ttu-id="4cd29-113">Microsoft Active Accessibility macht diese Schaltflächen als untergeordnete Elemente der Titelleiste verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4cd29-113">Microsoft Active Accessibility exposes these buttons as child elements of the title bar.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="4cd29-114">IAccessible-Methoden</span><span class="sxs-lookup"><span data-stu-id="4cd29-114">IAccessible Methods</span></span>

<span data-ttu-id="4cd29-115">Titelleisten unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="4cd29-115">Title bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="4cd29-116">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="4cd29-116">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="4cd29-117">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="4cd29-117">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="4cd29-118">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="4cd29-118">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="4cd29-119">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="4cd29-119">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="4cd29-120">IAccessible-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4cd29-120">IAccessible Properties</span></span>

<span data-ttu-id="4cd29-121">Titelleisten unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4cd29-121">Title bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4cd29-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4cd29-122">Property</span></span></th>
<th><span data-ttu-id="4cd29-123">Kommentare</span><span class="sxs-lookup"><span data-stu-id="4cd29-123">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4cd29-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="4cd29-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span></span></td>
<td><span data-ttu-id="4cd29-125">Die <strong>childCount</strong> -Eigenschaft ist 5.</span><span class="sxs-lookup"><span data-stu-id="4cd29-125">The <strong>ChildCount</strong> property is five.</span></span> <span data-ttu-id="4cd29-126">Die <strong>childCount</strong> -Eigenschaft enthält die Schaltflächen IME und kontextabhängige Hilfe, auch wenn Sie nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4cd29-126">The <strong>ChildCount</strong> property includes the IME and context-sensitive Help buttons even when they are not displayed.</span></span> <span data-ttu-id="4cd29-127">Schaltflächen, die nicht angezeigt werden, haben die Eigenschaft <strong>State</strong> <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4cd29-127">Buttons that are not displayed have the <strong>State</strong> property <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4cd29-128"><strong>get_accDescription</strong></span><span class="sxs-lookup"><span data-stu-id="4cd29-128"><strong>get_accDescription</strong></span></span></td>
<td><span data-ttu-id="4cd29-129">Die <strong>Description</strong> -Eigenschaft der Titelleiste selbst ist: &quot; zeigt den Namen des Fensters an und enthält Steuerelemente zum Bearbeiten. &quot; Die untergeordneten Schaltflächen in der Titelleiste haben folgende Beschreibungen:</span><span class="sxs-lookup"><span data-stu-id="4cd29-129">The <strong>Description</strong> property of the title bar itself is: &quot;Displays the name of the window and contains controls to manipulate it.&quot; The child buttons in the title bar have the following descriptions:</span></span><br/>
<ul>
<li><span data-ttu-id="4cd29-130">&quot;Verschiebt das Fenster aus</span><span class="sxs-lookup"><span data-stu-id="4cd29-130">&quot;Moves the window out of</span></span></li>
<li><span data-ttu-id="4cd29-131">&quot;Macht das Fenster voll</span><span class="sxs-lookup"><span data-stu-id="4cd29-131">&quot;Makes the window full</span></span></li>
<li><span data-ttu-id="4cd29-132">&quot;Legt eine minimierte oder</span><span class="sxs-lookup"><span data-stu-id="4cd29-132">&quot;Puts a minimized or</span></span></li>
<li><span data-ttu-id="4cd29-133">&quot;Schließt das Fenster.&quot;</span><span class="sxs-lookup"><span data-stu-id="4cd29-133">&quot;Closes the window&quot;</span></span></li>
<li><span data-ttu-id="4cd29-134">&quot;Gibt einen Kontext ein oder verlässt ihn:</span><span class="sxs-lookup"><span data-stu-id="4cd29-134">&quot;Enters or leaves context-</span></span></li>
<li><span data-ttu-id="4cd29-135">&quot;Zeigt die Tastatur beim Drücken an&quot;</span><span class="sxs-lookup"><span data-stu-id="4cd29-135">&quot;Brings up the keyboard when pressed&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4cd29-136"><strong>get_accName</strong></span><span class="sxs-lookup"><span data-stu-id="4cd29-136"><strong>get_accName</strong></span></span></td>
<td><span data-ttu-id="4cd29-137">Die <strong>Name</strong> -Eigenschaft wird von der Titelleiste selbst nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4cd29-137">The title bar itself does not support the <strong>Name</strong> property.</span></span> <span data-ttu-id="4cd29-138">Die untergeordneten Schaltflächen in der Titelleiste haben die folgenden Namen:</span><span class="sxs-lookup"><span data-stu-id="4cd29-138">The child buttons in the title bar have the following names:</span></span>
<ul>
<li><span data-ttu-id="4cd29-139">&quot;Minimieren&quot;</span><span class="sxs-lookup"><span data-stu-id="4cd29-139">&quot;Minimize&quot;</span></span></li>
<li><span data-ttu-id="4cd29-140">&quot;Maximieren &quot; oder &quot; Wiederherstellen &quot; ,</span><span class="sxs-lookup"><span data-stu-id="4cd29-140">&quot;Maximize&quot; or &quot;Restore&quot;,</span></span></li>
<li><span data-ttu-id="4cd29-141">&quot;Close&quot;</span><span class="sxs-lookup"><span data-stu-id="4cd29-141">&quot;Close&quot;</span></span></li>
<li><span data-ttu-id="4cd29-142">&quot;Kontexthilfe&quot;</span><span class="sxs-lookup"><span data-stu-id="4cd29-142">&quot;Context help&quot;</span></span></li>
<li><span data-ttu-id="4cd29-143">&quot;IME&quot;</span><span class="sxs-lookup"><span data-stu-id="4cd29-143">&quot;IME&quot;</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4cd29-144"><strong>get_accParent</strong></span><span class="sxs-lookup"><span data-stu-id="4cd29-144"><strong>get_accParent</strong></span></span></td>
<td><span data-ttu-id="4cd29-145">Die <strong>Parent</strong> -Eigenschaft der Titelleiste ist das Hauptanwendungsfenster ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ), das denselben Anwendungs definierten Fenster Klassennamen wie die Titelleiste hat.</span><span class="sxs-lookup"><span data-stu-id="4cd29-145">The <strong>Parent</strong> property of the title bar is the main application window ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ) that has the same application-defined window class name as the title bar.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4cd29-146"><strong>get_accRole</strong></span><span class="sxs-lookup"><span data-stu-id="4cd29-146"><strong>get_accRole</strong></span></span></td>
<td><span data-ttu-id="4cd29-147">Die <strong>Role</strong> -Eigenschaft ist <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4cd29-147">The <strong>Role</strong> property is <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>.</span></span> <span data-ttu-id="4cd29-148">In den untergeordneten Schaltflächen in der Titelleiste ist die <strong>Role</strong> -Eigenschaft <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4cd29-148">The child buttons in the title bar have the <strong>Role</strong> property <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4cd29-149"><strong>get_accState</strong></span><span class="sxs-lookup"><span data-stu-id="4cd29-149"><strong>get_accState</strong></span></span></td>
<td><span data-ttu-id="4cd29-150">Die <strong>State</strong> -Eigenschaft für die Titelleiste und die untergeordneten Schaltflächen können eine Kombination aus einem oder mehreren der folgenden <a href="object-state-constants.md">Werte</a>sein: <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="4cd29-150">The <strong>State</strong> property for the title bar and the child buttons can be a combination of one or more of the following <a href="object-state-constants.md">values</a>: <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4cd29-151"><strong>get_accValue</strong></span><span class="sxs-lookup"><span data-stu-id="4cd29-151"><strong>get_accValue</strong></span></span></td>
<td><span data-ttu-id="4cd29-152">Die <strong>value</strong> -Eigenschaft ist eine Zeichenfolge, die dem in der Titelleiste angezeigten Text entspricht.</span><span class="sxs-lookup"><span data-stu-id="4cd29-152">The <strong>Value</strong> property is a string that is the same as the text displayed in the title bar.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a><span data-ttu-id="4cd29-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="4cd29-153">Notes</span></span>

-   <span data-ttu-id="4cd29-154">Obwohl die Titelleiste einer Anwendung **das State-** eigenschaftflag **für das Zustands** System als [**\_ \_ focverwendbare**](object-state-constants.md)Eigenschaft aufweist, hat Sie niemals das Statusflag [**State \_ System \_ fokussiert**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4cd29-154">Although an application's title bar has the **State** property flag [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md), it never has the **State** flag [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md).</span></span> <span data-ttu-id="4cd29-155">Beim Festlegen des Fokus auf ein Titelleisten Objekt wird das Anwendungsfenster fokussiert.</span><span class="sxs-lookup"><span data-stu-id="4cd29-155">Setting focus to a title bar object focuses the application window.</span></span>
-   <span data-ttu-id="4cd29-156">Da das Titelleisten Objekt [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)nicht unterstützt, sind die Schaltflächen auf der Titelleiste einfache Elemente.</span><span class="sxs-lookup"><span data-stu-id="4cd29-156">Because the title bar object does not support [**get\_accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild), the buttons on the title bar are simple elements.</span></span> <span data-ttu-id="4cd29-157">Die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle selbst wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4cd29-157">They do not support the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface themselves.</span></span> <span data-ttu-id="4cd29-158">Das Titelleisten Objekt enthält Informationen zu diesen untergeordneten Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="4cd29-158">The title bar object provides information about these child buttons.</span></span>
-   <span data-ttu-id="4cd29-159">Da Titelleisten keinen Fokus erhalten und keine Standardaktion haben, werden die Methoden [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) und [**get \_ accdefaultaction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) für dieses Steuerelement nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4cd29-159">Because title bars do not get focus and have no default action, the [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) and [**get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) methods are not supported for this control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cd29-160">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4cd29-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cd29-161">IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4cd29-161">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





