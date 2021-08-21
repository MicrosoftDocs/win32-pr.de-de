---
description: Verwenden von COM+ CRM in einer Clusterumgebung
ms.assetid: 753461c5-880c-4df0-b552-b962dc06524f
title: Verwenden von COM+ CRM in einer Clusterumgebung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31a2d0800f98c9453e7d4454cdd59185dffb837649e391ebc415c965bee6ff80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499530"
---
# <a name="using-the-com-crm-in-a-cluster-environment"></a>Verwenden von COM+ CRM in einer Clusterumgebung

Bei der Entwicklung von COM+-CRMs, die in Clusterumgebungen funktionieren, ist der wichtigste Zu berücksichtigende Faktor, ob ein bestimmtes CRM den Knoten des Clusters, auf dem es ausgeführt wird, so wichtig ist. Wenn es sich bei der vom CRM verwalteten Ressource beispielsweise um das Dateisystem oder die Registrierung des Computers handelt, sind alle Änderungen spezifisch für den Knoten, auf dem die CRM-Serveranwendung zu diesem Zeitpunkt ausgeführt wird. In diesem Fall wäre ein Failover der CRM-Serveranwendung auf einen anderen Knoten nicht wünschenswert. In einem anderen Fall, in dem crm eine Ressource für den Cluster gemeinsam verwalten soll, ist ein Failover der CRM-Serveranwendung auf einen anderen Knoten nützlich.

Der Standardverzeichnisspeicherort für CRM-Protokolldateien ist dasselbe Verzeichnis wie die DTC-Protokolldatei. In Clustern wird die DTC-Protokolldatei auf einem freigegebenen Datenträger platziert, für den ein Failover zwischen den Knoten des Clusters ausgeführt wird. Dies bedeutet, dass das Standardverhalten für CRM-Serveranwendungen ein Failover zwischen Knoten des Clusters ist. Wenn für ein bestimmtes CRM das alternative Verhalten erforderlich ist, kein Ausführen eines Fehlers zwischen Knoten zu vermeiden, sollte daher der Speicherort der CRM-Protokolldatei für diese bestimmte CRM-Serveranwendung geändert werden.

Wenn ein Failover für die CRM-Anwendung erforderlich ist, sollte sie außerdem als generische Anwendung in einer Clustergruppe konfiguriert werden. Die Abhängigkeit sollte DTC sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+ Compensating Resource Manager Concepts](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



