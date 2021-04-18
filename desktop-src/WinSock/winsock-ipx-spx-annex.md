---
description: In diesem Abschnitt werden die für Internetwork Packet Exchange/sequenzierte Paket Austausch (IPX/SPX) spezifischen Winsock-Erweiterungen beschrieben. Außerdem werden Aspekte von Basis-Winsock-Funktionen beschrieben, die entweder besondere Überlegungen erfordern oder eindeutiges Verhalten aufweisen können.
ms.assetid: 8447e063-767a-40b8-b094-724393e85be2
title: WinSock-IPX/SPX-Anhang
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c533781fa07c997d7f2363dd6b00d6b4213f22e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354562"
---
# <a name="winsock-ipxspx-annex"></a>WinSock-IPX/SPX-Anhang

In diesem Abschnitt werden die für Internetwork Packet Exchange/sequenzierte Paket Austausch (IPX/SPX) spezifischen Winsock-Erweiterungen beschrieben. Außerdem werden Aspekte von Basis-Winsock-Funktionen beschrieben, die entweder besondere Überlegungen erfordern oder eindeutiges Verhalten aufweisen können.



| Element          | BESCHREIBUNG                                                                                                                                     |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Protokoll Name (n) | IPX, SPX                                                                                                                                        |
| BESCHREIBUNG      | Bietet Transportdienste über die IPX-Netzwerkebene: IPX für unzuverlässige Datagramme, SPX für zuverlässige, Verbindungs orientierte Nachrichtenströme. |
| Adressfamilie   | AF- \_ IPX                                                                                                                                         |
| Headerdatei      | Wsipx. h                                                                                                                                         |



 

In diesem Abschnitt wird erläutert, wie Winsock mit der IPX-Familie von Protokollen verwendet wird, sodass herkömmliche IPX-Anwendungen in Winsock portiert werden können. IPX-Netzwerke funktionieren in einer grundlegenden Weise als IP-Netzwerke, sodass solche Unterschiede bei der Verwendung von IPX/SPX berücksichtigt werden müssen.

 

 



