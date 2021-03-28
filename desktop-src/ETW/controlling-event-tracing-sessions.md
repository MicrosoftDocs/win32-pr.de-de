---
description: Ereignis Ablauf Verfolgungs Sitzungen zeichnen Ereignisse von einem oder mehreren Anbietern auf.
ms.assetid: 43841d2f-5a4c-493d-9531-21941311ffbc
title: Steuern von Ereignis Ablauf Verfolgungs Sitzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03f1917354679e7a68f9dbd001fc3aa10f09db0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977720"
---
# <a name="controlling-event-tracing-sessions"></a>Steuern von Ereignis Ablauf Verfolgungs Sitzungen

Ereignis Ablauf Verfolgungs Sitzungen zeichnen Ereignisse von einem oder mehreren [Anbietern](providing-events.md)auf. Der Controller definiert die Sitzung und aktiviert die Anbieter. Das Definieren der Sitzung umfasst in der Regel die Angabe von Sitzungs-und Protokoll Dateiname, Typ der zu verwendenden Protokolldatei und die Auflösung des Zeitstempels, der zum Aufzeichnen der Ereignisse verwendet wird. Controller können auch Ereignis Ablauf Verfolgungs Sitzungen aktualisieren und Abfragen.

In den folgenden Themen wird gezeigt, wie Sie eine Sitzung definieren und aktualisieren und Ereignis Ablauf Verfolgungs Anbieter aktivieren:

-   [Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung](configuring-and-starting-an-event-tracing-session.md)
-   [Konfigurieren und Starten einer systemtraceprovider-Sitzung](configuring-and-starting-a-systemtraceprovider-session.md)
-   [Konfigurieren und Starten einer autologger-Sitzung](configuring-and-starting-an-autologger-session.md)
-   [Konfigurieren und Starten einer Sitzung für private Logger](configuring-and-starting-a-private-logger-session.md)
-   [Aktualisieren einer Ereignis Ablauf Verfolgungs Sitzung](updating-an-event-tracing-session.md)
-   [Abrufen von zusätzlichen Ereignis Ablauf Verfolgungs Daten](retrieving-additional-event-tracing-data.md)

Informationen zum leeren und Abfragen von Sitzungen finden Sie unter [**controltrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) bzw. [**queryalltraces**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa).

Nur Benutzer, die mit erhöhten Administratorrechten ausgeführt werden, Benutzer in der Gruppe der Leistungs Protokoll Benutzer und Anwendungen, die als LocalSystem, LocalService oder Network Service ausgeführt werden, können Ereignisse für die Ereignis Ablauf Verfolgung steuern. Um einem eingeschränkten Benutzer die Möglichkeit zu geben, Ablauf Verfolgungs Sitzungen zu steuern, fügen Sie diese der Gruppe Leistungs Protokoll Benutzer hinzu.

**Windows XP und Windows 2000:** Jeder kann eine Ablauf Verfolgungs Sitzung steuern.

 

 
