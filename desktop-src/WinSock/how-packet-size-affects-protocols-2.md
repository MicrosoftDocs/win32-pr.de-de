---
description: Probleme mit der Medienpaketgröße, die im Thema Informationen zur Medienpaketgröße erläutert werden, wirken sich unterschiedlich auf die verschiedenen \_ PF-IPX-Protokolle aus.
ms.assetid: 7f0643b8-6bb2-4dbb-b306-d9b2e0d0e03c
title: Auswirkungen der Paketgröße auf Protokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa654e8884f56ae8079375fa32764ad240f0c870229d07e50623f6e18e42958b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051638"
---
# <a name="how-packet-size-affects-protocols"></a>Auswirkungen der Paketgröße auf Protokolle

Probleme mit der Medienpaketgröße, die im Thema Informationen zur [Medienpaketgröße](about-media-packet-size-2.md)erläutert werden, wirken sich auf die verschiedenen \_ PF-IPX-Protokolle unterschiedlich aus. Eine gängige Strategie für die Behandlung verschiedener Einschränkungen der Router- und Mediengröße ist die Verwendung der vollständigen Mediengröße, wenn die Netzwerknummer der Remotestation mit der lokalen Station übereinstimmt, und andernfalls ein Fallback auf die mindeste Paketgröße.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>NSPROTO \_ IPX
</dt> <dd>

Stellt einen Datagrammdienst bereit. jedes Datagramm muss sich innerhalb der maximalen Paketgröße befinden. Winsock legt die maximale Größe des Datagrammpakets auf die größe des lokalen Medienpakets abzüglich des IPX-Headers fest. Beachten Sie jedoch, dass beim Weiterleiten des Pakets routerbedingte Einschränkungen auftreten können. Stellen Sie sicher, dass Ihre Anwendung auf 546-Byte-Datagramme zurückgreifen kann.

</dd> <dt>

<span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>NSPROTO \_ SPX
</dt> <dd>

Stellt Datenstrom- und Sequenzpaketdienste bereit. Mit Winsock IPX/SPX können Datenströme und Nachrichten mehrere Pakete umfassen, sodass die Paketgröße die Menge der von [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) und [**recv**](/windows/desktop/api/winsock/nf-winsock-recv)verarbeiteten Daten nicht einschränkt. Die zugrunde liegende Mediengröße muss jedoch richtig festgelegt werden, oder das erste große Paket ist unerstellbar, und die Verbindung wird zurückgesetzt. Wenn sich die Zielstation im lokalen Netzwerk befindet, legt Winsock die Paketgröße auf die Größe des Medienpakets fest. Andernfalls wird standardmäßig 512 Bytes verwendet. Diese Größe kann sofort nach [**dem Herstellen**](/windows/desktop/api/Winsock2/nf-winsock2-connect) einer Verbindung oder [**dem Akzeptieren**](/windows/desktop/api/Winsock2/nf-winsock2-accept) über [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)geändert werden.

</dd> <dt>

<span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>NSPROTO \_ SPXII
</dt> <dd>

SPXII bietet eine große Internetpaketaushandlung, um eine optimale Größe für Pakete beizubehalten, und erfordert keinen Eingriff des Programmierers. Wenn die Remotestation jedoch SPXII nicht unterstützt und spx standardaushandelt, sind die NSPROTO \_ SPX-Regeln wirksam.



| Protokoll     | Medien      | Typ        | Datenpaketgröße |
|--------------|------------|-------------|------------------|
| NSPROTO \_ IPX | Ethernet   | Ethernet II |                  |
|              |            | 802.3       |                  |
|              |            | 802.2       | 1466             |
|              |            | Snap        |                  |
|              | Token Ring | 4 Megabit   |                  |
|              |            | 16 Megabit  |                  |
| NSPROTO \_ SPX | Ethernet   | Ethernet II |                  |
|              |            | 802.3       |                  |
|              |            | 802.2       | 1454             |
|              |            | Snap        |                  |
|              | Token Ring | 4 Megabit   |                  |
|              |            | 16 Megabit  |                  |



 

</dd> </dl>

 

 



