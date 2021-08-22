---
description: In diesem Abschnitt werden Winsock-Erweiterungen beschrieben, die spezifisch für Internetwork Packet Exchange/Sequenced Packet Exchange (IPX/SPX) sind. Außerdem werden Aspekte von Winsock-Basisfunktionen beschrieben, die entweder besondere Überlegungen erfordern oder ein eindeutiges Verhalten aufweisen können.
ms.assetid: 8447e063-767a-40b8-b094-724393e85be2
title: Winsock IPX/SPX Anhang
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e5a97b90dc29f577bf2335b93a15fb3fb2c87c8362e0585151e1ac8b1e3393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051348"
---
# <a name="winsock-ipxspx-annex"></a>Winsock IPX/SPX Anhang

In diesem Abschnitt werden Winsock-Erweiterungen beschrieben, die spezifisch für Internetwork Packet Exchange/Sequenced Packet Exchange (IPX/SPX) sind. Außerdem werden Aspekte von Winsock-Basisfunktionen beschrieben, die entweder besondere Überlegungen erfordern oder ein eindeutiges Verhalten aufweisen können.



| Element          | Beschreibung                                                                                                                                     |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Protokollnamen | IPX, SPX                                                                                                                                        |
| Beschreibung      | Stellt Transportdienste über die IPX-Netzwerkebene bereit: IPX für unzuverlässige Datagramme, SPX für zuverlässige, verbindungsorientierte Nachrichtenströme. |
| Adressfamilie   | AF \_ IPX                                                                                                                                         |
| Headerdatei      | Wsipx.h                                                                                                                                         |



 

In diesem Abschnitt wird erläutert, wie Sie Winsock mit der IPX-Protokollfamilie verwenden, sodass herkömmliche IPX-Anwendungen nach Winsock portiert werden können. IPX-Netzwerke funktionieren grundlegend anders als IP-Netzwerke. Daher müssen solche Unterschiede bei der Verwendung von IPX/SPX berücksichtigt werden.

 

 



