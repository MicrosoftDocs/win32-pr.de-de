---
title: Veröffentlichen in einem Domänensystemcontainer
description: Der Systemcontainer einer Domänenpartition enthält domänenspezifische Betriebsinformationen.
ms.assetid: 18bb3409-774e-42d9-8f27-6c582d74ca86
ms.tgt_platform: multiple
keywords:
- Veröffentlichen in einem Domänensystemcontainer AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb86a49bb14bc88d64a723ca9ab289723ff4ac2b9259f112323e19a04497362c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184954"
---
# <a name="publishing-in-a-domain-system-container"></a>Veröffentlichen in einem Domänensystemcontainer

Der Systemcontainer einer Domänenpartition enthält domänenspezifische Betriebsinformationen. Dies schließt die standardmäßige lokale Sicherheitsrichtlinie, die Dateiverknüpfungsnachverfolgung, Netzwerkbesprechungen und Container für Windows Sockets Registration and Resolution (RnR) und RPC Name Service (RpcNs)-Verbindungspunkte ein. Der Systemcontainer ist standardmäßig ausgeblendet und bietet einen praktischen Ort zum Speichern von Objekten, die für Administratoren, aber nicht für Endbenutzer von Interesse sind.

Dienste, die nicht an einen einzelnen Host gebunden sind, möchten ihre SCPs möglicherweise unter dem Systemcontainer einer Domänenpartition erstellen. Diese Alternative kann für Dienste nützlich sein, bei denen Replikate auf mehreren Hosts installiert sind, von denen jedes Replikat identische Dienste für Clients in der gesamten Domäne bietet. Sie können alle Objekte für den replizierten Dienst in einem einzelnen Container gruppieren.

Dienste, die dienstspezifische Objekte im Systemcontainer erstellen, müssen Folgendes tun:

1.  Erstellen Sie einen Untercontainer des **Objektklassencontainers** als unmittelbar untergeordnetes Objekt des Systemcontainers. Geben Sie diesem Untercontainer einen Namen, der ihn eindeutig als dienstspezifischen Container identifiziert.
2.  Erstellen Sie die dienstbezogenen Objekte in diesem Untercontainer. NetMeeting verwendet beispielsweise den Besprechungscontainer, um Netzwerkbesprechungsobjekte zu veröffentlichen.

Ein Anbieter mit mehreren Produkten kann eine ähnliche Strategie verwenden, um dienstbezogene Objekte für alle seine Produkte zu gruppieren. In diesem Fall können Sie ein **Containerobjekt** mit einem Namen erstellen, der den Anbieter eindeutig identifiziert. erstellen Sie dann **Containerobjekte** für jeden Dienst als children-Objekte des Anbietercontainers. Erstellen Sie den herstellerspezifischen Container als untergeordnetes Untersystem des Systemcontainers.

 

 




