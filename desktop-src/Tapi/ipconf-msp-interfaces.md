---
description: Der MSP für die IP-Konferenz implementiert mehrere anbieterspezifische Schnittstellen für die Teilnehmer Steuerung. Diese Schnittstellen werden für das-Objekt aufgerufen, wenn dieser MSP dem-Befehl zugeordnet ist.
ms.assetid: 01af2452-de2d-42ce-970d-82a83ae0b428
title: Ipconf-MSP-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edb3c04a93909d237ae25e06c3ed2e0fcc5db9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131044"
---
# <a name="ipconf-msp-interfaces"></a>Ipconf-MSP-Schnittstellen

\[ Die ipconf-MSP-Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Der MSP für die IP-Konferenz implementiert mehrere anbieterspezifische Schnittstellen für die Teilnehmer Steuerung. Diese Schnittstellen werden für das-Objekt aufgerufen, wenn dieser MSP dem-Befehl zugeordnet ist.

Die [**itparticipvorgänger Vent**](itparticipantevent.md) -Schnittstelle und die [**ienumparticipants**](ienumparticipant.md) -Schnittstelle sind eigenständige Objekte und werden hier zur Verfügung gestellt.



| Schnittstelle                                            | BESCHREIBUNG                                                                                                                                               |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Imulticastcontrol**](imulticastcontrol.md)       | Ermöglicht es einer Anwendung, den Loopback Modus ( [**Multicast- \_ Loopback \_ Modus**](multicast-loopback-mode.md)) für ein Multicast Konferenz Objekt festzulegen und zu erhalten. |
| [**Itteilnehmer**](itparticipant.md)               | Ermöglicht einer Anwendung das Abrufen von Informationen zu Konferenzteilnehmern und das Abrufen von Zeigern auf die Streams, die diesen Teilnehmern zugeordnet sind.             |
| [**Itparticipantcontrol**](itparticipantcontrol.md) | Ermöglicht es einer Anwendung, Zeiger auf die Teilnehmer einer Konferenz abzurufen.                                                                           |
| [**Itparticipvorgänger Vent**](itparticipantevent.md)     | Ermöglicht es einer Anwendung, Ereignis Informationen zu einem Konferenzteilnehmer abzurufen.                                                                  |
| [**Ienumteilnehmer**](ienumparticipant.md)         | Listet den [**itteilnehmer**](itparticipant.md)auf.                                                                                                        |



 

 

 



