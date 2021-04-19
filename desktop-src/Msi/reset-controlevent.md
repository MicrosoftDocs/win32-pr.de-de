---
description: Das Dialogfeld wird zurückgesetzt. Anders ausgedrückt werden alle Steuerelemente im Dialogfeld aufgerufen, um die von Ihnen durchgeführten Eigenschaften Änderungen rückgängig zu machen. Dieses Ereignis setzt alle Eigenschaftswerte auf die Elemente zurück, die beim Erstellen des Dialog Felds aufgetreten sind.
ms.assetid: 6449abb8-54cb-4400-9eb2-b7e7f1564747
title: ControlEvent zurücksetzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889f1b0f984f14b7522707db4ffbd958bff9c32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349300"
---
# <a name="reset-controlevent"></a><span data-ttu-id="e7dd3-105">ControlEvent zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="e7dd3-105">Reset ControlEvent</span></span>

<span data-ttu-id="e7dd3-106">Das Dialogfeld wird zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-106">The dialog box is reset.</span></span> <span data-ttu-id="e7dd3-107">Anders ausgedrückt werden alle Steuerelemente im Dialogfeld aufgerufen, um die von Ihnen durchgeführten Eigenschaften Änderungen rückgängig zu machen.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-107">In other words, all the controls on the dialog box are called to undo the property changes they have performed.</span></span> <span data-ttu-id="e7dd3-108">Dieses Ereignis setzt alle Eigenschaftswerte auf die Elemente zurück, die beim Erstellen des Dialog Felds aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-108">This event resets all the property values to what they were when the dialog box was created.</span></span>

<span data-ttu-id="e7dd3-109">Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-109">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="e7dd3-110">Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-110">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="e7dd3-111">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-111">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="e7dd3-112">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e7dd3-112">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="e7dd3-113">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="e7dd3-113">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="e7dd3-114">Es gibt einen Fall, der in der Praxis selten auftreten sollte und von diesem ControlEvent nicht ordnungsgemäß behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-114">There is a case, which should occur rarely in practice, that is not handled properly by this ControlEvent.</span></span> <span data-ttu-id="e7dd3-115">Wenn im gleichen Dialogfeld zwei oder mehr Steuerelemente vorhanden sind, die indirekt mit der gleichen Eigenschaft verknüpft sind, und mindestens eine von Ihnen mit einer anderen Eigenschaft begonnen hat, wird dieser Eigenschafts Wert manchmal auf den zweiten Wert zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-115">If there are two or more controls on the same dialog box linked indirectly to the same property and at least one of them started having some other property, then this property value will sometimes be reset to its second value.</span></span>

## <a name="published-by"></a><span data-ttu-id="e7dd3-116">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="e7dd3-116">Published By</span></span>

<span data-ttu-id="e7dd3-117">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-117">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="e7dd3-118">Argument</span><span class="sxs-lookup"><span data-stu-id="e7dd3-118">Argument</span></span>

<span data-ttu-id="e7dd3-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-119">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="e7dd3-120">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="e7dd3-120">Action on Subscribers</span></span>

<span data-ttu-id="e7dd3-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-121">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="e7dd3-122">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="e7dd3-122">Typical Use</span></span>

<span data-ttu-id="e7dd3-123">Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem modalen Dialogfeld wird verwendet, um alle Werte im Dialogfeld zurückzusetzen und alle Änderungen auf der Seite abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-123">A [PushButton](pushbutton-control.md) control on a modal dialog box is used to reset all the values on the dialog box and to cancel all the changes on the page.</span></span>

 

 



