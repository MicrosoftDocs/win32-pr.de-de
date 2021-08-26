---
description: Die folgenden Strukturen unterstützen die DRT-API-Funktionen (Distributed Routing Table).
ms.assetid: 3ff85b24-5ec0-4b26-b30e-1bf8030a575d
title: Verteilte Routingtabellenstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7613b63559eadd2b19229228b9d57fb438b6bd2bbb1b5a9d335a6513c1e8bfee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978940"
---
# <a name="distributed-routing-table-structures"></a>Verteilte Routingtabellenstrukturen

Die folgenden Strukturen unterstützen die DRT-API-Funktionen (Distributed Routing Table).



| Struktur                                                  | Beschreibung                                                                                                                                                                              |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DRT \_ DATA**](/windows/desktop/api/drt/ns-drt-drt_data)                              | Enthält ein Datenblob. Diese Struktur wird von mehreren DRT-Funktionen verwendet.                                                                                                                   |
| [**\_DRT-REGISTRIERUNG**](/windows/desktop/api/drt/ns-drt-drt_registration)              | Enthält die Schlüsselregistrierung. Dies ist ein Member der [**DRT \_ SEARCH \_ RESULT-Struktur**](/windows/desktop/api/drt/ns-drt-drt_search_result) und ein Argument, das an [**DrtRegisterKey übergeben wird.**](/windows/desktop/api/drt/nf-drt-drtregisterkey) |
| [**\_DRT-ADRESSE**](/windows/desktop/api/drt/ns-drt-drt_address)                        | Enthält Endpunktinformationen zu einem DRT-Knoten, der an einer Suche beteiligt war. Diese Informationen sind für das Debuggen von Konnektivitätsproblemen vorgesehen.                                   |
| [**\_DRT-ADRESSLISTE \_**](/windows/desktop/api/drt/ns-drt-drt_address_list)             | Enthält eine Reihe von [**DRT \_ ADDRESS-Strukturen,**](/windows/desktop/api/drt/ns-drt-drt_address) die die Knoten darstellen, die während einer Schlüsselsuche kontaktiert werden.                                                             |
| [**\_DRT-SICHERHEITSANBIETER \_**](/windows/desktop/api/Drt/ns-drt-drt_security_provider)   | Definiert die Schnittstelle, die von einem Sicherheitsanbieter implementiert werden muss.                                                                                                                   |
| [**DRT \_ \_ BOOTSTRAP-ANBIETER**](/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider) | Definiert die Schnittstelle, die von einem Bootstrapanbieter implementiert werden muss.                                                                                                                  |
| [**\_DRT-EINSTELLUNGEN**](/windows/desktop/api/drt/ns-drt-drt_settings)                      | Definiert DRT-Einstellungen bei der Initialisierung. Diese Struktur wird als Argument an [**DrtOpen übergeben.**](/windows/desktop/api/drt/nf-drt-drtopen)                                                                           |
| [**\_DRT-SUCHINFORMATIONEN \_**](/windows/desktop/api/drt/ns-drt-drt_search_info)               | Definiert eine Suchabfrage. Diese Struktur wird als Argument an [**DrtStartSearch übergeben.**](/windows/desktop/api/drt/nf-drt-drtstartsearch)                                                                             |
| [**\_DRT-SUCHERGEBNIS \_**](/windows/desktop/api/drt/ns-drt-drt_search_result)           | Enthält ein Suchergebnis. Diese Struktur wird von [**DrtGetSearchResult zurückgegeben.**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)                                                                                |
| [**\_DRT-EREIGNISDATEN \_**](/windows/desktop/api/drt/ns-drt-drt_event_data)                 | Enthält die Ereignisdaten, die durch Aufrufen von [**DrtGetEventData zurückgegeben werden,**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) nachdem eine Anwendung ein Ereignissignal empfangen hat.                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verteilte Routingtabellenenumeration](distributed-routing-table-enumerations.md)
</dt> <dt>

[Verteilte Routingtabellenfunktionen](distributed-routing-table-functions.md)
</dt> <dt>

[Distributed Routing Tabellen-API Reference](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



