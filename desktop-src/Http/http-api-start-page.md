---
title: HTTP-Server-API
description: Die HTTP-Server-API ermöglicht Anwendungen die Kommunikation über HTTP, ohne Microsoft Internet Information Server (IIS) zu verwenden.
ms.assetid: ef18716c-7511-4c8a-99bc-28369c3e46f4
keywords:
- HTTP-Server-API
- HTTP-Server-API, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8f99045b24d0ef79c267615791c62da50ed8e40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101623"
---
# <a name="http-server-api"></a>HTTP-Server-API

## <a name="purpose"></a>Zweck

Die HTTP-Server-API ermöglicht Anwendungen die Kommunikation über HTTP, ohne Microsoft Internet Information Server (IIS) zu verwenden. Anwendungen können sich registrieren, um HTTP-Anforderungen für bestimmte URLs zu empfangen, HTTP-Anforderungen zu empfangen und HTTP-Antworten zu senden. Die HTTP-Server-API umfasst SSL-Unterstützung, sodass Anwendungen Daten über sichere HTTP-Verbindungen ohne IIS austauschen können. Es ist auch für die Arbeit mit e/a-Abschlussports konzipiert.

## <a name="developer-audience"></a>Entwicklergruppe

Diese API ist für die Verwendung durch C/C++-Programmierer konzipiert.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die HTTP-Server-API wird auf Windows Server 2003-Betriebssystemen und unter Windows XP mit Service Pack 2 (SP2) unterstützt. Beachten Sie, dass Microsoft IIS 5, das unter Windows XP mit SP2 ausgeführt wird, Port 80 nicht gemeinsam mit anderen HTTP-Anwendungen freigeben kann, die gleichzeitig ausgeführt werden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                           | BESCHREIBUNG                                                                                             |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Informationen zur HTTP-Server-API](about-http-server-api.md)<br/>                   | Allgemeine Informationen zu http.<br/>                                                              |
| [Verwenden der HTTP-Server-API](using-http-server-api.md)<br/>                   | Leitfaden für Prozeduren zur Verwendung von http.<br/>                                                             |
| [HTTP-Server-API-Referenz](http-server-api-reference.md)<br/>           | Dokumentation zu bestimmten Funktionen, Strukturen und Enumerationstypen, die in http verfügbar sind.<br/>    |
| [Beispielanwendung für http-Server](http-server-sample-application.md)<br/> | Eine Beispielanwendung, die zeigt, wie die HTTP-Server-API verwendet wird, um Server seitige Aufgaben auszuführen.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

