---
title: Verwenden von Windows-Remoteverwaltung
description: Windows-Remoteverwaltung ist für die Verbesserung der Hardware Verwaltung in einer Netzwerkumgebung mit verschiedenen Geräten vorgesehen, auf denen eine Vielzahl von Betriebssystemen ausgeführt wird.
ms.assetid: 6ee2b238-5bc2-4274-b7ca-49dbc728d8f1
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c2934694de5913b467521510179fffdb220b601
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101999"
---
# <a name="using-windows-remote-management"></a><span data-ttu-id="9b0f4-103">Verwenden von Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="9b0f4-103">Using Windows Remote Management</span></span>

<span data-ttu-id="9b0f4-104">Windows-Remoteverwaltung ist für die Verbesserung der Hardware Verwaltung in einer Netzwerkumgebung mit verschiedenen Geräten vorgesehen, auf denen eine Vielzahl von Betriebssystemen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b0f4-104">Windows Remote Management is intended to improve hardware management in a network environment with various devices running a variety of operating systems.</span></span> <span data-ttu-id="9b0f4-105">Das gesamte Design des Diensts ist auf die Überwachung und Verwaltung von Remotecomputern ausgerichtet. Zu diesem Zweck wird ein interoperables Standardprotokoll implementiert.</span><span class="sxs-lookup"><span data-stu-id="9b0f4-105">The entire design of the service is focused on monitoring and managing remote computers by implementing an interoperable standard protocol.</span></span>

<span data-ttu-id="9b0f4-106">Da die [WinRM-Skript-API](winrm-scripting-api.md) und die [WinRM-C++-API](winrm-c---api.md) die für das WS-Management-Protokoll definierten Vorgänge implementieren und genau modellieren, empfangen Skripts und Anwendungen XML-Datenströme als Antwort auf Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="9b0f4-106">Because the [WinRM Scripting API](winrm-scripting-api.md) and the [WinRM C++ API](winrm-c---api.md) implement and closely model the operations defined for the WS-Management protocol, scripts and applications receive streams of XML in response to requests.</span></span> <span data-ttu-id="9b0f4-107">Eingabeparameter für Methodenaufrufe müssen in XML erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9b0f4-107">Input parameters to method calls must be constructed in XML.</span></span> <span data-ttu-id="9b0f4-108">Sie können die Methoden der [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) -API verwenden, um XML-Zeichen folgen anzuzeigen oder zu konstruieren.</span><span class="sxs-lookup"><span data-stu-id="9b0f4-108">You can use the methods of the [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) API to display or construct XML strings.</span></span> <span data-ttu-id="9b0f4-109">Ein Beispiel finden Sie unter [Anzeigen der XML-Ausgabe von WinRM-Skripts](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="9b0f4-109">For an example, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>

<span data-ttu-id="9b0f4-110">Die folgende Liste enthält Themen, in denen die Verwendung der WinRM-Skripterstellung beschrieben wird:</span><span class="sxs-lookup"><span data-stu-id="9b0f4-110">The following list includes topics that describe how to use WinRM scripting:</span></span>

-   [<span data-ttu-id="9b0f4-111">Erkennen, ob ein Remote Computer WS-Management Protokoll unterstützt</span><span class="sxs-lookup"><span data-stu-id="9b0f4-111">Detecting Whether a Remote Computer Supports WS-Management Protocol</span></span>](detecting-whether-a-remote-computer-supports-ws-management-protocol.md)
-   [<span data-ttu-id="9b0f4-112">Abrufen von Daten vom lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="9b0f4-112">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
-   [<span data-ttu-id="9b0f4-113">Abrufen von Daten von einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="9b0f4-113">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
-   [<span data-ttu-id="9b0f4-114">Auflisten oder Auflisten aller Instanzen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="9b0f4-114">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
-   [<span data-ttu-id="9b0f4-115">Abfragen für bestimmte Instanzen einer Ressource</span><span class="sxs-lookup"><span data-stu-id="9b0f4-115">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
-   [<span data-ttu-id="9b0f4-116">Anzeigen der XML-Ausgabe von WinRM-Skripts</span><span class="sxs-lookup"><span data-stu-id="9b0f4-116">Displaying XML Output from WinRM Scripts</span></span>](displaying-xml-output-from-winrm-scripts.md)

## <a name="tracing-winrm-activity"></a><span data-ttu-id="9b0f4-117">Ablauf Verfolgung für WinRM-Aktivität</span><span class="sxs-lookup"><span data-stu-id="9b0f4-117">Tracing WinRM Activity</span></span>

<span data-ttu-id="9b0f4-118">Da WinRM Daten über [Windows-Verwaltungsinstrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page)abruft, können Sie die WMI-Aktivität nachverfolgen, die sich aus WinRM-Meldungen ergibt.</span><span class="sxs-lookup"><span data-stu-id="9b0f4-118">Because WinRM obtains data through [Windows Management Instrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page), you can trace WMI activity that results from WinRM messages.</span></span> <span data-ttu-id="9b0f4-119">Ab Windows Vista verwendet der WMI-Dienst nicht mehr die [WMI-Protokolldateien](/windows/desktop/WmiSdk/wmi-log-files).</span><span class="sxs-lookup"><span data-stu-id="9b0f4-119">Starting with Windows Vista, the WMI service no longer uses the [WMI Log Files](/windows/desktop/WmiSdk/wmi-log-files).</span></span> <span data-ttu-id="9b0f4-120">Stattdessen werden [Ereignis Ablauf Verfolgung](/windows/desktop/ETW/event-tracing-portal) (ETW) verwendet, und Ereignisse sind über die **Ereignisanzeige** -Benutzeroberfläche oder das Befehlszeilen Tool evtutil verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9b0f4-120">Instead it uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events are available through the **Event Viewer** UI or the Evtutil command line tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b0f4-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9b0f4-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b0f4-122">Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="9b0f4-122">Windows Remote Management</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="9b0f4-123">Informationen zu Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="9b0f4-123">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="9b0f4-124">Windows-Remoteverwaltung Referenz</span><span class="sxs-lookup"><span data-stu-id="9b0f4-124">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> <dt>

[<span data-ttu-id="9b0f4-125">Skripterstellung in Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="9b0f4-125">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 