---
title: Informationen über Syslink-Steuerelemente
description: Bei einem Syslink-Steuerelement handelt es sich um ein Fenster, das markierten Text rendert und die Anwendung benachrichtigt, wenn Benutzer auf Ihre eingebetteten Hyperlinks klicken. Dieses Steuerelement stellt eine bequeme Alternative zum Verwenden der Befehls Link Schaltfläche dar. Weitere Informationen finden Sie unter Schaltflächen Typen.
ms.assetid: 38cfac3d-de60-4882-a434-4f498330b77d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deb0d15cac479b844b0ea8510c34cc57f56822be
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039671"
---
# <a name="about-syslink-controls"></a><span data-ttu-id="ed8fe-105">Informationen über Syslink-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="ed8fe-105">About SysLink Controls</span></span>

<span data-ttu-id="ed8fe-106">Bei einem Syslink-Steuerelement handelt es sich um ein Fenster, das markierten Text rendert und die Anwendung benachrichtigt, wenn Benutzer auf Ihre eingebetteten Hyperlinks klicken.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-106">A SysLink control is a window that renders marked-up text, and notifies the application when users click its embedded hyperlinks.</span></span> <span data-ttu-id="ed8fe-107">Dieses Steuerelement stellt eine bequeme Alternative zum Verwenden der [**Befehls Link Schaltfläche**](button-styles.md)dar.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-107">This control provides a convenient alternative to using the [**Command link button**](button-styles.md).</span></span> <span data-ttu-id="ed8fe-108">Weitere Informationen finden Sie unter [Schaltflächen Typen](button-types-and-styles.md).</span><span class="sxs-lookup"><span data-stu-id="ed8fe-108">For more information, see [Button Types](button-types-and-styles.md).</span></span>

<span data-ttu-id="ed8fe-109">Jedes Syslink-Steuerelement kann mehrere Hyperlinks unterstützen, und Sie können auf jeden Link über einen NULL basierten Index zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-109">Each SysLink control can support multiple hyperlinks, and you can access each hyperlink through a zero-based index.</span></span> <span data-ttu-id="ed8fe-110">Das Syslink-Steuerelement wird in der ComCtl32.dll Version 6 definiert und erfordert ein Manifest oder eine Direktive, die angibt, dass Version 6 der dll verwendet werden soll, wenn Sie verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-110">The SysLink control is defined in the ComCtl32.dll version 6, and it requires a manifest or directive that specifies that version 6 of the DLL should be used if it is available.</span></span> <span data-ttu-id="ed8fe-111">Weitere Informationen finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ed8fe-111">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

<span data-ttu-id="ed8fe-112">Dieser Artikel enthält folgende Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-112">This article contains the following sections.</span></span>

