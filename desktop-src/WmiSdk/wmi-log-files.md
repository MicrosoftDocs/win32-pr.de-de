---
description: WMI verwendet die Ereignisablaufverfolgung (Event Tracing, ETW), und Ereignisse können über die benutzeroberfläche Ereignisanzeige oder das Befehlszeilentool Wevtutil erhalten werden. Weitere Informationen finden Sie unter Ablaufverfolgung der WMI-Aktivität.
ms.assetid: 315b8355-03b9-40f9-a6c1-29a49f5a2cd8
ms.tgt_platform: multiple
title: WMI-Protokolldateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fff9064dd82484568282f649b3380f544d9ba58a569e36583664806d47b5e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739427"
---
# <a name="wmi-log-files"></a>WMI-Protokolldateien

WMI verwendet [die Ereignisablaufverfolgung](/windows/desktop/ETW/event-tracing-portal) (Event Tracing,  ETW), und Ereignisse können über die benutzeroberfläche Ereignisanzeige oder das Befehlszeilentool Wevtutil erhalten werden. Weitere Informationen finden Sie unter [Ablaufverfolgung der WMI-Aktivität](tracing-wmi-activity.md).

-   [Ereignisablaufverfolgung anstelle von Textprotokollen](#event-tracing-instead-of-text-logs)
-   [WMI-Protokolldateien](#wmi-log-files)
-   [Zugehörige Themen](#related-topics)

## <a name="event-tracing-instead-of-text-logs"></a>Ereignisablaufverfolgung anstelle von Textprotokollen

Die WMI-Dienstaktivität wird in der Datei WMITracing.log aufgezeichnet. Weitere Informationen zum Aktivieren der WMI-Ereignisablaufverfolgung und zum Zugreifen auf die Datei "WMITracing.log" finden Sie unter Ablaufverfolgung der [WMI-Aktivität](tracing-wmi-activity.md). Windows Treibermodellanbieter (WDM) melden sich weiterhin in der Datei Wbemprov.log an.

## <a name="wmi-log-files"></a>WMI-Protokolldateien

Der WMI-Dienst und einige Anbieter schreiben Textdateien zum Aufzeichnen von Ereignissen.

<dl> <dt>

<span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[Protokolldateien des WMI-Anbieters](wmi-provider-log-files.md)
</dt> <dd>

WMI-Anbieter können auch Protokolle verwalten. Welche Protokolldateien auf einem System angezeigt werden, hängt davon ab, welche Anbieter installiert sind.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Referenz](wmi-reference.md)
</dt> <dt>

[Nachverfolgen der WMI-Aktivität](tracing-wmi-activity.md)
</dt> <dt>

[Protokollieren der WMI-Aktivität](logging-wmi-activity.md)
</dt> </dl>

 

 
