---
title: Abbrechen des aktuellen Neustart-Manager-Vorgangs
description: Wenn eine Benutzeraktion das Installationsprogramm anweise, eine andere Aktion durchzuführen, kann die folgende Methode verwendet werden, um den aktuellen Neustart-Manager-Vorgang abzubricht.
ms.assetid: 87c8cf27-cd77-46fb-8298-cccbf4b1071a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c745a76ab8c72acaff0b9f1ae85ded380e1113c3687822e916b422cad9ef51f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010248"
---
# <a name="canceling-the-current-restart-manager-operation"></a>Abbrechen des aktuellen Neustart-Manager-Vorgangs

Wenn eine Benutzeraktion das Installationsprogramm anweise, eine andere Aktion durchzuführen, kann die folgende Methode verwendet werden, um den aktuellen Neustart-Manager-Vorgang abzubricht.

**So brechen Sie den aktuellen Neustart-Manager-Vorgang ab**

-   Das Installationsprogramm kann die [**RMCancelCurrentTask-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmcancelcurrenttask) aus einem anderen Thread aufrufen, um den aktuellen [**RmShutdown-**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) oder [**RmRestart-Vorgang**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) abzubruchen. Der Neustart-Manager kann den Vorgang abhängig davon abbrechen, in welchem Umfang der Vorgang abgeschlossen wurde, wenn die **RMCancelCurrentTask-Funktion** aufgerufen wird.

 

 




