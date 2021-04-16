---
description: Probleme mit der Medienpaket Größe, die im Thema Informationen zur Medienpaket Größe erläutert werden, wirken sich auf die verschiedenen PF- \_ IPX-Protokolle aus.
ms.assetid: 7f0643b8-6bb2-4dbb-b306-d9b2e0d0e03c
title: Auswirkungen der Paketgröße auf Protokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c778ee6c75cd558d19cdf1cbb76052065e03c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343508"
---
# <a name="how-packet-size-affects-protocols"></a>Auswirkungen der Paketgröße auf Protokolle

Probleme mit der Medienpaket Größe, die im Thema [Informationen zur Medienpaket Größe](about-media-packet-size-2.md)erläutert werden, wirken sich auf die verschiedenen PF- \_ IPX-Protokolle aus. Eine gängige Strategie für die Behandlung verschiedener Beschränkungen von Router und Mediengrößen besteht darin, die vollständige Mediengröße zu verwenden, wenn die Netzwerk Nummer der Remote Station mit der lokalen Station übereinstimmt, und andernfalls auf die minimale Paketgröße zurückgreifen.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>nsproto- \_ IPX
</dt> <dd>

Stellt einen Datagramm-Dienst bereit. jedes Datagramm muss innerhalb der maximalen Paketgröße liegen. Winsock legt die maximale datagrammpaketgröße auf die lokale Medienpaket Größe abzüglich des IPX-Headers fest. Beachten Sie jedoch, dass beim Weiterleiten des Pakets möglicherweise routereinschränkungen auf die Route-Route trifft. Stellen Sie sicher, dass die Anwendung auf die 546-Byte-Datagramme zurückgreifen kann.

</dd> <dt>

<span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>nsproto- \_ SPX
</dt> <dd>

Stellt Stream-und sequenzierte Paketdienste bereit. WinSock IPX/SPX ermöglicht Datenstreams und Nachrichten, die mehrere Pakete umfassen, sodass die Paketgröße nicht die Menge der von [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) und [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv)behandelten Daten beschränkt. Allerdings muss die Größe des zugrunde liegenden Mediums ordnungsgemäß festgelegt werden, oder das erste große Paket kann nicht zugestellt werden, und die Verbindung wird zurückgesetzt. Wenn sich die Zielstation im lokalen Netzwerk befindet, legt Winsock die Paketgröße auf die Medienpaket Größe fest. Andernfalls ist der Standardwert 512 Bytes. Diese Größe kann unmittelbar nach [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) oder [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) über [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)geändert werden.

</dd> <dt>

<span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>nsproto- \_ SPXII
</dt> <dd>

SPXII bietet eine große Internet Paket Aushandlung, um die Größe der Pakete mit der optimalen Anpassung zu gewährleisten und erfordert keinen programmiereingriff. Wenn die Remote Station SPXII jedoch nicht unterstützt und in Standard-SPX aushandiert, sind die nsproto \_ SPX-Regeln wirksam.



| Protokoll     | Medien      | type        | Größe des Datenpakets |
|--------------|------------|-------------|------------------|
| nsproto- \_ IPX | Ethernet   | Ethernet II |                  |
|              |            | 802.3       |                  |
|              |            | 802.2       | 1466             |
|              |            | Einbruch        |                  |
|              | Token Ring | 4 Megabit   |                  |
|              |            | 16 Megabit  |                  |
| nsproto- \_ SPX | Ethernet   | Ethernet II |                  |
|              |            | 802.3       |                  |
|              |            | 802.2       | 1454             |
|              |            | Einbruch        |                  |
|              | Token Ring | 4 Megabit   |                  |
|              |            | 16 Megabit  |                  |



 

</dd> </dl>

 

 



