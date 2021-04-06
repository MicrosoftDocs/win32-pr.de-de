---
title: SysLink
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit Syslink-Steuerelementen verwendet werden.
ms.assetid: 13a7b6d0-4bf1-480f-b447-838a550a5866
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9bbfaea9b86c2d8dc42c84d050e5bec997ceb18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947556"
---
# <a name="syslink"></a><span data-ttu-id="3e737-103">SysLink</span><span class="sxs-lookup"><span data-stu-id="3e737-103">SysLink</span></span>

<span data-ttu-id="3e737-104">Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit Syslink-Steuerelementen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e737-104">This section contains information about the programming elements used with SysLink controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="3e737-105">Übersichten</span><span class="sxs-lookup"><span data-stu-id="3e737-105">Overviews</span></span>



| <span data-ttu-id="3e737-106">Thema</span><span class="sxs-lookup"><span data-stu-id="3e737-106">Topic</span></span>                                    | <span data-ttu-id="3e737-107">Inhalte</span><span class="sxs-lookup"><span data-stu-id="3e737-107">Contents</span></span>                                                                                       |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e737-108">Syslink-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="3e737-108">SysLink Controls</span></span>](syslink-overview.md) | <span data-ttu-id="3e737-109">Das Syslink-Steuerelement stellt eine bequeme Möglichkeit zum Einbetten von Hypertext-Links in einem Fenster dar.</span><span class="sxs-lookup"><span data-stu-id="3e737-109">The SysLink control provides a convenient way to embed hypertext links in a window.</span></span><br/> |



 

### <a name="messages"></a><span data-ttu-id="3e737-110">Meldungen</span><span class="sxs-lookup"><span data-stu-id="3e737-110">Messages</span></span>



| <span data-ttu-id="3e737-111">Thema</span><span class="sxs-lookup"><span data-stu-id="3e737-111">Topic</span></span>                                           | <span data-ttu-id="3e737-112">Inhalte</span><span class="sxs-lookup"><span data-stu-id="3e737-112">Contents</span></span>                                                                             |
|-------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e737-113">**LM- \_ getidealheight**</span><span class="sxs-lookup"><span data-stu-id="3e737-113">**LM\_GETIDEALHEIGHT**</span></span>](lm-getidealheight.md) | <span data-ttu-id="3e737-114">Ruft die bevorzugte Höhe eines Links für die aktuelle Breite des Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="3e737-114">Retrieves the preferred height of a link for the control's current width.</span></span><br/> |
| [<span data-ttu-id="3e737-115">**LM- \_ getidealsize**</span><span class="sxs-lookup"><span data-stu-id="3e737-115">**LM\_GETIDEALSIZE**</span></span>](lm-getidealsize.md)     | <span data-ttu-id="3e737-116">Ruft die bevorzugte Höhe eines Links für die aktuelle Breite des Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="3e737-116">Retrieves the preferred height of a link for the control's current width.</span></span><br/> |
| [<span data-ttu-id="3e737-117">**LM- \_ GetItem**</span><span class="sxs-lookup"><span data-stu-id="3e737-117">**LM\_GETITEM**</span></span>](lm-getitem.md)               | <span data-ttu-id="3e737-118">Ruft die Zustände und Attribute eines Elements ab.</span><span class="sxs-lookup"><span data-stu-id="3e737-118">Retrieves the states and attributes of an item.</span></span><br/>                           |
| [<span data-ttu-id="3e737-119">**LM- \_ HitTest**</span><span class="sxs-lookup"><span data-stu-id="3e737-119">**LM\_HITTEST**</span></span>](lm-hittest.md)               | <span data-ttu-id="3e737-120">Bestimmt, ob der Benutzer auf den angegebenen Link geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="3e737-120">Determines whether the user clicked the specified link.</span></span><br/>                   |
| [<span data-ttu-id="3e737-121">**LM \_ -Element**</span><span class="sxs-lookup"><span data-stu-id="3e737-121">**LM\_SETITEM**</span></span>](lm-setitem.md)               | <span data-ttu-id="3e737-122">Legt die Zustände und Attribute eines Elements fest.</span><span class="sxs-lookup"><span data-stu-id="3e737-122">Sets the states and attributes of an item.</span></span><br/>                                |



 

### <a name="structures"></a><span data-ttu-id="3e737-123">Strukturen</span><span class="sxs-lookup"><span data-stu-id="3e737-123">Structures</span></span>



| <span data-ttu-id="3e737-124">Thema</span><span class="sxs-lookup"><span data-stu-id="3e737-124">Topic</span></span>                                | <span data-ttu-id="3e737-125">Inhalte</span><span class="sxs-lookup"><span data-stu-id="3e737-125">Contents</span></span>                                                                                                                                                                           |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e737-126">**Lhittestinfo**</span><span class="sxs-lookup"><span data-stu-id="3e737-126">**LHITTESTINFO**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lhittestinfo) | <span data-ttu-id="3e737-127">Wird verwendet, um Informationen über den Link zu erhalten, der einem bestimmten Speicherort entspricht.</span><span class="sxs-lookup"><span data-stu-id="3e737-127">Used to get information about the link corresponding to a given location.</span></span> <br/>                                                                                              |
| [<span data-ttu-id="3e737-128">**LItem**</span><span class="sxs-lookup"><span data-stu-id="3e737-128">**LITEM**</span></span>](/windows/win32/api/commctrl/ns-commctrl-litem)               | <span data-ttu-id="3e737-129">Wird verwendet, um Informationen zu einem Link Element festzulegen und abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3e737-129">Used to set and retrieve information about a link item.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="3e737-130">**Nmlink**</span><span class="sxs-lookup"><span data-stu-id="3e737-130">**NMLINK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlink)             | <span data-ttu-id="3e737-131">Der [**nmlink**](/windows/win32/api/commctrl/ns-commctrl-nmlink) enthält Benachrichtigungs Informationen.</span><span class="sxs-lookup"><span data-stu-id="3e737-131">The [**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) Contains notification information.</span></span> <span data-ttu-id="3e737-132">Senden Sie diese Struktur mit den [nm- \_ Click](nm-click-syslink.md) -oder [nm- \_ Rückgabe](nm-return.md) Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="3e737-132">Send this structure with the [NM\_CLICK](nm-click-syslink.md) or [NM\_RETURN](nm-return.md) messages.</span></span><br/> |



 

 

 





