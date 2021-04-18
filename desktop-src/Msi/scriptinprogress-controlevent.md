---
description: Das Installationsprogramm verwendet dieses Ereignis, um eine Informations Zeichenfolge anzuzeigen, während das Ausführungs Skript der Installation kompiliert wird.
ms.assetid: 088e91e0-734a-4f18-8ceb-cfa4f904f75c
title: Scriptinprogress ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788fdc9c0acec5979a835a6cd2a0ec09cc6f0c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347372"
---
# <a name="scriptinprogress-controlevent"></a><span data-ttu-id="af154-103">Scriptinprogress ControlEvent</span><span class="sxs-lookup"><span data-stu-id="af154-103">ScriptInProgress ControlEvent</span></span>

<span data-ttu-id="af154-104">Das Installationsprogramm verwendet dieses Ereignis, um eine Informations Zeichenfolge anzuzeigen, während das Ausführungs Skript der Installation kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="af154-104">The installer uses this event to display an informational string while the installation's execution script is being compiled.</span></span> <span data-ttu-id="af154-105">Die Informations Zeichenfolge kann in einem Dialogfeld durch ein [Text Steuer](text-control.md) Element angezeigt werden, das diese ControlEvent abonniert.</span><span class="sxs-lookup"><span data-stu-id="af154-105">The informational string can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="af154-106">Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="af154-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="af154-107">Diese ControlEvent kann von einer Benutzeroberfläche verarbeitet werden, die auf der [*grundlegenden*](b-gly.md)Benutzeroberfläche, der [*reduzierten*](r-gly.md)Benutzeroberfläche oder der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af154-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="af154-108">Weitere Informationen zu UI-Ebenen finden Sie unter [Benutzeroberflächen](user-interface-levels.md)Ebenen.</span><span class="sxs-lookup"><span data-stu-id="af154-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="af154-109">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="af154-109">Published By</span></span>

<span data-ttu-id="af154-110">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="af154-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="af154-111">Argument</span><span class="sxs-lookup"><span data-stu-id="af154-111">Argument</span></span>

<span data-ttu-id="af154-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="af154-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="af154-113">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="af154-113">Action on Subscribers</span></span>

<span data-ttu-id="af154-114">Ein [Text Steuer](text-control.md) Element, das scriptinprogress abonniert, zeigt die in der [UIText-Tabelle](uitext-table.md)angegebene Text Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="af154-114">A [Text control](text-control.md) subscribing to ScriptInProgress will display text string specified in [UIText table](uitext-table.md).</span></span>

## <a name="typical-use"></a><span data-ttu-id="af154-115">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="af154-115">Typical Use</span></span>

<span data-ttu-id="af154-116">Während das Ausführungs Skript kompiliert wird, zeigt das Installationsprogramm eine ProgressBar an, die die verbleibende Zeit vor dem Beginn der Skriptausführung angibt.</span><span class="sxs-lookup"><span data-stu-id="af154-116">While the execution script is being compiled, the installer displays a ProgressBar indicating the time remaining before the beginning of script execution.</span></span> <span data-ttu-id="af154-117">Der Paket Ersteller kann zu diesem Zeitpunkt eine vorläufige Meldung anzeigen, in der die ProgressBar erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="af154-117">The package author can display a preliminary message at this time explaining the ProgressBar.</span></span> <span data-ttu-id="af154-118">Um eine vorläufige Meldung anzuzeigen, schließen Sie ein [Text Steuer](text-control.md) Element in dasselbe nicht Modaldialogfeld wie die ProgressBar ein.</span><span class="sxs-lookup"><span data-stu-id="af154-118">To display a preliminary message, include a [Text control](text-control.md) on the same modeless dialog box as the ProgressBar.</span></span> <span data-ttu-id="af154-119">Legen Sie fest, dass dieses Text Steuerelement den scriptinprogress-ControlEvent über die [EventMapping-Tabelle](eventmapping-table.md)abonniert.</span><span class="sxs-lookup"><span data-stu-id="af154-119">Specify that this Text control subscribe to the ScriptInProgress ControlEvent via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="af154-120">Fügen Sie einen Eintrag in der [UIText-Tabelle](uitext-table.md) mit scriptinprogress ein, der im Schlüsselfeld angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="af154-120">Include an entry in the [UIText table](uitext-table.md) with ScriptInProgress specified in the Key field.</span></span> <span data-ttu-id="af154-121">Geben Sie die vorläufige Nachricht als Text Zeichenfolge im Textfeld der UIText-Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="af154-121">Specify the preliminary message as a text string in the Text field of the UIText table.</span></span> <span data-ttu-id="af154-122">Während der Skript Kompilierung zeigt das Installationsprogramm diese Zeichenfolge im Text Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="af154-122">Then during script compilation, the installer will display this string within the text control.</span></span> <span data-ttu-id="af154-123">Der angezeigte Text verschwindet, sobald die Skript Kompilierung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="af154-123">The displayed text disappears as soon as the script compilation is finished.</span></span>

<span data-ttu-id="af154-124">Das gleiche Text Steuerelement, das den scriptinprogress-ControlEvent abonniert, kann auch das [timeremainingcontrolevent](timeremaining-controlevent.md)abonnieren.</span><span class="sxs-lookup"><span data-stu-id="af154-124">The same text control that subscribes to the ScriptInProgress ControlEvent can also subscribe to the [TimeRemaining ControlEvent](timeremaining-controlevent.md).</span></span> <span data-ttu-id="af154-125">In diesem Fall wird der Text der vorläufigen scriptinprogress-Zeichenfolge durch die Zeichenfolge "verbleibende Zeit: XX Minuten" ersetzt.</span><span class="sxs-lookup"><span data-stu-id="af154-125">In this case, as text of the preliminary ScriptInProgress string disappears, it is replaced by the "Time Remaining: xx minutes" string.</span></span>

 

 



