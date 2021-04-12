---
title: Konfigurieren des Microsoft Locator Name Service-Anbieters
description: Sie können den von Ihnen angegebenen Namen Dienstanbieter ändern, indem Sie die Konfigurationsdatei rpkreg. dat bearbeiten, in der die NSP-Parameter und die RPC-Protokoll Einstellungen enthalten sind. Verwenden Sie einen Text-Editor, um NSP-Einträge zu ändern.
ms.assetid: b499e40e-d38f-4e51-bbce-41af3ff12a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a5334436ce307030048a862f1375a91000b41e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310416"
---
# <a name="configuring-the-microsoft-locator-name-service-provider"></a>Konfigurieren des Microsoft Locator Name Service-Anbieters

Sie können den von Ihnen angegebenen Namen Dienstanbieter ändern, indem Sie die Konfigurationsdatei rpkreg. dat bearbeiten, in der die NSP-Parameter und die RPC-Protokoll Einstellungen enthalten sind. Verwenden Sie einen Text-Editor, um NSP-Einträge zu ändern.

**So konfigurieren Sie den Microsoft Locator Name Service-Anbieter neu**

1.  Öffnen Sie die Datei rpkreg. dat mit einem Text-Editor.

    Rpkreg. dat befindet sich im Stammverzeichnis, es sei denn, Sie haben während des Setups einen anderen Pfad angegeben.

2.  Legen Sie die folgenden Werte für die Registrierungseinträge fest. 

    | Registrierungseintrag                                         | Wert                                                                                                                                                 |
    |--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Software \\ Microsoft \\ RPC- \\ Nameservice- \\ Protokoll       | Die Protokoll Sequenz für das Protokoll, das Sie verwenden. Der Standardwert ist **ncacn \_ NP**.                                                                   |
    | Software \\ Microsoft \\ RPC- \\ Nameservice \\ Network Address | Der Name des Computers, auf dem der Locator ausgeführt wird und der während der Suche nach Namen Diensten von Clients verwendet wird. Der Standardwert ist der primäre Domänen Controller. |
    | Software \\ Microsoft \\ RPC- \\ Nameservice- \\ Endpunkt       | Der Name des vom Namensdienst verwendeten Endpunkts. Der Standardwert \\ ist \\ pipelocator.                                                                    |

    

     

3.  Speichern und schließen Sie die Datei.

 

 




