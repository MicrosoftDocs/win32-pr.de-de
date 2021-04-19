---
description: 'Die PNRP-Namespace Anbieter-API verwendet die folgenden Strukturen:'
ms.assetid: 697fb99a-259f-429c-8818-0d725255bc86
title: PNRP-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e2ee85f3673395ade31417c79c010354f16b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362474"
---
# <a name="pnrp-structures"></a>PNRP-Strukturen

Die PNRP-Namespace Anbieter-API verwendet die folgenden Strukturen:



| Struktur                                                             | BESCHREIBUNG                                                                                                                                                         |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Peer- \_ PNRP- \_ Endpunkt \_ Informationen**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_endpoint_info)         | Enthält die IP-Adressen und Daten, die einem Peer Endpunkt zugeordnet sind.                                                                                                 |
| [**Peer- \_ PNRP- \_ \_ cloudinformationen**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_cloud_info)               | Enthält Informationen zu einer PNRP-Cloud (Peer Name Resolution Protocol).                                                                                            |
| [**Peer- \_ PNRP- \_ Registrierungs \_ Informationen**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_registration_info) | Enthält die Informationen, die von einer Peer Identität bereitgestellt werden, wenn Sie bei einer PNRP-Cloud registriert wird.                                                                           |
| [PNRP und BLOB](pnrp-and-blob.md)                                    | Übergibt während Aufrufen mehrerer Funktionen Daten an die [**wsaqueryset**](winsock-nsp-reference-links.md) -Struktur.                                                  |
| [PNRP und wsaqueryset](pnrp-and-wsaqueryset.md)                      | Ermöglicht das Auflösen von Namen und die Enumeration von Namen und Clouds.                                                                                         |
| [**PNRP- \_ Cloud- \_ ID**](/windows/desktop/api/Pnrpdef/ns-pnrpdef-pnrp_cloud_id)                              | Enthält die Werte, die eine netzwerkcloud definieren.                                                                                                                    |
| [**Pnrpcloudinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)                                | Auf den **lpblob** -Member der [**wsaqueryset**](winsock-nsp-reference-links.md) -Struktur verweist.                                                            |
| [**Pnrpinfo \_ v1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)                                      | Verweis auf den **lpblob** -Member der [**wsaqueryset**](winsock-nsp-reference-links.md) -Struktur                                                             |
| [**Pnrpinfo \_ v2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))                                   | Verweist auf das **lpblob** -Member der [**wsaqueryset**](winsock-nsp-reference-links.md) -Struktur und bietet Unterstützung für anwendungsspezifische, nicht transparente Daten. |



 

 

 
