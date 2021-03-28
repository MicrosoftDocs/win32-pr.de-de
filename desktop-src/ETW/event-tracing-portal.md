---
description: Diese Dokumentation ist für Benutzermodusanwendungen vorgesehen, die ETW verwenden möchten. Informationen zum Instrumentieren von Gerätetreibern, die im Kernel Modus ausgeführt werden, finden Sie unter WPP-Software Ablauf Verfolgung und Hinzufügen von Ereignis Ablauf Verfolgung zu Kernel-Mode Treibern im Windows-Treiberkit (WDK).
ms.assetid: 3de69436-671b-46a2-8d92-4eb3af2a4233
title: Ereignisablaufverfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9802635fffddfea79c979534771605af13949d69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349328"
---
# <a name="event-tracing"></a>Ereignisablaufverfolgung

## <a name="purpose"></a>Zweck

Mit der Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw) können Anwendungsprogrammierer Ereignis Ablauf Verfolgungs Sitzungen starten und beenden, eine Anwendung instrumentieren, um Ablauf Verfolgungs Ereignisse bereitzustellen und Ablauf Verfolgungs Ereignisse zu verarbeiten. Ablauf Verfolgungs Ereignisse enthalten einen Ereignis Header und Anbieter definierte Daten, die den aktuellen Zustand einer Anwendung oder eines Vorgangs beschreiben. Sie können die-Ereignisse verwenden, um eine Anwendung zu Debuggen und die Kapazitäts-und Leistungsanalyse auszuführen.

Diese Dokumentation ist für Benutzermodusanwendungen vorgesehen, die ETW verwenden möchten. Informationen zum Instrumentieren von Gerätetreibern, die im Kernel Modus ausgeführt werden, finden Sie unter [WPP-Software Ablauf Verfolgung](/windows-hardware/drivers/devtest/wpp-software-tracing) und [Hinzufügen von Ereignis Ablauf Verfolgung zu Kernel-Mode Treibern](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) im Windows-Treiberkit (WDK).

## <a name="where-applicable"></a>Anwendungsbereich

Verwenden Sie etw, wenn Sie Ihre Anwendung instrumentieren, Benutzer-oder Kernel Ereignisse in einer Protokolldatei protokollieren und Ereignisse aus einer Protokolldatei oder in Echtzeit verwenden möchten.

## <a name="developer-audience"></a>Entwicklergruppe

Etw wurde für C-und C++-Entwickler entwickelt, die Benutzermodus-Anwendungen schreiben.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Etw ist in Microsoft Windows 2000 und höher enthalten. Informationen dazu, welche Betriebssysteme für die Verwendung einer bestimmten Funktion erforderlich sind, finden Sie im Abschnitt "Anforderungen" in der Dokumentation für die Funktion.

## <a name="process-etw-traces-in-net-code"></a>Verarbeiten von etw-Ablauf Verfolgungen in .NET-Code

Sie können die [.net traceprocessing-API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) verwenden, um etw-Ablauf Verfolgungen für Ihre Anwendungen und andere Softwarekomponenten zu analysieren. Diese API wird intern bei Microsoft verwendet, um etw-Daten zu analysieren, die das Windows-Engineering-System erzeugt haben, und es wird auch verwendet, um mehrere Tabellen in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer)zu unterhalten. Diese API ist als nuget-Paket verfügbar.

[hier finden Sie weitere Informationen](/windows/apps/trace-processing/overview)

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                     | BESCHREIBUNG                                                                        |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Neuerungen bei der Ereignis Ablauf Verfolgung](what-s-new-in-event-tracing.md)<br/> | Neue Features, die in jeder Version der Ereignis Ablauf Verfolgung hinzugefügt wurden.<br/>          |
| [Informationen zur Ereignis Ablauf Verfolgung](about-event-tracing.md)<br/>                 | Allgemeine Informationen zur Ereignis Ablauf Verfolgung.<br/>                                |
| [Verwenden der Ereignis Ablauf Verfolgung](using-event-tracing.md)<br/>                 | Aufgabenbezogene Themen, in denen die Verwendung der ETW-API beschrieben wird.<br/>               |
| [Referenz zur Ereignis Ablauf Verfolgung](event-tracing-reference.md)<br/>         | Ausführliche Beschreibungen der etw-Funktionen und anderer Programmier Elemente. <br/> |



 

 

 
