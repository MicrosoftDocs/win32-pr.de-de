---
title: Pager-Steuerelement Stile (kommctrl. h)
description: In diesem Abschnitt werden die zum Erstellen von Pager-Steuerelementen verwendeten Fenster Stile aufgelistet.
ms.assetid: 619fd8cc-e231-41af-8744-a29d14f2c6f8
topic_type:
- apiref
api_name:
- PGS_AUTOSCROLL
- PGS_DRAGNDROP
- PGS_HORZ
- PGS_VERT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496737f714ecb58c0d5a349207114cbf338e2c54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372034"
---
# <a name="pager-control-styles"></a><span data-ttu-id="deedc-103">Pager-Steuerelement Stile</span><span class="sxs-lookup"><span data-stu-id="deedc-103">Pager Control Styles</span></span>

<span data-ttu-id="deedc-104">In diesem Abschnitt werden die zum Erstellen von Pager-Steuerelementen verwendeten Fenster Stile aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="deedc-104">This section lists the window styles used when creating pager controls.</span></span>



| <span data-ttu-id="deedc-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="deedc-105">Constant</span></span>                                                                                                                                                         | <span data-ttu-id="deedc-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="deedc-106">Description</span></span>                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGS_AUTOSCROLL"></span><span id="pgs_autoscroll"></span><dl> <span data-ttu-id="deedc-107"><dt>**PGS \_ AutoScroll**</dt></span><span class="sxs-lookup"><span data-stu-id="deedc-107"><dt>**PGS\_AUTOSCROLL**</dt></span></span> </dl> | <span data-ttu-id="deedc-108">Das Pager-Steuerelement führt einen Bildlauf durch, wenn der Benutzer mit der Maus auf eine der Bild Lauf Schaltflächen zeigt.</span><span class="sxs-lookup"><span data-stu-id="deedc-108">The pager control will scroll when the user hovers the mouse over one of the scroll buttons.</span></span><br/>                                                                                                                     |
| <span id="PGS_DRAGNDROP"></span><span id="pgs_dragndrop"></span><dl> <span data-ttu-id="deedc-109"><dt>**PGS- \_ DragNDrop**</dt></span><span class="sxs-lookup"><span data-stu-id="deedc-109"><dt>**PGS\_DRAGNDROP**</dt></span></span> </dl>    | <span data-ttu-id="deedc-110">Das enthaltene Fenster kann ein Drag & Drop-Ziel sein.</span><span class="sxs-lookup"><span data-stu-id="deedc-110">The contained window can be a drag-and-drop target.</span></span> <span data-ttu-id="deedc-111">Das Pager-Steuerelement führt automatisch einen Bildlauf durch, wenn ein Element von außerhalb des Pager über eine der Bild Lauf Schaltflächen hinausgezogen wird.</span><span class="sxs-lookup"><span data-stu-id="deedc-111">The pager control will automatically scroll if an item is dragged from outside the pager over one of the scroll buttons.</span></span><br/>                                     |
| <span id="PGS_HORZ"></span><span id="pgs_horz"></span><dl> <span data-ttu-id="deedc-112"><dt>**PGS \_ Horz**</dt></span><span class="sxs-lookup"><span data-stu-id="deedc-112"><dt>**PGS\_HORZ**</dt></span></span> </dl>                   | <span data-ttu-id="deedc-113">Erstellt ein Pager-Steuerelement, für das horizontal ein Bildlauf ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="deedc-113">Creates a pager control that can be scrolled horizontally.</span></span> <span data-ttu-id="deedc-114">Dieser Stil und der **PGS \_** -Stil "Vert" schließen sich gegenseitig aus und können nicht kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="deedc-114">This style and the **PGS\_VERT** style are mutually exclusive and cannot be combined.</span></span><br/>                                                                 |
| <span id="PGS_VERT"></span><span id="pgs_vert"></span><dl> <span data-ttu-id="deedc-115"><dt>**PGS- \_ Vert**</dt></span><span class="sxs-lookup"><span data-stu-id="deedc-115"><dt>**PGS\_VERT**</dt></span></span> </dl>                   | <span data-ttu-id="deedc-116">Erstellt ein Pager-Steuerelement, für das eine vertikale Bildlauf ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="deedc-116">Creates a pager control that can be scrolled vertically.</span></span> <span data-ttu-id="deedc-117">Dies ist die Standardrichtung, wenn kein Richtungs Format angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="deedc-117">This is the default direction if no direction style is specified.</span></span> <span data-ttu-id="deedc-118">Dieser Stil und der **PGS- \_ Horz** -Stil schließen sich gegenseitig aus und können nicht kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="deedc-118">This style and the **PGS\_HORZ** style are mutually exclusive and cannot be combined.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="deedc-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="deedc-119">Requirements</span></span>



| <span data-ttu-id="deedc-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="deedc-120">Requirement</span></span> | <span data-ttu-id="deedc-121">Wert</span><span class="sxs-lookup"><span data-stu-id="deedc-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="deedc-122">Header</span><span class="sxs-lookup"><span data-stu-id="deedc-122">Header</span></span><br/> | <dl> <span data-ttu-id="deedc-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="deedc-123"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





