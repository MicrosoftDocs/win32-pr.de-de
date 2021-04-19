---
description: 'Weitere Informationen finden Sie hier: Winsock-Ablauf Verfolgungs Ebenen'
ms.assetid: a92bc4d2-257a-478a-b10d-4fada4323c9b
title: Winsock-Ablauf Verfolgungs Ebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b225558015fb823cd02028a1ae1433d3d0549896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349584"
---
# <a name="winsock-tracing-levels"></a>Winsock-Ablauf Verfolgungs Ebenen

## <a name="levels-of-winsock-tracing"></a>Ebenen der Winsock-Ablauf Verfolgung

Die Winsock-Ablauf Verfolgung kann auf zwei Ebenen protokolliert werden:

-   Information
-   Ausführlich

Die Informationsebene verfolgt socketerstellungs-und schließereignisse sowie alle Fehler, die auf dem Socket auftreten.

Die ausführliche Ebene umfasst die Ereignisse auf Informationsebene und fügt zusätzliche Ablauf Verfolgung für Sende-und Empfangs Ereignisse hinzu. Die ausführliche Protokollierung wird verwendet, um Puffer Beschädigungs Probleme und schlecht geschriebene Anwendungen abzufangen.

Die Informationen oder die ausführliche Ebene können mit der Winsock-Netzwerk Ereignis Ablauf Verfolgung verwendet werden. Die Änderungs Ablauf Verfolgung für den Winsock-Katalog unterstützt nur Informationsebenen.

## <a name="information-event-tracing"></a>Ablauf Verfolgung von Informations Ereignissen

In der folgenden Liste sind die Winsock-netzwerkereignissocketvorgänge aufgeführt, die auf der Informationsebene nachverfolgt werden:

-   Socketerstellung

    Ein Ereignis wird bei der Socketerstellung protokolliert, die zum Verfolgen der Lebensdauer eines Sockets verwendet werden kann. Diese Ereignisse umfassen auch Sockets, die durch die Annahme von Verbindungen an einem Abhör Socket erstellt werden.

-   Bind

    Die lokale IP-Adresse wird protokolliert, um die Winsock-Ablauf Verfolgungs Informationen mit den socketaufrufen einer Anwendung zu korrelieren.

-   Verbinden

    Die Remote-IP-Adresse des verbundenen Sockets wird protokolliert, um die Winsock-Ablauf Verfolgungs Informationen mit den socketaufrufen einer Anwendung zu korrelieren.

-   Winsock-initiierte Abbrüche und Abbruch

    Jedes Mal, wenn Winsock eine Anforderung aktiv abbricht oder abbricht, wird das Ereignis protokolliert.

-   Vom Transport initiierte zurück Stellungen

    Jedes Mal, wenn der zugrunde liegende Transport angibt, dass eine Verbindung zurückgesetzt wurde, wird das Ereignis protokolliert.

-   Sende-und Empfangs Fehler

    Wenn ein Sende-oder Empfangs Aufruf an den zugrunde liegenden Transport fehlschlägt, wird das Ereignis protokolliert.

-   Sockettrennung und-schließen

    Ein Ereignis wird protokolliert, wenn ein Sockethandle geschlossen wird.

## <a name="verbose-event-tracing"></a>Ausführliche Ereignis Ablauf Verfolgung

Alle Informations Ereignisse werden auf ausführliche-Ebene verfolgt. In der folgenden Liste werden die zusätzlichen Winsock-netzwerkereignissocketvorgänge ausführlich erläutert, die auf ausführlicher Ebene verfolgt werden:

-   Sende-und Empfangs Puffer

    Ereignisse werden von Benutzer Puffer Adressen und-Längen protokolliert, wenn Sende-und Empfangs Aufrufe an Winsock gesendet werden, und nach Abschluss dieser Aufrufe. Dies ist nützlich für die Diagnose von Problemen bei der Wiederverwendung von Puffern sowie für die ineffiziente Verwendung von Puffern.

-   Socketoptionen

    Ein Ereignis wird protokolliert, wenn eine Anwendung bestimmte socketoptionswerte ändert. Zu den protokollierten Optionen zählen \_ beispielsweise sndbuf, \_ rcvbuf, die Option für \_ \_ zirkuläre \_ Warteschlangen und "fonbio".

-   Wsapoll und SELECT

    Ein Ereignis wird in der Verwendung von [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) und [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -Aufrufen der Anwendung protokolliert, die zum Auffinden von Leistungs Engpässen verwendet werden kann.

-   Winsock-initiierte Abbrüche und Abbruch

    Jedes Mal, wenn Winsock eine Anforderung aktiv abbricht oder abbricht, wird das Ereignis protokolliert.

-   Ereignis Maske

    Ein Ereignis wird von der Ereignis Maske protokolliert, die eine Anwendung für die Verwendung der [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) -Funktion registriert.

-   Datagramm

    Ein Ereignis wird immer dann protokolliert, wenn ein Datagramm eintrifft und kein Pufferbereich vorhanden ist, in dem es kopiert werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kontrolle über die Winsock-Ablauf Verfolgung](control-of-winsock-tracing.md)
</dt> <dt>

[Winsock-Ablauf Verfolgung](winsock-tracing.md)
</dt> <dt>

[Details zur Änderung der Winsock-Katalog Änderung](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Details der Winsock-Netzwerk Ereignis Ablauf Verfolgung](winsock-tracing-event-details.md)
</dt> </dl>

 

 
