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
# <a name="wmi-log-files"></a><span data-ttu-id="3260d-104">WMI-Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="3260d-104">WMI Log Files</span></span>

<span data-ttu-id="3260d-105">WMI verwendet die [Ereignis Ablauf Verfolgung (Event Tracing](/windows/desktop/ETW/event-tracing-portal) , etw), und Ereignisse können über die **Ereignisanzeige** -Benutzeroberfläche oder das Befehlszeilen Tool "wevtutil" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3260d-105">WMI uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events can be obtained through the **Event Viewer** user interface or the Wevtutil command line tool.</span></span> <span data-ttu-id="3260d-106">Weitere Informationen finden Sie unter Ablauf [Verfolgung von WMI-Aktivitäten](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="3260d-106">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

-   [<span data-ttu-id="3260d-107">Ereignis Ablauf Verfolgung anstelle von Text Protokollen</span><span class="sxs-lookup"><span data-stu-id="3260d-107">Event Tracing Instead of Text Logs</span></span>](#event-tracing-instead-of-text-logs)
-   [<span data-ttu-id="3260d-108">WMI-Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="3260d-108">WMI Log Files</span></span>](#wmi-log-files)
-   [<span data-ttu-id="3260d-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3260d-109">Related topics</span></span>](#related-topics)

## <a name="event-tracing-instead-of-text-logs"></a><span data-ttu-id="3260d-110">Ereignis Ablauf Verfolgung anstelle von Text Protokollen</span><span class="sxs-lookup"><span data-stu-id="3260d-110">Event Tracing Instead of Text Logs</span></span>

<span data-ttu-id="3260d-111">Die WMI-Dienst Aktivität wird in der Datei "wmitracing. log" aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3260d-111">WMI service activity is recorded in the WMITracing.log file.</span></span> <span data-ttu-id="3260d-112">Weitere Informationen zum Aktivieren der WMI-Ereignis Ablauf Verfolgung und zum Zugreifen auf die Datei "wmitracing. log" finden Sie unter [Tracing WMI Activity](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="3260d-112">For more information about enabling WMI event tracing and accessing the WMITracing.log file, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span> <span data-ttu-id="3260d-113">Windows-Treibermodell (WDM)-Anbieter melden sich weiterhin in der Datei "wbemprov. log" an.</span><span class="sxs-lookup"><span data-stu-id="3260d-113">Windows Driver Model (WDM) providers continue to log in the Wbemprov.log file.</span></span>

## <a name="wmi-log-files"></a><span data-ttu-id="3260d-114">WMI-Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="3260d-114">WMI Log Files</span></span>

<span data-ttu-id="3260d-115">Der WMI-Dienst und einige Anbieter schreiben Text Protokolldateien, um Ereignisse aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="3260d-115">The WMI service and some providers write text log files to record events.</span></span>

<dl> <dt>

<span data-ttu-id="3260d-116"><span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[Protokolldateien für WMI-Anbieter](wmi-provider-log-files.md)</span><span class="sxs-lookup"><span data-stu-id="3260d-116"><span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[WMI Provider Log Files](wmi-provider-log-files.md)</span></span>
</dt> <dd>

<span data-ttu-id="3260d-117">WMI-Anbieter können auch Protokolle verwalten.</span><span class="sxs-lookup"><span data-stu-id="3260d-117">WMI providers also may maintain logs.</span></span> <span data-ttu-id="3260d-118">Welche Protokolldateien auf einem System angezeigt werden, hängt davon ab, welche Anbieter installiert sind.</span><span class="sxs-lookup"><span data-stu-id="3260d-118">Which log files appear on a system depends on which providers are installed.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="3260d-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3260d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3260d-120">WMI-Referenz</span><span class="sxs-lookup"><span data-stu-id="3260d-120">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="3260d-121">WMI-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="3260d-121">Tracing WMI Activity</span></span>](tracing-wmi-activity.md)
</dt> <dt>

[<span data-ttu-id="3260d-122">Protokollieren der WMI-Aktivität</span><span class="sxs-lookup"><span data-stu-id="3260d-122">Logging WMI Activity</span></span>](logging-wmi-activity.md)
</dt> </dl>

 

 
