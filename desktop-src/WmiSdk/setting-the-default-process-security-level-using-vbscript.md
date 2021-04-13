---
title: Festlegen der Standardprozess-Sicherheitsstufe mit VBScript
description: Ein Skript kann die Standardeinstellungen für die WMI-Authentifizierung und den Identitätswechsel verwenden. Für das Skript ist jedoch möglicherweise eine Verbindung mit mehr Sicherheit erforderlich, oder es kann eine Verbindung mit einem Namespace hergestellt werden, der eine verschlüsselte Verbindung erfordert.
ms.assetid: cb477224-3117-45e4-9271-613b58e48b6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03fe69228021fe8d3f36f03e60cb2366b6132f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218312"
---
# <a name="set-the-default-process-security-level-with-vbscript"></a>Festlegen der Standardprozess-Sicherheitsstufe mit VBScript

Ein Skript kann die Standardeinstellungen für die WMI-Authentifizierung und den Identitätswechsel verwenden. Für das Skript ist jedoch möglicherweise eine Verbindung mit mehr Sicherheit erforderlich, oder es kann eine Verbindung mit einem Namespace hergestellt werden, der eine verschlüsselte Verbindung erfordert. Weitere Informationen finden Sie unter [Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md) und [erfordern einer verschlüsselten Verbindung mit einem Namespace](requiring-an-encrypted-connection-to-a-namespace.md).

Im einfachsten Fall kann ein Skript die Standardeinstellungen für die Authentifizierung und den Identitätswechsel verwenden. WMI wird normalerweise auf einem gemeinsamen Dienst Host ausgeführt und verwendet dieselbe Authentifizierung wie andere Prozesse auf dem Host. Wenn Sie den WMI-Prozess mit einer anderen Authentifizierungs Stufe ausführen möchten, führen Sie WMI mit dem [**WinMgmt**](winmgmt.md) -Befehl mit dem Schalter **/standalonehost** aus, und legen Sie die Authentifizierungs Ebene für WMI in der Regel fest. Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md).

Das folgende Skript verwendet die Standardeinstellungen für Identitätswechsel-und Authentifizierungs Ebenen.


```VB
strComputer = "." 
Set objServices = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



Sie können auch einen [Moniker](constructing-a-moniker-string.md) in einem Aufruf von [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)verwenden und die Standard Sicherheitseinstellungen festlegen, wie im folgenden Beispiel gezeigt.


```VB
strComputer = "." 
Set objServices = GetObject( _
    "winmgmts:{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!root/cimv2")
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



Weitere Informationen zum Festlegen von unterschiedlichen Identitätswechsel-oder Authentifizierungs Ebenen in einem Skript oder zum Festlegen der Standardwerte für einen Computer finden Sie in den folgenden Themen:

