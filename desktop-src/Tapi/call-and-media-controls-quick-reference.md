---
description: In der folgenden Tabelle sind DIE TAPI-COM-Schnittstellen der Version 3 nach Kategorie nach Wichtigkeit aufgelistet.
ms.assetid: fafb6d6e-934e-4942-8b90-dacb7ba09752
title: Kurzübersicht über Aufruf- und Mediensteuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9985f88997e454a05838f0dec499d9036fb114e3e89ea543619c8359d1a03d8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117948262"
---
# <a name="call-and-media-controls-quick-reference"></a>Kurzübersicht über Aufruf- und Mediensteuerelemente

\[Die [IPConf-MSP-Schnittstellen](ipconf-msp-interfaces.md) sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

In der folgenden Tabelle sind DIE TAPI-COM-Schnittstellen der Version 3 nach Kategorie nach Wichtigkeit aufgelistet. Die Schnittstellen werden nach den fünf grundlegenden Objekt der TAPI 3-Aufrufsteuerung gruppiert: TAPI, Address, Terminal, Call und CallHub. Verbleibende Schnittstellen werden nach ACD-Schnittstellen (Automatic Call Distribution) gruppiert, die Callcenterfunktionen bereitstellen. Enumeratorschnittstellen und eigenständige Objekte.



| Schnittstellengruppierungen                                          | Beschreibung                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TAPI-Objektschnittstellen](tapi-object-interfaces.md)         | Das TAPI-Objekt ist das Hauptobjekt für TAPI 3.                                                                                                                                                                                                              |
| [Adressobjektschnittstellen](address-object-interfaces.md)   | Das Address-Objekt stellt eine Entität dar, die Aufrufe vornehmen oder empfangen kann. Die zugeordneten Schnittstellen und Methoden ermöglichen einer Anwendung das Abrufen und Festlegen von Informationen zur Adresse, z. B. ob sie über Aufrufer-ID-Unterstützung verfügt.                             |
| [Terminalobjektschnittstellen](terminal-object-interfaces.md) | Das Terminalobjekt stellt die Senke oder Quelle am Beendigungs- oder Ursprungspunkt eines Aufrufs dar. Die zugeordneten Schnittstellen und Methoden ermöglichen einer Anwendung das Abrufen und Festlegen von Informationen über das Terminal, z. B. ob es derzeit verwendet wird. |
| [Aufrufen von Objektschnittstellen](call-object-interfaces.md)         | Das Call-Objekt stellt einen Aufruf dar und wird erstellt, wenn ein Aufruf eintritt. Die zugeordneten Schnittstellen und Methoden rufen Informationen zum Aufruf ab, z. B. den aktuellen Aufrufzustand, und legen sie fest.                                                           |
| [Telefon Objektschnittstellen](phone-object-interfaces.md)       | Das Telefon-Objekt ist die Entität, die das tatsächliche Telefongerät und alle zugehörigen Steuerelemente darstellt.                                                                                                                                                             |
| [IPConf-MSP-Schnittstellen](ipconf-msp-interfaces.md)           | Der IP-Konferenz-MSP implementiert mehrere Schnittstellen für die Teilnehmersteuerung, die für das Aufrufobjekt verfügbar gemacht werden.                                                                                                                                          |
| [CallHub-Objektschnittstellen](callhub-object-interfaces.md)   | Das CallHub-Objekt stellt eine Drittanbieteransicht eines Mehrparteienaufrufs dar. Die zugeordneten Schnittstellen und Methoden rufen Informationen zum Aufruf ab und legen diese fest, z. B. ob der Aufrufhub aktiv ist.                                                          |
| [Enumeratorschnittstellen](enumerator-interfaces.md)           | COM-Standard-Enumeratorschnittstellen.                                                                                                                                                                                                                         |
| [Ereignisschnittstellen](./event-interfaces.md)            | Die Ereignisschnittstellen werden auch mit ihren Objekt- oder Funktionsgruppierungen angezeigt.                                                                                                                                                                                |
| [Eigenständige Objekte](stand-alone-objects.md)               | Die verschiedenen eigenständigen TAPI 3-Objekte stellen Schnittstellen und Methoden für Vorgänge wie die unterstützte Telefonie oder Ereignisbehandlung bereit.                                                                                                                    |



 

 

 
