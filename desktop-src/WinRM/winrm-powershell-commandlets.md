---
title: Verwaltete Referenz für WinRM Windows PowerShell-Befehlsklassen
description: In Windows-Remoteverwaltung 2,0 (WinRM) können Windows PowerShell-Cmdlets für die Systemverwaltung verwendet werden. Windows PowerShell-Cmdlets ermöglichen Administratoren das Konfigurieren von WinRM und das erhalten von Daten oder das Verwalten von Ressourcen.
ms.assetid: 1ecdd41e-7257-483a-9a20-ae817f5f5ebe
ms.tgt_platform: multiple
keywords:
- Connectwsmancommand
- Disablewsmankredsspcommand
- Disconnectwsmancommand
- Enablewsmankredsspcommand
- Getwsmankredsspcommand
- Getwsmaninstancecommand
- Invokewsmanaktionsbefehl
- Newwsmaninstancecommand
- Newwsmansessionoptioncommand
- Removewsmaninstancecommand
- "\"Smansmaninstancecommand\""
- "\"Smansmanquickconfigcommand\""
- Testwsmancommand
- SessionOption
- AuthentifizierungMechanismus
- Proxy Access Type
- Proxy Authentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd74af81c1cec7874ec0e881dbc236f5dd94d11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214039"
---
# <a name="managed-reference-for-winrm-windows-powershell-command-classes"></a>Verwaltete Referenz für WinRM Windows PowerShell-Befehlsklassen

In Windows-Remoteverwaltung 2,0 (WinRM) können Windows PowerShell-Cmdlets für die Systemverwaltung verwendet werden. Windows PowerShell-Cmdlets ermöglichen Administratoren das Konfigurieren von WinRM und das erhalten von Daten oder das Verwalten von Ressourcen.

Windows PowerShell-Cmdlets für WinRM bieten die gleiche Funktionalität wie das WinRM-Befehlszeilen-Hilfsprogramm. Windows PowerShell führt jedoch auch die folgenden Schritte aus:

-   Automatisiert WinRM-Aufgaben in erweiterbarer und Verwaltungs orientierter Skriptsprache.
-   Stellt ein einzelnes Tool für alle Verwaltungsaufgaben bereit.

Weitere Informationen finden Sie in der [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) .

## <a name="ws-management-windows-powershell-classes"></a>WS-Management Windows PowerShell-Klassen

**Namespace**: Microsoft. WSMAN. Management

**Assembly**: System. Management. Automation

Die folgenden WinRM-Befehls Klassen werden von Windows PowerShell implementiert. Diese Klassen sind nur aus Gründen der Vollständigkeit in diesem Software Development Kit (SDK) enthalten. Die Member dieser Klassen können nicht direkt verwendet werden und sollten nicht zum Ableiten anderer Klassen verwendet werden.



