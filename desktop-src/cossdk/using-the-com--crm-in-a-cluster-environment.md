---
description: Verwenden des com+-CRM in einer Cluster Umgebung
ms.assetid: 753461c5-880c-4df0-b552-b962dc06524f
title: Verwenden des com+-CRM in einer Cluster Umgebung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a05ff281748c35128349ef5d0d0f43d7beae86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342239"
---
# <a name="using-the-com-crm-in-a-cluster-environment"></a>Verwenden des com+-CRM in einer Cluster Umgebung

Wenn Sie com+-CRMs für die Arbeit in Cluster Umgebungen entwickeln, besteht der wichtigste Faktor darin, zu berücksichtigen, ob ein bestimmtes CRM den Knoten des Clusters, auf dem er ausgeführt wird, interessiert. Wenn die vom CRM verwaltete Ressource z. b. das Dateisystem oder die Registrierung des Computers ist, gelten alle Änderungen speziell für den Knoten, auf dem die CRM-Serveranwendung zu diesem Zeitpunkt ausgeführt wird. In diesem Fall wäre es nicht wünschenswert, ein Failover der CRM-Serveranwendung auf einen anderen Knoten durchzusetzen. In einem anderen Fall, in dem das CRM einige Ressourcen verwaltet, die dem Cluster gemeinsam sind, ist das Failover der CRM-Serveranwendung auf einen anderen Knoten hilfreich.

Der Standardverzeichnis Pfad für CRM-Protokolldateien ist dasselbe Verzeichnis wie die DTC-Protokolldatei. In Clustern wird die DTC-Protokolldatei auf einem freigegebenen Datenträger platziert, für den ein Failover zwischen den Knoten des Clusters ausgeführt wird. Dies bedeutet, dass das Standardverhalten für CRM-Server Anwendungen für ein Failover zwischen den Knoten des Clusters verwendet wird. Wenn ein bestimmtes CRM das alternative Verhalten des Failovers zwischen Knoten erfordert, sollte daher der Speicherort der CRM-Protokolldatei für diese bestimmte CRM-Serveranwendung geändert werden.

Wenn außerdem ein Failover für die CRM-Anwendung erforderlich ist, sollte es als generische Anwendung in einer Clustergruppe konfiguriert werden. Die Abhängigkeit sollte DTC lauten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompensierende com+-Ressourcen-Manager Konzepte](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



