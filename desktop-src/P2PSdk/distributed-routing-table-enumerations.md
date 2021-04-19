---
description: Die folgenden Enumerationen unterstützen die DRT-API (verteilte Routing Tabelle).
ms.assetid: 38ce95a0-1603-42c2-8a5e-4370f52c8fc9
title: Verteilte Routing Tabellen-Enumerationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c432b156a9299a9f70026a394a6fd97f06528a25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349865"
---
# <a name="distributed-routing-table-enumerations"></a>Verteilte Routing Tabellen-Enumerationen

Die folgenden Enumerationen unterstützen die DRT-API (verteilte Routing Tabelle).



| Enumeration                                                            | Beschreibung                                                                                                                                                           |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DRT- \_ Bereich**](/windows/desktop/api/drt/ne-drt-drt_scope)                                        | Definiert den Satz von IPv6-Bereichen, in denen DRT verwendet wird, wenn der von [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)erstellte IPv6-UDP-Transport verwendet wird. |
| [**DRT \_ - \_ adressflags**](/windows/desktop/api/drt/ne-drt-drt_address_flags)                       | Definiert den Satz von Antworten, der von einem zwischen Knoten beim Ausführen einer Suche nach einem Schlüssel zurückgegeben werden kann.                                                         |
| [**DRT- \_ Status**](/windows/desktop/api/drt/ne-drt-drt_status)                                      | Definiert die möglichen Verbindungs-und Fehlerzustände eines lokalen Knotens.                                                                                                   |
| [**DRT-Übereinstimmungs \_ \_ Typ**](/windows/desktop/api/drt/ne-drt-drt_match_type)                             | Definiert die Genauigkeit der Ergebnisse, die zurückgegeben werden, wenn eine Suche durchgeführt wird.                                                                                                 |
| [**\_ \_ \_ regeländerungstyp für DRT-blattsatz \_**](/windows/desktop/api/drt/ne-drt-drt_leafset_key_change_type) | Definiert die Gruppe von Änderungs Typen, die auf einem lokalen Blatt Satz Knoten im lokalen DRT-Cache ausgeführt werden können.                                                                |
| [**DRT \_ - \_ Ereignistyp**](/windows/desktop/api/drt/ne-drt-drt_event_type)                             | Definiert den Satz von Ereignissen, die von der DRT ausgelöst werden können.                                                                                                              |
| [**DRT- \_ Sicherheits \_ Modus**](/windows/desktop/api/drt/ne-drt-drt_security_mode)                       | Definiert die möglichen Sicherheitsmodi des DRT. Diese Enumeration ist ein Feld der [**DRT- \_ Einstellungs**](/windows/desktop/api/drt/ns-drt-drt_settings) Struktur.                                   |
| [**DRT- \_ Registrierungs \_ Status**](/windows/desktop/api/drt/ne-drt-drt_registration_state)             | Definiert den Zustand eines registrierten Schlüssels.                                                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Strukturen verteilter Routing Tabellen](distributed-routing-table-structures.md)
</dt> <dt>

[Tabellen Funktionen für verteilte Routing](distributed-routing-table-functions.md)
</dt> <dt>

[Tabellen-API Referenz zu verteiltem Routing](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



