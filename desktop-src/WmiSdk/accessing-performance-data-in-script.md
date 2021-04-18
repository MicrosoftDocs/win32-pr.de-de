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
# <a name="accessing-performance-data-in-script"></a>Zugreifen auf Leistungsdaten im Skript

WMI-Skripts können auf die vorinstallierten WMI- [Leistungs Leistungs](/windows/desktop/CIMWin32Prov/performance-counter-classes)Daten-Klassen zugreifen, entweder auf dem lokalen Computer oder Remote. Skripts können zwar Daten von nicht berechneten Klassen, wie z. b. [**Win32 \_ perfrawdata \_ perfos- \_ Speicher**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), oder formatierte Klassen, [**Win32 \_ perfformatteddata \_ perfos- \_ Speicher**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), abrufen, die formatierten Daten Klassen können jedoch einfacher verwendet werden.

Zum Überwachen von Leistungsdaten mit den Leistungs Leistungsdaten-Klassen [*muss ein*](gloss-r.md)Aktualisierungs Programm verwendet werden. Verwenden Sie das Objekt " [**Swap**](swbemrefresher.md) -Refresh-up", um ein oder mehrere Leistungs Objekte zum Aktualisieren oder Aktualisieren eines einzelnen Objekts mit dem " [**Swap. Refresh**](swbemobjectex-refresh-.md) "-Aufrufs zu speichern. Weitere Informationen finden Sie unter Aktualisieren von [WMI-Daten in Skripts](refreshing-wmi-data-in-scripts.md).

Durch Festlegen der Eigenschaft " [**Swap. autoreconnetct**](swbemrefresher-autoreconnect.md) " auf " **true**" stellt WMI automatisch eine Verbindung mit einem Remote Anbieter her, wenn die Verbindung getrennt wird, sodass Sie den Verbindungsstatus nicht überprüfen müssen.

Wie im folgenden Skriptcode Beispielskript gezeigt, müssen Sie eine anfängliche Aktualisierung ausführen, um einen Startwert für das Objekt abzurufen, das Sie aktualisieren. Nachfolgende Aktualisierungs Aufrufe enthalten dann Daten.

> [!Note]  
> Wenn ein Skript auf WMI-Leistungsdaten von einem Remote Computer zugreift, kann das Skript nur unter dem aktuell angemeldeten Benutzerkonto ausgeführt werden. WMI unterstützt keinen [**Swap. ConnectServer**](swbemlocator-connectserver.md) -Aufrufe, der andere Benutzer Anmelde Informationen übergibt. Daher muss das Konto, das den Remote Computer aufrufen muss, bereits über die entsprechenden Berechtigungen auf diesem Computer verfügen.

 

Im folgenden Skriptcode Beispiel wird veranschaulicht, wie Sie ein " [**Swap**](swbemrefresher.md) "-Objekt für das Aktualisieren der Daten in Leistungs Objekt Objekten verwenden. Weitere Informationen zur Verwendung von Leistungsindikatoren in WMI finden Sie unter [zugreifen auf vorinstallierte WMI-Leistungsklassen](accessing-wmi-preinstalled-performance-classes.md).


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

Im folgenden Skriptcode Beispiel wird veranschaulicht, dass Sie eine anfängliche Aktualisierung ausführen müssen, um einen Startwert für das aktualisierte Objekt zu erhalten. Nachfolgende Aktualisierungs Aufrufe enthalten dann Daten.

Im folgenden Skriptcode Beispiel wird veranschaulicht, wie Sie ein " [**Swap**](swbemrefresher.md) "-Objekt für das Aktualisieren der Daten in Leistungs Objekt Objekten verwenden. Weitere Informationen zur Verwendung von Leistungsindikatoren in WMI finden Sie unter [zugreifen auf vorinstallierte WMI-Leistungsklassen](accessing-wmi-preinstalled-performance-classes.md).


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

[Leistungs Leistungsdaten-Klassen](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[WMI-Tasks: Leistungsüberwachung](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Überwachen von Leistungsdaten](monitoring-performance-data.md)
</dt> </dl>

 

 
