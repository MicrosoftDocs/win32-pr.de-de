---
description: Zum Herstellen einer Verbindung mit einem WMI-Namespace auf einem Remotecomputer müssen Sie möglicherweise die Einstellungen für Windows-Firewall, Benutzerkontensteuerung (User Account Control, UAC), DCOM oder Common Information Model Object Manager (CIMOM) ändern.
ms.assetid: 028b3101-0945-4288-bf32-ef4ad12a55f9
ms.tgt_platform: multiple
title: Einrichten einer WMI-Remoteverbindung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b88aa453646e60bf17e31f1197d76506bb4f75453eb800dc0fa272946a3bf8df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117925702"
---
# <a name="setting-up-a-remote-wmi-connection"></a>Einrichten einer WMI-Remoteverbindung

Zum Herstellen einer Verbindung mit einem WMI-Namespace auf einem Remotecomputer müssen Sie möglicherweise die Einstellungen für [Windows-Firewall,](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11))Benutzerkontensteuerung [(User Account Control, UAC),](/previous-versions/aa905108(v=msdn.10))DCOM oder Common Information Model Object Manager (CIMOM) ändern.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Windows-Firewalleinstellungen](#windows-firewall-settings)
-   [Einstellungen der Benutzerkontensteuerung](#user-account-control-settings)
-   [DCOM-Einstellungen](#dcom-settings)
-   [CIMOM-Einstellungen](#cimom-settings)
-   [Zugehörige Themen](#related-topics)

## <a name="windows-firewall-settings"></a>Windows-Firewalleinstellungen

WMI-Einstellungen für Windows-Firewalleinstellungen ermöglichen nur WMI-Verbindungen und nicht auch andere DCOM-Anwendungen.

Eine Ausnahme muss in der Firewall für WMI auf dem Remotezielcomputer festgelegt werden. Die Ausnahme für WMI ermöglicht WMI das Empfangen von Remoteverbindungen und asynchronen Rückrufen Unsecapp.exe. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen Aufruf](setting-security-on-an-asynchronous-call.md)von .

Wenn eine Clientanwendung eine eigene Senke erstellt, muss diese Senke explizit den Firewallausnahmen hinzugefügt werden, damit Rückrufe erfolgreich ausgeführt werden können.

Die Ausnahme für WMI funktioniert auch, wenn WMI mit einem festen Port mithilfe des **Befehls winmgmt /standalonehost gestartet** wurde. Weitere Informationen finden Sie unter [Einrichten eines festen Ports für WMI.](setting-up-a-fixed-port-for-wmi.md)

Sie können WMI-Datenverkehr über die Windows-Firewall-Benutzeroberfläche aktivieren oder deaktivieren.

**So aktivieren oder deaktivieren Sie WMI-Datenverkehr über die Firewallbenutzeroberfläche**

1.  Klicken Sie **Systemsteuerung** auf **Sicherheit** und dann auf **Windows-Firewall**.
2.  Klicken **Sie auf Einstellungen** ändern und dann auf die Registerkarte **Ausnahmen.**
3.  Aktivieren Sie im Fenster Ausnahmen das Kontrollkästchen für Windows-Verwaltungsinstrumentation **(WMI),** um WMI-Datenverkehr über die Firewall zu aktivieren. Deaktivieren Sie das Kontrollkästchen, um WMI-Datenverkehr zu deaktivieren.

Sie können WMI-Datenverkehr über die Firewall an der Eingabeaufforderung aktivieren oder deaktivieren.

**So aktivieren oder deaktivieren Sie WMI-Datenverkehr an der Eingabeaufforderung mithilfe der WMI-Regelgruppe**

-   Verwenden Sie die folgenden Befehle an einer Eingabeaufforderung. Geben Sie Folgendes ein, um WMI-Datenverkehr über die Firewall zu aktivieren.

    **netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=yes**

    Geben Sie den folgenden Befehl ein, um den WMI-Datenverkehr durch die Firewall zu deaktivieren.

    **netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=no**

Anstatt den einzelnen WMI-Regelgruppenbefehl zu verwenden, können Sie auch einzelne Befehle für jeden DCOM-, WMI-Dienst und jede Senke verwenden.

**So aktivieren Sie WMI-Datenverkehr mit separaten Regeln für DCOM, WMI, Rückrufsenke und ausgehende Verbindungen**

1.  Verwenden Sie den folgenden Befehl, um eine Firewallausnahme für DCOM-Port 135 zu erstellen.

    **netsh advfirewall firewall add rule dir=in name="DCOM" program=%systemroot% \\ system32 \\svchost.exe service=rpcss action=allow protocol=TCP localport=135**

2.  Verwenden Sie den folgenden Befehl, um eine Firewallausnahme für den WMI-Dienst zu erstellen.

    **netsh advfirewall firewall add rule dir=in name ="WMI" program=%systemroot% \\ system32 \\svchost.exe service=winmgmt action = allow protocol=TCP localport=any**

3.  Verwenden Sie den folgenden Befehl, um eine Firewallausnahme für die Senke zu erstellen, die Rückrufe von einem Remotecomputer empfängt.

    **netsh advfirewall firewall add rule dir=in name ="UnsecApp" program=%systemroot% \\ system32 \\ wbem \\unsecapp.exe action=allow**

4.  Verwenden Sie den folgenden Befehl, um eine Firewallausnahme für ausgehende Verbindungen mit einem Remotecomputer herzustellen, mit dem der lokale Computer asynchron kommuniziert.

    **netsh advfirewall firewall add rule dir=out name ="WMI \_ OUT" program=%systemroot% \\ system32 \\svchost.exe service=winmgmt action=allow protocol=TCP localport=any**

Verwenden Sie die folgenden Befehle, um die Firewallausnahmen separat zu deaktivieren.

**So deaktivieren Sie WMI-Datenverkehr mit separaten Regeln für DCOM, WMI, Rückrufsenke und ausgehende Verbindungen**

1.  So deaktivieren Sie die DCOM-Ausnahme.

    **netsh advfirewall firewall delete rule name="DCOM"**

2.  So deaktivieren Sie die WMI-Dienstausnahme.

    **netsh advfirewall firewall delete rule name="WMI"**

3.  So deaktivieren Sie die Senkenausnahme.

    **netsh advfirewall firewall delete rule name="UnsecApp"**

4.  So deaktivieren Sie die ausgehende Ausnahme.

    **netsh advfirewall firewall delete rule name="WMI \_ OUT"**

## <a name="user-account-control-settings"></a>Einstellungen der Benutzerkontensteuerung

Die Filterung von Zugriffstoken der Benutzerkontensteuerung (User Account Control, UAC) kann sich darauf auswirken, welche Vorgänge in WMI-Namespaces zulässig sind oder welche Daten zurückgegeben werden. Unter UAC werden alle Konten in der lokalen Administratorgruppe mit einem Standardbenutzerzugriffstoken [*ausgeführt,*](/windows/desktop/SecGloss/a-gly)das auch als UAC-Zugriffstokenfilterung bezeichnet wird. Ein Administratorkonto kann ein Skript mit erhöhten Rechten ausführen– "Als Administrator ausführen".

Wenn Sie keine Verbindung mit dem integrierten Administratorkonto herstellen, wirkt sich die UAC auf Verbindungen mit einem Remotecomputer unterschiedlich aus, je nachdem, ob sich die beiden Computer in einer Domäne oder Arbeitsgruppe befinden. Weitere Informationen zu UAC und Remoteverbindungen finden Sie unter [Benutzerkontensteuerung und WMI.](user-account-control-and-wmi.md)

## <a name="dcom-settings"></a>DCOM-Einstellungen

Weitere Informationen zu DCOM-Einstellungen finden Sie unter [Sichern einer WMI-Remoteverbindung.](securing-a-remote-wmi-connection.md) UAC wirkt sich jedoch auf Verbindungen für Benutzerkonten ohne Domänen aus. Wenn Sie eine Verbindung mit einem Remotecomputer herstellen, indem Sie ein Nichtdomänenbenutzerkonto verwenden, das in der lokalen Administratorgruppe des Remotecomputers enthalten ist, müssen Sie dem Konto explizit DCOM-Remotezugriffs-, Aktivierungs- und Startrechte gewähren.

## <a name="cimom-settings"></a>CIMOM-Einstellungen

Die CIMOM-Einstellungen müssen aktualisiert werden, wenn die Remoteverbindung zwischen Computern besteht, die keine Vertrauensstellung haben. Andernfalls kann eine asynchrone Verbindung nicht hergestellt werden. Diese Einstellung sollte nicht für Computer in derselben Domäne oder in vertrauenswürdigen Domänen geändert werden.

Der folgende Registrierungseintrag muss geändert werden, um anonyme Rückrufe zu ermöglichen:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **AllowAnonymousCallback**<dl> <dt>

               Data type
</dt> <dd>               REG \_ DWORD</dd> </dl>

Wenn der **AllowAnonymousCallback-Wert** auf 0 festgelegt ist, verhindert der WMI-Dienst anonyme Rückrufe an den Client. Wenn der Wert auf 1 festgelegt ist, lässt der WMI-Dienst anonyme Rückrufe an den Client zu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Herstellen einer Verbindung mit WMI auf einem Remotecomputer](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
