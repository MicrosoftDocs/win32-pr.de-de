---
description: Der systemtraceprovider ist ein Kernel Anbieter mit vordefinierten Kernel Ereignissen, die unter Windows 7, Windows Server 2008 R2 und höher unterstützt werden.
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: Konfigurieren und Starten einer systemtraceprovider-Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b718269801a7677572e7bb5b74cd8b89d3711e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977712"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a>Konfigurieren und Starten einer systemtraceprovider-Sitzung

Der systemtraceprovider ist ein Kernel Anbieter mit vordefinierten Kernel Ereignissen, die unter Windows 7, Windows Server 2008 R2 und höher unterstützt werden. Unter Windows 7 und Windows Server 2008 R2 konnte der systemtraceprovider nur für die NT Kernel Logger-Sitzung verwendet werden.

Unter Windows 8, Windows Server 2012 und höher kann der systemtraceprovider für bis zu 8 Protokollierungs Sitzungen multiplext werden. Die ersten beiden Slots für Protokollierungs Sitzungen sind für die NT-Kernel Protokollierung und die zirkuläre Kernel Kontext Protokollierung reserviert.

Weitere Informationen zur Verwendung der NT Kernel Logger-Sitzung als Ablauf Verfolgungs Anbieter finden Sie unter [Konfigurieren und Starten der NT-Kernel](configuring-and-starting-the-nt-kernel-logger-session.md)Protokollierungs Sitzung.

Führen Sie den folgenden Befehl aus, um den systemtraceprovider zum Starten einer anderen Sitzung als der NT-Kernel Protokollierung zu aktivieren.

**tracelog-Start MySession-f c: \\ Kernel1. ETL-EFLAG proc \_ Thread + Loader + cswitch**

Führen Sie die folgenden Schritte aus, um den systemtraceprovider Programm gesteuert zum Starten einer anderen Sitzung als der NT-Kernel Protokollierung zu aktivieren.

-   Definieren Sie einen Namen für die private Protokollierung.

    **\#definieren Sie den Namen der privaten Protokollierung \_ \_ L "Some private Trace Session".**

-   Legen Sie auf dem Controller die folgenden Member der [**\_ \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) Struktur der Ereignis Ablauf Verfolgung fest.

    Legen Sie **logfilemode** auf **Ereignis Ablauf \_ Verfolgungs \_ System \_ \_**-Protokollierungs Modus fest.

    Legen Sie **Loggername** anstelle des **\_ \_ namens der Kernel** Protokollierung auf private Logger fest.

    Stellen Sie sicher, dass das **wnode. GUID** -Element der Eigenschaften Struktur der [**Ereignis Ablauf \_ Verfolgung \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) nicht auf **systemtracecontrolguid** festgelegt ist. Sie müssen diesem Member eine neue **GUID** zuweisen.

-   Legen Sie auf dem Consumer den **Loggername** -Member der [**Ereignis Ablauf \_ Verfolgung \_ logfile**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) -Struktur auf diese private Protokollierung fest.

> [!Note]  
> Wenn ein nicht-Administratoren-oder ein nicht-TCB-Prozess in der Lage sein soll, eine Profilerstellungs-Ablauf Verfolgungs Sitzung mithilfe von systemtraceprovider im Namen von Drittanbieter Anwendungen zu starten, müssen Sie dem Benutzerprofil Berechtigungen erteilen und diesen Benutzer dann sowohl der Sitzungs- **GUID** (für die Protokollierungs Sitzung erstellt) als auch der **GUID** des System Ablauf Verfolgungs Anbieters hinzufügen Weitere Informationen finden Sie in der [**eventaccesscontrol**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) -Funktion.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren und Starten einer Sitzung für private Logger](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Konfigurieren und Starten einer autologger-Sitzung](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Konfigurieren und Starten der NT Kernel Logger-Sitzung](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[Aktualisieren einer Ereignis Ablauf Verfolgungs Sitzung](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
