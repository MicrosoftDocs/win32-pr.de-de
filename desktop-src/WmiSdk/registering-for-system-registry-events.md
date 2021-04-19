---
description: Zum Empfangen von Benachrichtigungen vom System Registrierungs Anbieter muss eine Verwaltungs Anwendung als temporärer Ereignisconsumer registriert werden.
ms.assetid: 4cac5fdd-c842-4d7e-a56e-2e1312df68b4
ms.tgt_platform: multiple
title: Registrierung für System Registrierungs Ereignisse
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 886046f5ffef366cdba2efb86629019f2ee0b5e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369055"
---
# <a name="registering-for-system-registry-events"></a>Registrierung für System Registrierungs Ereignisse

Zum Empfangen von Benachrichtigungen vom [System Registrierungs](/previous-versions/windows/desktop/regprov/system-registry-provider) Anbieter muss eine Verwaltungs Anwendung als temporärer Ereignisconsumer registriert werden. Die meisten Anforderungen für die Registrierung für den System Registrierungs Anbieter sind identisch mit allen anderen Ereignis Registrierungen, mit dem Unterschied, dass Sie auch das folgende Verfahren ausführen müssen.

Der Registrierungs Anbieter stellt Ereignis Klassen für Ereignisse in der Systemregistrierung bereit. Weitere Informationen zur allgemeinen Ereignis Registrierung finden Sie unter [empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md).

Im folgenden Verfahren wird beschrieben, wie Sie sich für System Registrierungs Ereignisse registrieren.

**So registrieren Sie sich für System Registrierungs Ereignisse**

1.  Ruft eine Benachrichtigungs Abfrage Methode auf.

    Verwenden Sie entweder in Skript oder C++ eine Benachrichtigungs Abfrage, z. b. [**SWbemServices.Execnotificationqueryasync**](swbemservices-execnotificationqueryasync.md) oder [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync). Erstellen Sie eine Abfrage Zeichenfolge für den *bstrinquery* -Parameter von **IWbemServices:: ExecNotificationQueryAsync** oder die ""- *Abfrage* "im Skript.

2.  Bestimmen Sie, welche Art von Ereignis Sie empfangen möchten, und erstellen Sie die Abfrage.

    In der folgenden Tabelle sind die Registrierungs Ereignis Klassen aufgelistet, die Sie verwenden können.

    

    | Ereignisklasse                                                      | Hive-Speicherort        | BESCHREIBUNG                                                 |
    |------------------------------------------------------------------|----------------------|-------------------------------------------------------------|
    | [**Registryevent**](/previous-versions/windows/desktop/regprov/registryevent)                       | –<br/>       | Abstrakte Basisklasse für Änderungen in der Registrierung.<br/> |
    | [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent)   | RootPath<br/>  | Überwacht Änderungen an einer Hierarchie von Schlüsseln.<br/>         |
    | [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)     | KEYPATH<br/>   | Überwacht Änderungen an einem einzelnen Schlüssel.<br/>                |
    | [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent) | ValueName<br/> | Überwacht Änderungen an einem einzelnen Wert.<br/>              |

    

     

    Diese Klassen verfügen über eine Eigenschaft namens **Hive** , die die Hierarchie von Schlüsseln identifiziert, die auf Änderungen überwacht werden sollen, z. b. **HKEY \_ local \_ Machine**.

    Änderungen an den **HKEY \_ - \_ Klassen root** und **HKEY \_ Current \_ User** -Strukturen werden von [**registryevent**](/previous-versions/windows/desktop/regprov/registryevent) oder von ihr abgeleiteten Klassen, z. b. [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), nicht unterstützt.

3.  Erstellen Sie die WHERE-Klausel für die Ereignis Registrierung.

    Der System Registrierungs Anbieter verfügt über bestimmte Regeln für WHERE-Klauseln. Weitere Informationen finden Sie unter [Erstellen einer richtigen WHERE-Klausel für den Registrierungs Anbieter](creating-a-proper-where-clause-for-the-registry-provider.md). Allgemeine Informationen zum Erstellen einer WHERE-Klausel finden Sie unter [Querying with WQL (Abfragen mit WQL](querying-with-wql.md)).

4.  Bestimmen Sie, ob Ihr Consumer Ereignisse empfängt.

    Der System Registrierungs Anbieter garantiert nicht, dass alle gesendeten Ereignisse übermittelt werden. Weitere Informationen finden Sie unter [empfangen von Registrierungs Ereignissen](receiving-registry-events.md).

Im folgenden VBScript-Codebeispiel wird gezeigt, wie eine Registrierungs Änderung in der HKEY-Software für **\_ lokale \_ Computer** \\  \\ **Microsoft** Hive oder Unterstruktur erkannt wird. Dabei handelt es sich um ein Überwachungs Skript, das zu Demonstrationszwecken in einem Prozess mit dem Namen Wscript.exe ausgeführt wird, bis er im **Task-Manager** beendet, WMI beendet oder das Betriebssystem neu gestartet wird. Das Skript verwendet einen [*semisynchronen*](gloss-s.md) Aufruf von [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md). Weitere Informationen zu semisynchronen aufrufen finden Sie unter [Erstellen eines semisynchronen Aufrufs mit VBScript](making-a-semisynchronous-call-with-vbscript.md).


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



Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie Sie die Änderung der Werte eines Schlüssels überwachen, indem Sie für den Registrierungs Anbieter-Ereignistyp [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)registrieren. Das Skript ruft eine asynchrone Methode auf, [**SWbemServices.Execnotificationqueryasync**](swbemservices-execnotificationqueryasync.md). Weitere Informationen zu asynchronen Aufrufen und zur Sicherheit finden Sie unter [Erstellen eines asynchronen Aufrufs mit VBScript](making-an-asynchronous-call-with-vbscript.md).

Das folgende Skript wird unbegrenzt ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird. Um das Skript manuell anzuhalten, verwenden Sie den Task-Manager, um den Prozess zu unterbinden. Verwenden Sie zum programmgesteuerten beenden die Methode " [**Beenden**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) " in der Win32- \_ Prozess Klasse.


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



 

