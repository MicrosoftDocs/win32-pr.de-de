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
ms.openlocfilehash: c6438f9a8d600e9df6956f61bb6317cec575c57f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480596"
---
# <a name="troubleshooting-packaging-deployment-and-query-of-windows-apps"></a>Problembehandlung beim Packen, Bereitstellen und Abfragen von Windows-Apps

Verwenden Sie diese Vorschläge, um Probleme zu beheben, die beim Packen, Bereitstellen oder Abfragen eines Windows-App-Pakets (.msix/.appx) als Entwickler auftreten.

> [!NOTE]
> Dieser Artikel richtet sich an Entwickler. Wenn Sie kein Entwickler sind und Hilfe zu einem Windows App-Installationsfehler suchen, finden Sie weitere Informationen unter [Windows Support](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10).

## <a name="get-diagnostic-information"></a>Abrufen von Diagnoseinformationen

Wenn eine API fehlschlägt, wird ein Fehlercode zurückgegeben, der das Problem beschreibt. Wenn der Fehlercode nicht genügend Informationen bereitstellt, finden Sie weitere Diagnoseinformationen in den ausführlichen Ereignisprotokollen.

Führen Sie die folgenden Schritte aus, um mit **Ereignisanzeige** auf die Paket- und Bereitstellungsereignisprotokolle zuzugreifen:

1. Führen Sie einen der folgenden Schritte aus:

    * Klicken Sie im menü Windows auf **Start,** geben Sie **Ereignisanzeige** ein, und **drücken Sie die EINGABETASTE.**
    * Führen Sie **eventvwr.msc aus.**

2. Erweitern Sie auf der linken Seite **Ereignisanzeige (lokal)**  >  **Anwendungs- und Dienstprotokolle**  >  **Microsoft**  >  **Windows**.
3. Suchen Sie nach verfügbaren Protokollen in diesen Kategorien:

    * **AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/Operational**
    * **AppXDeployment-Server**  >  **Microsoft-Windows-AppXDeploymentServer/Operational**

Sehen Sie sich zunächst die Protokolle unter **AppXDeployment-Server** an. Wenn der Fehler durch **0x80073CF0** oder **ERROR_INSTALL_OPEN_PACKAGE_FAILED** verursacht wurde, sind möglicherweise zusätzliche Details in den **AppxpackagingOM-Protokollen** vorhanden.

Sie können auch den Befehl [Get-AppxLog](/powershell/module/appx/get-appxlog) in PowerShell verwenden, um die ersten protokollierten Ereignisse abzurufen. Im folgenden Beispiel werden die Protokolle angezeigt, die dem letzten Bereitstellungsvorgang zugeordnet sind.

```PowerShell
Get-Appxlog
```

Im folgenden Beispiel werden die Protokolle, die dem letzten Bereitstellungsvorgang zugeordnet sind, in einer interaktiven Tabelle in einem separaten Fenster angezeigt.

```PowerShell
Get-Appxlog | Out-GridView
```

## <a name="common-error-codes"></a>Häufige Fehlermeldungen

