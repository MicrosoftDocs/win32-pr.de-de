---
description: Ereignisablaufverfolgungssitzungen zeichnen Ereignisse von einem oder mehreren Anbietern auf.
ms.assetid: 43841d2f-5a4c-493d-9531-21941311ffbc
title: Steuern von Ereignisablaufverfolgungssitzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5970eb160812991677aac775af60d08458c269152edca4aa2e30cdf30c111d96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130660"
---
# <a name="controlling-event-tracing-sessions"></a>Steuern von Ereignisablaufverfolgungssitzungen

Ereignisablaufverfolgungssitzungen zeichnen Ereignisse von einem oder [mehreren Anbietern auf.](providing-events.md) Der Controller definiert die Sitzung und aktiviert die Anbieter. Das Definieren der Sitzung umfasst in der Regel die Angabe des Sitzungs- und Protokolldateinamens, des Zu verwendenden Protokolldateityps und der Auflösung des Zeitstempels, der zum Aufzeichnen der Ereignisse verwendet wird. Controller können auch Ereignisablaufverfolgungssitzungen aktualisieren und abfragen.

In den folgenden Themen wird veranschaulicht, wie Sie eine Sitzung definieren und aktualisieren und Ereignisablaufverfolgungsanbieter aktivieren:

-   [Konfigurieren und Starten einer Ereignisablaufverfolgungssitzung](configuring-and-starting-an-event-tracing-session.md)
-   [Konfigurieren und Starten einer SystemTraceProvider-Sitzung](configuring-and-starting-a-systemtraceprovider-session.md)
-   [Konfigurieren und Starten einer AutoLogger-Sitzung](configuring-and-starting-an-autologger-session.md)
-   [Konfigurieren und Starten einer privaten Protokollierungssitzung](configuring-and-starting-a-private-logger-session.md)
-   [Aktualisieren einer Ereignisablaufverfolgungssitzung](updating-an-event-tracing-session.md)
-   [Abrufen zusätzlicher Ereignisablaufverfolgungsdaten](retrieving-additional-event-tracing-data.md)

Informationen zum Leeren und Abfragen von Sitzungen finden Sie unter [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) bzw. [**QueryAllTraces.**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa)

Nur Benutzer mit erhöhten Administratorrechten, Benutzer in der Gruppe Leistungsprotokollbenutzer und Anwendungen, die als LocalSystem, LocalService oder NetworkService ausgeführt werden, können Ereignisablaufverfolgungssitzungen steuern. Um einem eingeschränkten Benutzer die Möglichkeit zu gewähren, Ablaufverfolgungssitzungen zu steuern, fügen Sie sie der Gruppe Leistungsprotokollbenutzer hinzu.

**Windows XP und Windows 2000:** Jeder kann eine Ablaufverfolgungssitzung steuern.

 

 
