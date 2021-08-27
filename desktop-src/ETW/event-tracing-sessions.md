---
description: Ereignisablaufverfolgungssitzungen zeichnen Ereignisse von einem oder mehr Anbietern auf, die ein Controller aktiviert.
ms.assetid: 6e446ee3-47a3-4fe1-9eb7-3dd74cad4e56
title: Ereignisablaufverfolgungssitzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2edfe4bdfaf621575d8f2f8ab7d81a09aae8bfbddcb3f63890c4083378bb905b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083240"
---
# <a name="event-tracing-sessions"></a>Ereignisablaufverfolgungssitzungen

Ereignisablaufverfolgungssitzungen zeichnen Ereignisse von einem oder mehr Anbietern [auf,](providing-events.md) die ein [Controller](controlling-event-tracing-sessions.md) aktiviert. Die Sitzung ist auch für das Verwalten und Leeren der Puffer verantwortlich. Der Controller definiert die Sitzung, die in der Regel die Angabe des Sitzungs- und Protokolldateinamens, des Zu verwendenden Protokolldateityps und der Auflösung des Zeitstempels zum Aufzeichnen der Ereignisse umfasst.

Die Ereignisablaufverfolgung unterstützt maximal 64 Ereignisablaufverfolgungssitzungen, die gleichzeitig ausgeführt werden. Von diesen Sitzungen gibt es zwei Sitzungen für besondere Zwecke. Die verbleibenden Sitzungen sind für die allgemeine Verwendung verfügbar. Die beiden Sitzungen für besondere Zwecke sind:

-   Globale Protokollierungssitzung
-   NT-Kernelprotokollierungssitzung

Die Global Logger-Ereignisablaufverfolgungssitzung zeichnet Ereignisse auf, die früh im Startprozess des Betriebssystems auftreten, z. B. von Gerätetreibern generierte Ereignisse. Informationen zum Konfigurieren der Ereignisablaufverfolgungssitzung der globalen Protokollierung finden Sie unter Konfigurieren und [Starten der globalen Protokollierungssitzung.](configuring-and-starting-the-global-logger-session.md)

Die NT Kernel Logger-Ereignisablaufverfolgungssitzung zeichnet vordefinierte Systemereignisse auf, die vom Betriebssystem generiert werden, z. B. Datenträger-E/A- oder Seitenfehlerereignisse. Informationen zum Konfigurieren der Nt Kernel Logger-Ereignisablaufverfolgungssitzung finden Sie unter Konfigurieren und [Starten der NT-Kernelprotokollierungssitzung.](configuring-and-starting-the-nt-kernel-logger-session.md)

Informationen zum Definieren einer regulären Ereignisablaufverfolgungssitzung finden Sie unter Konfigurieren und [Starten einer Ereignisablaufverfolgungssitzung.](configuring-and-starting-an-event-tracing-session.md)

**Windows 2000:** Unterstützt nur 32 Ereignisablaufverfolgungssitzungen.

 

 



