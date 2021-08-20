---
title: Abrufen von Daten von einem Remotecomputer
description: Sie können Daten abrufen oder Ressourcen auf Remotecomputern sowie auf dem lokalen Computer verwalten. Das Herstellen einer Verbindung mit einem Remotecomputer in einem Windows Remoteverwaltungsskript ähnelt dem Herstellen einer lokalen Verbindung.
ms.assetid: 578eee80-a6c1-4456-9683-14e0a3386248
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cf3531e19c0848691ededa0c3b6b2fad642de33c2a5f2d465ac899716970a512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823407"
---
# <a name="obtaining-data-from-a-remote-computer"></a>Abrufen von Daten von einem Remotecomputer

Sie können Daten abrufen oder Ressourcen auf Remotecomputern sowie auf dem lokalen Computer verwalten. Das Herstellen einer Verbindung mit einem Remotecomputer in einem Windows Remoteverwaltungsskript ähnelt dem Herstellen einer lokalen Verbindung. WMI-Instanzdaten sind verfügbar. Wenn der Remotecomputer über BMC-Hardware verfügt, die mithilfe des WS-Management-Protokolls kommunizieren kann, sind auch [DIE DATEN (Intelligent Platform Management Interface, IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) verfügbar. Weitere Informationen finden Sie unter [Windows Remoteverwaltung und WMI](windows-remote-management-and-wmi.md) und [Remotehardwareverwaltung.](remote-hardware-management.md)

Möglicherweise müssen Sie ein [**ConnectionOptions-Objekt**](connectionoptions.md) erstellen, um Informationen zum Typ der für die Anmeldung angeforderten Authentifizierung anzugeben.

Wenn das Konto auf dem Remotecomputer über denselben Anmeldebenutzernamen und dasselbe Kennwort verfügt, benötigen Sie nur den Transport, den Domänennamen und den Computernamen. Aufgrund der [Benutzerkontensteuerung (User Account Control, UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista)muss das Remotekonto ein Domänenkonto und ein Mitglied der Gruppe "Remotecomputeradministratoren" sein. Wenn das Konto ein Mitglied des lokalen Computers der Gruppe Administratoren ist, lässt die UAC keinen Zugriff auf den WinRM-Dienst zu. Für den Zugriff auf einen WinRM-Remotedienst in einer Arbeitsgruppe muss die UAC-Filterung für lokale Konten deaktiviert werden, indem der folgende DWORD-Registrierungseintrag erstellt und dessen Wert auf 1: **\[ HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion Policies System \\ \\ \] LocalAccountTokenFilterPolicy .**

**So stellen Sie eine Verbindung mit einem Remotecomputer mit ihrem Benutzernamen und Kennwort für die Anmeldung**

1.  Geben Sie den Zielcomputer mit einem vollqualifizierten Domänennamen oder einer IP-Adresse an, und weisen Sie diesen einer Konstante zu. Wenn eine IPv6-Adresse angegeben wird, muss die Adresse in eckige Klammern eingeschlossen werden.

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  Erstellen Sie ein [**WSMan-Objekt.**](wsman.md)

    ```VB
    Set objWsman = CreateObject("WSMan.Automation")
    ```

    

3.  Erstellen Sie die Sitzung, geben Sie den Transport, HTTP oder HTTPS an, und verketten Sie sie mit der Konstante, die den Zielcomputer darstellt.

    ```VB
    
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

Das folgende VBScript-Codebeispiel zeigt das vollständige Skript. Das Skript enthält eine Unterroutine, um die Daten von unformatiertem XML in eine lesbare Form zu transformieren. Weitere Informationen finden Sie unter [Anzeigen der XML-Ausgabe von WinRM-Skripts.](displaying-xml-output-from-winrm-scripts.md)


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



**So stellen Sie mithilfe eines anderen Kontos eine Verbindung mit einem Remotecomputer herstellen**

1.  Geben Sie den Zielcomputer mit einem vollqualifizierten Domänennamen oder einer IP-Adresse an, und weisen Sie diesen einer Konstante zu. Wenn eine IPv6-Adresse angegeben wird, muss die Adresse in eckige Klammern eingeschlossen werden.

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  Erstellen Sie ein [**WSMan-Objekt.**](wsman.md)

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    
    ```

    

3.  Rufen Sie [**die WSMan.CreateConnectionOptions-Methode auf,**](wsman-createconnectionoptions.md) um ein [**ConnectionOptions-Objekt zu**](connectionoptions.md) erstellen. Das Konto auf dem Remotecomputer muss Mitglied der Administratorgruppe des lokalen Computers sein.

    ```VB
    Set objConnectionOptions = objWsman.CreateConnectionOptions
    objConnectionOptions.UserName = "Username"
    objConnectionOptions.Password = "Password"
    ```

    

4.  Geben Sie [**im WSman.CreateSession-Aufruf**](wsman-createsession.md) die entsprechenden Sitzungsverbindungsflags im *flags-Parameter* an. Weitere Informationen finden Sie unter [Sitzungskonst konstanten](session-constants.md). Geben Sie den Zielcomputer mit einem vollqualifizierten Computernamen oder einer IP-Adresse und dem Transport an – http oder https. Dieses Skript fordert die [*Kerberos-Authentifizierung*](windows-remote-management-glossary.md) vom WinRM-Remotedienst an.

    Im Gegensatz zu WMI-Skripts können Sie mehrere Authentifizierungsmethoden in WinRM-Skripts verwenden. Weitere Informationen finden Sie unter [Authentifizierung für Remoteverbindungen.](authentication-for-remote-connections.md)

    ```VB
    iFlags = objWsman.SessionFlagUseKerberos Or _
      objWsman.SessionFlagCredUserNamePassword
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
      iFlags, objConnectionOptions)
    ```

    

5.  Nachdem das Sitzungsobjekt verfügbar ist, [](session.md) können Sie eine der Session-Objektmethoden aufrufen, um Daten für eine Ressource zu erhalten. Sie können Daten für jede Ressource erhalten, die auf dem Computer verfügbar ist, auf dem die Sitzung ausgeführt wird. Weitere Informationen finden Sie unter [Abrufen von Daten vom lokalen Computer.](obtaining-data-from-the-local-computer.md)

Das folgende VBScript-Codebeispiel zeigt das vollständige Skript. Das Skript enthält eine Unterroutine, um die Daten von unformatiertem XML in eine lesbare Form zu transformieren. Weitere Informationen finden Sie unter [Anzeigen der XML-Ausgabe von WinRM-Skripts.](displaying-xml-output-from-winrm-scripts.md) Das Skript gibt die Kerberos-Authentifizierung an. Wenn sich der Remotecomputer jedoch in einer Arbeitsgruppe und nicht in einer Domäne befindet, generiert die Angabe von Kerberos einen Fehler.


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

[Informationen Windows Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Verwenden Windows Remoteverwaltung](using-windows-remote-management.md)
</dt> <dt>

[Windows Remoteverwaltungsreferenz](windows-remote-management-reference.md)
</dt> </dl>

 

 