| Klasse                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Connectwsmancommand          | Stellt eine Verbindung mit dem WinRM-Dienst auf einem Remotecomputer her. <br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im Cmdlet " [Connect-WSMAN](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) ".<br/>                                                                                                                                                                                                                                                                                                                                              |
| Disablewsmankredsspcommand   | Deaktiviert die kredssp-Authentifizierung auf einem Client.<br/> Ausführliche Informationen zu den Parametern und Beispielen finden Sie im Cmdlet " [Deaktivierte wsmankredssp](/powershell/module/Microsoft.WsMan.Management/Disable-WSManCredSSP?view=powershell-5.1&preserve-view=true) ".<br/>                                                                                                                                                                                                                                                                                                                                           |
| Disconnectwsmancommand       | Trennt die Verbindung mit dem WinRM-Dienst auf einem Remote Computer. <br/> Unter dem [Disconnect-WSMAN-](/powershell/module/Microsoft.WsMan.Management/Disconnect-WSMan?view=powershell-5.1&preserve-view=true) Cmdlet finden Sie Beispiele und ausführliche Informationen zu den Parametern.<br/>                                                                                                                                                                                                                                                                                                                                      |
| Enablewsmankredsspcommand    | Aktiviert die kredssp-Authentifizierung auf dem Client.<br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im Cmdlet [enable-wsmankredssp](/powershell/module/Microsoft.WsMan.Management/Enable-WSManCredSSP?view=powershell-5.1&preserve-view=true) .<br/>                                                                                                                                                                                                                                                                                                                                               |
| Getwsmankredsspcommand       | Ruft die mit dem Client verbundene Konfiguration für den Client ab.<br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im Cmdlet " [Get-wsmankredssp](/powershell/module/Microsoft.WsMan.Management/Get-WSManCredSSP?view=powershell-5.1&preserve-view=true) ".<br/>                                                                                                                                                                                                                                                                                                                                         |
| Getwsmaninstancecommand      | Zeigt Verwaltungsinformationen für eine durch einen Ressourcen-URI angegebene Ressourceninstanz an.<br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im Cmdlet " [Get-wsmaninstance](/powershell/module/Microsoft.WsMan.Management/Get-WSManInstance?view=powershell-5.1&preserve-view=true) ".<br/>                                                                                                                                                                                                                                                                                                          |
| Invokewsmanaktionsbefehl     | Ruft eine Aktion für das Zielobjekt auf, das durch den Ressourcen-URI und die Selektoren angegeben wird. <br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im Cmdlet " [Aufruf-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) ".<br/>                                                                                                                                                                                                                                                                                                         |
| Newwsmaninstancecommand      | Erstellt eine neue Instanz einer Verwaltungsressource. <br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im Cmdlet " [New-wsmaninstance](/powershell/module/Microsoft.WsMan.Management/New-WSManInstance?view=powershell-5.1&preserve-view=true) ".<br/>                                                                                                                                                                                                                                                                                                                                             |
| Newwsmansessionoptioncommand | Erstellt eine WinRM-Sitzungs Option-Hash Tabelle, die als Eingabeparameter für die folgenden WSMAN-Cmdlets verwendet werden soll: " [Get-wsmaninstance](/powershell/module/Microsoft.WsMan.Management/Get-WSManInstance?view=powershell-5.1&preserve-view=true)", " [Set-wsmaninstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)", " [Aufruf-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)" und " [Connect-WSMAN](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true)". <br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie unter " [New-wsmansessionoption](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true) ".<br/> |
| Removewsmaninstancecommand   | Löscht eine Instanz einer Verwaltungsressource. <br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im Cmdlet " [Remove-wsmaninstance](/powershell/module/Microsoft.WsMan.Management/Remove-WSManInstance?view=powershell-5.1&preserve-view=true) ".<br/>                                                                                                                                                                                                                                                                                                                                                   |
| "Smansmaninstancecommand"      | Ändert die mit einer Ressource verknüpften Verwaltungsinformationen. <br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im Cmdlet " [Set-wsmaninstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) ".<br/>                                                                                                                                                                                                                                                                                                                                       |
| "Smansmanquickconfigcommand"   | Konfiguriert den lokalen Computer für die Remoteverwaltung. <br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im Cmdlet " [Set-wsmanquickconfig](/powershell/module/Microsoft.WsMan.Management/Set-WSManQuickConfig?view=powershell-5.1&preserve-view=true) ".<br/>                                                                                                                                                                                                                                                                                                                                      |
| Testwsmancommand             | Überprüft, ob der WinRM-Dienst auf einem lokalen oder Remotecomputer ausgeführt wird. <br/> Beispiele und ausführliche Informationen zu den Parametern finden Sie im Cmdlet " [Test-WSMAN]( /powershell/module/microsoft.wsman.management/test-wsman?view=powershell-7&preserve-view=true) ".<br/>                                                                                                                                                                                                                                                                                                                        |
| SessionOption                | Definiert eine Reihe von erweiterten Optionen für die WS-Management-Sitzung.<br/> Beispiele und ausführliche Informationen zu den möglichen Werten finden Sie im Cmdlet " [Connect-WSMAN](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) ".<br/>                                                                                                                                                                                                                                                                                                                             |



 

## <a name="ws-management-windows-powershell-enumerations"></a>WS-Management von Windows PowerShell-Enumerationen

Die folgenden Enumerationen werden von Windows PowerShell implementiert. Diese Enumerationen sind nur aus Gründen der Vollständigkeit in diesem Software Development Kit (SDK) enthalten.



| Enumeration             | Beschreibung                                                                                                                                                                                                                                   |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AuthentifizierungMechanismus | Gibt den Authentifizierungsmechanismus an, der auf dem Server verwendet werden soll. <br/> Beispiele und ausführliche Informationen zu den möglichen Werten finden Sie im Cmdlet " [Connect-WSMAN](/powershell/module/Microsoft.WsMan.Management/Connect-WSMan?view=powershell-5.1&preserve-view=true) ".<br/>      |
| Proxy Access Type         | Gibt den Mechanismus an, mit dem der Proxyserver gesucht wird.<br/> Beispiele und ausführliche Informationen zu den möglichen Werten finden Sie im Cmdlet " [New-wsmansessionoption](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true) ".<br/> |
| Proxy Authentifizierung     | Gibt die Authentifizierungsmethode an, die auf dem Proxy verwendet wird.<br/> Beispiele und ausführliche Informationen zu den möglichen Werten finden Sie im Cmdlet " [New-wsmansessionoption](/powershell/module/Microsoft.WsMan.Management/New-WSManSessionOption?view=powershell-5.1&preserve-view=true) ".<br/>      |



 

 

