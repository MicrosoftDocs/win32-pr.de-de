---
description: Das Installationsprogramm verwendet das timeremainor-Ereignis, um die ungefähre verbleibende Zeit (in Sekunden) für die aktuelle Fortschritts Sequenz zu veröffentlichen.
ms.assetid: ec5fc2b3-13a9-4681-89f0-fd39bab1de5f
title: Timeremainung ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8978dfb7ed3be855921ad66af8554ea50972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050432"
---
# <a name="timeremaining-controlevent"></a><span data-ttu-id="026d1-103">Timeremainung ControlEvent</span><span class="sxs-lookup"><span data-stu-id="026d1-103">TimeRemaining ControlEvent</span></span>

<span data-ttu-id="026d1-104">Das Installationsprogramm verwendet das timeremainor-Ereignis, um die ungefähre verbleibende Zeit (in Sekunden) für die aktuelle Fortschritts Sequenz zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="026d1-104">The installer uses the TimeRemaining event to publish the approximate time remaining, in seconds, for the current progress sequence.</span></span> <span data-ttu-id="026d1-105">Die verbleibende Zeit kann in einem Dialogfeld durch ein [Text Steuer](text-control.md) Element angezeigt werden, das diese ControlEvent abonniert.</span><span class="sxs-lookup"><span data-stu-id="026d1-105">The time remaining can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="026d1-106">Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="026d1-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="026d1-107">Diese ControlEvent kann von einer Benutzeroberfläche verarbeitet werden, die auf der [*grundlegenden*](b-gly.md)Benutzeroberfläche, der [*reduzierten*](r-gly.md)Benutzeroberfläche oder der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="026d1-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="026d1-108">Weitere Informationen zu UI-Ebenen finden Sie unter [Benutzeroberflächen](user-interface-levels.md)Ebenen.</span><span class="sxs-lookup"><span data-stu-id="026d1-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="026d1-109">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="026d1-109">Published By</span></span>

<span data-ttu-id="026d1-110">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="026d1-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="026d1-111">Argument</span><span class="sxs-lookup"><span data-stu-id="026d1-111">Argument</span></span>

<span data-ttu-id="026d1-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="026d1-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="026d1-113">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="026d1-113">Action on Subscribers</span></span>

<span data-ttu-id="026d1-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="026d1-114">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="026d1-115">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="026d1-115">Typical Use</span></span>

<span data-ttu-id="026d1-116">Ein [Text Steuer](text-control.md) Element in einem nicht modalem Dialogfeld abonniert dieses Ereignis über die [EventMapping-Tabelle](eventmapping-table.md) und verwendet das [timeremainung-Attribut](timeremaining-control-attribute.md) , um die verbleibende Zeit anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="026d1-116">A [Text Control](text-control.md) on a modeless dialog box subscribes to this event through the [EventMapping table](eventmapping-table.md) and uses the [TimeRemaining attribute](timeremaining-control-attribute.md) to display the time remaining.</span></span>

<span data-ttu-id="026d1-117">Das gleiche Text Steuerelement, das das timeremainingcontrolevent abonniert, kann auch den [scriptinprogress ControlEvent](scriptinprogress-controlevent.md)abonnieren.</span><span class="sxs-lookup"><span data-stu-id="026d1-117">The same text control that subscribes to the TimeRemaining ControlEvent can also subscribe to the [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md).</span></span> <span data-ttu-id="026d1-118">In diesem Fall wird die vorläufige scriptinprogress-Meldungs Zeichenfolge durch die Zeichenfolge "verbleibende Zeit: XX Minuten" ersetzt.</span><span class="sxs-lookup"><span data-stu-id="026d1-118">In this case, as the preliminary ScriptInProgress message string, it is replaced by the "Time Remaining: xx minutes" string.</span></span>

 

 



