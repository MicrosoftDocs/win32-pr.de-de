---
title: Problembehandlung beim Packen, Bereitstellen und Abfragen von Windows-Apps
description: Verwenden Sie diese Vorschläge, um Probleme zu beheben, die beim Packen, Bereitstellen oder Abfragen eines App-Pakets auftreten.
ms.assetid: 38E327C6-0345-4FA6-BCDB-5FA2FCD421FB
ms.topic: article
ms.date: 02/20/2020
manager: dcscontentpm
ms.custom:
- CI 111497
- CSSTroubleshooting
- contperf-fy21q2
ms.openlocfilehash: ce602d4a65d0287154a9eee94665d025a628f6d8ce3a7f086700625820637a5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552312"
---
# <a name="troubleshooting-packaging-deployment-and-query-of-windows-apps"></a>Problembehandlung beim Packen, Bereitstellen und Abfragen von Windows-Apps

Verwenden Sie diese Vorschläge, um Probleme zu beheben, die beim Packen, Bereitstellen oder Abfragen eines Windows-App-Pakets (.msix/.appx) als Entwickler auftreten.

> [!NOTE]
> Dieser Artikel richtet sich an Entwickler. Wenn Sie kein Entwickler sind und Hilfe bei einem Fehler bei der Windows-App suchen, finden Sie weitere Informationen unter [Windows Support.](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10)

## <a name="get-diagnostic-information"></a>Diagnoseinformationen erhalten

Wenn eine API fehlschlägt, wird ein Fehlercode zurückgegeben, der das Problem beschreibt. Wenn der Fehlercode nicht genügend Informationen enthält, finden Sie weitere Diagnoseinformationen in den ausführlichen Ereignisprotokollen.

Führen Sie die folgenden Schritte aus, um mithilfe von Ereignisanzeige auf die **Paket-** und Bereitstellungsereignisprotokolle zu zugreifen:

1. Führen Sie einen der folgenden Schritte aus:

    * Klicken **Sie im** Menü Windows auf Start, geben Sie **Ereignisanzeige** ein, und drücken Sie **die EINGABETASTE.**
    * Führen **Sie eventvwr.msc aus.**

2. Erweitern Sie auf der linken Seite Ereignisanzeige **(Lokale) Anwendungs-** und  >  **Dienstprotokolle**  >  **Microsoft**  >  **Windows**.
3. Überprüfen Sie in den folgenden Kategorien nach verfügbaren Protokollen:

    * **AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/Operational**
    * **AppXDeployment-Server**  >  **Microsoft-Windows-AppXDeploymentServer/Operational**

Sehen Sie sich zunächst die Protokolle unter **AppXDeployment-Server an.** Wenn der Fehler durch **eine** 0x80073CF0 **oder** ERROR_INSTALL_OPEN_PACKAGE_FAILED wurde, sind möglicherweise zusätzliche Details in den **AppxpackagingOM-Protokollen** vorhanden.

Sie können auch den [Befehl Get-AppxLog](/powershell/module/appx/get-appxlog) in PowerShell verwenden, um die ersten protokollierten Ereignisse zu erhalten. Im folgenden Beispiel werden die Protokolle angezeigt, die dem letzten Bereitstellungsvorgang zugeordnet sind.

```PowerShell
Get-Appxlog
```

Im folgenden Beispiel werden die Protokolle, die dem letzten Bereitstellungsvorgang zugeordnet sind, in einer interaktiven Tabelle in einem separaten Fenster angezeigt.

```PowerShell
Get-Appxlog | Out-GridView
```

## <a name="common-error-codes"></a>Häufige Fehlermeldungen

