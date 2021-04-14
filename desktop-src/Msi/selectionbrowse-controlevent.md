---
description: Das SelectionTree-Steuerelement verwendet das selectionbrowse-Ereignis, um ein Dialogfeld zum Durchsuchen zu erzeugen, sodass es möglich ist, den Pfad des hervorgehobenen Elements zu ändern.
ms.assetid: 10a5af2e-3144-4b51-8295-294e56cdf801
title: Selectionbrowse-ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754f69f939f7c90dca705a2669a37af1fce0e79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350228"
---
# <a name="selectionbrowse-controlevent"></a><span data-ttu-id="7f58a-103">Selectionbrowse-ControlEvent</span><span class="sxs-lookup"><span data-stu-id="7f58a-103">SelectionBrowse ControlEvent</span></span>

<span data-ttu-id="7f58a-104">Das [SelectionTree-Steuer](selectiontree-control.md) Element verwendet das selectionbrowse-Ereignis, um ein Dialogfeld zum **Durchsuchen** zu erzeugen, sodass es möglich ist, den Pfad des hervorgehobenen Elements zu ändern.</span><span class="sxs-lookup"><span data-stu-id="7f58a-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionBrowse event to spawn a **Browse** dialog box making it possible to modify the path of the highlighted item.</span></span>

<span data-ttu-id="7f58a-105">Dieses Ereignis sollte von einem [PUSHBUTTON-Steuer](pushbutton-control.md) Element veröffentlicht werden, das sich im gleichen Dialogfeld befindet wie das Steuerelement, das dieses Ereignis abonniert.</span><span class="sxs-lookup"><span data-stu-id="7f58a-105">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="7f58a-106">Das Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7f58a-106">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="7f58a-107">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f58a-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="7f58a-108">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7f58a-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="7f58a-109">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="7f58a-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="7f58a-110">Alle Steuerelemente, die ein selectionbrowse-Ereignis veröffentlichen, werden deaktiviert, wenn eine Funktion ausgewählt wurde, die bereits installiert, nicht konfigurierbar oder nicht für die lokale Installation ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="7f58a-110">Any controls that publish a SelectionBrowse event become disabled if a feature has been selected that is already installed, not configurable, or not selected for local installation.</span></span> <span data-ttu-id="7f58a-111">Damit die Funktion konfiguriert werden kann, muss Sie über eine [öffentliche Eigenschaft](public-properties.md) verfügen, die in das Feld "Verzeichnis" \_ der [Funktions Tabelle](feature-table.md)eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7f58a-111">To be configurable, the feature must have a [public property](public-properties.md) entered in the Directory\_ field of the [Feature table](feature-table.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="7f58a-112">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="7f58a-112">Published By</span></span>

[<span data-ttu-id="7f58a-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="7f58a-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="7f58a-114">Argument</span><span class="sxs-lookup"><span data-stu-id="7f58a-114">Argument</span></span>

<span data-ttu-id="7f58a-115">Der Name des Dialog Felds, das erzeugt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f58a-115">The name of the dialog to be spawned.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="7f58a-116">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="7f58a-116">Action on Subscribers</span></span>

<span data-ttu-id="7f58a-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="7f58a-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="7f58a-118">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="7f58a-118">Typical Use</span></span>

<span data-ttu-id="7f58a-119">Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement im gleichen modalen Dialogfeld wie die SelectionTree verwendet dieses Ereignis, um das Dialogfeld **Durchsuchen** zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="7f58a-119">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the SelectionTree uses this event to trigger the **Browse** dialog box.</span></span>

 

 



