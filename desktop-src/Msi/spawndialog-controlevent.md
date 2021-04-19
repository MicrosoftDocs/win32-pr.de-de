---
description: Das handlevent spawndialog benachrichtigt den Installer, ein untergeordnetes Element eines modalen Dialog Felds zu erstellen, während das vorhandene Dialogfeld weiterhin ausgeführt wird.
ms.assetid: 2a341039-60dd-4e6c-9ef3-bf482ca53917
title: Spawndialog-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71aec632332a87d047913b618aa2c39843849e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346688"
---
# <a name="spawndialog-controlevent"></a><span data-ttu-id="c69f3-103">Spawndialog-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="c69f3-103">SpawnDialog ControlEvent</span></span>

<span data-ttu-id="c69f3-104">Das handlevent spawndialog benachrichtigt den Installer, ein untergeordnetes Element eines modalen Dialog Felds zu erstellen, während das vorhandene Dialogfeld weiterhin ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c69f3-104">The SpawnDialog ControlEvent notifies the installer to create a child of a modal dialog box while keeping the present dialog box running.</span></span>

<span data-ttu-id="c69f3-105">Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="c69f3-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="c69f3-106">Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c69f3-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="c69f3-107">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c69f3-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="c69f3-108">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c69f3-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="c69f3-109">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="c69f3-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="c69f3-110">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="c69f3-110">Published By</span></span>

<span data-ttu-id="c69f3-111">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="c69f3-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="c69f3-112">Argument</span><span class="sxs-lookup"><span data-stu-id="c69f3-112">Argument</span></span>

<span data-ttu-id="c69f3-113">Eine Zeichenfolge, bei der es sich um den Namen des neuen Dialog Felds handelt.</span><span class="sxs-lookup"><span data-stu-id="c69f3-113">A string that is the name of the new dialog box.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="c69f3-114">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="c69f3-114">Action on Subscribers</span></span>

<span data-ttu-id="c69f3-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="c69f3-115">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="c69f3-116">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="c69f3-116">Typical Use</span></span>

<span data-ttu-id="c69f3-117">Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem modalen Dialogfeld ist an dieses Ereignis in der Tabelle [ControlEvent](controlevent-table.md) gebunden, um ein untergeordnetes Dialogfeld zu erstellen, z. b. "möchten Sie den Vorgang wirklich abbrechen?"</span><span class="sxs-lookup"><span data-stu-id="c69f3-117">A [PushButton](pushbutton-control.md) control on a modal dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to create a child dialog, such as an "Are you sure you want to cancel?"</span></span> <span data-ttu-id="c69f3-118">.</span><span class="sxs-lookup"><span data-stu-id="c69f3-118">dialog box.</span></span>

 

 



