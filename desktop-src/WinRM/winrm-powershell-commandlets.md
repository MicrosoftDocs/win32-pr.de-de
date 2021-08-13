---
title: Verwaltete Referenz für WinRM Windows PowerShell-Befehlsklassen
description: Windows Die Remoteverwaltung 2.0 (WinRM) kann Windows PowerShell-Cmdlets für die Systemverwaltung verwenden. Windows PowerShell Cmdlets ermöglichen es einem Administrator, WinRM zu konfigurieren und Daten zu erhalten oder Ressourcen zu verwalten.
ms.assetid: 1ecdd41e-7257-483a-9a20-ae817f5f5ebe
ms.tgt_platform: multiple
keywords:
- ConnectWSManCommand
- DisableWSManCredSSPCommand
- DisconnectWSManCommand
- EnableWSManCredSSPCommand
- GetWSManCredSSPCommand
- GetWSManInstanceCommand
- InvokeWSManActionCommand
- NewWSManInstanceCommand
- NewWSManSessionOptionCommand
- RemoveWSManInstanceCommand
- SetWSManInstanceCommand
- SetWSManQuickConfigCommand
- TestWSManCommand
- SessionOption
- AuthentifizierungMechanismus
- ProxyAccessType
- ProxyAuthentication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d20a7615be5180350153596502386c9eac7c0c6820442284a717161ee1283e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412450"
---
# <a name="managed-reference-for-winrm-windows-powershell-command-classes"></a>Verwaltete Referenz für WinRM Windows PowerShell-Befehlsklassen

Windows Die Remoteverwaltung 2.0 (WinRM) kann Windows PowerShell-Cmdlets für die Systemverwaltung verwenden. Windows PowerShell Cmdlets ermöglichen es einem Administrator, WinRM zu konfigurieren und Daten zu erhalten oder Ressourcen zu verwalten.

Windows PowerShell-Cmdlets für WinRM bieten die gleiche Funktionalität wie das Befehlszeilenprogramm winrm. Allerdings führt Windows PowerShell auch folgende Schritte aus:

-   Automatisiert WinRM-Aufgaben in einer erweiterbaren und verwaltungsorientierten Skriptsprache.
-   Stellt ein einzelnes Tool für alle Verwaltungsaufgaben zur Verfügung.

Weitere [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) finden Sie unter .

## <a name="ws-management-windows-powershell-classes"></a>WS-Management Windows PowerShell-Klassen

**Namespace:** Microsoft.WsMan.Management

**Assembly:** System.Management.Automation

Die folgenden WinRM-Befehlsklassen werden von Windows PowerShell. Diese Klassen sind nur der Vollständigkeit halber in diesem Software Development Kit (SDK) enthalten. Die Member dieser Klassen können nicht direkt verwendet werden und sollten auch nicht zum Ableiten anderer Klassen verwendet werden.



