---
description: 'Die Syntax für das SetProperty-Ereignis unterscheidet sich von anderen ControlEvents anstelle des Namens des Ereignisses, wobei die Eigenschaft in eckige Klammern gesetzt wird: \[ Eigenschafts \_ Name \] .'
ms.assetid: a8e80d14-8d62-4398-9e53-9a0119a62d70
title: SetProperty-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59326ddd9f576b4871de7c232318ffcdcdb4fb36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373159"
---
# <a name="setproperty-controlevent"></a><span data-ttu-id="dad2d-103">SetProperty-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="dad2d-103">SetProperty ControlEvent</span></span>

<span data-ttu-id="dad2d-104">Die Syntax für das SetProperty-Ereignis unterscheidet sich von anderen ControlEvents anstelle des Namens des Ereignisses, wobei die Eigenschaft in eckige Klammern gesetzt wird: \[ Eigenschafts \_ Name \] .</span><span class="sxs-lookup"><span data-stu-id="dad2d-104">The syntax for the SetProperty event is different than for other ControlEvents In place of the name of the event one puts the property in square brackets: \[property\_name\].</span></span> <span data-ttu-id="dad2d-105">Das-Argument ist der neue Wert der-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dad2d-105">The argument is the new value of the property.</span></span> <span data-ttu-id="dad2d-106">Zum Deaktivieren der-Eigenschaft muss das-Argument lauten {} .</span><span class="sxs-lookup"><span data-stu-id="dad2d-106">To unset the property, the argument must be {}.</span></span> <span data-ttu-id="dad2d-107">Dies ist erforderlich, da das-Argument ein Primärschlüssel in der Tabelle ist und daher nicht NULL sein kann.</span><span class="sxs-lookup"><span data-stu-id="dad2d-107">This is necessary, because the argument is a primary key in the table and so cannot be null.</span></span> <span data-ttu-id="dad2d-108">Das-Argument wird mit der formattext-Methode formatiert, daher kann das-Argument jeden beliebigen Ausdruck enthalten, der von der formattext-Methode behandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="dad2d-108">The argument will be formatted using the FormatText method, therefore the argument can contain any expression that the FormatText method can handle.</span></span> <span data-ttu-id="dad2d-109">Die Eigenschaftswerte werden zum Zeitpunkt des ControlEvent ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="dad2d-109">The property values are evaluated at the moment of the ControlEvent.</span></span>

<span data-ttu-id="dad2d-110">Dieses Ereignis kann durch ein [PUSHBUTTON-Steuer](pushbutton-control.md)Element, ein [CheckBox-Steuer](checkbox-control.md)Element oder ein [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="dad2d-110">This event can be published by a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="dad2d-111">Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="dad2d-111">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="dad2d-112">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dad2d-112">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="dad2d-113">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="dad2d-113">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="dad2d-114">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="dad2d-114">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="dad2d-115">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="dad2d-115">Published By</span></span>

<span data-ttu-id="dad2d-116">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="dad2d-116">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="dad2d-117">Argument</span><span class="sxs-lookup"><span data-stu-id="dad2d-117">Argument</span></span>

<span data-ttu-id="dad2d-118">Der neue Wert der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dad2d-118">The new value of the property.</span></span> <span data-ttu-id="dad2d-119">{} für NULL.</span><span class="sxs-lookup"><span data-stu-id="dad2d-119">{} for null.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="dad2d-120">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="dad2d-120">Action on Subscribers</span></span>

<span data-ttu-id="dad2d-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="dad2d-121">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="dad2d-122">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="dad2d-122">Typical Use</span></span>

<span data-ttu-id="dad2d-123">Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem Dialogfeld, das mit diesem Ereignis verknüpft ist, sodass eine Eigenschaft geändert wird, wenn die Schaltfläche gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="dad2d-123">A [PushButton](pushbutton-control.md) control on a dialog box linked to this event so it changes a property when the button is pushed.</span></span>

 

 



