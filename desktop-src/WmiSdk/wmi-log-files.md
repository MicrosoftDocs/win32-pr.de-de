---
description: WMI verwendet die Ereignis Ablauf Verfolgung (Event Tracing, etw), und Ereignisse können über die Ereignisanzeige-Benutzeroberfläche oder das Befehlszeilen Tool "wevtutil" abgerufen werden. Weitere Informationen finden Sie unter Ablauf Verfolgung von WMI-Aktivitäten.
ms.assetid: 315b8355-03b9-40f9-a6c1-29a49f5a2cd8
ms.tgt_platform: multiple
title: WMI-Protokolldateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51dfe4efbec32e60812980511676f723fd5aee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350561"
---
# <a name="wmi-log-files"></a>WMI-Protokolldateien

WMI verwendet die [Ereignis Ablauf Verfolgung (Event Tracing](/windows/desktop/ETW/event-tracing-portal) , etw), und Ereignisse können über die **Ereignisanzeige** -Benutzeroberfläche oder das Befehlszeilen Tool "wevtutil" abgerufen werden. Weitere Informationen finden Sie unter Ablauf [Verfolgung von WMI-Aktivitäten](tracing-wmi-activity.md).

-   [Ereignis Ablauf Verfolgung anstelle von Text Protokollen](#event-tracing-instead-of-text-logs)
-   [WMI-Protokolldateien](#wmi-log-files)
-   [Zugehörige Themen](#related-topics)

## <a name="event-tracing-instead-of-text-logs"></a>Ereignis Ablauf Verfolgung anstelle von Text Protokollen

Die WMI-Dienst Aktivität wird in der Datei "wmitracing. log" aufgezeichnet. Weitere Informationen zum Aktivieren der WMI-Ereignis Ablauf Verfolgung und zum Zugreifen auf die Datei "wmitracing. log" finden Sie unter [Tracing WMI Activity](tracing-wmi-activity.md). Windows-Treibermodell (WDM)-Anbieter melden sich weiterhin in der Datei "wbemprov. log" an.

## <a name="wmi-log-files"></a>WMI-Protokolldateien

Der WMI-Dienst und einige Anbieter schreiben Text Protokolldateien, um Ereignisse aufzuzeichnen.

<dl> <dt>

<span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[Protokolldateien für WMI-Anbieter](wmi-provider-log-files.md)
</dt> <dd>

WMI-Anbieter können auch Protokolle verwalten. Welche Protokolldateien auf einem System angezeigt werden, hängt davon ab, welche Anbieter installiert sind.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Referenz](wmi-reference.md)
</dt> <dt>

[WMI-Ablauf Verfolgung](tracing-wmi-activity.md)
</dt> <dt>

[Protokollieren der WMI-Aktivität](logging-wmi-activity.md)
</dt> </dl>

 

 
