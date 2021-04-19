---
description: Die folgenden Strukturen unterstützen die DRT-API-Funktionen (verteilte Routing Tabelle).
ms.assetid: 3ff85b24-5ec0-4b26-b30e-1bf8030a575d
title: Strukturen verteilter Routing Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d454d2c28008422da897dc91ca9a3dc29db374b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349230"
---
# <a name="distributed-routing-table-structures"></a>Strukturen verteilter Routing Tabellen

Die folgenden Strukturen unterstützen die DRT-API-Funktionen (verteilte Routing Tabelle).



| Struktur                                                  | BESCHREIBUNG                                                                                                                                                                              |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DRT- \_ Daten**](/windows/desktop/api/drt/ns-drt-drt_data)                              | Enthält ein Daten-BLOB. Diese Struktur wird von mehreren DRT-Funktionen verwendet.                                                                                                                   |
| [**DRT- \_ Registrierung**](/windows/desktop/api/drt/ns-drt-drt_registration)              | Enthält die Schlüssel Registrierung. Dies ist ein Member der [**DRT- \_ Such \_ Ergebnis**](/windows/desktop/api/drt/ns-drt-drt_search_result) Struktur und ein Argument, das an [**drtregisterkey**](/windows/desktop/api/drt/nf-drt-drtregisterkey)übermittelt wird. |
| [**DRT- \_ Adresse**](/windows/desktop/api/drt/ns-drt-drt_address)                        | Enthält Endpunkt Informationen zu einem DRT-Knoten, der an einer Suche beteiligt war. Diese Informationen sind zum Debuggen von Konnektivitätsproblemen gedacht.                                   |
| [**Liste der DRT- \_ Adressen \_**](/windows/desktop/api/drt/ns-drt-drt_address_list)             | Enthält einen Satz von [**DRT- \_ Adress**](/windows/desktop/api/drt/ns-drt-drt_address) Strukturen, die die während einer Suche nach einem Schlüssel verbundenen Knoten darstellen.                                                             |
| [**DRT- \_ Sicherheits \_ Anbieter**](/windows/desktop/api/Drt/ns-drt-drt_security_provider)   | Definiert die Schnittstelle, die von einem Sicherheitsanbieter implementiert werden muss.                                                                                                                   |
| [**DRT- \_ Bootstrap- \_ Anbieter**](/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider) | Definiert die Schnittstelle, die von einem Bootstrap-Anbieter implementiert werden muss.                                                                                                                  |
| [**DRT- \_ Einstellungen**](/windows/desktop/api/drt/ns-drt-drt_settings)                      | Definiert DRT-Einstellungen bei der Initialisierung. Diese Struktur wird als Argument an [**drtopen**](/windows/desktop/api/drt/nf-drt-drtopen)übermittelt.                                                                           |
| [**DRT- \_ Such \_ Informationen**](/windows/desktop/api/drt/ns-drt-drt_search_info)               | Definiert eine Suchabfrage. Diese Struktur wird als Argument an [**drtstartsearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch)übermittelt.                                                                             |
| [**DRT- \_ Such \_ Ergebnis**](/windows/desktop/api/drt/ns-drt-drt_search_result)           | Enthält ein Suchergebnis. Diese Struktur wird von [**drtgetsearchresult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)zurückgegeben.                                                                                |
| [**DRT- \_ Ereignis \_ Daten**](/windows/desktop/api/drt/ns-drt-drt_event_data)                 | Enthält die Ereignisdaten, die zurückgegeben werden, indem [**drtgeteventdata**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) aufgerufen wird, nachdem eine Anwendung ein Ereignis Signal empfangen hat.                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verteilte Routing Tabellen-Enumerationen](distributed-routing-table-enumerations.md)
</dt> <dt>

[Tabellen Funktionen für verteilte Routing](distributed-routing-table-functions.md)
</dt> <dt>

[Tabellen-API Referenz zu verteiltem Routing](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