-   [Ändern der Standard Anmelde Informationen für die Authentifizierung mithilfe von VBScript](#changing-the-default-authentication-credentials-using-vbscript)
-   [Ändern der Standardeinstellungen für Identitätswechsel mithilfe von VBScript](#changing-the-default-impersonation-levels-using-vbscript)
-   [Festlegen der Standard Identitätswechsel Ebene mithilfe der Registrierung](#setting-the-default-impersonation-level-using-the-registry)
-   [Zugreifen auf das "Swap Security"-Objekt in VBScript](#accessing-the-swbemsecurity-object-in-vbscript)
-   [**Austausch Sicherheit**](swbemsecurity.md)

## <a name="changing-the-default-authentication-credentials-using-vbscript"></a>Ändern der Standard Anmelde Informationen für die Authentifizierung mithilfe von VBScript

Sie können die Authentifizierungs Ebene in einem Skript mithilfe der [Monikerzeichenfolge](constructing-a-moniker-string.md) und der Objekte " [**Swap-Locator**](swbemlocator.md) " und " [**taubemsecurity**](swbemsecurity.md) " ändern.

Die Authentifizierungs Ebene muss entsprechend den Anforderungen des Ziel Betriebssystems festgelegt werden, mit dem Sie eine Verbindung herstellen. Weitere Informationen finden Sie unter [Herstellen einer Verbindung zwischen verschiedenen Betriebssystemen](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).

Im folgenden VBScript-Codebeispiel wird gezeigt, wie die Authentifizierungs Ebene in einem Skript geändert wird, das die Daten des freien Speicherplatzes von einem Remote Computer mit dem Namen "Server1" abruft.


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{authenticationLevel=Pkt}!\\" _
    & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
    Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
        "FreeSpace: " & vbTab & objDisk.FreeSpace 
    NextstrComputer = "." 
    Set objServices = GetObject( "winmgmts:{impersonationLevel=impersonate," _
                               & "authenticationLevel=pktPrivacy}!root/cimv2")
    Set objProcessSet = objServices.ExecQuery("SELECT Name FROM Win32_Process",,48)
    For Each Process in objProcessSet
        WScript.Echo Process.Name
    Next
Next
```



Verwenden Sie in Skript-monikerverbindungen mit WMI den Kurznamen, der in der Spalte "monikerName/Beschreibung" der Tabelle unten angezeigt wird. Im folgenden Skript wird die Authentifizierungs Ebene beispielsweise auf **wbemauthenticationlevelpktintegrity** festgelegt.


```VB
SetobjWMIService = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!root\cimv2")
```



In der folgenden Tabelle sind die Authentifizierungs Ebenen aufgelistet, die Sie festlegen können. Diese Ebenen werden in wbemdisp. tlb in der Enumeration [wbemauthenticationlevelenumeration](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)definiert.



| Name/Wert                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Wbemauthenticationleveldefault**<br/> 0<br/>      | Moniker: Standard<br/> WMI verwendet die Standardeinstellung für die Windows-Authentifizierung. Dies ist die empfohlene Einstellung, die es WMI ermöglicht, bis zu dem vom Server benötigten Wert auszuhandeln, der Daten zurückgibt. Wenn für den Namespace jedoch eine Verschlüsselung erforderlich ist, verwenden Sie **wbemauthenticationlevelpktprivacy**.<br/> |
| **Wbemauthenticationlevelnone**<br/> 1<br/>         | Moniker: keine<br/> Verwendet keine Authentifizierung.<br/>                                                                                                                                                                                                                                            |
| **Wbemauthenticationlevelconnect**<br/> 2<br/>      | Moniker: verbinden<br/> Authentifiziert die Anmelde Informationen des Clients nur, wenn der Client eine Beziehung mit dem Server herstellt.<br/>                                                                                                                                                    |
| **Wbemauthenticationlevelcall**<br/> 3<br/>         | Aufruf<br/> Authentifiziert sich nur zu Beginn jedes Aufrufes, wenn der Server die Anforderung empfängt.<br/>                                                                                                                                                                                      |
| **Wbemauthenticationlevelpkt**<br/> 4<br/>          | Moniker: Pkt<br/> Authentifiziert, dass alle empfangenen Daten vom erwarteten Client stammen.<br/>                                                                                                                                                                                                   |
| **Wbemauthenticationlevelpktintegrity**<br/> 5<br/> | Moniker: PktIntegrity<br/> Authentifiziert und überprüft, ob keine der zwischen Client und Server übertragenen Daten geändert wurde.<br/>                                                                                                                                                  |
| **Wbemauthenticationlevelpktprivacy**<br/> 6<br/>   | Moniker: PKTPRIVACY<br/> Authentifiziert alle vorherigen Identitätswechsel Ebenen und verschlüsselt den Argument Wert jedes Remote Prozedur Aufrufes. Verwenden Sie diese Einstellung, wenn der Namespace, für den Sie eine Verbindung herstellen möchten, eine verschlüsselte Verbindung erfordert.<br/>                                               |



 

Um einen erfolgreichen-Rückruf zu ermitteln, überprüfen Sie den Rückgabewert, nachdem Sie die Authentifizierungs Ebene geändert haben.

Da z. b. lokale Verbindungen immer die Authentifizierungs Ebene **wbemauthenticationlevelpktprivacy** aufweisen, kann im folgenden Beispiel die Authentifizierungs Ebene nicht festgelegt werden, da Sie mit dem lokalen Computer verbunden ist.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!" _
    & "\\" & strComputer & "\root\cimv2")
```



Ein Anbieter kann die Sicherheit für einen Namespace so festlegen, dass keine Daten zurückgegeben werden, es sei denn, Sie verwenden den Paket Datenschutz (PKTPRIVACY) in der Verbindung mit diesem Namespace. Dadurch wird sichergestellt, dass die Daten beim Überschreiten des Netzwerks verschlüsselt werden. Wenn Sie versuchen, eine niedrigere Authentifizierungs Ebene festzulegen, erhalten Sie die Meldung "Zugriff verweigert". Weitere Informationen finden Sie unter [Sichern von WMI-Namespaces](securing-wmi-namespaces.md).

## <a name="changing-the-default-impersonation-levels-using-vbscript"></a>Ändern der Standard Identitätswechsel Ebenen mithilfe von VBScript

Wenn Sie Aufrufe der Skript-API für WMI ausführen, wird empfohlen, die Standardeinstellungen zu verwenden, die WMI für die Identitätswechsel Ebene bereitstellt. Remote Anrufe und einige Anbieter mit mehr als einem Netzwerkhop erfordern eine höhere Identitätswechsel Ebene als WMI verwendet. Wenn die Identitätswechsel Ebene nicht ausreicht, kann ein Anbieter eine Anforderung ablehnen oder unvollständige Informationen bereitstellen.

Wenn Sie die Identitätswechsel Ebene nicht in einem Moniker oder durch Festlegen von " [**Swap Security. Identitäts ationlevel**](swbemsecurity-impersonationlevel.md) " für ein Sicherungs fähiges Objekt festlegen, legen Sie die Standard-DCOM-Identitätswechsel Ebene für das Betriebssystem fest. Die Ebene des Identitäts Wechsels muss entsprechend den Anforderungen des Ziel Betriebssystems festgelegt werden, mit dem Sie eine Verbindung herstellen. Weitere Informationen finden Sie unter [Herstellen einer Verbindung zwischen verschiedenen Betriebssystemen](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).

Im folgenden VBScript-Codebeispiel wird gezeigt, wie die Identitätswechsel Ebene im gleichen Skript geändert wird.


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" _
                              & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
             "FreeSpace: " & vbTab & objDisk.FreeSpace 
Next
```



In der folgenden Tabelle werden die Authentifizierungs Ebenen in [wbemimpersonationlevelenum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) aufgelistet, die verwenden.



| Name/Wert                                                    | BESCHREIBUNG                                                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **wbemimpersonationlevelanonymous**<br/> 1<br/>   | Moniker: Anonym<br/> Verbirgt die Anmeldeinformationen des Aufrufers. Bei Verwendung dieser Identitätswechselebene können Aufrufe von WMI fehlschlagen.<br/>                                                                                                  |
| **wbemimpersonationlevelidentifizierung**<br/> 2<br/>    | Moniker: identifizieren<br/> Ermöglicht es Objekten, die Anmeldeinformationen des Aufrufers abzufragen. Bei Verwendung dieser Identitätswechselebene können Aufrufe von WMI fehlschlagen.<br/>                                                                                 |
| **wbemimpersonationlevelidentitäts-Ate**<br/> 3<br/> | Moniker: Identität annehmen<br/> Ermöglicht es Objekten, die Anmeldeinformationen des Aufrufers zu verwenden. Dies ist die empfohlene Identitätswechsel Ebene für die Skript-API für WMI-Aufrufe.<br/>                                                        |
| **wbemimpersonationleveldelegat**<br/> 4<br/>    | Moniker: Delegat<br/> Ermöglicht es Objekten, anderen Objekten die Verwendung der Anmeldeinformationen des Aufrufers zu gestatten. Dieser Identitätswechsel funktioniert mit der Skript-API für WMI-Aufrufe, kann jedoch ein unnötiges Sicherheitsrisiko darstellen.<br/> |



 

Im folgenden Beispiel wird gezeigt, wie der Identitätswechsel in einer Monikerzeichenfolge festgelegt wird, wenn eine bestimmte Instanz des [**Win32- \_ Prozesses**](/windows/desktop/CIMWin32Prov/win32-process)angefordert wird.


```VB
Set object = GetObject("winmgmts:{impersonationLevel=impersonate}!root\cimv2:Win32_Process.Handle='0'")
```



Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md).

## <a name="setting-the-default-impersonation-level-using-the-registry"></a>Festlegen der Standard Identitätswechsel Ebene mithilfe der Registrierung

Wenn Sie Zugriff auf die Registrierung haben, können Sie auch den Standard Registrierungsschlüssel für die Identitätswechsel Ebene festlegen. Dieser Schlüssel gibt an, welche Identitätswechsel Ebene die Skript-API für WMI verwendet, sofern nicht anders angegeben. Der folgende Pfad identifiziert den Registrierungs Pfad.

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **Scripting** \\ **Standard** Identitätswechsel Ebene

Standardmäßig ist der Registrierungsschlüssel auf 3 festgelegt. dabei wird die Identitätswechsel Ebene annehmen angegeben. Einige Anbieter erfordern möglicherweise eine höhere Identitätswechsel Ebene.

## <a name="accessing-the-swbemsecurity-object-in-vbscript"></a>Zugreifen auf das "Swap Security"-Objekt in VBScript

Die andere Möglichkeit, die Identitätswechsel Ebene festzulegen, ist das [**Swap**](swbemsecurity.md) -Sicherheits Objekt, das als [**\_ Sicherheits**](swbemservices-security-.md) Eigenschaft der Objekte " [**Swap Services**](swbemservices.md)", " [**errbewbject**](swbemobject.md)", " [**errbemubjectset**](swbemobjectset.md)", " [**errbemeventsource**](swbemeventsource.md)", " [**errbewbjectpath**](swbemobjectpath.md)" und " [**errbemlocator**](swbemlocator.md) " angezeigt wird.

WMI übergibt die Sicherheitseinstellung eines übergeordneten Objekts an die nachfolgenden Elemente des ursprünglichen Objekts. Aus diesem Grund können Sie die Identitätswechsel Ebene eines " [**errbemservices**](swbemservices.md) "-Objekts festlegen, nachdem Sie sich bei WMI-und API-Aufrufen mit diesem Objekt oder Objekten, die daraus erstellt wurden, anmelden, z. b. Objekte des Typs " [**Austausch Vorgang**](swbemobject.md)".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Sichern von Skript Clients](securing-scripting-clients.md)
</dt> </dl>

 

