---
description: Klassische Anbieter verwenden die TraceEventInstance-Funktion, um Ereignisse nachzuverfolgen, die Teil einer einzelnen Transaktion sind. Sie können diese Funktion auch zum Nachverfolgen von übergeordneten/untergeordneten Ereignissen verwenden.
ms.assetid: 246e9443-3120-49bf-a6e3-64dddba348fa
title: Schreiben verwandter Ereignisse in einem klassischen Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41443c0a05bd94e25ae4ca6a4549671c6aa0682b848660ca31683bb4bf8b75b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813812"
---
# <a name="writing-related-events-in-a-classic-provider"></a>Schreiben verwandter Ereignisse in einem klassischen Anbieter

[Klassische](about-event-tracing.md) Anbieter verwenden die [**TraceEventInstance-Funktion,**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) um Ereignisse nachzuverfolgen, die Teil einer einzelnen Transaktion sind. Sie können diese Funktion auch zum Nachverfolgen von übergeordneten/untergeordneten Ereignissen verwenden.

Vor dem Aufrufen der [**TraceEventInstance-Funktion**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) müssen Sie zunächst die [**CreateTraceInstanceId-Funktion**](/windows/win32/api/evntrace/nf-evntrace-createtraceinstanceid) aufrufen, um einen Transaktionsbezeichner abzurufen. Diese Funktion generiert einen eindeutigen Transaktionsbezeichner und ordnet ihn einem registrierten Klassen-GUID-Handle zu. Die Handles für registrierte Klassen-GUIDs sind in den **RegHandle-Membern** der [**TRACE \_ GUID \_ REGISTRATION-Strukturen**](/windows/win32/api/evntrace/ns-evntrace-trace_guid_registration) verfügbar, nachdem die [**RegisterTraceGuids-Funktion**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) aufgerufen wurde. Der Transaktionsbezeichner wird im **InstanceId-Member** einer [**EVENT INSTANCE \_ \_ INFO-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_instance_info) platziert, die Sie an die **CreateTraceInstanceId-Funktion** übergeben.

Die [**EVENT \_ INSTANCE \_ HEADER-Struktur,**](/windows/win32/api/evntrace/ns-evntrace-event_instance_header) die an die [**TraceEventInstance-Funktion**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) übergeben wird, ähnelt der [**EVENT TRACE \_ \_ HEADER-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) (siehe [Ablaufverfolgungsereignisse](tracing-events.md)), enthält jedoch zusätzliche Informationen im Zusammenhang mit -Instanzen und enthält keinen **GUID-Member.**

Ereignisinstanzen können verwendet werden, um eine hierarchische Beziehung zwischen Ereignissen herzustellen. Die [**TraceEventInstance-Funktion**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) akzeptiert instanzspezifische Informationen von zwei Ereignisinstanzen. Der *pInstInfo-Parameter* verweist auf die [**EVENT INSTANCE \_ \_ INFO-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_instance_info) der Ereignisinstanz, und der *pParentInstInfo-Parameter* verweist auf die **EVENT INSTANCE \_ \_ INFO-Struktur** einer übergeordneten Ereignisinstanz. Die Definition einer "übergeordneten" Ereignisinstanz ist anwendungsdefiniert. das übergeordnete Element kann eine beliebige Instanz sein, die bereits generiert wurde.

 

 
