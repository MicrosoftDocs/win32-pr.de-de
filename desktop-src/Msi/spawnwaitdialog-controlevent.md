---
description: Das handlevent spawnwaitdialog löst das von der Argument-Spalte der ControlEvent-Tabelle angegebene Dialogfeld aus, wenn der Ausdruck in der Spalte Bedingung als false ausgewertet wird.
ms.assetid: 38a5d896-2c11-4ce9-b829-104a882723b6
title: Spawnwaitdialog ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20059c936a8534d00799c93dfbe3408a19c6dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959034"
---
# <a name="spawnwaitdialog-controlevent"></a><span data-ttu-id="3faef-103">Spawnwaitdialog ControlEvent</span><span class="sxs-lookup"><span data-stu-id="3faef-103">SpawnWaitDialog ControlEvent</span></span>

<span data-ttu-id="3faef-104">Das handlevent spawnwaitdialog löst das von der Argument-Spalte der [ControlEvent-Tabelle](controlevent-table.md)angegebene Dialogfeld aus, wenn der Ausdruck in der Spalte Bedingung als false ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="3faef-104">The SpawnWaitDialog ControlEvent triggers the dialog box specified by the Argument column of the [ControlEvent table](controlevent-table.md), if the expression in the Condition column evaluates as FALSE.</span></span> <span data-ttu-id="3faef-105">Das Dialogfeld bleibt so lange aktiv, bis der bedingte Ausdruck false bleibt, und wird entfernt, sobald die Bedingung "true" ergibt.</span><span class="sxs-lookup"><span data-stu-id="3faef-105">The dialog box remains up for as long as the conditional expression remains FALSE and is removed as soon as the condition evaluates TRUE.</span></span>

<span data-ttu-id="3faef-106">Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="3faef-106">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="3faef-107">Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3faef-107">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="3faef-108">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3faef-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="3faef-109">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3faef-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="3faef-110">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="3faef-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="3faef-111">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="3faef-111">Published By</span></span>

<span data-ttu-id="3faef-112">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="3faef-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="3faef-113">Argument</span><span class="sxs-lookup"><span data-stu-id="3faef-113">Argument</span></span>

<span data-ttu-id="3faef-114">Ein Dialogfeld in der [Dialogfeld Tabelle](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="3faef-114">A dialog box in the [Dialog table](dialog-table.md).</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="3faef-115">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="3faef-115">Action on Subscribers</span></span>

<span data-ttu-id="3faef-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="3faef-116">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="3faef-117">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="3faef-117">Typical Use</span></span>

<span data-ttu-id="3faef-118">Das handlevent spawnwaitdialog kann verwendet werden, um auf alle Hintergrundaufgaben zu warten, deren Abschluss mit einem bedingten Ausdruck wie dem Zustand einer Eigenschaft getestet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3faef-118">The SpawnWaitDialog ControlEvent can be used to wait for any background task the completion of which can be tested using a conditional expression such as the state of a property.</span></span> <span data-ttu-id="3faef-119">Ein Beispiel für die Verwendung des handlevent spawnwaitdialog finden Sie im Abschnitt [Erstellen einer bedingten "Bitte warten..." ](authoring-a-conditional-please-wait-------message-box.md)Meldungs Feld.</span><span class="sxs-lookup"><span data-stu-id="3faef-119">For an example of using the SpawnWaitDialog ControlEvent, see the section [Authoring a Conditional "Please wait . . ." Message Box](authoring-a-conditional-please-wait-------message-box.md).</span></span>

 

 



