---
title: Veröffentlichen in einem Domänen System Container
description: Der System Container einer Domänen Partition enthält Betriebsinformationen pro Domäne.
ms.assetid: 18bb3409-774e-42d9-8f27-6c582d74ca86
ms.tgt_platform: multiple
keywords:
- Veröffentlichen in einem Domänen System-Container AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf7d1febd91e3540c7bc2002a36d33346820344
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855391"
---
# <a name="publishing-in-a-domain-system-container"></a>Veröffentlichen in einem Domänen System Container

Der System Container einer Domänen Partition enthält Betriebsinformationen pro Domäne. Dies schließt die standardmäßige lokale Sicherheitsrichtlinie, die Nachverfolgung von Datei Verknüpfungen, Netzwerk Besprechungen und Container für die Verbindungspunkte von Windows Sockets Registration and Resolution (RNR) und RPC Name Service (RpcNs) ein. Der System Container ist standardmäßig ausgeblendet und bietet einen geeigneten Ort zum Speichern von Objekten, die für Administratoren von Interesse sind, aber nicht für Endbenutzer.

Dienste, die nicht an einen einzelnen Host gebunden sind, können Ihre SCPs unter dem System Container einer Domänen Partition erstellen. Diese Alternative eignet sich für Dienste mit Replikaten, die auf mehreren Hosts installiert sind, wobei jedes Replikat für Clients in der gesamten Domäne identische Dienste bereitstellt. Sie ermöglicht es Ihnen, alle Objekte für den replizierten Dienst in einem einzelnen Container zu gruppieren.

Dienste, die Dienst spezifische Objekte im System Container erstellen, müssen folgende Aktionen ausführen:

1.  Erstellen Sie einen unter Container des Objektklassen **Containers** als direkt untergeordnetes Element des System Containers. Weisen Sie diesem unter Container einen Namen zu, der ihn im Zusammenhang mit dem Dienst eindeutig identifiziert.
2.  Erstellen Sie die Dienst bezogenen Objekte in diesem unter Container. Beispielsweise verwendet NetMeeting den Besprechungs Container zum Veröffentlichen von Netzwerk Besprechungs Objekten.

Ein Anbieter mit mehreren Produkten kann eine ähnliche Strategie zum Gruppieren von Dienst bezogenen Objekten für alle seine Produkte verwenden. In diesem Fall können Sie ein **Container** Objekt mit einem Namen erstellen, der den Anbieter eindeutig identifiziert. Erstellen Sie dann **Container** Objekte für jeden Dienst als untergeordnete Elemente des Hersteller Containers. Erstellen Sie den herstellerspezifischen Container als untergeordnetes Element des System Containers.

 

 