In dieser Tabelle sind einige der häufigsten Fehlercodes aufgeführt. Wenn Sie weitere Hilfe bei einem dieser Fehler benötigen oder wenn ein Fehlercode auftritt, der nicht in dieser Liste enthalten ist, finden Sie [weitere Hilfeoptionen.](#get-additional-help)


| Fehlercode | Wert | Beschreibung und mögliche Ursachen | 
|------------|-------|---------------------------------|
| <strong>E_FILENOTFOUND</strong> | 0x80070002 | Datei oder Pfad nicht gefunden. Dies kann während einer COM-Typelib-Überprüfung auftreten, bei der der Pfad für das Verzeichnis tatsächlich in Ihrem MSIX-Paket vorhanden ist.<br /> | 
| <strong>ERROR_BAD_FORMAT</strong> | 0x8007000B | Das Paket ist nicht ordnungsgemäß formatiert und muss neu erstellt oder neu signiert werden.<br /> Dieser Fehler tritt möglicherweise auf, wenn zwischen dem Antragstellernamen des Signaturzertifikats und dem Namen des AppxManifest.xml Herausgebers ein Konflikt besteht.<br /> Weitere Informationen finden Sie <a href="how-to-sign-a-package-using-signtool.md">unter Signieren eines App-Pakets mit SignTool.</a><br /> | 
| <strong>E_INVALIDARG</strong> | 0x80070057 | Mindestens ein Argument ist ungültig. Wenn Sie das ereignisprotokoll AppXDeployment-Server überprüfen und das folgende Ereignis angezeigt wird: "Während der Installation des Pakets konnte das System die Erweiterung windows.repositoryExtension aufgrund des folgenden Fehlers nicht registrieren: Der Parameter ist falsch." <br /> Dieser Fehler kann auftreten, wenn die Manifestelemente DisplayName oder Description Zeichen enthalten, die von Windows Firewall nicht zugelassen werden. Nämlich  |  und alle , aufgrund dessen Windows das AppContainer-Profil für das Paket nicht erstellen kann. Entfernen Sie diese Zeichen aus dem Manifest, und versuchen Sie, das Paket zu installieren. <br /> | 
| <strong>ERROR_INSTALL_OPEN_</strong><br /><strong>PACKAGE_FAILED</strong><br /> | 0x80073CF0 | Das Paket konnte nicht geöffnet werden.<br /> Mögliche Ursachen:<br /><ul><li>Das Paket ist nicht signiert.</li><li>Der Name des Herausgebers stimmt nicht mit dem Signaturzertifikat-Antragsteller überein.</li><li>Das präfix file:// fehlt, oder das Paket konnte am angegebenen Speicherort nicht gefunden werden.</li></ul>Weitere Informationen finden Sie im <strong>AppxPackagingOM-Ereignisprotokoll.</strong><br /> | 
| <strong>ERROR_INSTALL_PACKAGE_</strong><br /><strong>NOT_FOUND</strong><br /> | 0x80073CF1 | Das Paket konnte nicht gefunden werden.<br /> Dieser Fehler tritt möglicherweise auf, wenn Sie ein Paket entfernen, das für den aktuellen Benutzer nicht installiert ist.<br /> | 
| <strong>ERROR_INSTALL_INVALID_</strong><br /><strong>PAKET</strong><br /> | 0x80073CF2 | Die Paketdaten sind ungültig.<br /> | 
| <strong>ERROR_INSTALL_RESOLVE_</strong><br /><strong>DEPENDENCY_FAILED</strong><br /> | 0x80073CF3 | Fehler bei Updates, Abhängigkeiten oder Konfliktüberprüfung des Pakets.<br /> Mögliche Ursachen:<br /><ul><li>Das eingehende Paket ist mit einem installierten Paket nicht vereinbar.</li><li>Eine angegebene Paketabhängigkeit kann nicht gefunden werden.</li><li>Das Paket unterstützt nicht die richtige Prozessorarchitektur.</li></ul>Weitere Informationen finden Sie im <strong>Ereignisprotokoll AppXDeployment-Server.</strong><br /> | 
| <strong>ERROR_INSTALL_OUT_</strong><br /><strong>OF_DISK_SPACE</strong><br /> | 0x80073CF4 | Auf Ihrem Computer ist nicht genügend Speicherplatz vorhanden. Geben Sie Speicherplatz frei, und versuchen Sie es erneut.<br /> | 
| <strong>ERROR_INSTALL_NETWORK_</strong><br /><strong>FEHLER</strong><br /> | 0x80073CF5 | Das Paket kann nicht heruntergeladen werden.<br /> | 
| <strong>ERROR_INSTALL_</strong><br /><strong>REGISTRATION_FAILURE</strong><br /> | 0x80073CF6 | Das Paket kann nicht registriert werden.<br /> Weitere Informationen finden Sie im <strong>Ereignisprotokoll AppXDeployment-Server.</strong><br /> | 
| <strong>ERROR_INSTALL_</strong><br /><strong>DEREGISTRATION_EFAILURE</strong><br /> | 0x80073CF7 | Die Registrierung des Pakets kann nicht aufgehoben werden.<br /> Dieser Fehler kann beim Entfernen eines Pakets auftreten.<br /> Weitere Informationen finden Sie im <strong>Ereignisprotokoll AppXDeployment-Server.</strong><br /> | 
| <strong>ERROR_INSTALL_CANCEL</strong> | 0x80073CF8 | Der Benutzer hat die Installationsanforderung abgebrochen.<br /> | 
| <strong>ERROR_INSTALL_FAILED</strong> | 0x80073CF9 | Fehler bei der Paketinstallation. Wenden Sie sich an den Softwareanbieter.<br /> Weitere Informationen finden Sie im <strong>Ereignisprotokoll AppXDeployment-Server.</strong><br /> | 
| <strong>ERROR_REMOVE_FAILED</strong> | 0x80073CFA | Fehler beim Entfernen des Pakets.<br /> Möglicherweise erhalten Sie diesen Fehler bei Fehlern, die während der Paketdeinstallation auftreten.<br /> Weitere Informationen finden Sie unter <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>RemovePackageAsync.</strong></a><br /> | 
| <strong>ERROR_PACKAGE_</strong><br /><strong>ALREADY_EXISTS</strong><br /> | 0x80073CFB | Das bereitgestellte Paket ist bereits installiert, und eine erneute Installation des Pakets wird blockiert. <br /> Dieser Fehler kann auftreten, wenn Sie ein Paket installieren, das nicht bitweise identisch mit dem bereits installierten Paket ist. Beachten Sie, dass die digitale Signatur auch Teil des Pakets ist. Wenn ein Paket neu erstellt oder zurückgesetzt wird, ist es daher nicht mehr bitweise identisch mit dem zuvor installierten Paket. Zwei mögliche Optionen zum Beheben dieses Fehlers sind: (1) Erhöhen Sie die Versionsnummer der App, erstellen Sie das Paket neu, und stellen Sie es neu (2) Entfernen Sie das alte Paket für jeden Benutzer auf dem System, bevor Sie das neue Paket installieren. <br /> | 
| <strong>ERROR_NEEDS_REMEDIATION</strong> | 0x80073CFC | Die App kann nicht gestartet werden. Versuchen Sie, die App neu zu installieren.<br /> | 
| <strong>ERROR_INSTALL_</strong><br /><strong>PREREQUISITE_FAILED</strong><br /> | 0x80073CFD | Eine angegebene Installationsvoraussetzungen konnten nicht erfüllt werden.<br /> | 
| <strong>ERROR_PACKAGE_</strong><br /><strong>REPOSITORY_CORRUPTED</strong><br /> | 0x80073CFE | Das Paket-Repository ist beschädigt.<br /> Dieser Fehler kann auftreten, wenn der Ordner, auf den dieser Registrierungsschlüssel verweist, nicht vorhanden oder beschädigt ist: <br /><strong>HKLM\Software\Microsoft\Windows\</strong><br /><strong>CurrentVersion\Appx\PackageRepositoryRoot</strong><br /> Aktualisieren Sie Ihren PC, um diesen Zustand wiederherzustellen.<br /> | 
| <strong>ERROR_INSTALL_</strong><br /><strong>POLICY_FAILURE</strong><br /> | 0x80073CFF | Um diese App zu installieren, benötigen Sie eine Entwicklerlizenz oder ein Querladen aktiviertes System. <br /> Dieser Fehler kann auftreten, wenn das Paket eine der folgenden Anforderungen nicht erfüllt:<br /><ul><li>Die App wird mit F5 in Visual Studio auf einem Computer mit einer Windows Entwicklerlizenz bereitgestellt.</li><li>Das Paket wird mit einer Microsoft-Signatur signiert und als Teil von Windows oder über die Microsoft Store bereitgestellt.</li><li>Das Paket wird mit einer vertrauenswürdigen Signatur signiert und auf einem Computer mit einer Entwicklerlizenz, einem in die Domäne eingebundenen Computer mit aktivierter Richtlinie AllowAllTrustedApps oder einem Computer mit einer Windows Sideloading-Lizenz mit aktivierter AllowAllTrustedApps-Richtlinie installiert.</li></ul> | 
| <strong>ERROR_PACKAGE_UPDATING</strong> | 0x80073D00 | Die App kann nicht gestartet werden, da sie gerade aktualisiert wird.<br /> | 
| <strong>ERROR_DEPLOYMENT_</strong><br /><strong>BLOCKED_BY_POLICY</strong><br /> | 0x80073D01 | Der Paketbereitstellungsvorgang wird durch eine Richtlinie blockiert. Wenden Sie sich an Ihren Systemadministrator.<br /> Mögliche Ursachen:<br /><ul><li>Die Paketbereitstellung wird durch Anwendungssteuerungsrichtlinien blockiert.</li><li>Die Paketbereitstellung wird durch die Richtlinie "Bereitstellungsvorgänge in speziellen Profilen zulassen" blockiert.</li></ul>Einer der möglichen Gründe ist die Notwendigkeit eines Roamingprofils. Informationen zum Einrichten von Roamingbenutzerprofilen für Benutzerkonten finden Sie unter <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">Bereitstellen von Roamingbenutzerprofilen.</a> Wenn auf Ihrem System keine Richtlinien konfiguriert sind und dieser Fehler weiterhin angezeigt wird, sind Sie möglicherweise mit einem temporären Profil angemeldet. Melden Sie sich ab, melden Sie sich erneut an, und wiederholen Sie dann den Vorgang.<br /> | 
| <strong>ERROR_PACKAGES_IN_USE</strong> | 0x80073D02 | Das Paket konnte nicht installiert werden, da die geänderten Ressourcen derzeit verwendet werden.<br /> | 
| <strong>ERROR_RECOVERY_</strong><br /><strong>FILE_CORRUPT</strong><br /> | 0x80073D03 | Das Paket konnte nicht wiederhergestellt werden, da die für die Wiederherstellung erforderlichen Daten beschädigt sind.<br /> | 
| <strong>ERROR_INVALID_</strong><br /><strong>STAGED_SIGNATURE</strong><br /> | 0x80073D04 | Die Signatur ist ungültig. Um sich im Entwicklermodus zu registrieren, müssen AppxSignature.p7x und AppxBlockMap.xml gültig sein oder nicht vorhanden sein.<br /> Wenn Sie ein Entwickler sind, der F5 mit Visual Studio verwendet, stellen Sie sicher, dass Ihr erstelltes Projektverzeichnis keine Signatur- oder Blockzuordnungsdateien aus früheren Versionen des Pakets enthält.<br /> | 
| <strong>ERROR_DELETING_EXISTING_</strong><br /><strong>APPLICATIONDATA_STORE_FAILED</strong><br /> | 0x80073D05 | Fehler beim Löschen der zuvor vorhandenen Anwendungsdaten des Pakets.<br /> Sie können diesen Fehler erhalten, wenn der <a href="/previous-versions/hh441475(v=vs.110)">Simulator</a> ausgeführt wird. Schließen Sie den Simulator. Sie können diesen Fehler auch erhalten, wenn dateien in den App-Daten geöffnet sind (z. B. wenn eine Protokolldatei in einem Text-Editor geöffnet ist).<br /> | 
| <strong>ERROR_INSTALL_</strong><br /><strong>PACKAGE_DOWNGRADE</strong><br /> | 0x80073D06 | Das Paket konnte nicht installiert werden, da bereits eine höhere Version dieses Pakets installiert ist.<br /> | 
| <strong>ERROR_SYSTEM_</strong><br /><strong>NEEDS_REMEDIATION</strong><br /> | 0x80073D07 | Ein Fehler in einer Systembinärdatei wurde erkannt. Versuchen Sie, den PC zu aktualisieren, um das Problem zu beheben. <br /> | 
| <strong>ERROR_APPX_INTEGRITY_</strong><br /><strong>FAILURE_EXTERNAL</strong><br /> | 0x80073D08 | Auf dem System wurde eine beschädigte, nicht Windows Binärdatei erkannt. <br /> | 
| <strong>ERROR_RESILIENCY_</strong><br /><strong>FILE_CORRUPT</strong><br /> | 0x80073D09 | Der Vorgang konnte nicht fortgesetzt werden, da die für die Wiederherstellung erforderlichen Daten beschädigt sind. <br /> | 
| <strong>ERROR_INSTALL_FIREWALL_</strong><br /><strong>SERVICE_NOT_RUNNING</strong><br /> | 0x80073D0A | Das Paket konnte nicht installiert werden, da der Windows Firewalldienst nicht ausgeführt wird. Aktivieren Sie den Windows Firewalldienst, und versuchen Sie es erneut.<br /> | 
| <strong>ERROR_PACKAGE_MOVE_FAILED</strong> | 0x80073D0B | Fehler beim Verschieben des Pakets.<br /> | 
| <strong>ERROR_INSTALL_VOLUME_</strong><br /><strong>NOT_EMPTY</strong><br /> | 0x80073D0C | Fehler beim Bereitstellungsvorgang, weil das Volume nicht leer ist.<br /> | 
| <strong>ERROR_INSTALL_VOLUME_</strong><br /><strong>OFFLINE</strong><br /> | 0x80073D0D | Fehler beim Bereitstellungsvorgang, da das Volume offline ist. Bei einem Paketupdate bezieht sich das Volume auf das installierte Volume aller Paketversionen.<br /> | 
| <strong>ERROR_INSTALL_VOLUME_</strong><br /><strong>BESCHÄDIGT</strong><br /> | 0x80073D0E | Fehler beim Bereitstellungsvorgang, da das angegebene Volume beschädigt ist.<br /> | 
| <strong>ERROR_NEEDS_REGISTRATION</strong><br /><strong></strong><br /> | 0x80073D0F | Fehler beim Bereitstellungsvorgang, da die angegebene Anwendung zuerst registriert werden muss.<br /> | 
| <strong>ERROR_INSTALL_WRONG_</strong><br /><strong>PROCESSOR_ARCHITECTURE</strong><br /> | 0x80073D10 | Fehler beim Bereitstellungsvorgang, da das Paket auf die falsche Prozessorarchitektur zielt.<br /> | 
| <strong>ERROR_DEV_SIDELOAD_</strong><br /><strong>LIMIT_EXCEEDED</strong><br /> | 0x80073D11 | Sie haben die maximale Anzahl von von Entwicklern sideloaded-Paketen erreicht, die auf diesem Gerät zulässig sind. Deinstallieren Sie ein sideloaded-Paket, und versuchen Sie es erneut.<br /> | 
| <strong>ERROR_INSTALL_OPTIONAL_</strong><br /><strong>PACKAGE_REQUIRES_</strong><br /><strong>MAIN_PACKAGE</strong><br /> | 0x80073D12 | Zum Installieren dieses optionalen Pakets ist ein Haupt-App-Paket erforderlich. Installieren Sie zuerst das Hauptpaket, und versuchen Sie es erneut.<br /> | 
| <strong>ERROR_PACKAGE_NOT_</strong><br /><strong>SUPPORTED_ON_FILESYSTEM</strong><br /> | 0x80073D13 | Dieser App-Pakettyp wird in diesem Dateisystem nicht unterstützt.<br /> | 
| <strong>ERROR_PACKAGE_MOVE_</strong><br /><strong>BLOCKED_BY_STREAMING</strong><br /> | 0x80073D14 | Der Vorgang zum Verschieben von Paketen wird blockiert, bis das Streaming der Anwendung abgeschlossen ist.<br /> | 
| <strong>ERROR_INSTALL_OPTIONAL_</strong><br /><strong>PACKAGE_APPLICATIONID_</strong><br /><strong>NOT_UNIQUE</strong><br /> | 0x80073D15 | Ein Haupt- oder ein anderes optionales App-Paket verfügt über die gleiche Anwendungs-ID wie dieses optionale Paket. Ändern Sie die Anwendungs-ID für das optionale Paket, um Konflikte zu vermeiden.<br /> | 
| <strong>ERROR_PACKAGE_STAGING_</strong><br /><strong>ONHOLD</strong><br /> | 0x80073D16 | Diese Stagingsitzung wurde gehalten, damit ein anderer Stagingvorgang priorisiert werden kann.<br /> | 
| <strong>ERROR_INSTALL_INVALID_</strong><br /><strong>RELATED_SET_UPDATE</strong><br /> | 0x80073D17 | Ein verwandter Satz kann nicht aktualisiert werden, da der aktualisierte Satz ungültig ist. Alle Pakete in der verknüpften Gruppe müssen gleichzeitig aktualisiert werden.<br /> | 
| <strong>ERROR_INSTALL_OPTIONAL_</strong><br /><strong>PACKAGE_REQUIRES_MAIN_</strong><br /><strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br /> | 0x80073D18 | Für ein optionales Paket mit einem FullTrust-Einstiegspunkt muss das Hauptpaket über die <strong>Funktion runFullTrust</strong> verfügen.<br /> | 
| <strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br /><strong>BY_USER_LOG_OFF</strong><br /> | 0x80073D19 | Ein Fehler ist aufgetreten, weil ein Benutzer abgemelgt wurde.<br /> | 
| <strong>ERROR_PROVISION_OPTIONAL_</strong><br /><strong>PACKAGE_REQUIRES_MAIN_</strong><br /><strong>PACKAGE_PROVISIONED</strong><br /> | 0x80073D1A | Für eine optionale Paketbereitstellung muss auch das Abhängigkeits-Hauptpaket bereitgestellt werden.<br /> | 
| <strong>ERROR_PACKAGES_REPUTATION_</strong><br /><strong>CHECK_FAILED</strong><br /> | 0x80073D1B | Fehler bei den Paketen bei <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">der SmartScreen-Reputationsprüfung.</a><br /> | 
| <strong>ERROR_PACKAGES_REPUTATION_</strong><br /><strong>CHECK_TIMEDOUT</strong><br /> | 0x80073D1C | Beim <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen-Überprüfungsvorgang für</a> die Reputation ist ein Time out erfolgt.<br /> | 
| <strong>ERROR_DEPLOYMENT_OPTION_</strong><br /><strong>NOT_SUPPORTED</strong><br /> | 0x80073D1D | Die aktuelle Bereitstellungsoption wird nicht unterstützt.<br /> | 
| <strong>ERROR_APPINSTALLER_</strong><br /><strong>ACTIVATION_BLOCKED</strong><br /> | 0x80073D1E | Die Aktivierung wird aufgrund der Updateeinstellungen von .appinstaller für diese App blockiert.<br /> | 
| <strong>ERROR_REGISTRATION_FROM_</strong><br /><strong>REMOTE_DRIVE_NOT_SUPPORTED</strong><br /> | 0x80073D1F | Remotelaufwerke werden nicht unterstützt. Verwenden <strong> \\ Sie server\share,</strong> um ein Remotepaket zu registrieren.<br /> | 
| <strong>ERROR_APPX_RAW_</strong><br /><strong>DATA_WRITE_FAILED</strong><br /> | 0x80073D20 | Fehler beim Verarbeiten und Schreiben heruntergeladener Paketdaten auf den Datenträger.<br /> | 
| <strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br /><strong>BY_VOLUME_POLICY_PACKAGE</strong><br /> | 0x80073D21 | Der Bereitstellungsvorgang wurde aufgrund einer Richtlinie pro Paketfamilie blockiert, die Bereitstellungen auf einem nicht systembasierten Volume einschränkt. Pro Richtlinie muss diese App auf dem Systemlaufwerk installiert sein, aber dies ist nicht als Standard festgelegt. Ändern Storage einstellungen das Systemlaufwerk zum Standardspeicherort, um neue Inhalte zu speichern, und wiederholen Sie dann die Installation.<br /> | 
| <strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br /><strong>BY_VOLUME_POLICY_MACHINE</strong><br /> | 0x80073D22 | Der Bereitstellungsvorgang wurde aufgrund einer computerweiten Richtlinie blockiert, die Bereitstellungen auf einem nicht systembasierten Volume einschränkt. Pro Richtlinie muss diese App auf dem Systemlaufwerk installiert sein, aber dies ist nicht als Standard festgelegt. Machen Sie Storage Einstellungen das Systemlaufwerk zum Standardspeicherort, um neue Inhalte zu speichern, und wiederholen Sie dann die Installation.<br /> | 
| <strong>ERROR_DEPLOYMENT_BLOCKED_</strong><br /><strong>BY_PROFILE_POLICY</strong><br /> | 0x80073D23 | Der Bereitstellungsvorgang wurde blockiert, weil die Bereitstellung eines speziellen Profils nicht zulässig ist (spezielle Profile sind Benutzerprofile, bei denen Änderungen verworfen werden, nachdem sich der Benutzer abmeldet). Versuchen Sie, sich bei einem Konto anzumelden, das kein spezielles Profil ist. Sie können versuchen, sich beim aktuellen Konto anzumelden oder sich bei einem anderen Konto anzumelden.<br /> | 
| <strong>ERROR_DEPLOYMENT_FAILED_</strong><br /><strong>CONFLICTING_MUTABLE_PACKAGE_</strong><br /><strong>VERZEICHNIS</strong><br /> | 0x80073D24 | Fehler beim Bereitstellungsvorgang aufgrund des <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">änderbaren Paketverzeichnisses</a>eines in Konflikt geratenen Pakets. Entfernen Sie zum Installieren dieses Pakets das vorhandene Paket mit dem in Konflikt stehenden änderbaren Paketverzeichnis.<br /> | 
| <strong>ERROR_SINGLETON_RESOURCE_</strong><br /><strong>INSTALLED_IN_ACTIVE_USER</strong><br /> | 0x80073D25 | Fehler bei der Paketinstallation, weil eine Singletonressource angegeben wurde und ein anderer Benutzer mit dem installierten Paket angemeldet ist. Stellen Sie sicher, dass alle aktiven Benutzer mit installierten Paketen abgemeldet sind, und wiederholen Sie die Installation.<br /> | 
| ERROR_DIFFERENT_VERSION_<strong></strong><br /><strong>OF_PACKAGED_SERVICE_INSTALLED</strong><br /> | 0x80073D26 | Fehler bei der Paketinstallation, weil eine andere Version des Diensts installiert ist. Versuchen Sie, eine neuere Version des Pakets zu installieren.<br /> | 
| <strong>ERROR_SERVICE_EXISTS_</strong><br /><strong>AS_NON_PACKAGED_SERVICE</strong><br /> | 0x80073D27 | Fehler bei der Paketinstallation, weil eine Version des Diensts außerhalb eines .msix/.appx-Pakets vorhanden ist. Wenden Sie sich an Ihren Softwareanbieter.<br /> | 
| <strong>ERROR_PACKAGED_SERVICE_</strong><br /><strong>REQUIRES_ADMIN_PRIVILEGES</strong><br /> | 0x80073D28 | Fehler bei der Paketinstallation, weil Administratorrechte erforderlich sind. Wenden Sie sich an einen Administrator, um dieses Paket zu installieren.<br /> | 
| <strong>ERROR_REDIRECTION_TO_</strong><br /><strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong><br /> | 0x80073D29 | Fehler bei der Paketbereitstellung, da der Vorgang an das Standardkonto umgeleitet worden wäre, wenn der Aufrufer dies nicht gesagt hat.<br /> | 
| <strong>ERROR_PACKAGE_LACKS_</strong><br /><strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong><br /> | 0x80073D2A | Fehler bei der Paketbereitstellung, weil für das Paket eine Funktion erforderlich ist, um diesen Host nativ als Ziel festzulegen.<br /> | 
| <strong>ERROR_UNSIGNED_PACKAGE_</strong><br /><strong>INVALID_CONTENT</strong><br /> | 0x80073D2B | Fehler bei der Paketbereitstellung, weil der Inhalt für ein nicht signiertes Paket ungültig ist.<br /> | 
| <strong>ERROR_UNSIGNED_PACKAGE_</strong><br /><strong>INVALID_PUBLISHER_NAMESPACE</strong><br /> | 0x80073D2C | Fehler bei der Paketbereitstellung, weil sich der Herausgeber nicht im Namespace ohne Vorzeichen befindet.<br /> | 
| <strong>ERROR_SIGNED_PACKAGE_</strong><br /><strong>INVALID_PUBLISHER_NAMESPACE</strong><br /> | 0x80073D2D | Fehler bei der Paketbereitstellung, weil sich der Herausgeber nicht im signierten Namespace befindet.<br /> | 
| <strong>ERROR_PACKAGE_EXTERNAL_</strong><br /><strong>LOCATION_NOT_ALLOWED</strong><br /> | 0x80073D2E | Fehler bei der Paketbereitstellung, weil sich der Herausgeber nicht im signierten Namespace befindet.<br /> | 
| <strong>ERROR_INSTALL_FULLTRUST_</strong><br /><strong>HOSTRUNTIME_REQUIRES_MAIN_</strong><br /><strong>PACKAGE_FULLTRUST_CAPABILITY</strong><br /> | 0x80073D2F | Eine Hostruntimeabhängigkeit, die in ein Paket mit vollständig vertrauenswürdigem Inhalt aufgelöst wird, erfordert, dass das Hauptpaket über die <strong>runFullTrust-Funktion</strong> verfügt.<br /> | 
| <strong>APPX_E_PACKAGING_INTERNAL</strong> | 0x80080200 | Bei der Paket-API ist ein interner Fehler aufgetreten.<br /> | 
| <strong>APPX_E_INTERLEAVING_</strong><br /><strong>NOT_ALLOWED</strong><br /> | 0x80080201 | Das Paket ist ungültig, da sein Inhalt überlappend ist.<br /> | 
| <strong>APPX_E_RELATIONSHIPS_</strong><br /><strong>NOT_ALLOWED</strong><br /> | 0x80080202 | Das Paket ist ungültig, da es OPC-Beziehungen enthält.<br /> | 
| <strong>APPX_E_MISSING_</strong><br /><strong>REQUIRED_FILE</strong><br /> | 0x80080203 | Das Paket ist ungültig, da ein Manifest oder eine Blockzuordnung fehlt oder eine Codeintegritätsdatei vorhanden ist, aber eine Signaturdatei fehlt.<br /> Stellen Sie sicher, dass dem Paket mindestens eine dieser erforderlichen Dateien nicht fehlt:<br /><ul><li>\AppxManifest.xml</li><li>\AppxBlockMap.xml</li></ul>Wenn das Paket \AppxMetadata\CodeIntegrity.cat enthält, muss es auch \AppxSignature.p7x enthalten.<br /> | 
| <strong>APPX_E_INVALID_MANIFEST</strong> | 0x80080204 | Die AppxManifest.xml-Datei des Pakets ist ungültig.<br /> | 
| <strong>APPX_E_INVALID_BLOCKMAP</strong> | 0x80080205 | Die AppxBlockMap.xml-Datei des Pakets ist ungültig.<br /> | 
| <strong>APPX_E_CORRUPT_CONTENT</strong> | 0x80080206 | Der Paketinhalt kann nicht gelesen werden, da er beschädigt ist.<br /> | 
| <strong>APPX_E_BLOCK_</strong><br /><strong>HASH_INVALID</strong><br /> | 0x80080207 | Der berechnete Hashwert des Blocks stimmt nicht mit dem wert überein, der in der Blockzuordnung gespeichert ist.<br /> | 
| <strong>APPX_E_REQUESTED_</strong><br /><strong>RANGE_TOO_LARGE</strong><br /> | 0x80080208 | Der angeforderte Bytebereich liegt über 4 GB, wenn er in einen Bytebereich von Blöcken übersetzt wird.<br /> | 
| <strong>TRUST_E_NOSIGNATURE</strong> | 0x800B0100 | Im Betreff ist keine Signatur vorhanden.<br /> Dieser Fehler wird möglicherweise angezeigt, wenn das Paket nicht signiert ist oder die Signatur ungültig ist. Das Paket muss signiert sein, um bereitgestellt zu werden.<br /> | 
| <strong>CERT_E_UNTRUSTEDROOT</strong> | 0x800B0109 | Eine Zertifikatkette wurde verarbeitet, aber in einem Stammzertifikat beendet, das vom Vertrauensanbieter nicht als vertrauenswürdig eingestuft wird.<br /> Weitere Informationen <a href="/previous-versions/br230260(v=vs.110)">finden Sie unter Signieren eines Pakets.</a><br /> | 
| <strong>CERT_E_CHAINING</strong> | 0x800B010A | Eine Zertifikatkette konnte nicht für eine vertrauenswürdige Stammzertifizierungsstelle erstellt werden.<br /> Weitere Informationen <a href="/previous-versions/br230260(v=vs.110)">finden Sie unter Signieren eines Pakets.</a><br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>SIP_CLIENT_DATA</strong><br /> | 0x80080209 | Die <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO,</strong></a>die zum Signieren des Pakets verwendet wurde, enthält nicht die erforderlichen Daten.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>KEY_INFO</strong><br /> | 0x8008020A | Die <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO,</strong></a> die zum Verschlüsseln oder Entschlüsseln des Pakets verwendet wird, enthält ungültige Daten.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>CONTENTGROUPMAP</strong><br /> | 0x8008020B | Die Inhaltsgruppenzuordnung des .msix/.appx-Pakets ist ungültig.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>APPINSTALLER</strong><br /> | 0x8008020C | Die <a href="/windows/msix/app-installer/app-installer-root">APPINSTALLER-Datei</a> für das Paket ist ungültig.<br /> | 
| <strong>APPX_E_DELTA_BASELINE_</strong><br /><strong>VERSION_MISMATCH</strong><br /> | 0x8008020D | Die Baselinepaketversion im Deltapaket ist nicht mit der Version im zu aktualisierenden Baselinepaket übereinstimmen.<br /> | 
| <strong>APPX_E_DELTA_PACKAGE_</strong><br /><strong>MISSING_FILE</strong><br /> | 0x8008020E | Im Deltapaket fehlt eine Datei aus dem aktualisierten Paket.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>DELTA_PACKAGE</strong><br /> | 0x8008020F | Das Deltapaket ist ungültig.<br /> | 
| <strong>APPX_E_DELTA_APPENDED_</strong><br /><strong>PACKAGE_NOT_ALLOWED</strong><br /> | 0x80080210 | Das angefügte Deltapaket ist für den aktuellen Vorgang nicht zulässig.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>PACKAGING_LAYOUT</strong><br /> | 0x80080211 | Die Paketlayoutdatei ist ungültig.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>PACKAGESIGNCONFIG</strong><br /> | 0x80080212 | Die PackageSignConfig-Datei ist ungültig.<br /> | 
| <strong>APPX_E_RESOURCESPRI_</strong><br /><strong>NOT_ALLOWED</strong><br /> | 0x80080213 | Die Datei resources.pri ist nicht zulässig, wenn im Paketmanifest keine Ressourcenelemente enthalten sind.<br /> | 
| <strong>APPX_E_FILE_</strong><br /><strong>COMPRESSION_MISMATCH</strong><br /> | 0x80080214 | Der Komprimierungsstatus der Datei im Baseline- und aktualisierten Paket ist nicht übereinstimmend.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>PAYLOAD_PACKAGE_EXTENSION</strong><br /> | 0x80080215 | Nicht-AppX-Erweiterungen sind für Nutzlastpakete für ältere Plattformen nicht zulässig.<br /> | 
| <strong>APPX_E_INVALID_</strong><br /><strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong><br /> | 0x80080216 | Die Datei encryptionExclusionFileList ist ungültig.<br /> | 


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
- [Problembehandlung bei Signaturfehlern von App-Paketen](how-to-troubleshoot-app-package-signature-errors.md)
