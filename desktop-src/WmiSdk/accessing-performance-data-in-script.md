---
description: WMI-Skripts können entweder auf dem lokalen Computer oder remote auf die vorinstallierten WMI-Leistungsindikatorklassen zugreifen.
ms.assetid: 79e47173-c8b6-452d-9400-93e2bd6e9da5
ms.tgt_platform: multiple
title: Zugreifen auf Leistungsdaten in Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 42fe1ecdbaf5cdc5cbafc53117ad7c8f370dae2b4e1a3adcee3a4fcf719c995a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320443"
---
# <a name="accessing-performance-data-in-script"></a>Zugreifen auf Leistungsdaten in Skripts

WMI-Skripts können entweder auf [](/windows/desktop/CIMWin32Prov/performance-counter-classes)dem lokalen Computer oder remote auf die vorinstallierten WMI-Leistungsindikatorklassen zugreifen. Während Skripts Daten aus nicht berechneten Klassen abrufen können, z. B. [**Win32 \_ PerfRawData \_ PerfOS \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)oder formatierten Klassen, [**Win32 \_ PerfFormattedData \_ PerfOS-Arbeitsspeicher, \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)können die formatierten Datenklassen einfacher zu verwenden sein.

Die Überwachung von Leistungsdaten mit den Leistungsindikatorklassen erfordert die Verwendung eines [*Auffrischungs-.*](gloss-r.md) Verwenden Sie [**das SWbemRefresher-Objekt,**](swbemrefresher.md) um mindestens ein Leistungsobjekt für die Aktualisierung oder Aktualisierung eines einzelnen Objekts durch den [**Aufruf von SWbemObjectEx.Refresh zu**](swbemobjectex-refresh-.md) speichern. Weitere Informationen finden Sie unter [Aktualisieren von WMI-Daten in Skripts.](refreshing-wmi-data-in-scripts.md)

Durch Festlegen der [**SWbemRefresher.AutoReconnect-Eigenschaft**](swbemrefresher-autoreconnect.md) auf **TRUE** stellt WMI automatisch erneut eine Verbindung mit einem Remoteanbieter her, wenn die Verbindung unterbrochen wird, sodass Sie den Verbindungsstatus nicht überprüfen müssen.

Wie im folgenden Skriptcodebeispielskript gezeigt, müssen Sie einen ersten Aktualisierungsaufruf ausführen, um einen Startwert für das objekt zu erhalten, das Sie aktualisieren. Nachfolgende Aktualisierungsaufrufe enthalten dann Daten.

> [!Note]  
> Wenn ein Skript von einem Remotecomputer aus auf WMI-Leistungsindikatordaten zutritt, kann das Skript nur unter dem aktuell angemeldeten Benutzerkonto ausgeführt werden. WMI unterstützt keinen [**SWbemLocator.ConnectServer-Aufruf,**](swbemlocator-connectserver.md) der unterschiedliche Benutzeranmeldeinformationen übergibt. Daher muss das Konto, das den Remotecomputer aufruft, bereits über die entsprechenden Berechtigungen auf diesem Computer verfügen.

 

Das folgende Skriptcodebeispiel zeigt, wie sie ein [**SWbemRefresher-Objekt**](swbemrefresher.md) verwenden, um die Daten in Leistungsindikatorobjekten zu aktualisieren. Weitere Informationen zur Verwendung von Leistungsindikatoren in WMI finden Sie unter [Zugreifen auf vorinstallierte WMI-Leistungsklassen.](accessing-wmi-preinstalled-performance-classes.md)


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



## <a name="example"></a>Beispiel

Das folgende Skriptcodebeispiel zeigt, dass Sie einen ersten Aktualisierungsaufruf ausführen müssen, um einen Startwert für das aktualisierte Objekt zu erhalten. Nachfolgende Aktualisierungsaufrufe enthalten dann Daten.

Das folgende Skriptcodebeispiel zeigt, wie sie ein [**SWbemRefresher-Objekt**](swbemrefresher.md) verwenden, um die Daten in Leistungsindikatorobjekten zu aktualisieren. Weitere Informationen zur Verwendung von Leistungsindikatoren in WMI finden Sie unter [Zugreifen auf vorinstallierte WMI-Leistungsklassen.](accessing-wmi-preinstalled-performance-classes.md)


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Leistungsindikatorklassen](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[WMI-Aufgaben: Leistungsüberwachung](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Überwachen von Leistungsdaten](monitoring-performance-data.md)
</dt> </dl>

 

 
