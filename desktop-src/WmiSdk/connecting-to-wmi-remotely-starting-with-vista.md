---
description: Zum Herstellen einer Verbindung mit einem WMI-Namespace auf einem Remote Computer müssen Sie möglicherweise die Einstellungen für die Windows-Firewall, die Benutzerkontensteuerung (User Account Control, UAC), DCOM oder den Common Information Model Objekt-Manager (CIMOM) ändern.
ms.assetid: 028b3101-0945-4288-bf32-ef4ad12a55f9
ms.tgt_platform: multiple
title: Einrichten einer Remote-WMI-Verbindung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6ee254e12ecd806cd286d4a55746e203a3136b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528616"
---
# <a name="setting-up-a-remote-wmi-connection"></a>Einrichten einer Remote-WMI-Verbindung

Zum Herstellen einer Verbindung mit einem WMI-Namespace auf einem Remote Computer müssen Sie möglicherweise die Einstellungen für die [Windows-Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), die [Benutzerkontensteuerung (User Account Control, UAC)](/previous-versions/aa905108(v=msdn.10)), DCOM oder den Common Information Model Objekt-Manager (CIMOM) ändern.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Windows-Firewall-Einstellungen](#windows-firewall-settings)
-   [Einstellungen der Benutzerkontensteuerung](#user-account-control-settings)
-   [DCOM-Einstellungen](#dcom-settings)
-   [CIMOM-Einstellungen](#cimom-settings)
-   [Zugehörige Themen](#related-topics)

## <a name="windows-firewall-settings"></a>Windows-Firewalleinstellungen

WMI-Einstellungen für Windows-Firewall-Einstellungen ermöglichen nur WMI-Verbindungen und keine anderen DCOM-Anwendungen.

Eine Ausnahme muss in der Firewall für WMI auf dem Remote Zielcomputer festgelegt werden. Die Ausnahme für WMI ermöglicht WMI, Remote Verbindungen und asynchrone Rückrufe zu Unsecapp.exe zu empfangen. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.

Wenn eine Client Anwendung eine eigene Senke erstellt, muss diese Senke explizit den Firewallausnahmen hinzugefügt werden, damit Rückrufe erfolgreich ausgeführt werden können.

Die Ausnahme für WMI funktioniert auch, wenn WMI mit einem Fixed-Port mit dem Befehl **winmgmt/standalonehost** gestartet wurde. Weitere Informationen finden Sie unter [Einrichten eines Fixed-Ports für WMI](setting-up-a-fixed-port-for-wmi.md).

Sie können den WMI-Datenverkehr über die Benutzeroberfläche der Windows-Firewall aktivieren oder deaktivieren.

**So aktivieren oder deaktivieren Sie WMI-Datenverkehr über die Firewall**

1.  Klicken Sie in der **Systemsteuerung** auf **Sicherheit** und dann auf **Windows-Firewall**.
2.  Klicken Sie auf **Einstellungen ändern** und dann auf die Registerkarte **Ausnahmen** .
3.  Aktivieren Sie im Fenster Ausnahmen das Kontrollkästchen für **Windows-Verwaltungsinstrumentation (WMI)** , um den WMI-Datenverkehr über die Firewall zu aktivieren. Deaktivieren Sie das Kontrollkästchen, um den WMI-Datenverkehr zu deaktivieren.

Sie können den WMI-Datenverkehr über die Firewall an der Eingabeaufforderung aktivieren oder deaktivieren.

**So aktivieren oder deaktivieren Sie WMI-Datenverkehr an der Eingabeaufforderung mithilfe der WMI-Regelgruppe**

-   Verwenden Sie die folgenden Befehle an einer Eingabeaufforderung. Geben Sie Folgendes ein, um den WMI-Datenverkehr über die Firewall zu aktivieren.

    **netsh advfirewall firewall set rule Group = "Windows Management Instrumentation (WMI)" New enable = yes**

    Geben Sie folgenden Befehl ein, um den WMI-Datenverkehr über die Firewall zu deaktivieren.

    **netsh advfirewall firewall set rule Group = "Windows Management Instrumentation (WMI)" New enable = no**

Anstatt den einzelnen WMI-Regel Gruppen Befehl zu verwenden, können Sie auch einzelne Befehle für jeden DCOM-, WMI-Dienst und jede Senke verwenden.

**So aktivieren Sie WMI-Datenverkehr mit separaten Regeln für DCOM, WMI, Rückruf Senke und ausgehende Verbindungen**

1.  Verwenden Sie den folgenden Befehl, um eine Firewallausnahme für den DCOM-Port 135 einzurichten.

    **netsh advfirewall Firewall Add Rule dir = in Name = "DCOM" Program =% systemroot% \\ system32 \\svchost.exe Service = RPCSS Action = Allow Protocol = TCP localport = 135**

2.  Verwenden Sie den folgenden Befehl, um eine Firewallausnahme für den WMI-Dienst einzurichten.

    **netsh advfirewall Firewall Add Rule dir = in Name = "WMI" Program =% systemroot% \\ system32 \\svchost.exe Service = WinMgmt Action = Allow Protocol = TCP localport = any**

3.  Verwenden Sie den folgenden Befehl, um eine Firewallausnahme für die Senke zu erstellen, die Rückrufe von einem Remote Computer empfängt.

    **netsh advfirewall Firewall Add Rule dir = in Name = "unabcapp" Program =% systemroot% \\ system32 \\ WBEM \\unsecapp.exe Action = Allow**

4.  Verwenden Sie den folgenden Befehl, um eine Firewallausnahme für ausgehende Verbindungen mit einem Remote Computer einzurichten, mit dem der lokale Computer asynchron kommuniziert.

    **netsh advfirewall Firewall Add Rule dir = out Name = "WMI \_ out" Program =% systemroot% \\ system32 \\svchost.exe Service = WinMgmt Action = Allow Protocol = TCP localport = any**

Verwenden Sie die folgenden Befehle, um die Firewallausnahmen separat zu deaktivieren.

**So deaktivieren Sie WMI-Datenverkehr mit separaten Regeln für DCOM, WMI, Rückruf Senke und ausgehende Verbindungen**

1.  Zum Deaktivieren der DCOM-Ausnahme.

    **netsh advfirewall Firewall Delete Rule Name = "DCOM"**

2.  Zum Deaktivieren der Ausnahme des WMI-Dienstanbieter.

    **netsh advfirewall Firewall Delete Rule Name = "WMI"**

3.  , Wenn die Senke Ausnahme deaktiviert werden soll.

    **netsh advfirewall Firewall Delete Rule Name = "unabcapp"**

4.  , Wenn die ausgehende Ausnahme deaktiviert werden soll.

    **netsh advfirewall Firewall Delete Rule Name = "WMI \_ out"**

## <a name="user-account-control-settings"></a>Einstellungen der Benutzerkontensteuerung

Die Benutzerkontensteuerung (User Account Control, UAC)-Zugriffs Token-Filterung kann beeinflussen, welche Vorgänge in WMI-Namespaces zulässig sind oder welche Daten zurückgegeben werden. Unter UAC werden alle Konten in der lokalen Administratoren Gruppe mit einem Standardbenutzer [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly)ausgeführt, das auch als UAC-Zugriffs Token-Filterung bezeichnet wird. Ein Administrator Konto kann ein Skript mit erhöhten Berechtigungen ausführen – "als Administrator ausführen".

Wenn Sie keine Verbindung mit dem integrierten Administrator Konto herstellen, wirkt sich UAC anders auf die Verbindungen mit einem Remote Computer aus, je nachdem, ob sich die beiden Computer in einer Domäne oder Arbeitsgruppe befinden. Weitere Informationen zu UAC und Remote Verbindungen finden Sie unter [Benutzerkontensteuerung und WMI](user-account-control-and-wmi.md).

## <a name="dcom-settings"></a>DCOM-Einstellungen

Weitere Informationen zu DCOM-Einstellungen finden Sie unter [Sichern einer Remote-WMI-Verbindung](securing-a-remote-wmi-connection.md). Die UAC wirkt sich jedoch auf Verbindungen für nicht-Domänen Benutzerkonten aus. Wenn Sie über ein nicht-Domänen Benutzerkonto, das in der lokalen Administratoren Gruppe des Remote Computers enthalten ist, eine Verbindung mit einem Remote Computer herstellen, müssen Sie dem Konto explizit Remote-DCOM-Zugriff,-Aktivierung und-Startrechte erteilen.

## <a name="cimom-settings"></a>CIMOM-Einstellungen

Die CIMOM-Einstellungen müssen aktualisiert werden, wenn die Remote Verbindung zwischen Computern besteht, die keine Vertrauensstellung haben. Andernfalls tritt bei einer asynchronen Verbindung ein Fehler auf. Diese Einstellung sollte für Computer in derselben Domäne oder in vertrauenswürdigen Domänen nicht geändert werden.

Der folgende Registrierungs Eintrag muss geändert werden, um anonyme Rückrufe zuzulassen:

**HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Zuteilungs Nummer**<dl> <dt>

               Data type
</dt> <dd>               REG \_ DWORD</dd> </dl>

Wenn der Wert von "Zuordnungen" auf "0" festgelegt ist, verhindert der WMI-Dienst anonyme **Rückrufe** an den Client. Wenn der Wert auf 1 festgelegt ist, lässt der WMI-Dienst anonyme Rückrufe an den Client zu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
