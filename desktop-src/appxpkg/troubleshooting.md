---
title: Problembehandlung beim Packen, Bereitstellen und Abfragen von Windows-Apps
description: Verwenden Sie diese Vorschläge, um Probleme zu beheben, die beim Packen, bereitstellen oder Abfragen eines App-Pakets auftreten.
ms.assetid: 38E327C6-0345-4FA6-BCDB-5FA2FCD421FB
ms.topic: article
ms.date: 02/20/2020
manager: dcscontentpm
ms.custom:
- CI 111497
- CSSTroubleshooting
- contperf-fy21q2
ms.openlocfilehash: a2ee7c28e7de2d616bd01e9b5cae0de3c325caf4
ms.sourcegitcommit: 80198645ddacc3c12c72f3814b71ade0f415e705
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/25/2021
ms.locfileid: "106372785"
---
# <a name="troubleshooting-packaging-deployment-and-query-of-windows-apps"></a>Problembehandlung beim Packen, Bereitstellen und Abfragen von Windows-Apps

Verwenden Sie diese Vorschläge, um Probleme zu beheben, die beim Packen, bereitstellen oder Abfragen eines Windows-App-Pakets (. msix/. AppX) als Entwickler auftreten.

> [!NOTE]
> Dieser Artikel richtet sich an Entwickler. Wenn Sie kein Entwickler sind und Hilfe bei der Installation einer Windows-App suchen, finden Sie weitere Informationen unter [Windows-Support](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10).

## <a name="get-diagnostic-information"></a>Diagnoseinformationen erhalten

Wenn eine API fehlschlägt, wird ein Fehlercode zurückgegeben, der das Problem beschreibt. Wenn der Fehlercode nicht genügend Informationen liefert, finden Sie weitere Diagnoseinformationen in den detaillierten Ereignisprotokollen.

Führen Sie die folgenden Schritte aus, um mit **Ereignisanzeige** auf die Paket-und Bereitstellungs Ereignisprotokolle zuzugreifen:

1. Führen Sie einen der folgenden Schritte aus:

    * Klicken Sie im Menü Windows auf **Start** , geben Sie **Ereignisanzeige** ein, und **drücken Sie die EINGABETASTE**.
    * Führen Sie **eventvwr. msc** aus.

2. Erweitern Sie auf der linken Seite **Ereignisanzeige (local)**  >  **Anwendungs-und Dienst Protokolle**  >  **Microsoft**  >  **Windows**.
3. Überprüfen Sie die verfügbaren Protokolle in den folgenden Kategorien:

    * **Appxpackagingom**  >  **Microsoft-Windows-appxpackaging/Operational**
    * **Appxdeployment-Server**  >  **Microsoft-Windows-appxdeploymentserver/Operational**

Sehen Sie sich zunächst die Protokolle unter **appxdeployment-Server** an. Wenn der Fehler durch **0x80073cf0** oder **ERROR_INSTALL_OPEN_PACKAGE_FAILED** verursacht wurde, sind möglicherweise weitere Details in den **appxpackagingom** -Protokollen vorhanden.

Sie können auch den Befehl [Get-appxlog](/powershell/module/appx/get-appxlog) in PowerShell verwenden, um die ersten protokollierten Ereignisse zu erhalten. Im folgenden Beispiel werden die dem letzten Bereitstellungs Vorgang zugeordneten Protokolle angezeigt.

```PowerShell
Get-Appxlog
```

Im folgenden Beispiel werden die Protokolle angezeigt, die dem letzten Bereitstellungs Vorgang in einer interaktiven Tabelle in einem separaten Fenster zugeordnet sind.

```PowerShell
Get-Appxlog | Out-GridView
```

## <a name="common-error-codes"></a>Häufige Fehlermeldungen

