---
description: Die folgenden Enumerationen unterstützen die DRT-API (Distributed Routing Table).
ms.assetid: 38ce95a0-1603-42c2-8a5e-4370f52c8fc9
title: Verteilte Routingtabellenenumeration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ff0a955aed8d6ed6cdf14f3d0e7f6ac2605960123f8008c831dbef5be2da98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011598"
---
# <a name="distributed-routing-table-enumerations"></a>Verteilte Routingtabellenenumeration

Die folgenden Enumerationen unterstützen die DRT-API (Distributed Routing Table).



| Enumeration                                                            | Beschreibung                                                                                                                                                           |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_DRT-BEREICH**](/windows/desktop/api/drt/ne-drt-drt_scope)                                        | Definiert den Satz von IPv6-Geltungsbereichen, in denen DRT funktioniert, wenn der von [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)erstellte IPv6-UDP-Transport verwendet wird. |
| [**\_ \_ DRT-ADRESSFLAGS**](/windows/desktop/api/drt/ne-drt-drt_address_flags)                       | Definiert den Satz von Antworten, die von einem Zwischenknoten zurückgegeben werden können, wenn eine Suche nach einem Schlüssel ausgeführt wird.                                                         |
| [**\_DRT-STATUS**](/windows/desktop/api/drt/ne-drt-drt_status)                                      | Definiert die möglichen Konnektivitäts- und Fehlerzustände eines lokalen Knotens.                                                                                                   |
| [**\_ \_ DRT-ÜBEREINSTIMMUNGSTYP**](/windows/desktop/api/drt/ne-drt-drt_match_type)                             | Definiert die Genauigkeit der Ergebnisse, die zurückgegeben werden, wenn eine Suche ausgeführt wird.                                                                                                 |
| [**DRT \_ LEAFSET \_ KEY \_ CHANGE \_ TYPE**](/windows/desktop/api/drt/ne-drt-drt_leafset_key_change_type) | Definiert den Satz von Änderungstypen, die auf einem lokalen Blattsatzknoten im lokalen DRT-Cache ausgeführt werden können.                                                                |
| [**\_DRT-EREIGNISTYP \_**](/windows/desktop/api/drt/ne-drt-drt_event_type)                             | Definiert den Satz von Ereignissen, die vom DRT ausgelöst werden können.                                                                                                              |
| [**\_DRT-SICHERHEITSMODUS \_**](/windows/desktop/api/drt/ne-drt-drt_security_mode)                       | Definiert die möglichen Sicherheitsmodi des DRT. Diese Enumeration ist ein Feld der [**DRT \_ SETTINGS-Struktur.**](/windows/desktop/api/drt/ns-drt-drt_settings)                                   |
| [**\_DRT-REGISTRIERUNGSSTATUS \_**](/windows/desktop/api/drt/ne-drt-drt_registration_state)             | Definiert den Status eines registrierten Schlüssels.                                                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verteilte Routingtabellenstrukturen](distributed-routing-table-structures.md)
</dt> <dt>

[Verteilte Routingtabellenfunktionen](distributed-routing-table-functions.md)
</dt> <dt>

[Distributed Routing Tabellen-API Reference](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



