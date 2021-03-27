---
description: Klassische Anbieter verwenden die traceeventinstance-Funktion, um Ereignisse zu verfolgen, die Teil einer einzelnen Transaktion sind. Sie können diese Funktion auch verwenden, um übergeordnete/untergeordnete Ereignisse zu verfolgen.
ms.assetid: 246e9443-3120-49bf-a6e3-64dddba348fa
title: Schreiben verwandter Ereignisse in einem klassischen Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771b08a66625d5cd6e723fbc2e12eed87bd1d434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350328"
---
# <a name="writing-related-events-in-a-classic-provider"></a>Schreiben verwandter Ereignisse in einem klassischen Anbieter

[Klassische](about-event-tracing.md) Anbieter verwenden die [**traceeventinstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) -Funktion, um Ereignisse zu verfolgen, die Teil einer einzelnen Transaktion sind. Sie können diese Funktion auch verwenden, um übergeordnete/untergeordnete Ereignisse zu verfolgen.

Bevor Sie die [**traceeventinstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) -Funktion aufrufen, müssen Sie zuerst die [**createtraceinstanceid-**](/windows/win32/api/evntrace/nf-evntrace-createtraceinstanceid) Funktion aufrufen, um einen Transaktions Bezeichner zu erhalten. Diese Funktion generiert einen eindeutigen Transaktions Bezeichner und ordnet ihn einem registrierten Klassen-GUID-Handle zu. Die Handles für registrierte Klassen-GUIDs sind in den **reghandle** -Membern von [**Ablaufverfolgungs- \_ GUID- \_ Registrierungs**](/windows/win32/api/evntrace/ns-evntrace-trace_guid_registration) Strukturen nach dem Aufrufen der [**registertraceguids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) -Funktion verfügbar. Der Transaktions Bezeichner wird in den **InstanceId-** Member einer [**\_ ereignisinstanzinfo \_**](/windows/win32/api/evntrace/ns-evntrace-event_instance_info) -Struktur eingefügt, die Sie an die Funktion " **kreatetraceinstanceid** " übergeben.

Die [**Ereignis \_ Instanz- \_ Header**](/windows/win32/api/evntrace/ns-evntrace-event_instance_header) Struktur, die an die [**traceeventinstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) -Funktion weitergegeben wird, ähnelt der Ereignis-Ablauf Verfolgungs [**\_ \_ Header**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) -Struktur (siehe Ablauf [Verfolgungs Ereignisse](tracing-events.md)), mit der Ausnahme, dass Sie zusätzliche Informationen zu-Instanzen enthält und keinen **GUID** -Member enthält.

Ereignis Instanzen können verwendet werden, um eine hierarchische Beziehung zwischen Ereignissen herzustellen. Die [**traceeventinstance**](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance) -Funktion akzeptiert instanzspezifische Informationen aus zwei Ereignis Instanzen. Der *pinstinfo* -Parameter verweist auf die [**Ereignis \_ Instanz- \_ Informations**](/windows/win32/api/evntrace/ns-evntrace-event_instance_info) Struktur der Ereignis Instanz, und der *pparameentinstinfo* -Parameter verweist auf die **ereignisinstanzinfo \_ \_** -Struktur einer übergeordneten Ereignis Instanz. Die Definition einer "übergeordneten" Ereignis Instanz ist von der Anwendung definiert. das übergeordnete Element kann eine beliebige Instanz sein, die bereits generiert wurde.

 

 
