---
description: Das Installationsprogramm führt die Installations-Assistenten Sequenz des Beispiels nur dann aus, wenn die vollständige Benutzeroberflächen Ebene zum Installieren der Anwendung verwendet wird.
ms.assetid: 323d62ae-333b-49fd-96a1-55b228c8ab2c
title: Hinzufügen eines Steuerungs Ereignisses am Ende der Installation zum Ausführen des Starts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545901c4cfd0936f63078d5ad56586022fb4ec4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959549"
---
# <a name="adding-a-control-event-at-the-end-of-the-installation-to-run-launch"></a><span data-ttu-id="9d844-103">Hinzufügen eines Steuerungs Ereignisses am Ende der Installation zum Ausführen des Starts</span><span class="sxs-lookup"><span data-stu-id="9d844-103">Adding a Control Event at the End of the Installation to Run Launch</span></span>

<span data-ttu-id="9d844-104">Das Installationsprogramm führt die Installations-Assistenten Sequenz des Beispiels nur dann aus, wenn die [*vollständige Benutzer*](f-gly.md) Oberflächenebene zum Installieren der Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9d844-104">The installer runs the sample's installation wizard sequence only if the [*full UI*](f-gly.md) level is used to install the application.</span></span> <span data-ttu-id="9d844-105">Das letzte Dialogfeld der Beispiel dialogsequenz ist ein [Exit-Dialog](exit-dialog.md) Feld mit dem Namen Exitdialog.</span><span class="sxs-lookup"><span data-stu-id="9d844-105">The last dialog box of the sample dialog sequence is an [Exit Dialog](exit-dialog.md) named ExitDialog.</span></span> <span data-ttu-id="9d844-106">Wenn ein Benutzer mit der Schaltfläche OK in Exitdialog interagiert, wird zuerst ein [EndDialog-ControlEvent](enddialog-controlevent.md) veröffentlicht, das die Steuerung an den Installer zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9d844-106">When a user interacts with the OK button on ExitDialog, this first publishes an [EndDialog ControlEvent](enddialog-controlevent.md) that returns control to the installer.</span></span> <span data-ttu-id="9d844-107">Das-Steuerelement veröffentlicht dann einen [doaction-ControlEvent](doaction-controlevent.md) , der die benutzerdefinierte Aktion "Launch" ausführt.</span><span class="sxs-lookup"><span data-stu-id="9d844-107">The control then publishes a [DoAction ControlEvent](doaction-controlevent.md) that runs the Launch custom action.</span></span> <span data-ttu-id="9d844-108">Jedes Steuerelement Ereignis erfordert einen Datensatz in der [ControlEvent-Tabelle](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="9d844-108">Each control event requires a record in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="9d844-109">Weitere Informationen finden Sie unter [ControlEvent Overview](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9d844-109">See [ControlEvent Overview](controlevent-overview.md).</span></span>

[<span data-ttu-id="9d844-110">ControlEvent-Tabelle</span><span class="sxs-lookup"><span data-stu-id="9d844-110">ControlEvent Table</span></span>](controlevent-table.md)



| <span data-ttu-id="9d844-111">Dialog</span><span class="sxs-lookup"><span data-stu-id="9d844-111">Dialog</span></span>     | <span data-ttu-id="9d844-112">Steuerelement\_</span><span class="sxs-lookup"><span data-stu-id="9d844-112">Control\_</span></span> | <span data-ttu-id="9d844-113">Ereignis</span><span class="sxs-lookup"><span data-stu-id="9d844-113">Event</span></span>     | <span data-ttu-id="9d844-114">Argument</span><span class="sxs-lookup"><span data-stu-id="9d844-114">Argument</span></span> | <span data-ttu-id="9d844-115">Bedingung</span><span class="sxs-lookup"><span data-stu-id="9d844-115">Condition</span></span>                     | <span data-ttu-id="9d844-116">Sortieren</span><span class="sxs-lookup"><span data-stu-id="9d844-116">Ordering</span></span> |
|------------|-----------|-----------|----------|-------------------------------|----------|
| <span data-ttu-id="9d844-117">Exitdialog</span><span class="sxs-lookup"><span data-stu-id="9d844-117">ExitDialog</span></span> | <span data-ttu-id="9d844-118">OK</span><span class="sxs-lookup"><span data-stu-id="9d844-118">OK</span></span>        | <span data-ttu-id="9d844-119">EndDialog</span><span class="sxs-lookup"><span data-stu-id="9d844-119">EndDialog</span></span> | <span data-ttu-id="9d844-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d844-120">Return</span></span>   | <span data-ttu-id="9d844-121">1</span><span class="sxs-lookup"><span data-stu-id="9d844-121">1</span></span>                             | <span data-ttu-id="9d844-122">1</span><span class="sxs-lookup"><span data-stu-id="9d844-122">1</span></span>        |
| <span data-ttu-id="9d844-123">Exitdialog</span><span class="sxs-lookup"><span data-stu-id="9d844-123">ExitDialog</span></span> | <span data-ttu-id="9d844-124">OK</span><span class="sxs-lookup"><span data-stu-id="9d844-124">OK</span></span>        | <span data-ttu-id="9d844-125">DoAction</span><span class="sxs-lookup"><span data-stu-id="9d844-125">DoAction</span></span>  | <span data-ttu-id="9d844-126">Starten</span><span class="sxs-lookup"><span data-stu-id="9d844-126">Launch</span></span>   | <span data-ttu-id="9d844-127">Nicht installiert und $Tutorial = 3</span><span class="sxs-lookup"><span data-stu-id="9d844-127">NOT Installed AND $Tutorial=3</span></span> | <span data-ttu-id="9d844-128">2</span><span class="sxs-lookup"><span data-stu-id="9d844-128">2</span></span>        |



 

<span data-ttu-id="9d844-129">Die Bedingung im doaction-Steuerelement stellt sicher, dass die benutzerdefinierte Aktion nur während der ersten Installation der Anwendung ausgeführt wird und lokal installiert wird.</span><span class="sxs-lookup"><span data-stu-id="9d844-129">The condition on the DoAction control ensures the custom action only runs during the first installation of the application and that it is being installed locally.</span></span> <span data-ttu-id="9d844-130">Der Ausdruck $Tutorial = 3 bedeutet, dass der Aktionszustand der tutorialkomponente auf Local festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9d844-130">The phrase $Tutorial=3 means the action state of the Tutorial component is set to local.</span></span> <span data-ttu-id="9d844-131">Siehe [Syntax der Bedingungs Anweisung](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="9d844-131">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

<span data-ttu-id="9d844-132">Dadurch wird das Beispiel abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9d844-132">This completes the sample.</span></span>

 

 



