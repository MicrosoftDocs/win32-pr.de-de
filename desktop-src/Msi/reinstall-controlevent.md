---
description: Ermöglicht dem Autor das Initiieren einer Neuinstallation einiger oder aller Features, während das aktuelle Dialogfeld ausgeführt wird.
ms.assetid: bc667f20-3abe-4ef3-b51e-dc74da63f651
title: ControlEvent neu installieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d2adece3f89dbe57b77f2345d1714ece64b271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350207"
---
# <a name="reinstall-controlevent"></a><span data-ttu-id="27baa-103">ControlEvent neu installieren</span><span class="sxs-lookup"><span data-stu-id="27baa-103">Reinstall ControlEvent</span></span>

<span data-ttu-id="27baa-104">Mit der installieren Sie controleventkann der Autor eine Neuinstallation einiger oder aller Features initiieren, während das aktuelle Dialogfeld ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27baa-104">The Reinstall ControlEventallows the author to initiate a reinstall of some or all features, while the current dialog box is running.</span></span>

<span data-ttu-id="27baa-105">Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md) Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="27baa-105">This event can be published by a [PushButton control](pushbutton-control.md) or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="27baa-106">Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden und erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27baa-106">This event should be authored into the [ControlEvent table](controlevent-table.md), and requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="27baa-107">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="27baa-107">This event does not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="27baa-108">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="27baa-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="27baa-109">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="27baa-109">Published By</span></span>

<span data-ttu-id="27baa-110">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="27baa-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="27baa-111">Argument</span><span class="sxs-lookup"><span data-stu-id="27baa-111">Argument</span></span>

<span data-ttu-id="27baa-112">Eine Zeichenfolge, die entweder der Name der Funktion oder "All" ist.</span><span class="sxs-lookup"><span data-stu-id="27baa-112">A string that is either the name of the feature or "ALL".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="27baa-113">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="27baa-113">Action on Subscribers</span></span>

<span data-ttu-id="27baa-114">Diese ControlEvent führt keine Aktion für Abonnenten aus.</span><span class="sxs-lookup"><span data-stu-id="27baa-114">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="27baa-115">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="27baa-115">Typical Use</span></span>

<span data-ttu-id="27baa-116">Dieses Ereignis ist an ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem modalen Dialogfeld gebunden.</span><span class="sxs-lookup"><span data-stu-id="27baa-116">This event is tied to a [PushButton](pushbutton-control.md) control on a modal dialog box.</span></span> <span data-ttu-id="27baa-117">Das gleiche [PUSHBUTTON](pushbutton-control.md) -Steuerelement sollte auch an eine [REINSTALLMODE](reinstallmode-controlevent.md) -ControlEvent gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="27baa-117">The same [PushButton](pushbutton-control.md) control should also be tied to a [ReinstallMode](reinstallmode-controlevent.md) ControlEvent.</span></span>

 

 