-   [<span data-ttu-id="ed8fe-113">Syslink-Markup</span><span class="sxs-lookup"><span data-stu-id="ed8fe-113">SysLink Markup</span></span>](#syslink-markup)
-   [<span data-ttu-id="ed8fe-114">Verknüpfungs Attribute</span><span class="sxs-lookup"><span data-stu-id="ed8fe-114">Link Attributes</span></span>](#link-attributes)
-   [<span data-ttu-id="ed8fe-115">Link Zustände</span><span class="sxs-lookup"><span data-stu-id="ed8fe-115">Link States</span></span>](#link-states)
-   [<span data-ttu-id="ed8fe-116">Einschränkungen bei der bidirektionalen Text Anzeige</span><span class="sxs-lookup"><span data-stu-id="ed8fe-116">Limitations on Bidirectional Text Display</span></span>](#limitations-on-bidirectional-text-display)

## <a name="syslink-markup"></a><span data-ttu-id="ed8fe-117">Syslink-Markup</span><span class="sxs-lookup"><span data-stu-id="ed8fe-117">SysLink Markup</span></span>

<span data-ttu-id="ed8fe-118">Das Syslink-Steuerelement unterstützt das Anchor-Tag ( &lt; a &gt; ) zusammen mit den Attributen **href** und **ID**.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-118">The SysLink control supports the anchor tag(&lt;a&gt;) along with the attributes **HREF** and **ID**.</span></span> <span data-ttu-id="ed8fe-119">Ein **href** kann ein beliebiges Protokoll sein, z. b. http, FTP und mailto.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-119">An **HREF** can be any protocol, such as http, ftp, and mailto.</span></span> <span data-ttu-id="ed8fe-120">Eine **ID** ist ein optionaler Name, der innerhalb eines Syslink-Steuer Elements eindeutig ist und mit einem einzelnen Link verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-120">An **ID** is an optional name, unique within a SysLink control, and it is associated with an individual link.</span></span> <span data-ttu-id="ed8fe-121">Links wird auch ein NULL basierter Index gemäß ihrer Position innerhalb der Zeichenfolge zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-121">Links are also assigned a zero-based index according to their position within the string.</span></span> <span data-ttu-id="ed8fe-122">Dieser Index wird für den Zugriff auf einen Link verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-122">This index is used to access a link.</span></span>

## <a name="link-attributes"></a><span data-ttu-id="ed8fe-123">Verknüpfungs Attribute</span><span class="sxs-lookup"><span data-stu-id="ed8fe-123">Link Attributes</span></span>

<span data-ttu-id="ed8fe-124">Die Attribute jedes Links können entweder innerhalb des Anker Tags für die einzelnen Links oder durch Senden der [**LM- \_ SetItem**](lm-setitem.md) -Nachricht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-124">Each link's attributes can be set either within the anchor tag for each link or by sending the [**LM\_SETITEM**](lm-setitem.md) message.</span></span> <span data-ttu-id="ed8fe-125">Durch Festlegen eines Attributs durch Angabe in der Initialisierungs Zeichenfolge wird der Wert lediglich initialisiert.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-125">Setting an attribute by specifying it within the initialization string merely initializes the value.</span></span> <span data-ttu-id="ed8fe-126">Sie können den Wert eines Attributs durch nachfolgende Verwendung der **LM- \_** Nachricht nach dem Festlegen der Nachricht ändern.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-126">You can change the value of an attribute through subsequent use of the **LM\_SETITEM** message.</span></span>

## <a name="link-states"></a><span data-ttu-id="ed8fe-127">Link Zustände</span><span class="sxs-lookup"><span data-stu-id="ed8fe-127">Link States</span></span>

<span data-ttu-id="ed8fe-128">Verknüpfungs Elemente können einen von drei Zuständen aufweisen, die durch die-Flags in der folgenden Tabelle dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-128">Link items can be in any one of three states, represented by the flags in the following table.</span></span>



| <span data-ttu-id="ed8fe-129">Statusflag</span><span class="sxs-lookup"><span data-stu-id="ed8fe-129">State flag</span></span>   | <span data-ttu-id="ed8fe-130">Darstellung und Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ed8fe-130">Appearance and meaning</span></span>                                            |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="ed8fe-131">LIS im \_ Fokus</span><span class="sxs-lookup"><span data-stu-id="ed8fe-131">LIS\_FOCUSED</span></span> | <span data-ttu-id="ed8fe-132">Der Link hat den Tastaturfokus, und durch Drücken der EINGABETASTE wird er aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-132">The link has the keyboard focus, and pressing Enter activates it.</span></span> |
| <span data-ttu-id="ed8fe-133">LIS \_ aktiviert</span><span class="sxs-lookup"><span data-stu-id="ed8fe-133">LIS\_ENABLED</span></span> | <span data-ttu-id="ed8fe-134">Der Link ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-134">The link is enabled.</span></span>                                              |
| <span data-ttu-id="ed8fe-135">LIS \_ besucht</span><span class="sxs-lookup"><span data-stu-id="ed8fe-135">LIS\_VISITED</span></span> | <span data-ttu-id="ed8fe-136">Der Benutzer hat die durch den Link dargestellte URL bereits besucht.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-136">The user has already visited the URL represented by the link.</span></span>     |



 

## <a name="limitations-on-bidirectional-text-display"></a><span data-ttu-id="ed8fe-137">Einschränkungen bei der bidirektionalen Text Anzeige</span><span class="sxs-lookup"><span data-stu-id="ed8fe-137">Limitations on Bidirectional Text Display</span></span>

<span data-ttu-id="ed8fe-138">Einige Sprachen, z. b. Arabisch oder Hebräisch, werden von rechts nach links (RTL) geschrieben. Englisch wird von links nach rechts (LTR) geschrieben.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-138">Some languages, such as Arabic or Hebrew, are written right-to-left (RTL); English is written left-to-right (LTR).</span></span> <span data-ttu-id="ed8fe-139">Das Kombinieren von RTL mit Ltr heißt bidirektionaler Text.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-139">Combining RTL with LTR is called bidirectional text.</span></span> <span data-ttu-id="ed8fe-140">Wenn Sie in Ressourcen Zeichenfolgen als bidirektionale Fluss Marker, die den Ablauf von Zeichen folgen steuern, eine Kombination aus LTR-und RTL-Unicode-oder HTML-direktionalen Markup-Konstrukten durchführen</span><span class="sxs-lookup"><span data-stu-id="ed8fe-140">Mixing LTR and RTL Unicode or HTML directional markup constructs in resource strings, as bidirectional flow markers to control the flow of strings, may not produce the expected result when using a SysLink control.</span></span> <span data-ttu-id="ed8fe-141">Beispielsweise kann ein mit Ltr markierten Satz im RTL-Kontext nicht ordnungsgemäß angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-141">For instance, an LTR-marked sentence may not display correctly in RTL context.</span></span>

> [!Note]  
> <span data-ttu-id="ed8fe-142">Syslink-Steuerelemente unterstützen nicht die bidirektionale Anzeige in allen Szenarien.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-142">SysLink controls do not support bidirectional display under all scenarios.</span></span> <span data-ttu-id="ed8fe-143">Verwenden Sie ein Syslink-Steuerelement nur, wenn Sie wissen, dass ein einfaches ltr-oder RTL-Layout ausreichend ist.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-143">Use a SysLink control only if you know that a simple LTR or RTL layout is adequate.</span></span> <span data-ttu-id="ed8fe-144">Andernfalls sollten Sie die Verwendung einer erweiterten Technologie wie [MSHTML](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85))in Erwägung gezogen.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-144">Otherwise, consider using a more advanced technology such as [MSHTML](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85)).</span></span>

 

 

 