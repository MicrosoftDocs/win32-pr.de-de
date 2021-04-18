---
description: WMI-Skripts können auf die vorinstallierten WMI-Leistungs Leistungsdaten-Klassen zugreifen, entweder auf dem lokalen Computer oder Remote.
ms.assetid: 79e47173-c8b6-452d-9400-93e2bd6e9da5
ms.tgt_platform: multiple
title: Zugreifen auf Leistungsdaten im Skript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e203acfc7fc23fe0dab466eee383223aad0bf889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351139"
---
# <a name="accessing-performance-data-in-script"></a><span data-ttu-id="c5dc0-103">Zugreifen auf Leistungsdaten im Skript</span><span class="sxs-lookup"><span data-stu-id="c5dc0-103">Accessing Performance Data in Script</span></span>

<span data-ttu-id="c5dc0-104">WMI-Skripts können auf die vorinstallierten WMI- [Leistungs Leistungs](/windows/desktop/CIMWin32Prov/performance-counter-classes)Daten-Klassen zugreifen, entweder auf dem lokalen Computer oder Remote.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-104">WMI scripts can access the preinstalled WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes), either on the local computer or remotely.</span></span> <span data-ttu-id="c5dc0-105">Skripts können zwar Daten von nicht berechneten Klassen, wie z. b. [**Win32 \_ perfrawdata \_ perfos- \_ Speicher**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), oder formatierte Klassen, [**Win32 \_ perfformatteddata \_ perfos- \_ Speicher**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), abrufen, die formatierten Daten Klassen können jedoch einfacher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-105">While scripts can obtain data from uncalculated classes, such as [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), or formatted classes, [**Win32\_PerfFormattedData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), the formatted data classes can be easier to use.</span></span>