| Klasse                        | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ConnectWSManCommand          | Stellt eine Verbindung mit dem WinRM-Dienst auf einem Remotecomputer her. <br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im Cmdlet [Verbinden-WSMan.](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                                                              |
| DisableWSManCredSSPCommand   | Deaktiviert die CredSSP-Authentifizierung auf einem Client.<br/> Ausführliche Informationen zu den Parametern und Beispiele finden Sie im Cmdlet [Disable-WSManCredSSP.](/powershell/module/Microsoft.WsMan.Management/Disable-WSManCredSSP?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                                                           |
| DisconnectWSManCommand       | Trennt die Verbindung mit dem WinRM-Dienst auf einem Remotecomputer. <br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im [Disconnect-WSMan-Cmdlet.](/powershell/module/Microsoft.WsMan.Management/Disconnect-WSMan?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                                                      |
| EnableWSManCredSSPCommand    | Aktiviert die CredSSP-Authentifizierung auf dem Client.<br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im [Cmdlet Enable-WSManCredSSP.](/powershell/module/Microsoft.WsMan.Management/Enable-WSManCredSSP?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                                                               |
| GetWSManCredSSPCommand       | Ruft die CredSSP-bezogene Konfiguration für den Client ab.<br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im [Get-WSManCredSSP-Cmdlet.](/powershell/module/Microsoft.WsMan.Management/Get-WSManCredSSP?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                                                         |
| GetWSManInstanceCommand      | Zeigt Verwaltungsinformationen für eine durch einen Ressourcen-URI angegebene Ressourceninstanz an.<br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im [Cmdlet Get-WSManInstance.](/powershell/module/Microsoft.WsMan.Management/Get-WSManInstance?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                          |
| InvokeWSManActionCommand     | Ruft eine Aktion für das Zielobjekt auf, das vom Ressourcen-URI und den Selektoren angegeben wird. <br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im [Invoke-WSManAction-Cmdlet.](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                         |
| NewWSManInstanceCommand      | Erstellt eine neue Instanz einer Verwaltungsressource. <br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im Cmdlet [New-WSManInstance.](/powershell/module/Microsoft.WsMan.Management/New-WSManInstance?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                                                             |
| NewWSManSessionOptionCommand | Erstellt eine Hashtabelle für die WinRM-Sitzungsoption, die als Eingabeparameter für die folgenden WSMan-Cmdlets verwendet wird: [Get-WSManInstance,](/powershell/module/Microsoft.WsMan.Management/Get-WSManInstance?view=powershell-5.1&preserve-view=true) [Set-WSManInstance,](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) [Invoke-WSManAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)und [Verbinden-WSMan](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true). <br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie unter [New-WSManSessionOption.](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true)<br/> |
| RemoveWSManInstanceCommand   | Löscht eine Instanz einer Verwaltungsressource. <br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im [Remove-WSManInstance-Cmdlet.](/powershell/module/Microsoft.WsMan.Management/Remove-WSManInstance?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                                                                   |
| SetWSManInstanceCommand      | Ändert die mit einer Ressource verknüpften Verwaltungsinformationen. <br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im [Set-WSManInstance-Cmdlet.](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                                                       |
| SetWSManQuickConfigCommand   | Konfiguriert den lokalen Computer für die Remoteverwaltung. <br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im Cmdlet [Set-WSManQuickConfig.](/powershell/module/Microsoft.WsMan.Management/Set-WSManQuickConfig?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                                                      |
| TestWSManCommand             | Überprüft, ob der WinRM-Dienst auf einem lokalen oder Remotecomputer ausgeführt wird. <br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im [Test-WSMan-Cmdlet.]( /powershell/module/microsoft.wsman.management/test-wsman?view=powershell-7&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                                        |
| SessionOption                | Definiert eine Reihe von erweiterten Optionen für die WS-Management-Sitzung.<br/> Beispiele und ausführliche Informationen zu den möglichen Werten finden Sie im Cmdlet [Verbinden-WSMan.](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true)<br/>                                                                                                                                                                                                                                                                                                                             |



 

## <a name="ws-management-windows-powershell-enumerations"></a>WS-Management Windows PowerShell Enumerationen

Die folgenden Enumerationen werden von Windows PowerShell. Diese Enumerationen sind nur der Vollständigkeit halber in diesem Software Development Kit (SDK) enthalten.



| Enumeration             | Beschreibung                                                                                                                                                                                                                                   |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AuthentifizierungMechanismus | Gibt den Authentifizierungsmechanismus an, der auf dem Server verwendet werden soll. <br/> Beispiele und ausführliche Informationen zu den möglichen Werten finden Sie im Cmdlet [Verbinden-WSMan.](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true)<br/>      |
| ProxyAccessType         | Gibt den Mechanismus an, mit dem der Proxyserver gesucht wird.<br/> Beispiele und ausführliche Informationen zu den möglichen Werten finden Sie im Cmdlet [New-WSManSessionOption.](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true)<br/> |
| ProxyAuthentication     | Gibt die Authentifizierungsmethode an, die auf dem Proxy verwendet wird.<br/> Beispiele und ausführliche Informationen zu den möglichen Werten finden Sie im Cmdlet [New-WSManSessionOption.](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true)<br/>      |



 

 

