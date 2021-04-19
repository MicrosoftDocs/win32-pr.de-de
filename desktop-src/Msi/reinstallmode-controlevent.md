---
description: Ermöglicht es dem Autor, den Validierungs Modus oder die Modi während einer erneuten Installation anzugeben, während das aktuelle Dialogfeld ausgeführt wird.
ms.assetid: d7cd41c6-c019-49d6-b593-a1d31c8f5a81
title: REINSTALLMODE-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ff5ff662b2880a3f4ab0fb79738b49cdeeccd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349843"
---
# <a name="reinstallmode-controlevent"></a><span data-ttu-id="cc833-103">REINSTALLMODE-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="cc833-103">ReinstallMode ControlEvent</span></span>

<span data-ttu-id="cc833-104">Der REINSTALLMODE-controleventermöglicht es dem Autor, den Validierungs Modus oder die Modi während einer erneuten Installation anzugeben, während das aktuelle Dialogfeld ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc833-104">The ReinstallMode ControlEventallows the author to specify the validation mode or modes during a reinstallation, and while the current dialog box is running.</span></span>

<span data-ttu-id="cc833-105">Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md) Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="cc833-105">This event can be published by a [PushButton Control](pushbutton-control.md) or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="cc833-106">Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden und erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc833-106">This event should be authored into the [ControlEvent table](controlevent-table.md), and requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="cc833-107">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cc833-107">This event does not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="cc833-108">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="cc833-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="cc833-109">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="cc833-109">Published By</span></span>

<span data-ttu-id="cc833-110">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="cc833-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="cc833-111">Argument</span><span class="sxs-lookup"><span data-stu-id="cc833-111">Argument</span></span>

<span data-ttu-id="cc833-112">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cc833-112">A string.</span></span> <span data-ttu-id="cc833-113">Eine Liste möglicher Werte finden Sie unter [**REINSTALLMODE**](reinstallmode.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cc833-113">For a list of possible values, see [**REINSTALLMODE**](reinstallmode.md) property.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="cc833-114">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="cc833-114">Action on Subscribers</span></span>

<span data-ttu-id="cc833-115">Diese ControlEvent führt keine Aktion für Abonnenten aus.</span><span class="sxs-lookup"><span data-stu-id="cc833-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="cc833-116">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="cc833-116">Typical Use</span></span>

<span data-ttu-id="cc833-117">Dieses Ereignis ist an ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem modalen Dialogfeld gebunden.</span><span class="sxs-lookup"><span data-stu-id="cc833-117">This event is tied to a [PushButton](pushbutton-control.md) control on a modal dialog box.</span></span> <span data-ttu-id="cc833-118">Das gleiche [PUSHBUTTON](pushbutton-control.md) -Steuerelement sollte auch an eine [neuinstallationscontrolevent](reinstall-controlevent.md) gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="cc833-118">The same [PushButton](pushbutton-control.md) control should also be tied to a [Reinstall](reinstall-controlevent.md) ControlEvent.</span></span>

 

 



