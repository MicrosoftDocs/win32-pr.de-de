---
description: Um Benachrichtigungen vom Systemregistrierungsanbieter zu erhalten, muss sich eine Verwaltungsanwendung als temporärer Ereignisverbraucher registrieren.
ms.assetid: 4cac5fdd-c842-4d7e-a56e-2e1312df68b4
ms.tgt_platform: multiple
title: Registrieren für Systemregistrierungsereignisse
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1c6f60b21dee729a879aaeab676da67b06ca0a822bcfd6509bc0f406f96fecec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554245"
---
# <a name="registering-for-system-registry-events"></a>Registrieren für Systemregistrierungsereignisse

Um Benachrichtigungen vom [Systemregistrierungsanbieter zu](/previous-versions/windows/desktop/regprov/system-registry-provider) erhalten, muss sich eine Verwaltungsanwendung als temporärer Ereignisverbraucher registrieren. Die meisten Anforderungen für die Registrierung für den Systemregistrierungsanbieter sind identisch mit allen anderen Ereignisregistrierungen, mit der Ausnahme, dass Sie auch das folgende Verfahren ausführen müssen.

Der Registrierungsanbieter stellt Ereignisklassen für Ereignisse in der Systemregistrierung zur Verfügung. Weitere Informationen zur allgemeinen Ereignisregistrierung finden Sie unter [Empfangen eines WMI-Ereignisses.](receiving-a-wmi-event.md)

Im folgenden Verfahren wird beschrieben, wie Sie sich für Systemregistrierungsereignisse registrieren.

**So registrieren Sie sich für Systemregistrierungsereignisse**

1.  Rufen Sie eine Benachrichtigungsabfragemethode auf.

    Verwenden Sie in Skript oder C++ eine Benachrichtigungsabfrage wie [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) oder [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync). Erstellen Sie eine Abfragezeichenfolge für den *bstrQuery-Parameter* von **IWbemServices::ExecNotificationQueryAsync** oder *strQuery* im Skript.

2.  Bestimmen Sie, welche Art von Ereignis Sie empfangen möchten, und erstellen Sie die Abfrage.

    In der folgenden Tabelle sind die Registrierungsereignisklassen aufgeführt, die Sie verwenden können.

    

    | Ereignisklasse                                                      | Hive-Speicherort        | Beschreibung                                                 |
    |------------------------------------------------------------------|----------------------|-------------------------------------------------------------|
    | [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent)                       | Nicht zutreffend<br/>       | Abstrakte Basisklasse für Änderungen in der Registrierung.<br/> |
    | [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent)   | Rootpath<br/>  | Überwacht Änderungen an einer Schlüsselhierarchie.<br/>         |
    | [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)     | KeyPath<br/>   | Überwacht Änderungen an einem einzelnen Schlüssel.<br/>                |
    | [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent) | ValueName<br/> | Überwacht Änderungen an einem einzelnen Wert.<br/>              |

    

     

    Diese Klassen verfügen über eine Eigenschaft namens **Hive,** die die Hierarchie von Schlüsseln identifiziert, die auf Änderungen überwacht werden sollen, z. B. **HKEY \_ LOCAL \_ MACHINE**.

    Änderungen an **den Hives "HKEY \_ CLASSES \_ ROOT"** und **"HKEY \_ CURRENT \_ USER"** werden von [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent) oder von daraus abgeleiteten Klassen wie [**RegistryTreeChangeEvent nicht unterstützt.**](/previous-versions/windows/desktop/regprov/registrytreechangeevent)

3.  Erstellen Sie die WHERE-Klausel für Ihre Ereignisregistrierung.

    Der Systemregistrierungsanbieter verfügt über bestimmte Regeln für WHERE-Klauseln. Weitere Informationen finden Sie unter [Creating a Proper WHERE Clause for the Registry Provider](creating-a-proper-where-clause-for-the-registry-provider.md). Allgemeinere Informationen zum Erstellen einer WHERE-Klausel finden Sie unter [Abfragen mit WQL.](querying-with-wql.md)

4.  Bestimmen Sie, ob Ihr Consumer Ereignisse empfängt.

    Der Systemregistrierungsanbieter garantiert nicht, dass alle gesendeten Ereignisse übermittelt werden. Weitere Informationen finden Sie unter [Empfangen von Registrierungsereignissen.](receiving-registry-events.md)

Das folgende VBScript-Codebeispiel zeigt, wie Eine Registrierungsänderung in der **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft-Struktur** oder -Unterstruktur erkannt wird. Dies ist ein Überwachungsskript, das zu Demonstrationszwecken in einem Prozess namens Wscript.exe ausgeführt wird, bis es in **Task-Manager** beendet, WMI beendet oder das Betriebssystem neu gestartet wird. Das Skript verwendet einen [*semisynchronen Aufruf*](gloss-s.md) vonSWbemServices.Exe [**cNotificationQuery.**](swbemservices-execnotificationquery.md) Weitere Informationen zu semisynchronen Aufrufen finden Sie unter Erstellen eines [semisynchronen Aufrufs mit VBScript.](making-a-semisynchronous-call-with-vbscript.md)


```VB
Set wmiServices = GetObject("winmgmts:root/default") 
Set colTreeChanges = wmiServices.ExecNotificationQuery _
    ("SELECT * FROM RegistryTreeChangeEvent " _
    & "WHERE Hive='HKEY_LOCAL_MACHINE' " _
    & "AND RootPath='SOFTWARE\\Microsoft'")

While (True)
   Set TreeChange = colTreeChanges.NextEvent
   TreeChange.GetObjectText_()
   Wscript.Echo  "Hive = " & TreeChange.Hive & VBNewLine _
      & "RootPath = "& TreeChange.RootPath _
      & TreeChange.GetObjectText_()      
Wend
```



Das folgende VBScript-Codebeispiel zeigt, wie die Änderung der Werte eines Schlüssels durch Registrierung für den Registrierungsanbieterereignistyp [**RegistryKeyChangeEvent überwacht wird.**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) Das Skript ruft eine asynchrone Methode auf,SWbemServices.Exe [**cNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md). Weitere Informationen zu asynchronen Aufrufen und zur Sicherheit finden Sie unter [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).

Das folgende Skript wird unbegrenzt ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird. Um das Skript manuell zu beenden, verwenden Sie Task-Manager, um den Prozess zu beenden. Verwenden Sie zum programmgesteuerten Beenden die [**Terminate-Methode**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) in der Win32 \_ Process-Klasse.


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:root/default") 
Set wmiSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink", "SINK_") 
Set ObjRegistry = GetObject("winmgmts:_
    {impersonationLevel = impersonate}!\\" _
    & strComputer & "\root\default:StdRegProv")

' Create a new key
strPath = "SOFTWARE\MyKey\MySubKey\"
Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

' Start listening for change in key
objWMIServices.ExecNotificationQueryAsync wmiSink, _ 
    "SELECT * FROM RegistryKeyChangeEvent " _ 
    & "WHERE Hive='HKEY_LOCAL_MACHINE' AND " _ 
    & "KeyPath='SOFTWARE\\MyKey\\MySubKey\\'" 
WScript.Echo "Listening for Registry Change Events..." 

While(True) 
    WScript.Sleep 1000
' You can use Regedit to make a change in the key 
' HKEY_LOCAL_MACHINE\SOFTWARE\MyKey\MySubKey\ 
'    to see an event generated.
Wend 

Sub SINK_OnObjectReady(EventObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Change Event" & vbCrLf & _
      EventObject.GetObjectText_() 
End Sub
```



 