In dieser Tabelle sind einige der häufigsten Fehlercodes aufgeführt. Wenn Sie weitere Hilfe zu einem dieser Fehler benötigen oder wenn ein Fehlercode auftritt, der nicht in dieser Liste enthalten ist, finden Sie weitere [Hilfeoptionen.](#get-additional-help)

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
<td>Datei oder Pfad nicht gefunden. Dies kann während einer COM-Typelib-Überprüfung auftreten, die erfordert, dass der Pfad für das Verzeichnis tatsächlich in Ihrem MSIX-Paket vorhanden ist.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_BAD_FORMAT</strong></td>
<td>0x8007000B</td>
<td>Das Paket ist nicht ordnungsgemäß formatiert und muss neu erstellt oder erneut signiert werden.<br/> Dieser Fehler wird möglicherweise angezeigt, wenn ein Konflikt zwischen dem Namen des Signaturzertifikats und dem Namen des AppxManifest.xml auftritt.<br/> Siehe <a href="how-to-sign-a-package-using-signtool.md">Signieren eines App-Pakets mit SignTool</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>E_INVALIDARG</strong></td>
<td>0x80070057</td>
<td>Mindestens ein Argument ist ungültig. Wenn Sie das AppXDeployment-Server-Ereignisprotokoll überprüfen und das folgende Ereignis sehen: "Während der Installation des Pakets konnte das System die Erweiterung windows.repositoryExtension aufgrund des folgenden Fehlers nicht registrieren: Der Parameter ist falsch." <br/> Dieser Fehler wird möglicherweise angezeigt, wenn die Manifestelemente DisplayName oder Description Zeichen enthalten, die von der Firewall Windows werden. und |  und alle , wodurch Windows das AppContainer-Profil für das Paket nicht erstellen kann. Entfernen Sie diese Zeichen aus dem Manifest, und versuchen Sie, das Paket zu installieren. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OPEN_</strong><br/> <strong>PACKAGE_FAILED</strong><br/></td>
<td>0x80073CF0</td>
<td>Das Paket konnte nicht geöffnet werden.<br/> Mögliche Ursachen:<br/>
<ul>
<li>Das Paket ist nicht signiert.</li>
<li>Der Herausgebername ist nicht mit dem Signaturzertifikat-Betreff übereinstimmen.</li>
<li>Das file:// präfix fehlt, oder das Paket konnte am angegebenen Speicherort nicht gefunden werden.</li>
</ul>
Weitere Informationen finden Sie im <strong>Ereignisprotokoll AppxPackagingOM.</strong><br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_PACKAGE_</strong><br/> <strong>NOT_FOUND</strong><br/></td>
<td>0x80073CF1</td>
<td>Das Paket wurde nicht gefunden.<br/> Dieser Fehler tritt möglicherweise auf, wenn Sie ein Paket entfernen, das für den aktuellen Benutzer nicht installiert ist.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_INVALID_</strong><br/> <strong>Paket</strong><br/></td>
<td>0x80073CF2</td>
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
Weitere Informationen finden Sie im <strong>Ereignisprotokoll AppXDeployment-Server.</strong><br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OUT_</strong><br/> <strong>OF_DISK_SPACE</strong><br/></td>
<td>0x80073CF4</td>
<td>Auf Ihrem Computer ist nicht genügend Speicherplatz vorhanden. Geben Sie Speicherplatz frei, und versuchen Sie es erneut.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_NETWORK_</strong><br/> <strong>Fehler</strong><br/></td>
<td>0x80073CF5</td>
<td>Das Paket kann nicht heruntergeladen werden.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>REGISTRATION_FAILURE</strong><br/></td>
<td>0x80073CF6</td>
<td>Das Paket kann nicht registriert werden.<br/> Weitere Informationen finden Sie im <strong>Ereignisprotokoll AppXDeployment-Server.</strong><br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>DEREGISTRATION_EFAILURE</strong><br/></td>
<td>0x80073CF7</td>
<td>Die Registrierung des Pakets kann nicht aufgehoben werden.<br/> Dieser Fehler kann beim Entfernen eines Pakets angezeigt werden.<br/> Weitere Informationen finden Sie im <strong>Ereignisprotokoll AppXDeployment-Server.</strong><br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_CANCEL</strong></td>
<td>0x80073CF8</td>
<td>Der Benutzer hat die Installationsanforderung abgebrochen.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_FAILED</strong></td>
<td>0x80073CF9</td>
<td>Fehler bei der Paket installieren. Wenden Sie sich an den Softwarehersteller.<br/> Weitere Informationen finden Sie im <strong>Ereignisprotokoll AppXDeployment-Server.</strong><br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_REMOVE_FAILED</strong></td>
<td>0x80073CFA</td>
<td>Fehler beim Entfernen des Pakets.<br/> Möglicherweise erhalten Sie diesen Fehler bei Fehlern, die während der Paketdeinstallation auftreten.<br/> Weitere Informationen finden Sie unter <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>RemovePackageAsync.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_</strong><br/> <strong>ALREADY_EXISTS</strong><br/></td>
<td>0x80073CFB</td>
<td>Das bereitgestellte Paket ist bereits installiert, und eine erneute Installation des Pakets wird blockiert. <br/> Dieser Fehler kann auftreten, wenn Sie ein Paket installieren, das nicht bitweise mit dem bereits installierten Paket identisch ist. Beachten Sie, dass die digitale Signatur auch Teil des Pakets ist. Wenn ein Paket neu erstellt oder zurückgesetzt wird, ist es daher nicht mehr bitweise identisch mit dem zuvor installierten Paket. Zwei mögliche Optionen zum Beheben dieses Fehlers sind: (1) Erhöhen Sie die Versionsnummer der App, erstellen Sie das Paket neu, und stellen Sie es neu (2) Entfernen Sie das alte Paket für jeden Benutzer auf dem System, bevor Sie das neue Paket installieren. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_NEEDS_REMEDIATION</strong></td>
<td>0x80073CFC</td>
<td>Die App kann nicht gestartet werden. Versuchen Sie, die App neu zu installieren.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>PREREQUISITE_FAILED</strong><br/></td>
<td>0x80073CFD</td>
<td>Eine angegebene Installationsvoraussetzungen konnten nicht erfüllt werden.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_</strong><br/> <strong>REPOSITORY_CORRUPTED</strong><br/></td>
<td>0x80073CFE</td>
<td>Das Paket-Repository ist beschädigt.<br/> Dieser Fehler kann auftreten, wenn der Ordner, auf den dieser Registrierungsschlüssel verweist, nicht vorhanden oder beschädigt ist: <br/> <strong>HKLM\Software\Microsoft\Windows\</strong><br/> <strong>CurrentVersion\Appx\PackageRepositoryRoot</strong><br/> Aktualisieren Sie Ihren PC, um diesen Zustand wiederherzustellen.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>POLICY_FAILURE</strong><br/></td>
<td>0x80073CFF</td>
<td>Um diese App zu installieren, benötigen Sie eine Entwicklerlizenz oder ein Querladen aktiviertes System. <br/> Dieser Fehler kann auftreten, wenn das Paket eine der folgenden Anforderungen nicht erfüllt:<br/>
<ul>
<li>Die App wird mit F5 in Visual Studio auf einem Computer mit einer Windows Entwicklerlizenz bereitgestellt.</li>
<li>Das Paket wird mit einer Microsoft-Signatur signiert und als Teil von Windows oder aus dem Microsoft Store bereitgestellt.</li>
<li>Das Paket wird mit einer vertrauenswürdigen Signatur signiert und auf einem Computer mit einer Entwicklerlizenz, einem in die Domäne eingebundenen Computer mit aktivierter Richtlinie AllowAllTrustedApps oder einem Computer mit einer Windows Sideloading-Lizenz mit aktivierter Richtlinie AllowAllTrustedApps installiert.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_UPDATING</strong></td>
<td>0x80073D00</td>
<td>Die App kann nicht gestartet werden, da sie gerade aktualisiert wird.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_</strong><br/> <strong>BLOCKED_BY_POLICY</strong><br/></td>
<td>0x80073D01</td>
<td>Der Paketbereitstellungsvorgang wird durch eine Richtlinie blockiert. Wenden Sie sich an Ihren Systemadministrator.<br/> Mögliche Ursachen:<br/>
<ul>
<li>Die Paketbereitstellung wird durch Anwendungssteuerungsrichtlinien blockiert.</li>
<li>Die Paketbereitstellung wird durch die &quot; Richtlinie Bereitstellungsvorgänge in speziellen Profilen zulassen &quot; blockiert.</li>
</ul>
Einer der möglichen Gründe ist die Notwendigkeit eines Roamingprofils. Informationen zum Einrichten von Roamingbenutzerprofilen für Benutzerkonten finden Sie unter <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">Bereitstellen von Roamingbenutzerprofilen.</a> Wenn auf Ihrem System keine Richtlinien konfiguriert sind und dieser Fehler weiterhin angezeigt wird, werden Sie möglicherweise mit einem temporären Profil angemeldet. Melden Sie sich ab, melden Sie sich erneut an, und wiederholen Sie dann den Vorgang.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGES_IN_USE</strong></td>
<td>0x80073D02</td>
<td>Das Paket konnte nicht installiert werden, da die geänderten Ressourcen derzeit verwendet werden.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_RECOVERY_</strong><br/> <strong>FILE_CORRUPT</strong><br/></td>
<td>0x80073D03</td>
<td>Das Paket konnte nicht wiederhergestellt werden, da die für die Wiederherstellung erforderlichen Daten beschädigt sind.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INVALID_</strong><br/> <strong>STAGED_SIGNATURE</strong><br/></td>
<td>0x80073D04</td>
<td>Die Signatur ist ungültig. Um sich im Entwicklermodus zu registrieren, müssen AppxSignature.p7x und AppxBlockMap.xml gültig sein oder nicht vorhanden sein.<br/> Wenn Sie ein Entwickler sind, der F5 mit Visual Studio verwendet, stellen Sie sicher, dass Ihr erstelltes Projektverzeichnis keine Signatur- oder Blockzuordnungsdateien aus früheren Versionen des Pakets enthält.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DELETING_EXISTING_</strong><br/> <strong>APPLICATIONDATA_STORE_FAILED</strong><br/></td>
<td>0x80073D05</td>
<td>Fehler beim Löschen der zuvor vorhandenen Anwendungsdaten des Pakets.<br/> Sie können diesen Fehler erhalten, wenn der <a href="/previous-versions/hh441475(v=vs.110)">Simulator</a> ausgeführt wird. Schließen Sie den Simulator. Sie können diesen Fehler auch erhalten, wenn dateien in den App-Daten geöffnet sind (z. B. wenn eine Protokolldatei in einem Text-Editor geöffnet ist).<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_</strong><br/> <strong>PACKAGE_DOWNGRADE</strong><br/></td>
<td>0x80073D06</td>
<td>Das Paket konnte nicht installiert werden, da bereits eine höhere Version dieses Pakets installiert ist.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SYSTEM_</strong><br/> <strong>NEEDS_REMEDIATION</strong><br/></td>
<td>0x80073D07</td>
<td>Ein Fehler in einer Systembinärdatei wurde erkannt. Versuchen Sie, den PC zu aktualisieren, um das Problem zu beheben. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPX_INTEGRITY_</strong><br/> <strong>FAILURE_EXTERNAL</strong><br/></td>
<td>0x80073D08</td>
<td>Auf dem System wurde eine beschädigte, nicht Windows Binärdatei erkannt. <br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_RESILIENCY_</strong><br/> <strong>FILE_CORRUPT</strong><br/></td>
<td>0x80073D09</td>
<td>Der Vorgang konnte nicht fortgesetzt werden, da die für die Wiederherstellung erforderlichen Daten beschädigt sind. <br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_FIREWALL_</strong><br/> <strong>SERVICE_NOT_RUNNING</strong><br/></td>
<td>0x80073D0A</td>
<td>Das Paket konnte nicht installiert werden, da der Windows Firewalldienst nicht ausgeführt wird. Aktivieren Sie den Windows Firewalldienst, und versuchen Sie es erneut.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_MOVE_FAILED</strong></td>
<td>0x80073D0B</td>
<td>Fehler beim Verschieben des Pakets.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>NOT_EMPTY</strong><br/></td>
<td>0x80073D0C</td>
<td>Fehler beim Bereitstellungsvorgang, weil das Volume nicht leer ist.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>Offline</strong><br/></td>
<td>0x80073D0D</td>
<td>Fehler beim Bereitstellungsvorgang, weil das Volume offline ist. Bei einem Paketupdate bezieht sich das Volume auf das installierte Volume aller Paketversionen.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_VOLUME_</strong><br/> <strong>Beschädigt</strong><br/></td>
<td>0x80073D0E</td>
<td>Fehler beim Bereitstellungsvorgang, weil das angegebene Volume beschädigt ist.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_NEEDS_REGISTRATION</strong><br/> <strong></strong><br/></td>
<td>0x80073D0F</td>
<td>Fehler beim Bereitstellungsvorgang, weil die angegebene Anwendung zuerst registriert werden muss.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_WRONG_</strong><br/> <strong>PROCESSOR_ARCHITECTURE</strong><br/></td>
<td>0x80073D10</td>
<td>Fehler beim Bereitstellungsvorgang, weil das Paket auf die falsche Prozessorarchitektur ausgerichtet ist.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEV_SIDELOAD_</strong><br/> <strong>LIMIT_EXCEEDED</strong><br/></td>
<td>0x80073D11</td>
<td>Sie haben die maximale Anzahl von vom Entwickler quergeladenen Paketen erreicht, die auf diesem Gerät zulässig sind. Deinstallieren Sie ein quergeladenes Paket, und versuchen Sie es erneut.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_</strong><br/> <strong>MAIN_PACKAGE</strong><br/></td>
<td>0x80073D12</td>
<td>Ein Haupt-App-Paket ist erforderlich, um dieses optionale Paket zu installieren. Installieren Sie zuerst das Hauptpaket, und versuchen Sie es erneut.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_NOT_</strong><br/> <strong>SUPPORTED_ON_FILESYSTEM</strong><br/></td>
<td>0x80073D13</td>
<td>Dieser App-Pakettyp wird in diesem Dateisystem nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_MOVE_</strong><br/> <strong>BLOCKED_BY_STREAMING</strong><br/></td>
<td>0x80073D14</td>
<td>Der Paketschiebevorgang wird blockiert, bis das Streaming der Anwendung abgeschlossen ist.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_APPLICATIONID_</strong><br/> <strong>NOT_UNIQUE</strong><br/></td>
<td>0x80073D15</td>
<td>Ein haupt- oder ein anderes optionales App-Paket verfügt über die gleiche Anwendungs-ID wie dieses optionale Paket. Ändern Sie die Anwendungs-ID für das optionale Paket, um Konflikte zu vermeiden.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGE_STAGING_</strong><br/> <strong>ONHOLD</strong><br/></td>
<td>0x80073D16</td>
<td>Diese Stagingsitzung wurde gehalten, damit ein anderer Stagingvorgang priorisiert werden kann.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_INVALID_</strong><br/> <strong>RELATED_SET_UPDATE</strong><br/></td>
<td>0x80073D17</td>
<td>Ein verwandter Satz kann nicht aktualisiert werden, da der aktualisierte Satz ungültig ist. Alle Pakete in der verknüpften Gruppe müssen gleichzeitig aktualisiert werden.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_INSTALL_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br/></td>
<td>0x80073D18</td>
<td>Ein optionales Paket mit einem FullTrust-Einstiegspunkt erfordert, dass das Hauptpaket über die <strong>runFullTrust-Funktion</strong> verfügt.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_USER_LOG_OFF</strong><br/></td>
<td>0x80073D19</td>
<td>Ein Fehler ist aufgetreten, weil ein Benutzer abgemeldet wurde.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PROVISION_OPTIONAL_</strong><br/> <strong>PACKAGE_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_PROVISIONED</strong><br/></td>
<td>0x80073D1A</td>
<td>Eine optionale Paketbereitstellung erfordert, dass auch das Abhängigkeitshauptpaket bereitgestellt wird.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_PACKAGES_REPUTATION_</strong><br/> <strong>CHECK_FAILED</strong><br/></td>
<td>0x80073D1B</td>
<td>Bei den Paketen ist bei der <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen-Zuverlässigkeitsprüfung</a>ein Fehler aufgetreten.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGES_REPUTATION_</strong><br/> <strong>CHECK_TIMEDOUT</strong><br/></td>
<td>0x80073D1C</td>
<td>Beim <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen-Vorgang</a> zur Überprüfung der Zuverlässigkeit ist ein Time out (Time-Out) erfolgt.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_OPTION_</strong><br/> <strong>NOT_SUPPORTED</strong><br/></td>
<td>0x80073D1D</td>
<td>Die aktuelle Bereitstellungsoption wird nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPINSTALLER_</strong><br/> <strong>ACTIVATION_BLOCKED</strong><br/></td>
<td>0x80073D1E</td>
<td>Die Aktivierung wird aufgrund der .appinstaller-Updateeinstellungen für diese App blockiert.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_REGISTRATION_FROM_</strong><br/> <strong>REMOTE_DRIVE_NOT_SUPPORTED</strong><br/></td>
<td>0x80073D1F</td>
<td>Remotelaufwerke werden nicht unterstützt. Verwenden Sie <strong> \\ server\share,</strong> um ein Remotepaket zu registrieren.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_APPX_RAW_</strong><br/> <strong>DATA_WRITE_FAILED</strong><br/></td>
<td>0x80073D20</td>
<td>Fehler beim Verarbeiten und Schreiben heruntergeladener Paketdaten auf den Datenträger.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_VOLUME_POLICY_PACKAGE</strong><br/></td>
<td>0x80073D21</td>
<td>Der Bereitstellungsvorgang wurde aufgrund einer Richtlinie pro Paketfamilie blockiert, die Bereitstellungen auf einem Nicht-Systemvolume einschränkt. Pro Richtlinie muss diese App auf dem Systemlaufwerk installiert werden, aber dies ist nicht als Standardeinstellung festgelegt. Machen Sie Storage Einstellungen das Systemlaufwerk zum Standardspeicherort, um neue Inhalte zu speichern, und wiederholen Sie dann die Installation.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_VOLUME_POLICY_MACHINE</strong><br/></td>
<td>0x80073D22</td>
<td>Der Bereitstellungsvorgang wurde aufgrund einer computerweiten Richtlinie blockiert, die Bereitstellungen auf einem Nicht-Systemvolume einschränkt. Pro Richtlinie muss diese App auf dem Systemlaufwerk installiert werden, aber dies ist nicht als Standardeinstellung festgelegt. Machen Sie Storage Einstellungen das Systemlaufwerk zum Standardspeicherort, um neue Inhalte zu speichern, und wiederholen Sie dann die Installation.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br/> <strong>BY_PROFILE_POLICY</strong><br/></td>
<td>0x80073D23</td>
<td>Der Bereitstellungsvorgang wurde blockiert, da die Bereitstellung eines speziellen Profils nicht zulässig ist (spezielle Profile sind Benutzerprofile, bei denen Änderungen verworfen werden, nachdem sich der Benutzer abmeldet). Versuchen Sie, sich bei einem Konto anzumelden, das kein spezielles Profil ist. Sie können versuchen, sich beim aktuellen Konto anzumelden oder sich bei einem anderen Konto anzumelden.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_DEPLOYMENT_FAILED_</strong><br/> <strong>CONFLICTING_MUTABLE_PACKAGE_</strong><br/> <strong>Verzeichnis</strong><br/></td>
<td>0x80073D24</td>
<td>Fehler beim Bereitstellungsvorgang aufgrund des <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">änderbaren Paketverzeichnisses</a>eines in Konfliktstehenden Pakets. Entfernen Sie zum Installieren dieses Pakets das vorhandene Paket mit dem in Konflikt stehenden änderbaren Paketverzeichnis.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SINGLETON_RESOURCE_</strong><br/> <strong>INSTALLED_IN_ACTIVE_USER</strong><br/></td>
<td>0x80073D25</td>
<td>Fehler bei der Paketinstallation, weil eine Singletonressource angegeben wurde und ein anderer Benutzer mit dem installierten Paket angemeldet ist. Stellen Sie sicher, dass alle aktiven Benutzer mit installierten Paketen abgemeldet sind, und wiederholen Sie die Installation.<br/></td>
</tr>
<tr class="even">
<td>ERROR_DIFFERENT_VERSION_<strong></strong><br/> <strong>OF_PACKAGED_SERVICE_INSTALLED</strong><br/></td>
<td>0x80073D26</td>
<td>Fehler bei der Paketinstallation, weil eine andere Version des Diensts installiert ist. Versuchen Sie, eine neuere Version des Pakets zu installieren.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SERVICE_EXISTS_</strong><br/> <strong>AS_NON_PACKAGED_SERVICE</strong><br/></td>
<td>0x80073D27</td>
<td>Fehler bei der Paketinstallation, weil eine Version des Diensts außerhalb eines .msix/.appx-Pakets vorhanden ist. Wenden Sie sich an Ihren Softwareanbieter.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGED_SERVICE_</strong><br/> <strong>REQUIRES_ADMIN_PRIVILEGES</strong><br/></td>
<td>0x80073D28</td>
<td>Fehler bei der Paketinstallation, weil Administratorrechte erforderlich sind. Wenden Sie sich an einen Administrator, um dieses Paket zu installieren.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_REDIRECTION_TO_</strong><br/> <strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong><br/></td>
<td>0x80073D29</td>
<td>Fehler bei der Paketbereitstellung, da der Vorgang an das Standardkonto umgeleitet worden wäre, wenn der Aufrufer dies nicht gesagt hat.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_LACKS_</strong><br/> <strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong><br/></td>
<td>0x80073D2A</td>
<td>Fehler bei der Paketbereitstellung, weil für das Paket eine Funktion erforderlich ist, um diesen Host nativ als Ziel festzulegen.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_UNSIGNED_PACKAGE_</strong><br/> <strong>INVALID_CONTENT</strong><br/></td>
<td>0x80073D2B</td>
<td>Fehler bei der Paketbereitstellung, weil der Inhalt für ein nicht signiertes Paket ungültig ist.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_UNSIGNED_PACKAGE_</strong><br/> <strong>INVALID_PUBLISHER_NAMESPACE</strong><br/></td>
<td>0x80073D2C</td>
<td>Fehler bei der Paketbereitstellung, weil sich der Herausgeber nicht im Namespace ohne Vorzeichen befindet.<br/></td>
</tr>
<tr class="odd">
<td><strong>ERROR_SIGNED_PACKAGE_</strong><br/> <strong>INVALID_PUBLISHER_NAMESPACE</strong><br/></td>
<td>0x80073D2D</td>
<td>Fehler bei der Paketbereitstellung, weil sich der Herausgeber nicht im signierten Namespace befindet.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_PACKAGE_EXTERNAL_</strong><br/> <strong>LOCATION_NOT_ALLOWED</strong><br/></td>
<td>0x80073D2E</td>
<td>Fehler bei der Paketbereitstellung, weil sich der Herausgeber nicht im signierten Namespace befindet.<br/></td>
</tr>
<tr class="even">
<td><strong>ERROR_INSTALL_FULLTRUST_</strong><br/> <strong>HOSTRUNTIME_REQUIRES_MAIN_</strong><br/> <strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br/></td>
<td>0x80073D2F</td>
<td>Eine Hostruntimeabhängigkeit, die in ein Paket mit vollständig vertrauenswürdigem Inhalt aufgelöst wird, erfordert, dass das Hauptpaket über die <strong>runFullTrust-Funktion</strong> verfügt.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_PACKAGING_INTERNAL</strong></td>
<td>0x80080200</td>
<td>Bei der Paket-API ist ein interner Fehler aufgetreten.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INTERLEAVING_</strong><br/> <strong>NOT_ALLOWED</strong><br/></td>
<td>0x80080201</td>
<td>Das Paket ist ungültig, da sein Inhalt überlappend ist.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_RELATIONSHIPS_</strong><br/> <strong>NOT_ALLOWED</strong><br/></td>
<td>0x80080202</td>
<td>Das Paket ist ungültig, da es OPC-Beziehungen enthält.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_MISSING_</strong><br/> <strong>REQUIRED_FILE</strong><br/></td>
<td>0x80080203</td>
<td>Das Paket ist ungültig, da ein Manifest oder eine Blockzuordnung fehlt oder eine Codeintegritätsdatei vorhanden ist, aber eine Signaturdatei fehlt.<br/> Stellen Sie sicher, dass dem Paket mindestens eine dieser erforderlichen Dateien nicht fehlt:<br/>
<ul>
<li>\AppxManifest.xml</li>
<li>\AppxBlockMap.xml</li>
</ul>
Wenn das Paket \AppxMetadata\CodeIntegrity.cat enthält, muss es auch \AppxSignature.p7x enthalten.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_MANIFEST</strong></td>
<td>0x80080204</td>
<td>Die AppxManifest.xml-Datei des Pakets ist ungültig.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_BLOCKMAP</strong></td>
<td>0x80080205</td>
<td>Die AppxBlockMap.xml-Datei des Pakets ist ungültig.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_CORRUPT_CONTENT</strong></td>
<td>0x80080206</td>
<td>Der Paketinhalt kann nicht gelesen werden, da er beschädigt ist.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_BLOCK_</strong><br/> <strong>HASH_INVALID</strong><br/></td>
<td>0x80080207</td>
<td>Der berechnete Hashwert des Blocks stimmt nicht mit dem wert überein, der in der Blockzuordnung gespeichert ist.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_REQUESTED_</strong><br/> <strong>RANGE_TOO_LARGE</strong><br/></td>
<td>0x80080208</td>
<td>Der angeforderte Bytebereich liegt über 4 GB, wenn er in einen Bytebereich von Blöcken übersetzt wird.<br/></td>
</tr>
<tr class="even">
<td><strong>TRUST_E_NOSIGNATURE</strong></td>
<td>0x800B0100</td>
<td>Im Betreff ist keine Signatur vorhanden.<br/> Dieser Fehler kann angezeigt werden, wenn das Paket nicht signiert ist oder die Signatur ungültig ist. Das Paket muss signiert sein, um bereitgestellt zu werden.<br/></td>
</tr>
<tr class="odd">
<td><strong>CERT_E_UNTRUSTEDROOT</strong></td>
<td>0x800B0109</td>
<td>Eine Zertifikatkette wurde verarbeitet, aber in einem Stammzertifikat beendet, das vom Vertrauensanbieter nicht als vertrauenswürdig eingestuft wird.<br/> Weitere Informationen <a href="/previous-versions/br230260(v=vs.110)">finden Sie unter Signieren eines Pakets.</a><br/></td>
</tr>
<tr class="even">
<td><strong>CERT_E_CHAINING</strong></td>
<td>0x800B010A</td>
<td>Eine Zertifikatkette konnte nicht für eine vertrauenswürdige Stammzertifizierungsstelle erstellt werden.<br/> Weitere Informationen <a href="/previous-versions/br230260(v=vs.110)">finden Sie unter Signieren eines Pakets.</a><br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong> <br/> <strong>SIP_CLIENT_DATA</strong> <br/></td>
<td>0x80080209</td>
<td>Die <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO,</strong></a>die zum Signieren des Pakets verwendet wurde, enthält nicht die erforderlichen Daten.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong> <br/> <strong>KEY_INFO</strong> <br/></td>
<td>0x8008020A</td>
<td>Die <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO,</strong></a> die zum Verschlüsseln oder Entschlüsseln des Pakets verwendet wird, enthält ungültige Daten.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>CONTENTGROUPMAP</strong><br/></td>
<td>0x8008020B</td>
<td>Die Inhaltsgruppenzuordnung des .msix/.appx-Pakets ist ungültig.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>APPINSTALLER</strong><br/></td>
<td>0x8008020C</td>
<td>Die <a href="/windows/msix/app-installer/app-installer-root">APPINSTALLER-Datei</a> für das Paket ist ungültig.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_DELTA_BASELINE_</strong><br/> <strong>VERSION_MISMATCH</strong><br/></td>
<td>0x8008020D</td>
<td>Die Baselinepaketversion im Deltapaket ist nicht mit der Version im zu aktualisierenden Baselinepaket übereinstimmen.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_DELTA_PACKAGE_</strong><br/> <strong>MISSING_FILE</strong><br/></td>
<td>0x8008020E</td>
<td>Im Deltapaket fehlt eine Datei aus dem aktualisierten Paket.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>DELTA_PACKAGE</strong><br/></td>
<td>0x8008020F</td>
<td>Das Deltapaket ist ungültig.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_DELTA_APPENDED_</strong><br/> <strong>PACKAGE_NOT_ALLOWED</strong><br/></td>
<td>0x80080210</td>
<td>Das angefügte Deltapaket ist für den aktuellen Vorgang nicht zulässig.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>PACKAGING_LAYOUT</strong><br/></td>
<td>0x80080211</td>
<td>Die Paketlayoutdatei ist ungültig.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>PACKAGESIGNCONFIG</strong><br/></td>
<td>0x80080212</td>
<td>Die PackageSignConfig-Datei ist ungültig.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_RESOURCESPRI_</strong><br/> <strong>NOT_ALLOWED</strong><br/></td>
<td>0x80080213</td>
<td>Die Datei resources.pri ist nicht zulässig, wenn im Paketmanifest keine Ressourcenelemente enthalten sind.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_FILE_</strong><br/> <strong>COMPRESSION_MISMATCH</strong><br/></td>
<td>0x80080214</td>
<td>Der Komprimierungsstatus der Datei im Baseline- und aktualisierten Paket ist nicht übereinstimmend.<br/></td>
</tr>
<tr class="odd">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>PAYLOAD_PACKAGE_EXTENSION</strong><br/></td>
<td>0x80080215</td>
<td>Nicht-AppX-Erweiterungen sind für Nutzlastpakete für ältere Plattformen nicht zulässig.<br/></td>
</tr>
<tr class="even">
<td><strong>APPX_E_INVALID_</strong><br/> <strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong><br/></td>
<td>0x80080216</td>
<td>Die Datei encryptionExclusionFileList ist ungültig.<br/></td>
</tr>
</tbody>
</table>

## <a name="applications-dont-start-and-their-names-are-dimmed"></a>Anwendungen werden nicht gestartet, und ihre Namen sind abgeblendet.

Auf einem Windows 10-basierten Computer können Sie einige Anwendungen nicht starten, und die Anwendungsnamen werden abgeblendet angezeigt.

![Einige Anwendungsnamen werden abgeblendet in der Startmenü](./images/app-names-dimmed.png)

Wenn Sie versuchen, eine Anwendung zu öffnen, indem Sie den abgeblendierten Namen auswählen, erhalten Sie möglicherweise eine der folgenden Fehlermeldungen:

> Es liegt ein Problem mit \<*application name*> vor. Wenden Sie sich an Ihren Systemadministrator, um ihn zu reparieren oder neu zu installieren.  
> Fehler: Diese App kann nicht geöffnet werden.

Darüber hinaus werden die folgenden Ereigniseinträge im Protokoll "Microsoft-Windows-TWinUI/Operational" unter Anwendungen und **Dienste\Microsoft\Windows\Apps protokolliert:**

> Protokollname: Microsoft-Windows-TWinUI/Operational  
> Quelle: Microsoft-Windows-Immersive-Shell  
> Datum: <*Datum*>  
> Ereignis-ID: 5960  
> Aufgabenkategorie: (5960)  
> Ebene: Fehler  
> Schlüsselwörter:  
> Beschreibung:  
> Aktivierung des App-Microsoft.BingNews_8wekyb3d8bbwe! AppexErklär für die Windows. Der Startvertrag wurde mit dem Fehler 0x80073CFC, da sich das Paket im Status Geändert befindet.  

### <a name="cause"></a>Ursache

Dieses Problem tritt auf, weil der Registrierungseintrag für den Statuswert des entsprechenden Pakets der Anwendung geändert wurde.

### <a name="resolution"></a>Lösung

> [!WARNING]
> Durch die unsachgemäße Änderung der Registrierung mit dem Registrierungs-Editor oder einer anderen Methode können schwerwiegende Probleme verursacht werden. U. U. ist in einem solchen Fall sogar die Neuinstallation des Betriebssystems erforderlich. Microsoft garantiert nicht, dass diese Probleme behoben werden können. Das Bearbeiten der Registrierung erfolgt auf eigenes Risiko.

So beheben Sie dieses Problem:

1. Starten Sie den Registrierungs-Editor, und suchen Sie **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** unteren Schlüssel.
2. Klicken Sie zum Sichern der Unterschlüsseldaten mit der rechten Maustaste auf **PackageList,** wählen Sie **Exportieren** aus, und speichern Sie die Daten dann als Registrierungsdatei.
3. Führen Sie für jede der Anwendungen, die in den Protokolleinträgen ereignis-ID 5960 aufgeführt sind, die folgenden Schritte aus:  
   1. Suchen Sie den **Eintrag PackageStatus.**
   2. Legen Sie den Wert von **PackageStatus** auf 0 **(null) fest.**
   > [!NOTE]  
   > Wenn unter **PackageList** keine Einträge für die Anwendung enthalten sind, hat das Problem eine andere Ursache. Im Fall des Beispielereignis in diesem Artikel wird der vollständige Unterschlüssel **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**
4. Starten Sie den Computer neu.

## <a name="get-additional-help"></a>Zusätzliche Hilfe abrufen

Wenn Sie weitere Hilfe bei der Lösung eines Problems benötigen, das beim Packen, Bereitstellen oder Abfragen eines Windows-App-Pakets (.msix/.appx) als Entwickler auftritt, lesen Sie diese zusätzlichen Supportressourcen für Entwickler.

- [Microsoft Q&A](/answers/topics/uwp.html?filter=all&sort=active) bietet relevante und zeitnahe Antworten auf Ihre technischen Probleme aus einer Community von Experten und Microsoft-Technikern.
- Um Unterstützung von der Community bei Entwicklungsfragen zu erhalten, gibt es unsere [Foren](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required)und [StackOverflow](https://stackoverflow.com/questions).
- Auf [der Supportwebsite für Windows Entwickler](https://developer.microsoft.com/windows/support) werden weitere Supportoptionen erläutert.

## <a name="related-topics"></a>Zugehörige Themen

- [Signieren eines App-Pakets mit SignTool](how-to-sign-a-package-using-signtool.md)
- [Behandeln von Fehlern bei der Signatur von App-Paketen](how-to-troubleshoot-app-package-signature-errors.md)
