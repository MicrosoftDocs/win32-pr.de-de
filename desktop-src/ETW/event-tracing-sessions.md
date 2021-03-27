---
description: Ereignis Ablauf Verfolgungs Sitzungen zeichnen Ereignisse von einem oder mehreren Anbietern auf, die ein Controller ermöglicht.
ms.assetid: 6e446ee3-47a3-4fe1-9eb7-3dd74cad4e56
title: Ereignis Ablauf Verfolgungs Sitzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce49453881d9106119dab15b64ac0698e9a493f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866428"
---
# <a name="event-tracing-sessions"></a>Ereignis Ablauf Verfolgungs Sitzungen

Ereignis Ablauf Verfolgungs Sitzungen zeichnen Ereignisse von einem oder mehreren [Anbietern](providing-events.md) auf, die ein [Controller](controlling-event-tracing-sessions.md) ermöglicht. Die Sitzung ist auch für das Verwalten und leeren der Puffer verantwortlich. Der Controller definiert die Sitzung, in der Regel die Sitzungs-und Protokoll Dateiname, der Typ der zu verwendenden Protokolldatei und die Auflösung des Zeitstempels, der zum Aufzeichnen der Ereignisse verwendet wird, angegeben werden.

Die Ereignis Ablauf Verfolgung unterstützt maximal 64 Ereignis Ablauf Verfolgungs Sitzungen, die gleichzeitig ausgeführt werden. In diesen Sitzungen gibt es zwei besondere Zweck Sitzungen. Die verbleibenden Sitzungen sind für die allgemeine Verwendung verfügbar. Die zwei speziellen Zweck Sitzungen sind:

-   Globale Protokollierungs Sitzung
-   NT-Kernel Protokollierungs Sitzung

Die Ereignis Ablauf Verfolgungs Sitzung für globale Protokollierung zeichnet Ereignisse auf, die früh im Startprozess des Betriebssystems auftreten, z. b. die von Gerätetreibern generierten Ereignisse. Weitere Informationen zum Konfigurieren der Ereignis Ablauf Verfolgungs Sitzung für globale Protokollierung finden Sie unter [Konfigurieren und Starten der globalen](configuring-and-starting-the-global-logger-session.md)Protokollierungs Sitzung.

Die NT Kernel Logger-Ereignis Ablauf Verfolgungs Sitzung zeichnet vordefinierte Systemereignisse auf, die vom Betriebssystem generiert werden, z. b. Datenträger-e/a oder Seiten Fehler Weitere Informationen zum Konfigurieren der NT Kernel Logger-Ereignis Ablauf Verfolgungs Sitzung, zum [Konfigurieren und Starten der NT Kernel Logger-Sitzung](configuring-and-starting-the-nt-kernel-logger-session.md).

Weitere Informationen zum Definieren einer regulären Ereignis Ablauf Verfolgungs Sitzung finden Sie unter [Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung](configuring-and-starting-an-event-tracing-session.md).

**Windows 2000:** Unterstützt nur 32-Ereignis Ablauf Verfolgungs Sitzungen.

 

 



