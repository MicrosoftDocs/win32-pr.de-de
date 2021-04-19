---
description: Der Netzwerk-DDE-Agent startet Network DDE, wenn er die DDE-Aktivität des lokalen Netzwerks erkennt.
ms.assetid: bc1e6a06-be07-4ae8-94da-9603a885b3a5
title: Netzwerk-DDE-Agent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a6259b512782102936f54f65646454509c6b37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345651"
---
# <a name="network-dde-agent"></a>Netzwerk-DDE-Agent

\[Network DDE wird nicht mehr unterstützt. Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]

Der Netzwerk-DDE-Agent startet Network DDE, wenn er die DDE-Aktivität des lokalen Netzwerks erkennt. Ein Remote Client, der versucht, eine Verbindung herzustellen, wird nicht erkannt. Daher muss Netzwerk DDE auf dem Server Computer gestartet werden, bevor der Client erfolgreich eine Verbindung herstellen kann. Beachten Sie, dass Network DDE nicht standardmäßig gestartet wird. Führen Sie NETDDE.EXE aus, um Network DDE zu starten. Diese Datei befindet sich in Ihrem Windows-Verzeichnis.

Der Netzwerk-DDE-Agent startet außerdem die Anwendungen, die für Netzwerk DDE erforderlich sind. Nachdem Network DDE gestartet wurde, werden DDE-Konversationen über ein Netzwerk-DDE-Fenster gesteuert, das einer der Netzwerk-DDE-Anwendungen zugeordnet ist. Diese Anwendung fungiert als Proxy. Er kommuniziert mit allen lokalen und Remote-DDE-Anwendungen.

 

 



