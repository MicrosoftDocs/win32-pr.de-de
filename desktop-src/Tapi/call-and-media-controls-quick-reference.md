---
description: In der folgenden Tabelle sind die COM-Schnittstellen der TAPI-Version 3 nach Kategorie nach Wichtigkeit aufgelistet.
ms.assetid: fafb6d6e-934e-4942-8b90-dacb7ba09752
title: Kurzübersicht über Aufrufe und mediensteuer Elemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ed3105612205d6d516b8d0c5e4f0a7bf9719b3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361123"
---
# <a name="call-and-media-controls-quick-reference"></a>Kurzübersicht über Aufrufe und mediensteuer Elemente

\[ Die [ipconf-MSP-Schnittstellen](ipconf-msp-interfaces.md) sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

In der folgenden Tabelle sind die COM-Schnittstellen der TAPI-Version 3 nach Kategorie nach Wichtigkeit aufgelistet. Die Schnittstellen sind gemäß der fünf grundlegenden Aufruf Steuerungs Objekte von TAPI 3 gruppiert: TAPI, Address, Terminal, Anruf und callhub. Verbleibende Schnittstellen sind gemäß den Schnittstellen für die automatische aufrufsverteilung (ACD) gruppiert, die die Callcenter-Funktionalität bereitstellen. Enumeratorschnittstellen und eigenständige Objekte.



| Schnittstellen Gruppierungen                                          | BESCHREIBUNG                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TAPI-Objekt Schnittstellen](tapi-object-interfaces.md)         | Das TAPI-Objekt ist das Hauptobjekt für TAPI 3.                                                                                                                                                                                                              |
| [Adress Objekt Schnittstellen](address-object-interfaces.md)   | Das Address-Objekt stellt eine Entität dar, die Aufrufe ausführen oder empfangen kann. Die zugeordneten Schnittstellen und Methoden ermöglichen es einer Anwendung, Informationen über die Adresse zu erhalten und festzulegen, z. b. ob Sie die Unterstützung für Aufrufer                             |
| [Terminal Objekt Schnittstellen](terminal-object-interfaces.md) | Das Terminal Objekt stellt die Senke oder Quelle am Beendigungs-oder Ursprungs Punkt eines Aufrufes dar. Mithilfe der zugeordneten Schnittstellen und Methoden kann eine Anwendung Informationen über das Terminal erhalten und festlegen, z. b., ob Sie zurzeit verwendet wird. |
| [Objekt Schnittstellen abrufen](call-object-interfaces.md)         | Das callsobjekt stellt einen-Rückruf dar und wird erstellt, wenn ein-Rückruf vorhanden ist. Die zugeordneten Schnittstellen und Methoden abrufen und legen Informationen über den-Befehl fest, z. b. den aktuellen aufrufzustand.                                                           |
| [Telefon Objekt Schnittstellen](phone-object-interfaces.md)       | Das Telefon Objekt ist die Entität, die das eigentliche Telefongerät und alle seine Steuerelemente darstellt.                                                                                                                                                             |
| [Ipconf-MSP-Schnittstellen](ipconf-msp-interfaces.md)           | Der IP-Konferenz-MSP implementiert verschiedene Schnittstellen für Teilnehmer Steuerelemente, die für das calltobjekt verfügbar gemacht werden.                                                                                                                                          |
| [Callhub-Objekt Schnittstellen](callhub-object-interfaces.md)   | Das callhub-Objekt stellt eine Drittanbieter Ansicht eines aufgerufenen von mehreren Parteien dar. Die zugeordneten Schnittstellen und Methoden abrufen und legen Informationen über den-Befehl fest, z. b. ob der callhub aktiv ist.                                                          |
| [Enumeratorschnittstellen](enumerator-interfaces.md)           | COM-Standard-Enumeratorschnittstellen.                                                                                                                                                                                                                         |
| [Ereignis Schnittstellen](./event-interfaces.md)            | Die Ereignis Schnittstellen werden auch mit ihren Objekt-oder Funktions Gruppierungen angezeigt.                                                                                                                                                                                |
| [Eigenständige Objekte](stand-alone-objects.md)               | Die eigenständigen TAPI 3-Objekte stellen Schnittstellen und Methoden für Vorgänge wie z. b. die unterstützte Telefonie oder Ereignis Behandlung bereit.                                                                                                                    |



 

 

 