<span data-ttu-id="c5dc0-106">Zum Überwachen von Leistungsdaten mit den Leistungs Leistungsdaten-Klassen [*muss ein*](gloss-r.md)Aktualisierungs Programm verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-106">Monitoring performance data with the performance counter classes requires the use of a [*refresher*](gloss-r.md).</span></span> <span data-ttu-id="c5dc0-107">Verwenden Sie das Objekt " [**Swap**](swbemrefresher.md) -Refresh-up", um ein oder mehrere Leistungs Objekte zum Aktualisieren oder Aktualisieren eines einzelnen Objekts mit dem " [**Swap. Refresh**](swbemobjectex-refresh-.md) "-Aufrufs zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-107">Use the [**SWbemRefresher**](swbemrefresher.md) object to store one or more performance objects for refresh or refresh a single object by the [**SWbemObjectEx.Refresh**](swbemobjectex-refresh-.md) call.</span></span> <span data-ttu-id="c5dc0-108">Weitere Informationen finden Sie unter Aktualisieren von [WMI-Daten in Skripts](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="c5dc0-108">For more information, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="c5dc0-109">Durch Festlegen der Eigenschaft " [**Swap. autoreconnetct**](swbemrefresher-autoreconnect.md) " auf " **true**" stellt WMI automatisch eine Verbindung mit einem Remote Anbieter her, wenn die Verbindung getrennt wird, sodass Sie den Verbindungsstatus nicht überprüfen müssen.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-109">By setting the [**SWbemRefresher.AutoReconnect**](swbemrefresher-autoreconnect.md) property to **TRUE**, WMI automatically reconnects to a remote provider if the connection is broken so that you do not need to check for connection status.</span></span>

<span data-ttu-id="c5dc0-110">Wie im folgenden Skriptcode Beispielskript gezeigt, müssen Sie eine anfängliche Aktualisierung ausführen, um einen Startwert für das Objekt abzurufen, das Sie aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-110">As shown in the following script code example script, you must make an initial refresh call to get a starting value for the object you are refreshing.</span></span> <span data-ttu-id="c5dc0-111">Nachfolgende Aktualisierungs Aufrufe enthalten dann Daten.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-111">Subsequent refresh calls then contain data.</span></span>

> [!Note]  
> <span data-ttu-id="c5dc0-112">Wenn ein Skript auf WMI-Leistungsdaten von einem Remote Computer zugreift, kann das Skript nur unter dem aktuell angemeldeten Benutzerkonto ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-112">When a script is accessing WMI performance counter data from a remote computer, the script can only run under the current logged-on user account.</span></span> <span data-ttu-id="c5dc0-113">WMI unterstützt keinen [**Swap. ConnectServer**](swbemlocator-connectserver.md) -Aufrufe, der andere Benutzer Anmelde Informationen übergibt.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-113">WMI does not support an [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) call that passes in different user credentials.</span></span> <span data-ttu-id="c5dc0-114">Daher muss das Konto, das den Remote Computer aufrufen muss, bereits über die entsprechenden Berechtigungen auf diesem Computer verfügen.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-114">Therefore, the account calling the remote computer must already have the appropriate privileges on that computer.</span></span>

 

<span data-ttu-id="c5dc0-115">Im folgenden Skriptcode Beispiel wird veranschaulicht, wie Sie ein " [**Swap**](swbemrefresher.md) "-Objekt für das Aktualisieren der Daten in Leistungs Objekt Objekten verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-115">The following script code example shows how to use an [**SWbemRefresher**](swbemrefresher.md) object to update the data in performance counter objects.</span></span> <span data-ttu-id="c5dc0-116">Weitere Informationen zur Verwendung von Leistungsindikatoren in WMI finden Sie unter [zugreifen auf vorinstallierte WMI-Leistungsklassen](accessing-wmi-preinstalled-performance-classes.md).</span><span class="sxs-lookup"><span data-stu-id="c5dc0-116">For more information about using performance counters in WMI, see [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>


```VB
' Get raw and cooked data performance counter instances for the
" wscript process running this script

set RawProc = GetObject("winmgmts:Win32_PerfRawdata_Perfproc_process.name='wscript'")
set CookedProc = GetObject("winmgmts:Win32_Perfformatteddata_Perfproc_process.name='wscript'")

' Display the same property in raw and cooked form in a loop
for I = 1 to 6
    Wscript.Echo "wscript process raw PageFaultsPerSec = & RawProc.PageFaultsPerSec _
                 & " cooked PageFaultsPerSec= " & CookedProc.PageFaultsPerSec 

' Wait 2 seconds
    Wscript.Sleep 2000
    
    ' Refresh the object
    RawProc.Refresh_
    CookedProc.Refresh_
next
```



## <a name="example"></a><span data-ttu-id="c5dc0-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c5dc0-117">Example</span></span>

<span data-ttu-id="c5dc0-118">Im folgenden Skriptcode Beispiel wird veranschaulicht, dass Sie eine anfängliche Aktualisierung ausführen müssen, um einen Startwert für das aktualisierte Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-118">The following script code example shows that you must make an initial refresh call to get a starting value for the refreshed object.</span></span> <span data-ttu-id="c5dc0-119">Nachfolgende Aktualisierungs Aufrufe enthalten dann Daten.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-119">Subsequent refresh calls then contain data.</span></span>

<span data-ttu-id="c5dc0-120">Im folgenden Skriptcode Beispiel wird veranschaulicht, wie Sie ein " [**Swap**](swbemrefresher.md) "-Objekt für das Aktualisieren der Daten in Leistungs Objekt Objekten verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5dc0-120">The following script code example shows how to use an [**SWbemRefresher**](swbemrefresher.md) object to update the data in performance counter objects.</span></span> <span data-ttu-id="c5dc0-121">Weitere Informationen zur Verwendung von Leistungsindikatoren in WMI finden Sie unter [zugreifen auf vorinstallierte WMI-Leistungsklassen](accessing-wmi-preinstalled-performance-classes.md).</span><span class="sxs-lookup"><span data-stu-id="c5dc0-121">For more information about using performance counters in WMI, see [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>


```VB
' Get raw and cooked data performance counter instances for the
" wscript process running this script

set RawProc = GetObject("winmgmts:" _
                        & "Win32_PerfRawdata_Perfproc_process." _
                        & "name='wscript'")
set CookedProc = GetObject("winmgmts:" _ 
                & "Win32_Perfformatteddata_Perfproc_process." _
                & "name='wscript'")

' Display the same property in raw and cooked form in a loop
for I = 1 to 6
    Wscript.Echo "wscript process raw PageFaultsPerSec = " _
                 & RawProc.PageFaultsPerSec _
                 & " cooked PageFaultsPerSec= " _
                 & CookedProc.PageFaultsPerSec 

' Wait 2 seconds
    Wscript.Sleep 2000
    
    ' Refresh the object
    RawProc.Refresh_
    CookedProc.Refresh_
next
```



## <a name="related-topics"></a><span data-ttu-id="c5dc0-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c5dc0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5dc0-123">Leistungs Leistungsdaten-Klassen</span><span class="sxs-lookup"><span data-stu-id="c5dc0-123">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="c5dc0-124">WMI-Tasks: Leistungsüberwachung</span><span class="sxs-lookup"><span data-stu-id="c5dc0-124">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="c5dc0-125">Überwachen von Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="c5dc0-125">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
