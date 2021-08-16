---
description: Diese Dokumentation gilt für Benutzermodusanwendungen, die ETW verwenden möchten. Informationen zum Instrumentieren von Gerätetreibern, die im Kernelmodus ausgeführt werden, finden Sie unter WPP-Softwareablaufverfolgung und Hinzufügen der Ereignisablaufverfolgung zu Kernel-Mode-Treibern im Windows Driver Kit (WDK).
ms.assetid: 3de69436-671b-46a2-8d92-4eb3af2a4233
title: Ereignisablaufverfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 908e935d48749d80e5b2cfe237efeed5413c839157e53b489f4857c0349b4a1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070220"
---
# <a name="event-tracing"></a>Ereignisablaufverfolgung

## <a name="purpose"></a>Zweck

Die Ereignisablaufverfolgung für Windows (ETW) bietet Anwendungsprogrammierern die Möglichkeit, Ereignisablaufverfolgungssitzungen zu starten und zu beenden, eine Anwendung zu instrumentierung, um Ablaufverfolgungsereignisse zur Verfügung zu stellen, und Ablaufverfolgungsereignisse zu nutzen. Ablaufverfolgungsereignisse enthalten einen Ereignisheader und anbieterdefinierte Daten, die den aktuellen Zustand einer Anwendung oder eines Vorgangs beschreiben. Sie können die Ereignisse verwenden, um eine Anwendung zu debuggen und Kapazitäts- und Leistungsanalysen durchzuführen.

Diese Dokumentation gilt für Benutzermodusanwendungen, die ETW verwenden möchten. Informationen zum Instrumentieren von Gerätetreibern, die im Kernelmodus ausgeführt werden, finden Sie unter [WPP-Softwareablaufverfolgung](/windows-hardware/drivers/devtest/wpp-software-tracing) und [Hinzufügen](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) der Ereignisablaufverfolgung zu Kernel-Mode-Treibern im Windows Driver Kit (WDK).

## <a name="where-applicable"></a>Anwendungsbereich

Verwenden Sie ETW, wenn Sie Ihre Anwendung instrumentieren, Benutzer- oder Kernelereignisse in einer Protokolldatei protokollieren und Ereignisse aus einer Protokolldatei oder in Echtzeit nutzen möchten.

## <a name="developer-audience"></a>Entwicklergruppe

ETW ist für C- und C++-Entwickler konzipiert, die Anwendungen im Benutzermodus schreiben.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

ETW ist in Microsoft Windows 2000 und höher enthalten. Informationen dazu, welche Betriebssysteme für die Verwendung einer bestimmten Funktion erforderlich sind, finden Sie im Abschnitt Anforderungen der Dokumentation für die Funktion.

## <a name="process-etw-traces-in-net-code"></a>Verarbeiten von ETW-Ablaufverfolgungen in .NET-Code

Sie können die [.NET TraceProcessing-API verwenden,](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) um ETW-Ablaufverfolgungen für Ihre Anwendungen und andere Softwarekomponenten zu analysieren. Diese API wird intern bei Microsoft verwendet, um ETW-Daten zu analysieren, die das Windows Engineering-System erzeugt haben, [und](/windows-hardware/test/wpt/windows-performance-analyzer)sie wird auch verwendet, um mehrere Tabellen in Windows Leistungsanalyse. Diese API ist als Paket NuGet verfügbar.

Weitere Informationen finden Sie in [diesem Artikel](/windows/apps/trace-processing/overview).

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                     | BESCHREIBUNG                                                                        |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Neues bei der Ereignisablaufverfolgung](what-s-new-in-event-tracing.md)<br/> | Neue Features, die der Ereignisablaufverfolgung in jedem Release hinzugefügt wurden.<br/>          |
| [Informationen zur Ereignisablaufverfolgung](about-event-tracing.md)<br/>                 | Allgemeine Informationen zur Ereignisablaufverfolgung.<br/>                                |
| [Verwenden der Ereignisablaufverfolgung](using-event-tracing.md)<br/>                 | Aufgabenbezogene Themen, in denen die Verwendung der ETW-API beschrieben wird.<br/>               |
| [Referenz zur Ereignisablaufverfolgung](event-tracing-reference.md)<br/>         | Ausführliche Beschreibungen von ETW-Funktionen und anderen Programmierelementen. <br/> |



 

 

 
