---
description: SystemTraceProvider ist ein Kernelanbieter mit vordefinierten Kernelereignissen, die unter Windows 7, Windows Server 2008 R2 und höher unterstützt werden.
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: Konfigurieren und Starten einer SystemTraceProvider-Sitzung
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 66e9d672a7c8e6358c2a92e7661e0d4e2a5878ab
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386740"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a>Konfigurieren und Starten einer SystemTraceProvider-Sitzung

SystemTraceProvider ist ein Kernelanbieter mit vordefinierten Kernelereignissen, die unter Windows 7, Windows Server 2008 R2 und höher unterstützt werden. Unter Windows 7 und Windows Server 2008 R2 konnte SystemTraceProvider nur für die NT-Kernelprotokollierungssitzung verwendet werden.

Auf Windows 8, Windows Server 2012 und höher, kann SystemTraceProvider für bis zu acht Protokollierungssitzungen multiplexiert werden. Die ersten beiden Slots für Protokollierungssitzungen sind für die NT-Kernelprotokollierung und die Circular Kernel Context Logger reserviert.

Weitere Informationen zur Verwendung der NT-Kernelprotokollierungssitzung als Ablaufverfolgungsanbieter finden Sie unter [Konfigurieren und Starten der NT-Kernelprotokollierungssitzung.](configuring-and-starting-the-nt-kernel-logger-session.md)

Auf Windows 10 SDK-Build 20348 und höher kann SystemTraceProvider über separate Systemanbieter konfiguriert werden, die mit [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) wie standardmäßige Ereignisablaufverfolgung für Windows-Ereignisanbieter gesteuert werden können. Eine vollständige Liste der Systemanbieter, Schlüsselwörter und entsprechenden Legacyflags und -gruppen finden Sie unter [Systemanbieter.](system-providers.md)

## <a name="enable-a-systemtraceprovider-session"></a>Aktivieren einer SystemTraceProvider-Sitzung

Führen Sie den folgenden Befehl aus, damit SystemTraceProvider eine andere Sitzung als die NT-Kernelprotokollierung starten kann:

**tracelog -start MySession -f c: \\ Kernel1.etl -eflag PROC \_ THREAD+LOADER+CSWITCH**

Um systemTraceProvider programmgesteuert so zu aktivieren, dass eine andere Sitzung als die NT-Kernelprotokollierung gestartet wird, gehen Sie wie folgt vor.

-   Definieren Sie einen namen für die private Protokollierung.

    **\#define PRIVATE \_ LOGGER \_ NAME L"Some Private Trace Session"**

-   Legen Sie auf dem Controller die folgenden Member der [**EVENT \_ TRACE \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) fest.

    Legen Sie **LogFileMode** auf **EVENT TRACE SYSTEM \_ \_ \_ LOGGER \_ MODE** fest.

    Legen Sie **LoggerName** anstelle von **KERNEL \_ LOGGER \_ NAME** auf private Protokollierung fest.

    Stellen Sie sicher, dass der **Wnode.Guid-Member** der [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) nicht auf **SystemTraceControlGuid** festgelegt ist. Sie müssen diesem Element eine neue **GUID** zuweisen.

-   Legen Sie auf dem Consumer den **Member LoggerName** der [**EVENT TRACE \_ \_ LOGFILE-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) auf diese private Protokollierung fest.

> [!Note]  
> Wenn Sie möchten, dass ein Nicht-Administratoren- oder Nicht-TCB-Prozess eine Profilerstellungs-Ablaufverfolgungssitzung mit systemTraceProvider im Auftrag von Anwendungen von Drittanbietern starten kann, müssen Sie dem Benutzerprofil berechtigungen gewähren und diesen Benutzer dann sowohl der **Sitzungs-GUID** (erstellt für die Protokollierungssitzung) als auch der **GUID** des Systemablaufverfolgungsanbieters hinzufügen, um den Systemablaufverfolgungsanbieter zu aktivieren. Weitere Informationen finden Sie in der [**EventAccessControl-Funktion.**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol)

 

## <a name="related-topics"></a>Zugehörige Themen

[Konfigurieren und Starten einer privaten Protokollierungssitzung](configuring-and-starting-a-private-logger-session.md)

[Konfigurieren und Starten einer AutoLogger-Sitzung](configuring-and-starting-an-autologger-session.md)

[Konfigurieren und Starten einer Ereignisablaufverfolgungssitzung](configuring-and-starting-an-event-tracing-session.md)

[Konfigurieren und Starten der NT-Kernelprotokollierungssitzung](configuring-and-starting-the-nt-kernel-logger-session.md)

[Systemanbieter](system-providers.md)

[Aktualisieren einer Ereignisablaufverfolgungssitzung](updating-an-event-tracing-session.md)

 

 
