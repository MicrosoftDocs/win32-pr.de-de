---
title: Der aktuelle Neustart-Manager-Vorgang wird abgebrochen.
description: Wenn eine Benutzeraktion den Installer anweist, eine andere Aktion auszuführen, kann die folgende Methode verwendet werden, um den aktuellen Neustart-Manager-Vorgang abzubrechen.
ms.assetid: 87c8cf27-cd77-46fb-8298-cccbf4b1071a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633882cc723f19823c6b832ee6927c5a3aacaab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714658"
---
# <a name="canceling-the-current-restart-manager-operation"></a><span data-ttu-id="d17ea-103">Der aktuelle Neustart-Manager-Vorgang wird abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="d17ea-103">Canceling the Current Restart Manager Operation</span></span>

<span data-ttu-id="d17ea-104">Wenn eine Benutzeraktion den Installer anweist, eine andere Aktion auszuführen, kann die folgende Methode verwendet werden, um den aktuellen Neustart-Manager-Vorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="d17ea-104">When a user action directs the installer to perform a different action, the following method can be used to cancel the current Restart Manager operation.</span></span>

<span data-ttu-id="d17ea-105">**So brechen Sie den aktuellen Neustart-Manager-Vorgang ab**</span><span class="sxs-lookup"><span data-stu-id="d17ea-105">**To cancel the current Restart Manager operation**</span></span>

-   <span data-ttu-id="d17ea-106">Das Installationsprogramm kann die [**rmcancelcurrenttask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) -Funktion von einem anderen Thread aus abrufen, um den aktuellen [**rmshutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) -oder [**rmrestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) -Vorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="d17ea-106">The installer can call the [**RMCancelCurrentTask**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) function from another thread to cancel the current [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) or [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) operation.</span></span> <span data-ttu-id="d17ea-107">Der Neustart-Manager kann den Vorgang abhängig davon abbrechen, in welchem Umfang der Vorgang abgeschlossen ist, wenn die **rmcancelcurrenttask** -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d17ea-107">The Restart Manager may cancel the operation depending on the extent to which the operation has completed when the **RMCancelCurrentTask** function is called.</span></span>

 

 




