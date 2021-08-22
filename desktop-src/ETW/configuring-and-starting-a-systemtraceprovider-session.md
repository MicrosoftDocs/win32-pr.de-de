---
description: SystemTraceProvider ist ein Kernelanbieter mit vordefinierten Kernelereignissen, die unter Windows 7, Windows Server 2008 R2 und höher unterstützt werden.
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: Konfigurieren und Starten einer SystemTraceProvider-Sitzung
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 0e5d46ceb800479c56ef02d0bb03c3426f73d080e79356f2d7462e27db3a259a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070250"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a>Konfigurieren und Starten einer SystemTraceProvider-Sitzung

SystemTraceProvider ist ein Kernelanbieter mit vordefinierten Kernelereignissen, die unter Windows 7, Windows Server 2008 R2 und höher unterstützt werden. Unter Windows 7 und Windows Server 2008 R2 konnte SystemTraceProvider nur für die NT-Kernelprotokollierungssitzung verwendet werden.

Bei Windows 8, Windows Server 2012 und höher kann der SystemTraceProvider für bis zu 8 Protokollierungssitzungen multiplexiert werden. Die ersten beiden Slots für Protokollierungssitzungen sind für die NT-Kernelprotokollierung und die zirkuläre Kernelkontextprotokollierung reserviert.

Weitere Informationen zur Verwendung der NT-Kernelprotokollierungssitzung als Ablaufverfolgungsanbieter finden Sie unter Konfigurieren und Starten der [NT-Kernelprotokollierungssitzung](configuring-and-starting-the-nt-kernel-logger-session.md).

In Windows 10 SDK-Build 20348 und höher kann Der SystemTraceProvider über separate Systemanbieter konfiguriert werden, die mit [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) wie der Standardereignisablaufverfolgung für Windows-Ereignisanbieter gesteuert werden können. Eine vollständige Liste der Systemanbieter, Schlüsselwörter und entsprechenden Legacyflags und Gruppen finden Sie unter [Systemanbieter.](system-providers.md)

## <a name="enable-a-systemtraceprovider-session"></a>Aktivieren einer SystemTraceProvider-Sitzung

Um SystemTraceProvider das Starten einer anderen Sitzung als der NT-Kernelprotokollierung zu ermöglichen, führen Sie den folgenden Befehl aus:

**tracelog -start MySession -f c: \\ Kernel1.etl -eflag PROC \_ THREAD+LOADER+CSWITCH**

Um den SystemTraceProvider programmgesteuert zu aktivieren, um eine andere Sitzung als die NT-Kernelprotokollierung zu starten, verwenden Sie die folgenden Schritte.

-   Definieren Sie einen Namen für die private Protokollierung.

    **\#PRIVATE \_ PROTOKOLLIERUNGSNAME \_ L"Einige private Ablaufverfolgungssitzung" definieren**

-   Legen Sie am Controller die folgenden Member der [**EVENT \_ TRACE \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) fest.

    Legen **Sie LogFileMode auf** EVENT TRACE SYSTEM **\_ \_ \_ LOGGER MODE \_ fest.**

    Legen **Sie LoggerName auf** private Protokollierung anstelle des **\_ KERNELPROTOKOLLIERUNGSNAMENs \_ fest.**

    Stellen Sie sicher, dass das **Wnode.Guid-Member** der [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) nicht auf **SystemTraceControlGuid festgelegt ist.** Sie müssen diesem **Member eine neue GUID** zuweisen.

-   Legen Sie auf dem Consumer den **Member LoggerName** der [**EVENT TRACE \_ \_ LOGFILE-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) auf diese private Protokollierung fest.

> [!Note]  
> Wenn sie möchten, dass ein Nichtadministrator oder ein Nicht-TCB-Prozess eine Profilerstellungs-Ablaufverfolgungssitzung mit systemTraceProvider im Namen von Anwendungen von Drittanbietern starten kann, müssen Sie dem Benutzerprofil Berechtigungen erteilen und diesen Benutzer dann sowohl der **Sitzungs-GUID** (erstellt für die Protokollierungssitzung) als auch der **GUID** des Systemverfolgungsanbieters hinzufügen, um den Systemverfolgungsanbieter zu aktivieren. Weitere Informationen finden Sie unter Der [**EventAccessControl-Funktion.**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol)

 

## <a name="related-topics"></a>Zugehörige Themen

[Konfigurieren und Starten einer privaten Protokollierungssitzung](configuring-and-starting-a-private-logger-session.md)

[Konfigurieren und Starten einer AutoLogger-Sitzung](configuring-and-starting-an-autologger-session.md)

[Konfigurieren und Starten einer Ereignisablaufverfolgungssitzung](configuring-and-starting-an-event-tracing-session.md)

[Konfigurieren und Starten der NT-Kernelprotokollierungssitzung](configuring-and-starting-the-nt-kernel-logger-session.md)

[Systemanbieter](system-providers.md)

[Aktualisieren einer Ereignisablaufverfolgungssitzung](updating-an-event-tracing-session.md)

 

 
