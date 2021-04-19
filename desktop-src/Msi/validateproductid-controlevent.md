---
description: Das ValidateProductID-Ereignis legt die ProductID-Eigenschaft auf die vollständige Produkt-ID fest. Wenn die Überprüfung nicht erfolgreich ist, werden mit diesem Ereignis eine Fehlermeldung und ein modales Dialogfeld für einen Benutzereintrag der Produkt-ID angezeigt.
ms.assetid: 44002cae-154a-4938-a15c-456c293e94fb
title: ValidateProductID ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b86cacfc4561fe9e4d94436724b42a78d3d8792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355519"
---
# <a name="validateproductid-controlevent"></a><span data-ttu-id="815ab-104">ValidateProductID ControlEvent</span><span class="sxs-lookup"><span data-stu-id="815ab-104">ValidateProductID ControlEvent</span></span>

<span data-ttu-id="815ab-105">Das ValidateProductID-Ereignis legt die [**ProductID-**](productid.md) Eigenschaft auf die vollständige Produkt-ID fest.</span><span class="sxs-lookup"><span data-stu-id="815ab-105">The ValidateProductID event sets the [**ProductID**](productid.md) property to the full Product ID.</span></span> <span data-ttu-id="815ab-106">Wenn die Überprüfung nicht erfolgreich ist, werden mit diesem Ereignis eine Fehlermeldung und ein modales Dialogfeld für einen Benutzereintrag der Produkt-ID angezeigt.</span><span class="sxs-lookup"><span data-stu-id="815ab-106">If the validation is unsuccessful, then this event puts up an error message and modal dialog box for a user entry of the Product ID.</span></span>

<span data-ttu-id="815ab-107">Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="815ab-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="815ab-108">Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="815ab-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="815ab-109">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="815ab-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="815ab-110">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="815ab-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="815ab-111">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="815ab-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="815ab-112">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="815ab-112">Published By</span></span>

<span data-ttu-id="815ab-113">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="815ab-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="815ab-114">Argument</span><span class="sxs-lookup"><span data-stu-id="815ab-114">Argument</span></span>

<span data-ttu-id="815ab-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="815ab-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="815ab-116">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="815ab-116">Action on Subscribers</span></span>

<span data-ttu-id="815ab-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="815ab-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="815ab-118">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="815ab-118">Typical Use</span></span>

<span data-ttu-id="815ab-119">Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem modalen Dialogfeld ist an dieses Ereignis gebunden und wird verwendet, um den Benutzereintrag der Produkt-ID zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="815ab-119">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event and is used to check the user's entry of the Product ID.</span></span> <span data-ttu-id="815ab-120">Wenn der Benutzereintrag gültig ist, wird das nächste Dialogfeld geöffnet.</span><span class="sxs-lookup"><span data-stu-id="815ab-120">If the user's entry is valid, then the next dialog box will open.</span></span>

 

 



