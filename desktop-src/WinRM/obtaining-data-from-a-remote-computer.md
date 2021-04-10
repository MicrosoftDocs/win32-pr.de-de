---
title: Abrufen von Daten von einem Remote Computer
description: Sie können Daten abrufen oder Ressourcen sowohl auf Remote Computern als auch auf dem lokalen Computer verwalten. Das Herstellen einer Verbindung mit einem Remote Computer in einem Windows-Remoteverwaltung Skript ähnelt dem Herstellen einer lokalen Verbindung.
ms.assetid: 578eee80-a6c1-4456-9683-14e0a3386248
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8cfc95a73dab4c9a0f19481b7ba41f3c40a3862d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858266"
---
# <a name="obtaining-data-from-a-remote-computer"></a>Abrufen von Daten von einem Remote Computer

Sie können Daten abrufen oder Ressourcen sowohl auf Remote Computern als auch auf dem lokalen Computer verwalten. Das Herstellen einer Verbindung mit einem Remote Computer in einem Windows-Remoteverwaltung Skript ähnelt dem Herstellen einer lokalen Verbindung. WMI-Instanzdaten sind verfügbar. wenn auf dem Remote Computer BMC-Hardware vorhanden ist, die mithilfe des WS-Management Protokolls kommunizieren kann, sind auch die Daten der [Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) verfügbar. Weitere Informationen finden Sie unter [Windows-Remoteverwaltung und WMI](windows-remote-management-and-wmi.md) und [Remote Hardware Verwaltung](remote-hardware-management.md).

Möglicherweise müssen Sie ein [**ConnectionOptions**](connectionoptions.md) -Objekt erstellen, um Informationen über den Authentifizierungstyp anzugeben, der für die Anmeldung angefordert wurde.

Wenn das Konto auf dem Remote Computer über denselben Anmelde Namen und dasselbe Kennwort verfügt, benötigen Sie lediglich den Transport, den Domänen Namen und den Computernamen. Aufgrund der [Benutzerkontensteuerung (User Account Control, UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista)muss das Remote Konto ein Domänen Konto und ein Mitglied der Gruppe "Remote Computer Administratoren" sein. Wenn das Konto Mitglied der Gruppe "Administratoren" ist, ist der Zugriff auf den WinRM-Dienst nicht möglich. Für den Zugriff auf einen WinRM-Remote Dienst in einer Arbeitsgruppe muss die UAC-Filterung für lokale Konten deaktiviert werden, indem der folgende DWORD-Registrierungs Eintrag erstellt und der Wert auf 1 festgelegt wird: **\[ HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Policies \\ System \] LocalAccountTokenFilterPolicy**.

**So stellen Sie mithilfe Ihres Anmelde namens und Kennworts eine Verbindung mit einem Remote Computer her**

1.  Geben Sie den Zielcomputer mit einem voll qualifizierten Domänen Namen oder einer IP-Adresse an, und weisen Sie ihn einer Konstanten zu. Wenn eine IPv6-Adresse angegeben ist, muss die Adresse in eckige Klammern eingeschlossen werden.

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  Erstellen Sie ein [**WSMAN**](wsman.md) -Objekt.

    ```VB
    Set objWsman = CreateObject("WSMan.Automation")
    ```

    

3.  Erstellen Sie die Sitzung, geben Sie den Transport, http oder HTTPS an, und verketten Sie Sie mit der Konstante, die den Zielcomputer darstellt.

    ```VB
    
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

Das folgende VBScript-Codebeispiel zeigt das komplette Skript. Das Skript enthält eine Unterroutine zum Transformieren der Daten aus unformatierten XML-Daten in eine lesbare Form. Weitere Informationen finden Sie unter [Anzeigen der XML-Ausgabe von WinRM-Skripts](displaying-xml-output-from-winrm-scripts.md).


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



**So stellen Sie eine Verbindung mit einem Remote Computer mit einem anderen Konto her**

1.  Geben Sie den Zielcomputer mit einem voll qualifizierten Domänen Namen oder einer IP-Adresse an, und weisen Sie ihn einer Konstanten zu. Wenn eine IPv6-Adresse angegeben ist, muss die Adresse in eckige Klammern eingeschlossen werden.

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  Erstellen Sie ein [**WSMAN**](wsman.md) -Objekt.

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    
    ```

    

3.  Rufen Sie die [**WSMAN. kreateconnectionoptions**](wsman-createconnectionoptions.md) -Methode auf, um ein [**ConnectionOptions**](connectionoptions.md) -Objekt zu erstellen. Das Konto auf dem Remote Computer muss Mitglied der Gruppe "lokale Computer Administratoren" sein.

    ```VB
    Set objConnectionOptions = objWsman.CreateConnectionOptions
    objConnectionOptions.UserName = "Username"
    objConnectionOptions.Password = "Password"
    ```

    

4.  Geben Sie im [**WSMAN. kreatesession**](wsman-createsession.md) -Befehl die entsprechenden sitzungsverbindungsflags im *Flags* -Parameter an. Weitere Informationen finden Sie unter [Sitzungs Konstanten](session-constants.md). Geben Sie den Zielcomputer mit einem voll qualifizierten Computernamen oder einer IP-Adresse und dem Transport-– http oder HTTPS an. Dieses Skript fordert die [*Kerberos*](windows-remote-management-glossary.md) -Authentifizierung vom Remote-WinRM-Dienst an.

    Anders als bei WMI-Skripts können Sie verschiedene Authentifizierungsmethoden in WinRM-Skripts verwenden. Weitere Informationen finden Sie unter [Authentifizierung für Remote Verbindungen](authentication-for-remote-connections.md).

    ```VB
    iFlags = objWsman.SessionFlagUseKerberos Or _
      objWsman.SessionFlagCredUserNamePassword
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
      iFlags, objConnectionOptions)
    ```

    

5.  Nachdem das Sitzungs Objekt verfügbar ist, können Sie eine beliebige [**Sitzungs**](session.md) Objektmethode zum Abrufen von Daten für eine Ressource abrufen. Sie können Daten für alle Ressourcen erhalten, die auf dem Computer verfügbar sind, auf dem die Sitzung ausgeführt wird. Weitere Informationen finden Sie unter Abrufen [von Daten vom lokalen Computer](obtaining-data-from-the-local-computer.md).

Das folgende VBScript-Codebeispiel zeigt das komplette Skript. Das Skript enthält eine Unterroutine zum Transformieren der Daten aus unformatierten XML-Daten in eine lesbare Form. Weitere Informationen finden Sie unter [Anzeigen der XML-Ausgabe von WinRM-Skripts](displaying-xml-output-from-winrm-scripts.md). Das Skript gibt die Kerberos-Authentifizierung an, aber wenn sich der Remote Computer in einer Arbeitsgruppe und nicht in einer Domäne befindet, wird bei der Angabe von Kerberos ein Fehler generiert.


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("Wsman.Automation")
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "Username"
objConnectionOptions.Password = "Password"
iFlags = objWsman.SessionFlagUseKerberos Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
  iFlags, objConnectionOptions)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml2.DOMDocument.3.0") 
    Set xslFile = CreateObject("MSXml2.DOMDocument.3.0")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Windows-Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Verwenden von Windows-Remoteverwaltung](using-windows-remote-management.md)
</dt> <dt>

[Windows-Remoteverwaltung Referenz](windows-remote-management-reference.md)
</dt> </dl>

 

 