In dieser Tabelle sind einige der häufigsten Fehlercodes aufgeführt. Wenn Sie bei einem dieser Fehler weitere Hilfe benötigen oder wenn Sie einen Fehlercode finden, der nicht in dieser Liste enthalten ist, finden Sie weitere Informationen unter [zusätzliche Hilfe Optionen](#get-additional-help).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Fehlercode</th>
<th>Wert</th>
<th>Beschreibung und mögliche Ursachen</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td><strong>E_FILENOTFOUND</strong></td>
<td>0x80070002</td>
<td>Datei oder Pfad nicht gefunden. Dies kann während einer com-Export der Typbibliothek-Validierung vorkommen, dass der Pfad für das Verzeichnis tatsächlich in Ihrem msix-Paket vorhanden ist.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_BAD_FORMAT</strong></td>
<td>0x8007000B</td>
<td>Das Paket ist nicht ordnungsgemäß formatiert und muss neu erstellt oder neu signiert werden.<br/> Dieser Fehler kann auftreten, wenn der Antragsteller Name des Signatur Zertifikats und der Name des AppxManifest.xml Verlegers nicht übereinstimmen.<br/> Weitere Informationen finden <a href="how-to-sign-a-package-using-signtool.md">Sie unter Signieren eines App-Pakets mit SignTool</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>E_INVALIDARG</strong></td>
<td>0x80070057</td>
<td>Mindestens ein Argument ist ungültig. Wenn Sie das AppXDeployment-Server-Ereignisprotokoll überprüfen und folgendes Ereignis sehen: "beim Installieren des Pakets konnte die Windows. repositoryExtension-Erweiterung aufgrund des folgenden Fehlers nicht registriert werden: der Parameter ist falsch." <br/> Dieser Fehler wird möglicherweise angezeigt, wenn die Elemente Display Name oder Description des Manifests Zeichen enthalten, die von der Windows-Firewall nicht zugelassen werden. nämlich |  und alle, da Windows das appcontainer-Profil für das Paket nicht erstellen konnte. Entfernen Sie diese Zeichen aus dem Manifest, und versuchen Sie, das Paket zu installieren. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OPEN_</strong><br/> <strong>PACKAGE_FAILED</strong><br/></td>
<td>0x80073CF0</td>
<td>Das Paket konnte nicht geöffnet werden.<br/> Mögliche Ursachen:<br/>
<ul>
<li>Das Paket ist nicht signiert.</li>
<li>Der Herausgeber Name stimmt nicht mit dem Signaturzertifikat Betreff.</li>
<li>Das file://-Präfix fehlt, oder das Paket wurde am angegebenen Speicherort nicht gefunden.</li>
</ul>
Weitere Informationen finden Sie im Ereignisprotokoll " <strong>appxpackagingom</strong> ".<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_PACKAGE_</strong><br/> <strong>NOT_FOUND</strong><br/></td>
<td>0x80073cf1</td>
<td>Das Paket wurde nicht gefunden.<br/> Dieser Fehler wird möglicherweise angezeigt, wenn Sie ein Paket entfernen, das nicht für den aktuellen Benutzer installiert ist.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_INVALID_</strong><br/> <strong>Paketen</strong><br/></td>
<td>0x80073cf2</td>
<td>Die Paketdaten sind ungültig.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_RESOLVE_</strong><br/> <strong>DEPENDENCY_FAILED</strong><br/></td>
<td>0x80073CF3</td>
<td>Fehler bei Updates, Abhängigkeiten oder Konfliktüberprüfung des Pakets.<br/> Mögliche Ursachen:<br/>
<ul>
<li>Das eingehende Paket ist mit einem installierten Paket nicht vereinbar.</li>
<li>Eine angegebene Paketabhängigkeit wurde nicht gefunden.</li>
<li>Das Paket unterstützt nicht die richtige Prozessorarchitektur.</li>
</ul>
Überprüfen Sie das Ereignisprotokoll " <strong>appxdeployment-Server</strong> ", um weitere Informationen zu erhalten.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OUT_</strong><br/> <strong>OF_DISK_SPACE</strong><br/></td>
<td>0x80073cf4</td>
<td>Auf Ihrem Computer ist nicht genügend Speicherplatz vorhanden. Freigeben Sie Speicherplatz, und versuchen Sie es noch mal.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_NETWORK_</strong><br/> <strong>Fehler</strong><br/></td>
<td>0x80073cf5</td>
<td>Das Paket kann nicht heruntergeladen werden.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>REGISTRATION_FAILURE</strong><br/></td>
<td>0x80073cf6</td>
<td>Das Paket kann nicht registriert werden.<br/> Weitere Informationen finden Sie im Ereignisprotokoll " <strong>appxdeployment-Server</strong> ".<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>DEREGISTRATION_EFAILURE</strong><br/></td>
<td>0x80073cf7</td>
<td>Die Registrierung des Pakets kann nicht aufgehoben werden.<br/> Dieser Fehler kann beim Entfernen eines Pakets auftreten.<br/> Weitere Informationen finden Sie im Ereignisprotokoll " <strong>appxdeployment-Server</strong> ".<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_CANCEL</strong></td>
<td>0x80073cf8</td>
<td>Der Benutzer hat die Installations Anforderung abgebrochen.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_FAILED</strong></td>
<td>0x80073cf9</td>
<td>Fehler beim Installieren des Pakets. Wenden Sie sich an den Softwarehersteller.<br/> Weitere Informationen finden Sie im Ereignisprotokoll " <strong>appxdeployment-Server</strong> ".<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_REMOVE_FAILED</strong></td>
<td>0x80073cfa</td>
<td>Fehler beim Entfernen des Pakets.<br/> Dieser Fehler tritt möglicherweise für Fehler auf, die während der Paket Deinstallation auftreten.<br/> Weitere Informationen finden Sie unter <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>removepackageasync</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_</strong><br/> <strong>ALREADY_EXISTS</strong><br/></td>
<td>0x80073CFB</td>
<td>Das bereitgestellte Paket ist bereits installiert, und eine erneute Installation des Pakets wird blockiert. <br/> Dieser Fehler wird möglicherweise angezeigt, wenn Sie ein Paket installieren, das nicht bitweise mit dem bereits installierten Paket identisch ist. Beachten Sie, dass die digitale Signatur auch Teil des Pakets ist. Wenn ein Paket neu erstellt oder zurückgetreten wird, ist es daher nicht mehr bitweise identisch mit dem zuvor installierten Paket. Es gibt zwei Möglichkeiten, diesen Fehler zu beheben: (1) Inkrementieren Sie die Versionsnummer der APP, erstellen Sie das Paket neu, und setzen Sie es ab (2) entfernen Sie das alte Paket für jeden Benutzer im System, bevor Sie das neue Paket installieren. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_NEEDS_REMEDIATION</strong></td>
<td>0x80073cfc</td>
<td>Die APP kann nicht gestartet werden. Versuchen Sie, die APP erneut zu installieren.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>PREREQUISITE_FAILED</strong><br/></td>
<td>0x80073cfd</td>
<td>Eine angegebene Installations Voraussetzung konnte nicht erfüllt werden.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_</strong><br/> <strong>REPOSITORY_CORRUPTED</strong><br/></td>
<td>0x80073cfe</td>
<td>Das Paketrepository ist beschädigt.<br/> Dieser Fehler kann angezeigt werden, wenn der Ordner, auf den dieser Registrierungsschlüssel verweist, nicht vorhanden oder beschädigt ist: <br/> <strong>HKLM\Software\Microsoft\Windows</strong><br/> <strong>Currentversion\appx\packagerepositorienroot</strong><br/> Aktualisieren Sie Ihren PC, um diesen Status wiederherzustellen.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>POLICY_FAILURE</strong><br/></td>
<td>0x80073CFF</td>
<td>Zum Installieren dieser APP benötigen Sie eine Entwicklerlizenz oder ein Sideload-fähiges System. <br/> Dieser Fehler kann auftreten, wenn das Paket nicht eine der folgenden Anforderungen erfüllt:<br/>
<ul>
<li>Die APP wird mit F5 in Visual Studio auf einem Computer mit einer Windows-Entwicklerlizenz bereitgestellt.</li>
<li>Das Paket wird mit einer Microsoft-Signatur signiert und als Teil von Windows oder im Microsoft Store bereitgestellt.</li>
<li>Das Paket wird mit einer vertrauenswürdigen Signatur signiert und auf einem Computer installiert, auf dem eine Entwicklerlizenz, ein in die Domäne eingebundener Computer mit der Richtlinie "zukerwallvertrauensatpps" aktiviert ist, oder ein Computer mit einer Windows-Sideload-Lizenz mit aktivierter Richtlinie "Zuordners"</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_UPDATING</strong></td>
<td>0x80073d00</td>
<td>Die APP kann nicht gestartet werden, da Sie zurzeit aktualisiert wird.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_</strong><br/> <strong>BLOCKED_BY_POLICY</strong><br/></td>
<td>0x80073d01</td>
<td>Der Paket Bereitstellungs Vorgang wird durch die Richtlinie blockiert. Wenden Sie sich an Ihren Systemadministrator.<br/> Mögliche Ursachen:<br/>
<ul>
<li>Die Paket Bereitstellung wird durch Anwendungs Steuerungs Richtlinien blockiert.</li>
<li>Die Paket Bereitstellung wird durch die &quot; Richtlinie Bereitstellung von Vorgängen in speziellen Profilen zulassen blockiert &quot; .</li>
</ul>
Einer der möglichen Gründe ist die Notwendigkeit eines roamingprofils. Informationen zum Einrichten Roamingbenutzerprofile für Benutzerkonten finden Sie unter Bereitstellen von <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">Roamingbenutzerprofilen</a>. Wenn auf Ihrem System keine Richtlinien konfiguriert sind und dieser Fehler weiterhin angezeigt wird, sind Sie möglicherweise mit einem temporären Profil angemeldet. Melden Sie sich ab, und melden Sie sich erneut an. Wiederholen Sie dann den Vorgang.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGES_IN_USE</strong></td>
<td>0x80073d02</td>
<td>Das Paket konnte nicht installiert werden, da die von ihm modifizierenden Ressourcen zurzeit verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_RECOVERY_</strong><br/> <strong>FILE_CORRUPT</strong><br/></td>
<td>0x80073d03</td>
<td>Das Paket konnte nicht wieder hergestellt werden, da für die Wiederherstellung erforderliche Daten beschädigt sind.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INVALID_</strong><br/> <strong>STAGED_SIGNATURE</strong><br/></td>
<td>0x80073d04</td>
<td>Die Signatur ist ungültig. Zum Registrieren im Entwicklermodus müssen appxsignature. P7X "und AppxBlockMap.xml gültig sein oder nicht vorhanden sein.<br/> Wenn Sie ein Entwickler sind, der mit Visual Studio F5 verwendet, stellen Sie sicher, dass Ihr erstelltes Projektverzeichnis keine Signatur-oder Blockierungs Dateien aus früheren Versionen des Pakets enthält.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DELETING_EXISTING_</strong><br/> <strong>APPLICATIONDATA_STORE_FAILED</strong><br/></td>
<td>0x80073d05</td>
<td>Beim Löschen der bereits vorhandenen Anwendungsdaten des Pakets ist ein Fehler aufgetreten.<br/> Dieser Fehler kann angezeigt werden, wenn der <a href="/previous-versions/hh441475(v=vs.110)">Simulator</a> ausgeführt wird. Schließen Sie den Simulator. Dieser Fehler kann auch ausgegeben werden, wenn Dateien in den App-Daten geöffnet sind (wenn Sie z. b. eine Protokolldatei in einem Text-Editor geöffnet haben).<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>PACKAGE_DOWNGRADE</strong><br/></td>
<td>0x80073d06</td>
<td>Das Paket konnte nicht installiert werden, da bereits eine höhere Version dieses Pakets installiert ist.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SYSTEM_</strong><br/> <strong>NEEDS_REMEDIATION</strong><br/></td>
<td>0x80073d07</td>
<td>Ein Fehler in einer System Binärdatei wurde erkannt. Versuchen Sie, den PC zu aktualisieren, um das Problem zu beheben. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPX_INTEGRITY_</strong><br/> <strong>FAILURE_EXTERNAL</strong><br/></td>
<td>0x80073d08</td>
<td>Auf dem System wurde eine beschädigte nicht-Windows-Binärdatei erkannt. <br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_RESILIENCY_</strong><br/> <strong>FILE_CORRUPT</strong><br/></td>
<td>0x80073d09</td>
<td>Der Vorgang konnte nicht fortgesetzt werden, da für die Wiederherstellung erforderliche Daten beschädigt sind. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_FIREWALL_</strong><br/> <strong>SERVICE_NOT_RUNNING</strong><br/></td>
<td>0x80073d0a</td>
<td>Das Paket konnte nicht installiert werden, da der Windows-Firewall-Dienst nicht ausgeführt wird. Aktivieren Sie den Windows-Firewall-Dienst, und versuchen Sie es erneut<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_MOVE_FAILED</strong></td>
<td>0x80073d0b</td>
<td>Fehler beim Verschieben des Pakets.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>NOT_EMPTY</strong><br/></td>
<td>0x80073d0c</td>
<td>Der Bereitstellungs Vorgang ist fehlgeschlagen, da das Volume nicht leer ist.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>Aufzu</strong><br/></td>
<td>0x80073d0d</td>
<td>Fehler beim Bereitstellungs Vorgang, weil das Volume offline ist. Bei einem Paket Update verweist das Volume auf das installierte Volume aller Paketversionen.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>Kork</strong><br/></td>
<td>0x80073d0e</td>
<td>Der Bereitstellungs Vorgang ist fehlgeschlagen, da das angegebene Volume beschädigt ist.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_NEEDS_REGISTRATION</strong><br/> <strong></strong><br/></td>
<td>0x80073d0f</td>
<td>Der Bereitstellungs Vorgang ist fehlgeschlagen, da die angegebene Anwendung zuerst registriert werden muss.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_WRONG_</strong><br/> <strong>PROCESSOR_ARCHITECTURE</strong><br/></td>
<td>0x80073d10</td>
<td>Der Bereitstellungs Vorgang ist fehlgeschlagen, weil das Paket die falsche Prozessorarchitektur als Ziel hat.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEV_SIDELOAD_</strong><br/> <strong>LIMIT_EXCEEDED</strong><br/></td>
<td>0x80073d11</td>
<td>Sie haben die maximal zulässige Anzahl von Entwicklern, die auf diesem Gerät zulässig sind, erreicht. Deinstallieren Sie ein Sideload-Paket, und versuchen Sie es erneut.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_</strong><br/> <strong>MAIN_PACKAGE</strong><br/></td>
<td>0x80073d12</td>
<td>Zum Installieren dieses optionalen Pakets ist ein Haupt-App-Paket erforderlich. Installieren Sie zuerst das Hauptpaket, und wiederholen Sie den Vorgang.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_NOT_</strong><br/> <strong>SUPPORTED_ON_FILESYSTEM</strong><br/></td>
<td>0x80073d13</td>
<td>Dieser APP-Pakettyp wird in diesem Dateisystem nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_MOVE_</strong><br/> <strong>BLOCKED_BY_STREAMING</strong><br/></td>
<td>0x80073d14</td>
<td>Der paketverschiebungs Vorgang wird blockiert, bis die Anwendung das Streaming abgeschlossen hat.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_APPLICATIONID_</strong><br/> <strong>NOT_UNIQUE</strong><br/></td>
<td>0x80073d15</td>
<td>Ein Haupt-oder ein anderes optionales App-Paket verfügt über dieselbe Anwendungs-ID wie dieses optionale Paket. Ändern Sie die Anwendungs-ID für das optionale Paket, um Konflikte zu vermeiden.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_STAGING_</strong><br/> <strong>ONHOLD</strong><br/></td>
<td>0x80073d16</td>
<td>Diese stagingsitzung wurde gespeichert, damit ein anderer stagingvorgang priorisiert werden kann.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_INVALID_</strong><br/> <strong>RELATED_SET_UPDATE</strong><br/></td>
<td>0x80073d17</td>
<td>Ein zugehöriger Satz kann nicht aktualisiert werden, da der aktualisierte Satz ungültig ist. Alle Pakete in der zugehörigen Gruppe müssen gleichzeitig aktualisiert werden.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br/></td>
<td>0x80073d18</td>
<td>Ein optionales Paket mit einem FullTrust-Einstiegspunkt erfordert, dass das Hauptpaket über die Funktion " <strong>runfulltrust</strong> " verfügt.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_USER_LOG_OFF</strong><br/></td>
<td>0x80073d19</td>
<td>Ein Fehler ist aufgetreten, da ein Benutzer abgemeldet wurde.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PROVISION_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_PROVISIONED</strong><br/></td>
<td>0x80073d1a</td>
<td>Für eine optionale Paket Bereitstellung muss das Abhängigkeits Hauptpaket ebenfalls bereitgestellt werden.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGES_REPUTATION_</strong><br/> <strong>CHECK_FAILED</strong><br/></td>
<td>0x80073d1b</td>
<td>Fehler bei der <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">Überprüfung des SmartScreen-Rufs</a>durch die Pakete.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGES_REPUTATION_</strong><br/> <strong>CHECK_TIMEDOUT</strong><br/></td>
<td>0x80073d1c</td>
<td>Timeout beim <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">Überprüfen der SmartScreen-Ruf</a> .<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_OPTION_</strong><br/> <strong>NOT_SUPPORTED</strong><br/></td>
<td>0x80073d1d</td>
<td>Die aktuelle Bereitstellungs Option wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPINSTALLER_</strong><br/> <strong>ACTIVATION_BLOCKED</strong><br/></td>
<td>0x80073d1e</td>
<td>Die Aktivierung wird aufgrund der appinstaller-Aktualisierungs Einstellungen für diese APP blockiert.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_REGISTRATION_FROM_</strong><br/> <strong>REMOTE_DRIVE_NOT_SUPPORTED</strong><br/></td>
<td>0x80073d1f</td>
<td>Remote Laufwerke werden nicht unterstützt. Verwenden Sie <strong> \\ "Server\Freigabe"</strong> zum Registrieren eines Remote Pakets.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPX_RAW_</strong><br/> <strong>DATA_WRITE_FAILED</strong><br/></td>
<td>0x80073d20</td>
<td>Fehler beim Verarbeiten und schreiben heruntergeladener Paketdaten auf den Datenträger.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_VOLUME_POLICY_PACKAGE</strong><br/></td>
<td>0x80073d21</td>
<td>Der Bereitstellungs Vorgang wurde aufgrund einer Paket familienrichtlinie blockiert, die bereit Stellungen auf einem nicht-System Volume einschränkt. Gemäß der Richtlinie muss diese APP auf dem Systemlaufwerk installiert werden, dies ist jedoch nicht als Standard festgelegt. Legen Sie unter Speichereinstellungen das Systemlaufwerk als Standard Speicherort fest, um neuen Inhalt zu speichern, und wiederholen Sie dann die Installation.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_VOLUME_POLICY_MACHINE</strong><br/></td>
<td>0x80073d22</td>
<td>Der Bereitstellungs Vorgang wurde aufgrund einer Computer weiten Richtlinie blockiert, die bereit Stellungen auf einem nicht-System Volume einschränkt. Gemäß der Richtlinie muss diese APP auf dem Systemlaufwerk installiert werden, dies ist jedoch nicht als Standard festgelegt. Legen Sie unter Speichereinstellungen das Systemlaufwerk als Standard Speicherort fest, um neuen Inhalt zu speichern, und wiederholen Sie dann die Installation.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_PROFILE_POLICY</strong><br/></td>
<td>0x80073d23</td>
<td>Der Bereitstellungs Vorgang wurde blockiert, weil eine spezielle Profil Bereitstellung nicht zulässig ist (spezielle Profile sind Benutzerprofile, bei denen Änderungen verworfen werden, nachdem sich der Benutzer abgemeldet hat). Melden Sie sich bei einem Konto an, das kein spezielles Profil ist. Sie können versuchen, sich beim aktuellen Konto anzumelden und sich wieder anzumelden oder sich bei einem anderen Konto anzumelden.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_FAILED_</strong><br/> <strong>CONFLICTING_MUTABLE_PACKAGE_</strong><br/> <strong>Befinden</strong><br/></td>
<td>0x80073d24</td>
<td>Der Bereitstellungs Vorgang ist aufgrund des <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">änderbaren Paket Verzeichnisses</a>eines in Konflikt stehenden Pakets fehlgeschlagen. Entfernen Sie das vorhandene Paket mit dem in Konflikt stehenden änderbaren Paket Verzeichnis, um dieses Paket zu installieren.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SINGLETON_RESOURCE_</strong><br/> <strong>INSTALLED_IN_ACTIVE_USER</strong><br/></td>
<td>0x80073d25</td>
<td>Die Paketinstallation ist fehlgeschlagen, weil eine Singleton-Ressource angegeben und ein anderer Benutzer mit installiertem Paket angemeldet ist. Stellen Sie sicher, dass alle aktiven Benutzer mit installiertem Paket abgemeldet werden, und wiederholen Sie die Installation.<br/></td>
</tr>
<tr class="even">
<td>ERROR_DIFFERENT_VERSION_<strong></strong><br/> <strong>OF_PACKAGED_SERVICE_INSTALLED</strong><br/></td>
<td>0x80073d26</td>
<td>Die Paketinstallation ist fehlgeschlagen, da eine andere Version des Dienstanbieter installiert ist. Versuchen Sie, eine neuere Version des Pakets zu installieren.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SERVICE_EXISTS_</strong><br/> <strong>AS_NON_PACKAGED_SERVICE</strong><br/></td>
<td>0x80073d27</td>
<td>Die Paketinstallation ist fehlgeschlagen, da eine Version des Dienstanbieter außerhalb eines msix-/AppX-Pakets vorhanden ist. Wenden Sie sich an den Softwarehersteller.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGED_SERVICE_</strong><br/> <strong>REQUIRES_ADMIN_PRIVILEGES</strong><br/></td>
<td>0x80073d28</td>
<td>Die Paketinstallation ist fehlgeschlagen, da Administratorrechte erforderlich sind. Bitten Sie einen Administrator, dieses Paket zu installieren.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_REDIRECTION_TO_</strong><br/> <strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong><br/></td>
<td>0x80073d29</td>
<td>Die Paket Bereitstellung ist fehlgeschlagen, da der Vorgang zu einem Standardkonto umgeleitet worden wäre, als der Aufrufer dies nicht getan hat.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_LACKS_</strong><br/> <strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong><br/></td>
<td>0x80073d2a</td>
<td>Die Paket Bereitstellung ist fehlgeschlagen, da das Paket eine Funktion zum systemeigenen Ziel dieses Hosts erfordert.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_UNSIGNED_PACKAGE_</strong><br/> <strong>INVALID_CONTENT</strong><br/></td>
<td>0x80073d2b</td>
<td>Fehler bei der Paket Bereitstellung, weil der zugehörige Inhalt für ein nicht signiertes Paket ungültig ist.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_UNSIGNED_PACKAGE_</strong><br/> <strong>INVALID_PUBLISHER_NAMESPACE</strong><br/></td>
<td>0x80073d2c</td>
<td>Die Paket Bereitstellung ist fehlgeschlagen, da sich der Verleger nicht im nicht signierten Namespace befindet.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SIGNED_PACKAGE_</strong><br/> <strong>INVALID_PUBLISHER_NAMESPACE</strong><br/></td>
<td>0x80073d2d</td>
<td>Fehler bei der Paket Bereitstellung, weil der Verleger nicht im signierten Namespace ist.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_EXTERNAL_</strong><br/> <strong>LOCATION_NOT_ALLOWED</strong><br/></td>
<td>0x80073d2e</td>
<td>Fehler bei der Paket Bereitstellung, weil der Verleger nicht im signierten Namespace ist.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_FULLTRUST_</strong><br/> <strong>HOSTRUNTIME_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br/></td>
<td>0x80073d2f</td>
<td>Eine Host Laufzeitabhängigkeit zum Auflösen eines Pakets mit voll vertrauenswürdigem Inhalt erfordert, dass das Hauptpaket über die Funktion " <strong>runfulltrust</strong> " verfügt.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_PACKAGING_INTERNAL</strong></td>
<td>0x80080200</td>
<td>Interner Fehler bei der Paket-API.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INTERLEAVING_</strong><br/> <strong>NOT_ALLOWED</strong><br/></td>
<td>0x80080201</td>
<td>Das Paket ist ungültig, weil sein Inhalt überlappend ist.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_RELATIONSHIPS_</strong><br/> <strong>NOT_ALLOWED</strong><br/></td>
<td>0x80080202</td>
<td>Das Paket ist ungültig, weil es OPC-Beziehungen enthält.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_MISSING_</strong><br/> <strong>REQUIRED_FILE</strong><br/></td>
<td>0x80080203</td>
<td>Das Paket ist ungültig, weil ein Manifest oder eine Block Zuordnung fehlt, oder eine Code Integritäts Datei ist vorhanden, aber eine Signatur Datei fehlt.<br/> Stellen Sie sicher, dass für das Paket mindestens eine der folgenden erforderlichen Dateien fehlt:<br/>
<ul>
<li>\AppxManifest.xml</li>
<li>\AppxBlockMap.xml</li>
</ul>
Wenn das Paket \AppxMetadata\CodeIntegrity.cat enthält, muss es auch \appxsignature.p7xenthalten.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_MANIFEST</strong></td>
<td>0x80080204</td>
<td>Die AppxManifest.xml Datei des Pakets ist ungültig.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_BLOCKMAP</strong></td>
<td>0x80080205</td>
<td>Die AppxBlockMap.xml Datei des Pakets ist ungültig.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_CORRUPT_CONTENT</strong></td>
<td>0x80080206</td>
<td>Der Paket Inhalt kann nicht gelesen werden, da er beschädigt ist.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_BLOCK_</strong><br/> <strong>HASH_INVALID</strong><br/></td>
<td>0x80080207</td>
<td>Der berechnete Hashwert des Blocks entspricht nicht dem in der Block Zuordnung gespeicherten Wert.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_REQUESTED_</strong><br/> <strong>RANGE_TOO_LARGE</strong><br/></td>
<td>0x80080208</td>
<td>Der angeforderte Byte Bereich beträgt mehr als 4 GB, wenn er in einen Byte Bereich von Blöcken übersetzt wird.<br/></td>
</tr>
<tr class="even">
<td><strong>TRUST_E_NOSIGNATURE</strong></td>
<td>0x800B0100</td>
<td>Es ist keine Signatur im Betreff vorhanden.<br/> Dieser Fehler kann angezeigt werden, wenn das Paket nicht signiert oder die Signatur ungültig ist. Das Paket muss zur Bereitstellung signiert sein.<br/></td>
</tr>
<tr class="odd">
<td><strong>CERT_E_UNTRUSTEDROOT</strong></td>
<td>0x800B0109</td>
<td>Eine Zertifikat Kette wurde verarbeitet, aber in einem Stamm Zertifikat beendet, dem der Vertrauens Anbieter nicht vertraut.<br/> Siehe <a href="/previous-versions/br230260(v=vs.110)">Signieren eines Pakets</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>CERT_E_CHAINING</strong></td>
<td>0x800b010a</td>
<td>Eine Zertifikat Kette konnte nicht für eine vertrauenswürdige Stamm Zertifizierungsstelle erstellt werden.<br/> Siehe <a href="/previous-versions/br230260(v=vs.110)">Signieren eines Pakets</a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong> <br/> <strong>SIP_CLIENT_DATA</strong> <br/></td>
<td>0x80080209</td>
<td>Die <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>Struktur, die zum Signieren des Pakets verwendet wurde, enthielt nicht die erforderlichen Daten.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong> <br/> <strong>KEY_INFO</strong> <br/></td>
<td>0x8008020a</td>
<td>Die <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> Struktur, die zum Verschlüsseln oder Entschlüsseln des Pakets verwendet wird, enthält ungültige Daten.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>Contentgroupmap</strong><br/></td>
<td>0x8008020b</td>
<td>Die Inhalts Gruppen Zuordnung des msix/AppX-Pakets ist ungültig.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>Appinstaller</strong><br/></td>
<td>0x8008020c</td>
<td>Die <a href="/windows/msix/app-installer/app-installer-root">appinstaller-Datei</a> für das Paket ist ungültig.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_DELTA_BASELINE_</strong><br/> <strong>VERSION_MISMATCH</strong><br/></td>
<td>0x8008020d</td>
<td>Die baselinepaketversion im Delta Paket stimmt nicht mit der Version in dem zu aktualisierenden Basispaket ab.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_DELTA_PACKAGE_</strong><br/> <strong>MISSING_FILE</strong><br/></td>
<td>0x8008020e</td>
<td>Im Delta Paket fehlt eine Datei aus dem aktualisierten Paket.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>DELTA_PACKAGE</strong><br/></td>
<td>0x8008020f</td>
<td>Das Delta Paket ist ungültig.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_DELTA_APPENDED_</strong><br/> <strong>PACKAGE_NOT_ALLOWED</strong><br/></td>
<td>0x80080210</td>
<td>Das angefügte Delta Paket ist für den aktuellen Vorgang nicht zulässig.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>PACKAGING_LAYOUT</strong><br/></td>
<td>0x80080211</td>
<td>Die paketlayoutdatei ist ungültig.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>Packagesignconfig</strong><br/></td>
<td>0x80080212</td>
<td>Die Datei "packagesignconfig" ist ungültig.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_RESOURCESPRI_</strong><br/> <strong>NOT_ALLOWED</strong><br/></td>
<td>0x80080213</td>
<td>Die Datei "Resources. pri" ist nicht zulässig, wenn das Paket Manifest keine Ressourcen Elemente enthält.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_FILE_</strong><br/> <strong>COMPRESSION_MISMATCH</strong><br/></td>
<td>0x80080214</td>
<td>Der Komprimierungs Status der Datei in der Baseline und des aktualisierten Pakets stimmt nicht mit.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>PAYLOAD_PACKAGE_EXTENSION</strong><br/></td>
<td>0x80080215</td>
<td>Nicht-AppX-Erweiterungen sind bei Nutz Last Paketen, die auf ältere Plattformen abzielen, nicht zulässig.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong><br/></td>
<td>0x80080216</td>
<td>Die Datei "verschlüsselungsexclusionfilelist" ist ungültig.<br/></td>
</tr>
</tbody>
</table>

## <a name="applications-dont-start-and-their-names-are-dimmed"></a>Anwendungen werden nicht gestartet, und ihre Namen sind abdimmt.

Auf einem Windows 10-basierten Computer können Sie einige Anwendungen nicht starten, und die Anwendungsnamen werden abgeblendet angezeigt.

![Einige Anwendungsnamen werden im Startmenü abgeblendet angezeigt.](./images/app-names-dimmed.png)

Wenn Sie versuchen, eine Anwendung durch Auswahl des abzurufenden namens zu öffnen, erhalten Sie möglicherweise eine der folgenden Fehlermeldungen:

> Es gibt ein Problem mit \<*application name*> . Bitten Sie den Systemadministrator, ihn zu reparieren oder neu zu installieren.  
> Fehler: diese APP kann nicht geöffnet werden.

Außerdem werden die folgenden Ereignis Einträge im Protokoll "Microsoft-Windows-twinui/Operational" unter "Applications" **und "services\microsoft\windows\apps**" protokolliert:

> Protokoll Name: Microsoft-Windows-twinui/Operational  
> Quelle: Microsoft-Windows-immersive Shell  
> Datum: <*Datum*>  
> Ereignis-ID: 5960  
> Aufgaben Kategorie: (5960)  
> Ebene: Fehler  
> Schlüsselwörter:  
> Beschreibung:  
> Aktivierung der APP Microsoft.BingNews_8wekyb3d8bbwe! Appexnews für Windows. Der Start Vertrag wurde mit dem Fehler 0x80073cfc blockiert, weil sich das zugehörige Paket im Status "geändert" befindet.  

### <a name="cause"></a>Ursache

Dieses Problem tritt auf, weil der Registrierungs Eintrag für den Statuswert des entsprechenden Pakets der Anwendung geändert wurde.

### <a name="resolution"></a>Lösung

> [!WARNING]
> Durch die unsachgemäße Änderung der Registrierung mit dem Registrierungs-Editor oder einer anderen Methode können schwerwiegende Probleme verursacht werden. U. U. ist in einem solchen Fall sogar die Neuinstallation des Betriebssystems erforderlich. Microsoft garantiert nicht, dass diese Probleme behoben werden können. Das Bearbeiten der Registrierung erfolgt auf eigenes Risiko.

So beheben Sie dieses Problem:

1. Starten Sie den Registrierungs-Editor, und suchen Sie dann den **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** Unterschlüssel.
2. Um die Unterschlüssel Daten zu sichern, klicken Sie mit der rechten Maustaste auf **PackageList**, wählen Sie **exportieren** aus, und speichern Sie die Daten dann als Registrierungsdatei.
3. Führen Sie für jede Anwendung, die in den Ereignis-ID 5960-Protokoll Einträgen aufgeführt ist, die folgenden Schritte aus:  
   1. Suchen Sie den Eintrag **packagestatus** .
   2. Legen Sie den Wert von **packagestatus** auf **0**(null) fest.
   > [!NOTE]  
   > Wenn unter **PackageList** keine Einträge für die Anwendung vorhanden sind, hat das Problem eine andere Ursache. Im Fall des Beispiel Ereignisses in diesem Artikel wird der vollständige Unterschlüssel **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**
4. Starten Sie den Computer neu.

## <a name="get-additional-help"></a>Zusätzliche Hilfe abrufen

Wenn Sie weitere Hilfe bei der Behebung eines Problems benötigen, das Sie beim Verpacken, bereitstellen oder Abfragen eines Windows-App-Pakets (. msix/. AppX) als Entwickler haben, finden Sie weitere Informationen unter Support Ressourcen für Entwickler.

- [Microsoft Q&a](/answers/topics/uwp.html?filter=all&sort=active) bietet relevante und rechtzeitige Antworten auf technische Probleme von einer Community von Experten und Microsoft-Technikern.
- Zur Unterstützung der Community bei der Entwicklung finden Sie in unseren [Foren](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required)und [StackOverflow](https://stackoverflow.com/questions).
- Auf der [Windows Developer Support](https://developer.microsoft.com/windows/support) -Website werden Weitere Supportoptionen erläutert.

## <a name="related-topics"></a>Zugehörige Themen

- [Signieren eines App-Pakets mit SignTool](how-to-sign-a-package-using-signtool.md)
- [Problembehandlung bei App-Paket Signatur Fehlern](how-to-troubleshoot-app-package-signature-errors.md)
