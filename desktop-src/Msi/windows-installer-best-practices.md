---
description: 'In diesem Abschnitt wird eine Liste mit Tipps aufgeführt, die mit der Hauptdokumentation Windows Installer SDK verknüpft sind, um Anwendungsentwickler, Setupautoren, IT-Experten und Infrastrukturentwickler bei der Ermittlung bewährter Methoden für die Verwendung des Windows Installers zu unterstützen:'
ms.assetid: ff48d995-fe6f-4d1b-898d-67574ed3c5b7
title: Windows Bewährte Methoden für den Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e430cf8871279e18107b3ab1deb1f347e9d4779b619ab6cf8133d30cdfa4ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808960"
---
# <a name="windows-installer-best-practices"></a>Windows Bewährte Methoden für den Installer

In diesem Abschnitt wird eine Liste mit Tipps aufgeführt, die mit der Hauptdokumentation Windows Installer SDK verknüpft sind, um Anwendungsentwickler, Setupautoren, IT-Experten und Infrastrukturentwickler bei der Ermittlung bewährter Methoden für die Verwendung des Windows Installers zu unterstützen:

-   [Aktualisieren Sie die Windows Installer-Version.](#update-the-windows-installer-version)
-   [Erfüllen Sie die Windows Logo-Zertifizierungsanforderungen.](#meet-the-windows-logo-certification-requirements)
-   [Bereiten Sie das Paket für die Lokalisierung vor.](#prepare-the-package-for-localization)
-   [Aktualisieren Sie Die Entwicklungstools und Dokumentation für den Windows Installer.](#update-your-windows-installer-development-tools-and-documentation)
-   [Wenn Sie sich dafür entscheiden, eine ältere Setupanwendung neu zu packen, befolgen Sie die bewährten Methoden für das Erneute Packen.](#if-you-decide-to-repackage-a-legacy-setup-application-follow-good-repackaging-practices)
-   [Versuchen Sie nicht, geschützte Ressourcen zu ersetzen.](#do-not-try-to-replace-protected-resources)
-   [Verlassen Sie sich nicht auf nicht kritische Ressourcen.](#do-not-depend-upon-non-critical-resources)
-   [Verwenden Sie die API, um Windows Installer-Konfigurationsinformationen abzurufen.](#use-the-api-to-retrieve-windows-installer-configuration-information)
-   [Organisieren Sie die Installation Ihrer Anwendung um Komponenten herum.](#organize-the-installation-of-your-application-around-components)
-   [Reduzieren Sie die Größe großer Windows Installer-Pakete.](#reduce-the-size-of-large-windows-installer-packages)
-   [Wenn Sie benutzerdefinierte Aktionen verwenden, befolgen Sie bewährte Methoden für benutzerdefinierte Aktionen.](#if-you-use-custom-actions-follow-good-custom-action-practices)
-   [Wenn Sie Assemblys verwenden, befolgen Sie bewährte Assemblymethoden.](#if-you-use-assemblies-follow-good-assembly-practices)
-   [Versenden Sie keine gleichzeitigen Installationen.](#do-not-ship-concurrent-installations)
-   [Halten Sie Paketnamen und Paketcodes konsistent.](#keep-package-names-and-package-codes-consistent)
-   [Verwenden Sie nicht die Tabellen SelfReg und TypeLib.](#do-not-use-the-selfreg-and-typelib-tables)
-   [Geben Sie die Option zum Installieren ohne Benutzeroberfläche an.](#provide-the-option-to-install-without-a-user-interface)
-   [Vermeiden Sie die Verwendung der AlwaysInstallElevated-Richtlinie.](#avoid-using-the-alwaysinstallelevated-policy)
-   [Aktivieren Sie die Richtlinie DisableMedia, um die nicht autorisierte Installation einzuschränken.](#enable-the-disablemedia-policy-to-limit-unauthorized-installation)
-   [Halten Sie die ursprünglichen Paketquelldateien sicher und für Benutzer verfügbar.](#keep-the-original-package-source-files-secure-and-available-to-users)
-   [Aktivieren Sie bei der Problembehandlung bei der Bereitstellung die ausführliche Protokollierung auf dem Computer des Benutzers.](#enable-verbose-logging-on-users-computer-when-troubleshooting-deployment)
-   [Durch die Deinstallation bleibt der Computer des Benutzers in einem fehlerfreien Zustand.](#uninstallation-leaves-the-users-computer-in-a-clean-state)
-   [Testen Sie Pakete für die Bereitstellung pro Benutzer und Pro-Computer-Installation.](#test-packages-for-both-per-user-and-per-machine-installation-deployment)
-   [Planen und testen Sie eine Wartungsstrategie, bevor Sie die Anwendung versenden.](#plan-and-test-a-servicing-strategy-before-shipping-the-application)
-   [Reduzieren Sie die Abhängigkeit von Updates von den ursprünglichen Quellen.](#reduce-the-dependency-of-updates-upon-the-original-sources)
-   [Verteilen Sie keine nicht verwendbaren Mergemodule.](#do-not-distribute-unserviceable-merge-modules)
-   [Vermeiden Sie das Patchen von Administratorinstallationen.](#avoid-patching-administrative-installations)
-   [Registrieren Sie Updates für die Ausführung mit erhöhten Rechten.](#register-updates-to-run-with-elevated-privilege)
-   [Verwenden Sie die MsiPatchSequence-Tabelle zum Sequenzen von Patches.](#use-the-msipatchsequence-table-to-sequence-patches)
-   [Testen Sie das Installationspaket gründlich.](#test-the-installation-package-thoroughly)
-   [Beheben Sie alle Validierungsfehler, bevor Sie ein neues oder überarbeitetes Installationspaket bereitstellen.](#fix-all-validation-errors-before-deploying-a-new-or-revised-installation-package)
-   [Erstellen sie eine sichere Installation.](#author-a-secure-installation)
-   [Verwenden von PMSIHANDLE anstelle von HANDLE](#use-pmsihandle-instead-of-handle)

## <a name="update-the-windows-installer-version"></a>Aktualisieren Sie die Windows Installer-Version.

-   Verwenden Sie Windows Installer 5.0 auf Windows Server 2008 R2 und Windows 7. Dies ist die Windows Installer-Version, die mit dem Betriebssystem bereitgestellt wird.
-   Verwenden Sie Windows Installer 4.5 auf Windows Server 2008, Windows Server 2003 mit Service Pack 1 (SP1), Windows Vista mit Service Pack 1 (SP1) oder Windows XP mit Service Pack 2 (SP2). Informationen zum Abrufen der aktuellen Version Windows Installers finden Sie unter [Windows Installer Redistributables](windows-installer-redistributables.md).
-   Verwenden Sie Windows Installer 3.1 unter Windows 2000 mit Service Pack 3 (SP3). Windows Die Installationsprogrammversion 3.1 verfügt über Features, die eine bessere Anwendungswartung und [das Patchen](patching.md)von ermöglichen.
-   Viele wichtige Features wurden mit Version 3.0 eingeführt und sind im Abschnitt [Nicht unterstützt in Windows Installer Version 2.0](not-supported-in-windows-installer-version-2-0.md)aufgeführt. Installationspakete und Updates, die für Windows Installer 2.0 erstellt wurden, können mit Windows Installer 3.0 und höher installiert werden. Patchpakete, die die neuen Tabellen enthalten, die von Windows Installer 3.0 verwendet werden, können weiterhin mit früheren Versionen von Windows Installer angewendet werden, jedoch ohne die Patchfunktionen von Windows Installer 3.0. Es ist auch möglich, Patches zu erstellen, die explizit die Windows Installer 3.0 erfordern, die von früheren Versionen von Windows Installer nicht angewendet werden können. Wenn ein Benutzer die Installationsprogrammversion nicht aktualisieren kann, stellen Sie sicher, dass Die Anwendung oder das Update mit einem zukünftigen Update des Windows Installers kompatibel ist.
-   Eine Liste der Windows Installer-Features, die von früheren Versionen des Windows Installers nicht unterstützt werden, finden Sie unter [Neuerungen in Windows Installer.](what-s-new-in-windows-installer.md)

## <a name="meet-the-windows-logo-certification-requirements"></a>Erfüllen Sie die Windows Logo-Zertifizierungsanforderungen.

-   Auch wenn Sie Ihre Anwendung nicht an das Logo-Programm übermitteln möchten, können Sie die Richtlinien für die Logozertifizierung befolgen, um ihr Windows Installer-Paket zu verbessern. Eine Übersicht über die Logoanforderungen und Links zu bestimmten Logozertifizierungsprogrammen finden Sie unter [Windows Installer und Logoanforderungen.](windows-installer-and-logo-requirements.md)

## <a name="prepare-the-package-for-localization"></a>Bereiten Sie das Paket für die Lokalisierung vor.

-   Es ist eine bewährte Methode, sich beim Erstellen des ursprünglichen Installationspakets auf die zukünftige Lokalisierung vorzubereiten. Sie können die vorgeschlagene Paketlokalisierungsprozedur unter [Lokalisieren eines Windows Installer-Pakets befolgen.](localizing-a-windows-installer-package.md)

## <a name="update-your-windows-installer-development-tools-and-documentation"></a>Aktualisieren Sie Die Entwicklungstools und Dokumentation für den Windows Installer.

-   Die [Windows Installer Development Tools](windows-installer-development-tools.md) sind nicht weitervertrenbar, und Sie sollten nur die Versionen dieser Tools verwenden, die von Microsoft verfügbar sind. Diese sind in den [Windows SDK-Komponenten für Windows Installer-Entwickler](platform-sdk-components-for-windows-installer-developers.md) im Microsoft Windows Software Development Kit (SDK) verfügbar.
-   Mehrere unabhängige Softwarehersteller bieten Tools zum Erstellen oder Ändern Windows Installer-Pakete an. Diese Tools können eine Paketerstellungsumgebung bereitstellen, die möglicherweise einfacher zu verwenden ist als die Tools, die im Windows Installer SDK bereitgestellt werden. Weitere Informationen zu diesen Tools finden Sie in den Informationsressourcen, die unter [Andere Quellen von Windows Installer-Informationen](other-sources-of-windows-installer-information.md)erläutert werden.
-   Die Möglichkeit, ein Paket aus Textdateien zu erstellen, kann für einige Entwickler intuitiver sein. Das auf [Sourceforge.net](https://sourceforge.net/projects/wix) verfügbare WIX-Toolset (Windows Installer XML) erstellt Windows Installationspakete aus XML-Quellcode.
-   Die Dokumentation im [Windows Installer SDK,](./windows-installer-portal.md) das in der MSDN Online Library veröffentlicht wurde, wird am häufigsten aktualisiert.
-   Verwenden Sie die aktuelle Version von [Msizap.exe](msizap-exe.md) (Version 3.1.4000.2726 oder höher), die in den [Windows SDK-Komponenten für Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) for Windows Vista oder höher verfügbar ist. Kleinere Versionen von Msizap.exe können Informationen zu allen Updates entfernen, die auf andere Anwendungen auf dem Computer des Benutzers angewendet wurden. Wenn diese Informationen entfernt werden, müssen diese anderen Anwendungen möglicherweise entfernt und neu installiert werden, um zusätzliche Updates zu erhalten.
-   Der [Datenbanktabellen-EditorOrca.exe](orca-exe.md) ist ein Datenbanktabellen-Editor zum Erstellen und Bearbeiten Windows Installer-Paketen und Mergemodulen. Sie verfügt über eine einfache GUI-Schnittstelle, unterstützt aber die erweiterte Bearbeitung von Windows Installer-Datenbanken. Auch wenn Sie eine andere Anwendung als primäres Entwicklungstool verwenden, ist die Verwendung von Orca.exe bei der Problembehandlung und beim Testen eines Pakets praktisch.
-   Informationen zu aktuellen Windows Installer finden Sie unter [Weitere Quellen für Windows Installer,](other-sources-of-windows-installer-information.md) die in Blogs, technischen Chats, Newsgroups, technischen Artikeln und Websites verfügbar sind.

## <a name="if-you-decide-to-repackage-a-legacy-setup-application-follow-good-repackaging-practices"></a>Wenn Sie sich dafür entscheiden, eine ältere Setupanwendung neu zu packen, befolgen Sie die bewährten Methoden für das Erneute Packen.

Viele Anwendungsanbieter stellen native Windows Installer-Pakete für die Installation oder ihre Produkte bereit. Software, die eine vorhandene Legacy-Setupanwendung in ein Windows Installer-Paket konvertiert, wird als Tool zum Erneuten Packen bezeichnet. Im Whitepaper [Step-by-Step Guide to Creating Windows Installer Packages and Repackaging Software for the Windows Installer (Schrittweise Anleitung zum Erstellen von Windows Installer-Paketen und Neupaketieren](https://www.microsoft.com/technet/prodtechnol/windows2000serv/howto/winstall.mspx) von Software für den Windows Installer) wird ein kommerziell verfügbares Tool zum Umpacken beschrieben. Das Erneute Packen einer vorhandenen Setupanwendung ist nicht die bewährte Methode für die Entwicklung. Anwendungen, die von Anfang an so entworfen wurden, dass sie von Windows Installer-Features profitieren, können für Benutzer einfacher zu installieren und zu bedienen sein. Wenn Sie sich für die Verwendung einer Neupaketsoftware entscheiden, können Sie mithilfe der folgenden Methoden ein besseres Windows Installer-Paket erstellen.

-   Neupakettools konvertieren Legacyinstallationen in ein Windows Installer-Paket, indem sie vor und nach der Installation ein Bild von einem Stagingsystem machen. Alle Registrierungsänderungen, Dateiänderungen oder Systemeinstellungen, die während des Aufzeichnungsprozesses auftreten, sind in der Installation enthalten. Konfigurieren Sie die Hardware und Software des Computers, der zum erneuten Packen der Installation verwendet wird, so nah wie möglich am System des vorgesehenen Benutzers. Erstellen Sie ein separates Paket für jede andere Hardwarekonfiguration. Erneutes Packen mithilfe eines sauberen Stagingcomputers. Entfernen Sie alle unnötigen Anwendungen. Beenden Sie alle unnötigen Prozesse. Schließen Sie alle nicht wesentlichen Systemdienste.
-   Erstellen Sie immer eine Kopie der ursprünglichen Installation, bevor Sie damit beginnen, sie zu bearbeiten. Arbeiten Sie immer an der Kopie. Beenden Sie ein Erneutes Packen niemals, bevor die Paketerstellung abgeschlossen ist. Wenn das Umpacken das Paket beschädigt, verfügen Sie weiterhin über das originale Paket.
-   Packen Sie Microsoft-Softwareupdates nicht erneut in ein Windows Installer-Paket. Microsoft veröffentlicht Softwareupdates wie Service Packs als selbstextrahierende Dateien, die die Installation automatisch durchführen. Diese Updates verwenden andere Installationsprogramme als der Windows Installer, um geschützte Windows Ressourcen zu ersetzen und können nicht in ein Windows Installer-Paket konvertiert werden. Informationen zum Bereitstellen Windows Service Packs finden Sie im Service Pack-Bereitstellungshandbuch auf [Microsoft TechNet.](https://technet.microsoft.com/)
-   Verwenden Sie kein Neupakettool, um ein Windows Installer-Paket in ein neues Paket zu konvertieren. Der Windows Installer fügt Dem System und den Anwendungsressourcen Konfigurationsinformationen hinzu. Wenn ein Neupakettool das System vor und nach der Installation vergleicht, interpretiert der Neupaketierer die Konfigurationsinformationen als Teil der Anwendung falsch. Dadurch wird in der Regel die neu gepackte Anwendung beschädigt. Verwenden Sie stattdessen [Anpassungstransformationen,](a-customization-transform-example.md) um ein vorhandenes Windows Installer-Paket zu ändern oder ein neues Paket zu erstellen. Sie können Anpassungstransformationen mit dem [Msitran.exe-Tool ](msitran-exe.md) erstellen.
-   Verwenden Sie kein Neupaketierungstool, um mehrere Pakete Windows Installer in einem einzelnen Paket zu konsolidieren. Stattdessen können Sie das tool [Msistuff.exe](msistuff-exe.md) verwenden, um die ausführbare Datei Setup.exe Bootstrap so zu konfigurieren, dass die Pakete nacheinander installiert werden.
-   Erstellen Sie Windows Installer-Paket, damit es vom Kunden problemlos angepasst werden kann. Globale Variablen, die vom Windows Installer während einer Installation verwendet werden, können mithilfe öffentlicher Eigenschaften [oder](properties.md) [Anpassungstransformationen festgelegt werden.](a-customization-transform-example.md) Stellen Sie Dokumentation für die Verwendung dieser Eigenschaften und praktische Standardwerte für alle anpassbaren Werte zur Verfügung. Informationen zum Abrufen und Festlegen von Eigenschaften finden Sie unter [Verwenden von Eigenschaften.](using-properties.md) Ein Beispiel für eine Anpassungstransformation finden Sie unter [Beispiel für eine Anpassungstransformation.](a-customization-transform-example.md)

## <a name="do-not-try-to-replace-protected-resources"></a>Versuchen Sie nicht, geschützte Ressourcen zu ersetzen.

Windows Installerpakete sollten nicht versuchen, geschützte Ressourcen während der Installation oder des Updates zu ersetzen. Der Windows Installer entfernt oder ersetzt diese Ressourcen nicht, da Windows das Ersetzen wichtiger Systemdateien, Ordner und Registrierungsschlüssel verhindert. Der Schutz dieser Ressourcen verhindert Anwendungs- und Betriebssystemfehler.

-   Bei der Ausführung auf Windows Server 2008 oder Windows Vista überspringt der Windows-Installer die Installation von Dateien oder Registrierungsschlüsseln, die durch [Windows Resource Protection](../wfp/windows-resource-protection-portal.md) (WRP) geschützt sind. Das Installationsprogramm gibt eine Warnung in die Protokolldatei ein und fährt mit dem Rest der Installation ohne Fehler fort. Weitere Informationen finden Sie unter [Using Windows Installer and Windows Resource Protection](windows-resource-protection-on-windows-vista.md).
-   WRP ist der neue Name für Windows File Protection (WFP). WRP schützt Registrierungsschlüssel und Ordner sowie wichtige Systemdateien. In Windows Server 2003, Windows XP und Windows 2000, als der Windows Installer eine WFP-geschützte Datei gefunden hat, fordert das Installationsprogramm an, dass WFP die Datei installiert. Weitere Informationen finden Sie unter [Using Windows Installer and Windows Resource Protection](windows-resource-protection-on-windows-vista.md).

## <a name="do-not-depend-upon-non-critical-resources"></a>Verlassen Sie sich nicht auf nicht kritische Ressourcen.

Die Installation oder das Update sollte aus den folgenden Gründen nicht von der Installation nicht kritischer Ressourcen abhängen.

-   Benutzerdefinierte Aktionen können fehlschlagen, wenn sie von einer Komponente abhängen, die zu einem Feature gehört, das der Benutzer anklickt und nicht installiert.
-   Benutzerdefinierte Aktionen, die vor der [InstallFinalize-Aktion](installfinalize-action.md) sequenziert wurden, können fehlschlagen, wenn sie von einer Komponente abhängen, die eine assembly enthält, die installiert wird. Der Windows Installer führt erst dann einen Commit für Assemblys in den globalen Assemblycache (GAC) durch, wenn die Aktion InstallFinalize abgeschlossen ist.

## <a name="use-the-api-to-retrieve-windows-installer-configuration-information"></a>Verwenden Sie die API, um Windows Installer-Konfigurationsinformationen abzurufen.

Die Installation Ihrer Anwendung oder Ihres Updates sollte nicht vom direkten Zugriff auf Windows Installer-Konfigurationsinformationen abhängig sein, die auf Ihrem Computer gespeichert sind. Verwenden Sie stattdessen die Windows Installer-Anwendungsprogrammierschnittstelle, um Konfigurationsinformationen abzurufen. Der Speicherort und das Format der Konfigurationsinformationen werden vom Windows Installer-Dienst verwaltet und können sich ändern.

-   Die Installations- und Konfigurationsfunktionen der Windows Installer-API werden in der [Referenz zur Installer-Funktion beschrieben.](installer-function-reference.md)
-   Die [Konfigurationseigenschaften](property-reference.md) werden in der Eigenschaftenreferenz beschrieben.
-   Die Automatisierungsmethoden und -eigenschaften werden in der [Referenz zur Automation-Schnittstelle beschrieben.](automation-interface-reference.md) Das Beispielskript, WiLstPrd.vbs verbindung mit einem Installer-Objekt herstellt und registrierte Produkte und Produktinformationen aufzählt. Weitere Informationen finden Sie [unter Auflisten von Produkten, Eigenschaften, Features und Komponenten.](list-products-properties-features-and-components.md)

## <a name="organize-the-installation-of-your-application-around-components"></a>Organisieren Sie die Installation Ihrer Anwendung um Komponenten herum.

Der Windows Installer-Dienst installiert oder entfernt Sammlungen von Ressourcen, die als Komponenten bezeichnet [werden.](windows-installer-components.md) Da Komponenten häufig freigegeben werden, muss der Autor eines Installationspakets regeln, wenn die Komponenten eines Features oder einer Anwendung angegeben werden.

-   Befolgen Sie die [](organizing-applications-into-components.md) Komponentenregeln beim Organisieren von Anwendungen in Komponenten, um sicherzustellen, dass neue Komponenten oder neue Versionen von Komponenten installiert und entfernt werden können, ohne dass andere Anwendungen beschädigt werden. Sie können das unter Definieren von [Installerkomponenten beschriebene Verfahren befolgen.](defining-installer-components.md)
-   Das Installationsprogramm verfolgt jede Komponente mit der entsprechenden Komponenten-ID-GUID nach, die in der [Komponententabelle angegeben ist.](component-table.md) Für den Betrieb des Referenzzählmechanismus des Windows Installers ist es wichtig, dass die Komponenten-ID-GUID korrekt ist. Befolgen Sie die Richtlinien unter [Ändern des Komponentencodes.](changing-the-component-code.md)
-   Wenn Ihr Paket die Komponentenregeln nicht einhalten muss, beachten Sie die möglichen Konsequenzen, und stellen Sie sicher, dass Ihre Installation diese Komponenten niemals installiert, wo sie Komponenten auf dem System des Benutzers beschädigen können. Weitere Informationen finden Sie [unter Was geschieht, wenn die Komponentenregeln verletzt werden?](what-happens-if-the-component-rules-are-broken.md).
-   Beachten Sie, wie der Windows Installer beim Ersetzen vorhandener Dateien die [Dateiversionsregeln](file-versioning-rules.md) [an wendet.](replacing-existing-files.md) Der Windows Installer bestimmt zunächst, ob die Schlüsseldatei der Komponente bereits installiert ist, bevor versucht wird, eine der Dateien der Komponente zu installieren. Wenn das Installationsprogramm eine Datei mit dem gleichen Namen wie die Schlüsseldatei der Komponente findet, die am Zielspeicherort installiert ist, vergleicht es Version, Datum und Sprache der beiden Schlüsseldateien und verwendet Dateiversionsregeln, um zu bestimmen, ob die vom Paket bereitgestellte Komponente installiert werden soll. Wenn das Installationsprogramm feststellt, dass die Komponentenbasis auf der Schlüsseldatei ersetzt werden muss, verwendet es die Dateiversionsregeln für jede installierte Datei, um zu bestimmen, ob die Datei ersetzt werden soll.

## <a name="reduce-the-size-of-large-windows-installer-packages"></a>Reduzieren Sie die Größe von großen Windows Installer-Paketen.

Sehr große Windows Pakete nehmen Systemressourcen und können für Benutzer schwierig zu installieren sein. Es wird bewährte Methode, die Größe sehr großer Installationspakete Windows folgenden Methoden zu reduzieren.

-   Komprimieren Sie die Dateien in der Installation, und speichern Sie sie in einer .cab Datei . Mit dem Installer kann .cab Datei als separate externe Datei oder als Datenstrom im MSI-Paket selbst gespeichert werden. Weitere Informationen finden Sie [unter Verwenden von Schränken und komprimierten Quellen.](using-cabinets-and-compressed-sources.md)
-   Entfernen Sie verschwendeten Speicherplatz in der .msi-Datei mithilfe einer der Unter Reduzieren der Größe einer .msi [Datei erläuterten Optionen.](reducing-the-size-of-an--msi-file.md)
-   Wenn Ihr Windows Installer-Paket mehr als 32767 Dateien enthält, müssen Sie das Schema der Datenbank ändern. Weitere Informationen finden Sie [unter Erstellen eines großen Pakets.](authoring-a-large-package.md)

## <a name="if-you-use-custom-actions-follow-good-custom-action-practices"></a>Wenn Sie benutzerdefinierte Aktionen verwenden, befolgen Sie die bewährten Methoden für benutzerdefinierte Aktionen.

Der Windows Installer verfügt über viele integrierte [Standardaktionen](standard-actions-reference.md) für die Installation und Wartung von Anwendungen. Entwickler sollten versuchen, sich so weit wie möglich auf die Standardaktionen zu verlassen, anstatt ihre eigenen benutzerdefinierten [Aktionen zu erstellen.](custom-actions.md) Es gibt jedoch Situationen, in denen der Entwickler eines Installationspakets es für erforderlich hält, eine benutzerdefinierte Aktion zu schreiben.

-   Befolgen Sie die Richtlinien für [die Verwendung benutzerdefinierter Aktionen.](using-custom-actions.md)
-   Befolgen Sie [die Richtlinien zum Schützen benutzerdefinierter Aktionen.](guidelines-for-securing-custom-actions.md) Benutzerdefinierte Aktionen, die vertrauliche Informationen verwenden, sollten diese Informationen nicht in das Protokoll schreiben. Weitere Informationen finden Sie unter [Custom Action Security](custom-action-security.md).
-   Benutzerdefinierte Aktionen dürfen nicht versuchen, einen Einstiegspunkt für die Systemwiederherstellung aus einer benutzerdefinierten Aktion zu erstellen. Weitere Informationen finden Sie [unter Festlegen eines Wiederherstellungspunkts aus einer benutzerdefinierten Aktion.](setting-a-restore-point-from-a-custom-action.md)
-   Geben Sie Fehlermeldungen von benutzerdefinierten Aktionen zurück, und schreiben Sie sie in das Protokoll, um die Problembehandlung für benutzerdefinierte Aktionen zu vereinfachen. Weitere Informationen finden Sie [unter Benutzerdefinierte Aktionen für Fehlermeldungen](error-message-custom-actions.md) und [Zurückgeben von Fehlermeldungen von benutzerdefinierten Aktionen.](returning-error-messages-from-custom-actions.md)
-   Ändern Sie den Systemstatus nicht durch eine sofortige benutzerdefinierte Aktion. Benutzerdefinierte Aktionen, die das System direkt ändern oder einen anderen Systemdienst aufrufen, müssen auf den Zeitpunkt der Ausführung des Installationsskripts zurückgestellt werden. Jeder [benutzerdefinierten Aktion mit](deferred-execution-custom-actions.md) verzögerter Ausführung, die den Systemstatus ändert, muss eine benutzerdefinierte [Rollbackaktion](rollback-custom-actions.md) vorangestellt werden, um die Systemstatusänderung bei einem Installationsrollback rückgängig zu machen. Weitere Informationen finden Sie [unter Ändern des Systemstatus mithilfe einer benutzerdefinierten Aktion.](changing-the-system-state-using-a-custom-action.md)
-   Benutzerdefinierte Aktionen, die komplexe Installationsvorgänge ausführen, sollten eine ausführbare [Datei oder](executable-files.md) eine Dynamic Link [Library sein.](dynamic-link-libraries.md) Beschränken Sie die Verwendung benutzerdefinierter Aktionen basierend auf [Skripts](scripts.md) auf einfache Installationsvorgänge.
-   Machen Sie die Details zu den Aktionen Ihrer benutzerdefinierten Aktion für das System für Systemadministratoren leicht erkennbar. Legen Sie die Details der Registrierungseinträge und Dateien, die von Ihrer benutzerdefinierten Aktion verwendet werden, in eine benutzerdefinierte Tabelle ein, und lassen Sie die benutzerdefinierte Aktion aus dieser Tabelle lesen. Dies wird im Beispiel unter Using a Custom Action to Create User Accounts on a Local Computer (Verwenden einer benutzerdefinierten Aktion zum [Erstellen von Benutzerkonten auf einem lokalen Computer) gezeigt.](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md) Informationen zum Hinzufügen benutzerdefinierter Tabellen zu einer Datenbank finden Sie unter [Working with Queries](working-with-queries.md) and [Examples of Database Queries Using SQL and Script](examples-of-database-queries-using-sql-and-script.md).
-   In benutzerdefinierten Aktionen sollte kein Dialogfeld angezeigt werden. Benutzerdefinierte Aktionen, die eine Benutzeroberfläche erfordern, können stattdessen die [**MsiProcessMessage-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) verwenden. Siehe [Senden von Nachrichten an Windows Installer mit msiProcessMessage.](sending-messages-to-windows-installer-using-msiprocessmessage.md)
-   Benutzerdefinierte Aktionen dürfen keine der auf der Seite aufgeführten Funktionen verwenden: Funktionen, die [nicht in benutzerdefinierten Aktionen verwendet werden.](functions-not-for-use-in-custom-actions.md)
-   Wenn die Installation auf einem Terminalserver ausgeführt werden soll, testen Sie, ob alle benutzerdefinierten Aktionen auf einem Terminalserver ausgeführt werden können. Weitere Informationen finden Sie unter [**TerminalServer-Eigenschaft.**](terminalserver.md)
-   Damit eine benutzerdefinierte Aktion ausgeführt wird, wenn ein bestimmter Patch deinstalliert wird, muss die benutzerdefinierte Aktion entweder in der ursprünglichen Anwendung vorhanden oder in einem Patch für das Produkt vorhanden sein, das immer angewendet wird. Weitere Informationen finden Sie unter [Benutzerdefinierte Aktionen zur Patchdeinstallation.](patch-uninstall-custom-actions.md)
-   Benutzerdefinierte Aktionen sollten die Benutzeroberflächenebene nicht als Bedingung für das Senden von Fehlermeldungen an das Installationsprogramm verwenden, da dies die Protokollierung und externe Meldungen beeinträchtigen kann. Weitere Informationen finden Sie [unter Bestimmen der Benutzeroberflächenebene aus einer benutzerdefinierten Aktion.](determining-ui-level-from-a-custom-action.md)
-   Verwenden Sie [](conditional-statement-syntax.md) bedingte Anweisungen und Syntax für bedingte Anweisungen, um sicherzustellen, dass ihr Paket benutzerdefinierte Aktionen ordnungsgemäß ausgeführt, keine benutzerdefinierten Aktionen oder alternative benutzerdefinierte Aktionen ausgeführt, wenn das Paket deinstalliert wird. Testen Sie, ob das Paket wie erwartet funktioniert, wenn [Sie benutzerdefinierte Aktionen deinstallieren.](uninstalling-custom-actions.md) Weitere Informationen finden Sie unter [Konditionierungsaktionen, die während des Entfernens ausgeführt werden sollen.](conditioning-actions-to-run-during-removal.md)
-   Wenn die Installation von Benutzern ohne Administratorrechte ausgeführt werden kann, testen Sie, um sicherzustellen, dass alle benutzerdefinierten Aktionen mit Nichtadministratorberechtigungen ausgeführt werden können. Benutzerdefinierte Aktionen erfordern erhöhte Rechte, um teile des Systems zu ändern, die nicht benutzerspezifisch sind. Das Installationsprogramm kann benutzerdefinierte Aktionen mit erhöhten Rechten ausführen, wenn eine verwaltete Anwendung installiert wird oder die Systemrichtlinie für erhöhte Rechte angegeben wurde. Alle benutzerdefinierten Aktionen, für die erhöhte Rechte erforderlich sind, müssen die benutzerdefinierten Aktionen msidbCustomActionTypeInScript und msidbCustomActionTypeNoImpersonate [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md) (Ausführungsoptionen) im benutzerdefinierten Aktionstyp enthalten. Dies wird im Beispiel unter Using a Custom Action to Create User Accounts on a Local Computer (Verwenden einer benutzerdefinierten Aktion zum [Erstellen von Benutzerkonten auf einem lokalen Computer) gezeigt.](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)

## <a name="if-you-use-assemblies-follow-good-assembly-practices"></a>Wenn Sie Assemblys verwenden, befolgen Sie bewährte Assemblymethoden.

Wenn Ihr Paket Softwareassemblys [verwendet,](assemblies.md)befolgen Sie die Richtlinien zum Hinzufügen von Assemblys zu einem [Paket,](adding-assemblies-to-a-package.md)Aktualisieren von [Assemblys](updating-assemblies.md)und [Installieren und Entfernen von Assemblys](installing-and-removing-assemblies.md).

## <a name="do-not-ship-concurrent-installations"></a>Versenden Sie keine gleichzeitigen Installationen.

[Bei gleichzeitigen](concurrent-installations.md)Installationen ( auch geschachtelte Installationen genannt) wird während einer derzeit ausgeführten Installation ein Windows Installer-Paket installiert. Die Verwendung gleichzeitiger Installationen ist keine bewährte Methode, da sie für Kunden schwierig zu bedienen sind. Patchen und Upgraden funktionieren bei gleichzeitigen Installationen möglicherweise nicht. Die empfohlene Alternative zur Verwendung gleichzeitiger Installationen besteht darin, stattdessen eine Setupanwendung und einen externen Ui-Handler zu verwenden, um mehrere Windows Installer-Pakete sequenziell zu installieren.

Weitere Informationen zur Verwendung eines externen Ui-Handlers finden Sie unter [Überwachen einer Installation mithilfe von MsiSetExternalUI.](monitoring-an-installation-using-msisetexternalui.md) Weitere Informationen zur Verwendung eines datensatzbasierten externen Handlers finden Sie unter [Überwachen einer Installation mit MsiSetExternalUIRecord.](monitoring-an-installation-using-msisetexternaluirecord.md)

Gleichzeitige Installationen werden manchmal in kontrollierten Unternehmensumgebungen verwendet, um Anwendungen zu installieren, die nicht für die Öffentlichkeit bestimmt sind. Befolgen Sie diese Richtlinien, wenn Sie gleichzeitige Installationen verwenden möchten.

-   Verwenden Sie keine gleichzeitigen Installationen, um ein Versandprodukt zu installieren oder zu aktualisieren.
-   Gleichzeitige Installationen sollten keine Komponenten gemeinsam nutzen.
-   Eine Administratorinstallation sollte keine gleichzeitige Installation enthalten.
-   Integrierte ProgressBars sollten nicht mit gleichzeitigen Installationen verwendet werden.
-   Ressourcen, die angekündigt werden sollen, sollten nicht von einer gleichzeitigen Installation installiert werden.
-   Ein Paket, das eine gleichzeitige Installation einer Anwendung ausführt, sollte auch die gleichzeitige Anwendung deinstallieren, wenn das übergeordnete Produkt deinstalliert wird. Eine geschachtelte Installation ist unter dem Kontext des übergeordneten Produkts in der Systemsteuerung Programme hinzufügen/entfernen vorhanden.

## <a name="keep-package-names-and-package-codes-consistent"></a>Halten Sie Paketnamen und Paketcodes konsistent.

Der .msi-Datei kann ein beliebiger Name gegeben werden, mit dem Benutzer das Paket identifizieren können. Der Name sollte jedoch nicht geändert werden, ohne auch den Produktcode zu ändern.

-   Geben Sie ihrer .msi-Datei einen benutzerfreundlichen Namen, mit dem der Benutzer den Inhalt des Windows Installer-Pakets identifizieren kann.
-   Der [Produktcode](product-codes.md) ist die Hauptidentifikation einer Anwendung und muss sich ändern, wenn eine umfassende Aktualisierung der Anwendung erfolgt. Weitere Informationen finden Sie unter [**ProductCode**](productcode.md) und [Ändern des Produktcodes.](changing-the-product-code.md) Das Ändern des Namens der .msi Datei der Anwendung gilt als umfassende Änderung und erfordert immer eine entsprechende Änderung des Produktcodes, um die Konsistenz zu gewährleisten.
-   Der [Paketcode](package-codes.md) ist der primäre Bezeichner, der vom Installationsprogramm verwendet wird, um das richtige Paket für eine bestimmte Installation zu suchen und zu überprüfen. Keine zwei nichtidentischen .msi Dateien sollten jemals den gleichen Paketcode aufweisen. Wenn ein Paket geändert wird, ohne den Paketcode zu ändern, verwendet das Installationsprogramm das neuere Paket möglicherweise nicht, wenn für das Installationsprogramm noch auf beide zugegriffen werden kann. Der Paketcode wird in der [**Revision Number Summary-Eigenschaft**](revision-number-summary.md) des [Zusammenfassungsinformationsdatenstroms](summary-information-stream.md)gespeichert.
-   Beachten Sie, dass Die Buchstaben in den [GUIDs](guid.md) für Produktcode und Paketcode groß geschrieben sein müssen.

## <a name="do-not-use-the-selfreg-and-typelib-tables"></a>Verwenden Sie nicht die Tabellen SelfReg und TypeLib.

-   Installationspaketautoren wird dringend davon abgeraten, die Selbstregistrierung und die [SelfReg-Tabelle](selfreg-table.md) zu verwenden. Stattdessen sollten Sie Module registrieren, indem sie eine oder mehrere Tabellen in der [Registrierungstabellengruppe erstellen.](registry-tables-group.md) Viele der Vorteile des Windows Installers gehen bei der Selbstregistrierung verloren, da Routinen für die Selbstregistrierung dazu tendieren, wichtige Konfigurationsinformationen auszublenden. Eine Liste der Gründe für die Vermeidung der Selbstregistrierung finden Sie in der [SelfReg-Tabelle](selfreg-table.md).
-   Installationspaketautoren wird dringend davon abgeraten, die [TypeLib-Tabelle](typelib-table.md) zu verwenden. Anstatt die TypeLib-Tabelle zu verwenden, registrieren Sie Typbibliotheken mithilfe der [Registrierungstabelle.](registry-table.md) Wenn bei einer Installation mit der TypeLib-Tabelle ein Fehler auftritt und ein Rollback ausgeführt werden muss, wird der Computer möglicherweise nicht in dem Zustand wiederhergestellt, der vor dem Rollback vorhanden war.

## <a name="provide-the-option-to-install-without-a-user-interface"></a>Geben Sie die Option zum Installieren ohne Benutzeroberfläche an.

Administratoren bevorzugen häufig die Bereitstellung von Anwendungen innerhalb eines Unternehmens, ohne dass eine Benutzerinteraktion erforderlich ist. Es ist eine bewährte Methode, es Ihrer Anwendung zu ermöglichen, die Option zur Installation mit der [Benutzeroberflächesebene](user-interface-levels.md) "None" bereitzustellen.

-   Verwenden Sie [öffentliche Eigenschaften](public-properties.md) für Konfigurationsinformationen. Administratoren können diese Informationen über die Befehlszeile bereitstellen.
-   Es ist nicht erforderlich, dass die Installation von Informationen abhängig ist, die aus der Benutzerinteraktion mit Dialogfeldern gesammelt wurden. Diese Informationen sind während einer automatischen Installation nicht verfügbar.
-   Starten Sie den Computer des Benutzers während einer unbeaufsichtigten Installation nicht automatisch neu.
-   Administratoren können die [Benutzeroberflächenebene](user-interface-levels.md) bei der Installation mithilfe der [Befehlszeilenoption](command-line-options.md) "/q" festlegen. Die Benutzeroberflächenebene kann auch programmgesteuert mit einem Aufruf von [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)festgelegt werden.

## <a name="avoid-using-the-alwaysinstallelevated-policy"></a>Vermeiden Sie die Verwendung der AlwaysInstallElevated-Richtlinie.

Wenn die [AlwaysInstallElevated-Richtlinie](alwaysinstallelevated.md) nicht festgelegt ist, werden anwendungen, die nicht vom Administrator verteilt werden, mit den Berechtigungen des Benutzers installiert, und nur verwaltete Anwendungen erhalten erhöhte Rechte. Durch Festlegen dieser Richtlinie wird Windows Installer anweisen, systemberechtigungen zu verwenden, wenn die Anwendung auf dem System installiert wird. Diese Methode kann einen Computer mit einem Sicherheitsrisiko öffnen, da ein Benutzer ohne Administratorrechte Installationen mit erhöhten Rechten ausführen und auf sichere [*Speicherorte*](e-gly.md) auf dem Computer zugreifen kann, wenn diese Richtlinie festgelegt ist. Es ist eine bewährte Methode, eine andere Methode als die AlwaysInstallElevated-Richtlinie zu verwenden, wenn [Sie ein Paket mit erhöhten Rechten für einen Nichtadministrator](installing-a-package-with-elevated-privileges-for-a-non-admin.md) installieren oder Per-User verwaltete Anwendungen [patchen.](patching-per-user-managed-applications.md)

## <a name="enable-the-disablemedia-policy-to-limit-unauthorized-installation"></a>Aktivieren Sie die Richtlinie DisableMedia, um die nicht autorisierte Installation einzuschränken.

Die [DisableMedia-Richtlinie](disablemedia.md) kann eine nicht autorisierte Installation von Anwendungen verhindern. Wenn diese Richtlinie aktiviert ist, werden Benutzer und Administratoren, die eine Wartungsinstallation eines Produkts ausführen, daran gehindert, das Dialogfeld Durchsuchen zum Durchsuchen von Medienquellen wie CD-ROM für die Quellen anderer installierbarer Produkte zu verwenden. Das Suchen nach anderen Produkten wird unabhängig davon verhindert, ob die Installation mit erhöhten Rechten erfolgt. Es ist weiterhin möglich, dass der Benutzer das Produkt über Medien neu installiert, wenn der Benutzer über eine ordnungsgemäß bezeichnete Medienquelle verfügt.

## <a name="keep-the-original-package-source-files-secure-and-available-to-users"></a>Halten Sie die ursprünglichen Paketquelldateien sicher und für Benutzer verfügbar.

In einigen Fällen kann die ursprüngliche Quelle des Windows Installer-Pakets erforderlich sein, um eine Anwendung bei Bedarf zu installieren, zu reparieren oder zu aktualisieren. Wenn das Installationsprogramm keine verfügbare Quelle finden kann, wird der Benutzer aufgefordert, Medien bereitzustellen oder zu einem Netzwerkspeicherort zu wechseln, der die erforderlichen Quellen enthält. Es empfiehlt sich, sicherzustellen, dass das Installationsprogramm über die benötigten Quellen verfügt, ohne den Benutzer dazu auffordern zu müssen.

-   Verwenden Sie [digitale Signaturen und externe Cab-Dateien,](digital-signatures-and-external-cabinet-files.md) um sicherzustellen, dass die vom Installationsprogramm verwendeten Origialquellen sicher sind. Ein nicht komprimiertes Quellimage, das an einem öffentlichen Speicherort gespeichert ist, ist nicht sicher.
-   Fügen Sie eine vollständige Liste der Netzwerk- oder URL-Quellpfade zum Installationspaket der Anwendung in die [**SOURCELIST-Eigenschaft**](sourcelist.md) ein.
-   Verwenden Sie eine verteiltes Dateisystem -Freigabe (DFS) für den Quellpfad.
-   Verwenden Sie die Windows Installer-API, um Quelllisteninformationen für Windows Installer-Anwendungen und Patches abzurufen und zu ändern. Weitere Informationen finden Sie unter [Verwalten von Installationsquellen.](managing-installation-sources.md)
-   Verwenden Sie die Methoden und Eigenschaften von [**Installer-Objekt,**](installer-object.md) [**Produktobjekt**](product-object.md)und [**Patchobjekt,**](patch-object.md) um Quelllisteninformationen für Windows Installer-Anwendungen und -Patches abzurufen und zu ändern.
-   Halten Sie sich an die Punkte, die unter Verhindern, dass [ein Patch Zugriff auf die ursprünglichen Installationsquellpunkte](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md) erfordert aufgeführt sind, um die Möglichkeit zu minimieren, dass Ihr Patch Zugriff auf die ursprünglichen Quellen benötigt.
-   Store die Paketquelldateien an einem Speicherort ab, der nicht der temporäre Ordner des Systems ist. Windows Im temporären Ordner gespeicherte Installationsquelldateien können für Benutzer nicht mehr verfügbar sein.

## <a name="enable-verbose-logging-on-users-computer-when-troubleshooting-deployment"></a>Aktivieren Sie bei der Problembehandlung bei der Bereitstellung die ausführliche Protokollierung auf dem Computer des Benutzers.

[Windows Installer-Protokollierung](windows-installer-logging.md) enthält eine ausführliche Protokollierungsoption, die auf dem Computer eines Benutzers aktiviert werden kann. Die Informationen in einem ausführlichen Protokoll können bei der Problembehandlung Windows Paketbereitstellung des Installers hilfreich sein.

-   Sie können die ausführliche Protokollierung auf dem Computer des Benutzers aktivieren, indem Sie [befehlszeilenoptionen](command-line-options.md), die [**MsiLogging-Eigenschaft,**](msilogging.md) [die Protokollierungsrichtlinie,](logging.md) [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)und die [**EnableLog-Methode verwenden.**](installer-enablelog.md)
-   Eine sehr nützliche Ressource zum Interpretieren Windows Installer-Protokolldateien ist [Wilogutl.exe](wilogutl-exe.md). Dieses Tool unterstützt die Analyse von Protokolldateien und zeigt vorgeschlagene Lösungen für Fehler an, die in einer Protokolldatei gefunden werden.
-   Weitere Informationen zum Interpretieren Windows Installer-Protokolldateien finden Sie im Whitepaper auf der TechNet-Website: [Windows Installer: Vorteile und Implementierung für Systemadministratoren.](https://www.microsoft.com/technet/prodtechnol/windows2000serv/maintain/featusability/winmsi.mspx)
-   Die ausführliche Protokollierungsoption sollte nur zu Problembehandlungszwecken verwendet werden und sollte nicht verlassen werden, da sie negative Auswirkungen auf die Systemleistung und den Speicherplatz haben kann. Jedes Mal, wenn Sie das Tool Zum Hinzufügen/Entfernen von Programmen in Systemsteuerung verwenden, wird eine neue Datei erstellt.

## <a name="uninstallation-leaves-the-users-computer-in-a-clean-state"></a>Durch die Deinstallation bleibt der Computer des Benutzers in einem fehlerfreien Zustand.

Das Entfernen von Anwendungen ist genauso wichtig wie die Installation. Wenn ein Windows Installer-Paket deinstalliert wird, sollte es keine unnötigen Teile von sich selbst auf dem Computer des Benutzers zurücklassen.

-   Wenn eine Datei, die vom Computer des Benutzers entfernt werden sollte, nach dem Ausführen einer Deinstallation installiert bleibt, entfernt das Installationsprogramm die Komponente, die die Datei enthält, möglicherweise nicht aus einem oder mehreren der unter Entfernen von [hängenden Dateien beschriebenen](removing-stranded-files.md)Gründe.
-   Wenn eine Anwendung registriert werden muss, erstellen Sie das Paket, um Registrierungsinformationen zu entfernen, wenn die Anwendung deinstalliert wird. Weitere Informationen finden Sie unter [Hinzufügen oder Entfernen von Registrierungsschlüsseln bei der Installation oder Entfernung von Komponenten.](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md) Wenn eine Anwendung nicht registriert ist, wird die Anwendung nicht im Feature Software in Systemsteuerung aufgeführt und kann nicht mithilfe des Windows Installers verwaltet werden.
-   Um eine Anwendung in Systemsteuerung aus der Funktion "Programme hinzufügen" oder "Entfernen" auszublenden und trotzdem den Windows Installer zum Verwalten der Anwendung verwenden zu können, befolgen Sie die Unter Hinzufügen und Entfernen einer Anwendung beschriebenen Richtlinien [und lassen keine Ablaufverfolgung in der Registrierung.](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
-   Benutzerdefinierte Aktionen sollten bei der Deinstallation so ausgeführt werden, dass sie nicht wie erforderlich ausgeführt werden. Bei der Installation und Deinstallation müssen möglicherweise verschiedene benutzerdefinierte Aktionen ausgeführt werden.
-   Benutzerspezifische Anpassungsinformationen können in einer Textdatei auf dem Computer gespeichert werden. Dies hat den Vorteil, dass die Datei entfernt werden kann, wenn die Anwendung deinstalliert wird, auch wenn der Benutzer dieser Anpassung derzeit nicht angemeldet ist.

## <a name="test-packages-for-both-per-user-and-per-machine-installation-deployment"></a>Testen Sie Pakete für die Bereitstellung pro Benutzer und Pro-Computer-Installation.

Es ist eine bewährte Methode, Kunden die Entscheidung zu ermöglichen, ob ein Paket für die Installation entweder im Pro-Computer- oder benutzerbezogenen [Installationskontext](installation-context.md)bereitgestellt werden soll.

-   Überlegen Sie, ob die Anwendung während des Entwicklungsprozesses nur bestimmten Benutzern oder allen Benutzern des Computers zur Verfügung stehen soll.
-   Testen Sie, ob das Paket sowohl für die Installation pro Benutzer als auch für den Installationskontext pro Computer ordnungsgemäß funktioniert.
-   Machen Sie das Paket einfach anpassbar, und lassen Sie Kunden entscheiden, ob es pro Benutzer oder pro Computer bereitgestellt werden soll.

## <a name="plan-and-test-a-servicing-strategy-before-shipping-the-application"></a>Planen und testen Sie eine Wartungsstrategie, bevor Sie die Anwendung versenden.

Sie sollten entscheiden, wie Sie die Anwendung warten möchten, bevor Sie die Anwendung zum ersten Mal bereitstellen.

-   Berücksichtigen Sie die Typen von Updates, die Sie voraussichtlich für die zukünftige Verwendung ihrer Anwendung verwenden werden. Der Windows Installer bietet drei Arten von Updates: [Kleines Update,](small-updates.md) [Kleineres Upgrade](minor-upgrades.md)und [Hauptupgrades.](major-upgrades.md) Die Unterschiede zwischen diesen werden im Thema [Patchen und Upgrades](patching-and-upgrades.md) beschrieben.
-   Testen Sie vor dem Versand Ihrer Anwendung, ob sie nach der Wartung mit jedem Updatetyp wie erwartet funktioniert.

## <a name="reduce-the-dependency-of-updates-upon-the-original-sources"></a>Reduzieren Sie die Abhängigkeit von Updates von den ursprünglichen Quellen.

Wenn die ursprünglichen Quelldateien zum Aktualisieren Ihrer Anwendung erforderlich sind, kann dies die Wartung der Anwendung erschweren. Die folgenden Methoden können dazu beitragen, die Abhängigkeit von Updates von den ursprünglichen Quellen zu verringern.

-   Verwenden Sie einen [*Deltapatch,*](d-gly.md) um die Baselineversionen Ihrer Anwendung zu aktualisieren, z. B. die RTM-Version und die Service Pack-Versionen. Befolgen Sie die Richtlinien für die Verwendung von Deltapatches, die im Thema Reduzieren der [Patchgröße](reducing-patch-size.md)beschrieben sind.
-   Befolgen Sie die Empfehlungen im Thema [Verhindern, dass ein Patch Zugriff auf die ursprüngliche Installationsquelle erfordert.](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md)

## <a name="do-not-distribute-unserviceable-merge-modules"></a>Verteilen Sie keine nicht verwendbaren Mergemodule.

Anwendungen sollten bei der Installation der Komponente nicht von [Mergemodulen](merge-modules.md) abhängig sein, wenn sich der Besitzer des Mergemoduls und der Besitzer der Anwendung unterscheiden. Dadurch kann es schwierig sein, die Anwendung zu bedienen, da beide Besitzer die Aktualisierung der Anwendung oder des Moduls koordinieren müssen. Ohne alle Anwendungen zu kennen, die das Mergemodul verwendet haben, kann der Besitzer der Anwendung das Mergemodul nicht aktualisieren, ohne zu riskieren, dass das Update möglicherweise mit einer anderen Anwendung nicht kompatibel ist. Der Besitzer des Mergemoduls verfügt über keine direkte Methode zum Aktualisieren Windows Installer-Pakete, die das Mergemodul bereits installiert haben.

-   Erwägen Sie die Bereitstellung der erforderlichen Komponenten für Benutzer als weitere installation Windows Installer.

## <a name="avoid-patching-administrative-installations"></a>Vermeiden Sie das Patchen von Administratorinstallationen.

Stellen Sie in einem Netzwerk eine [Administrative Installation](administrative-installation.md) des ursprünglichen Windows Installer-Pakets Ihrer Anwendung bereit, um Mitgliedern einer Arbeitsgruppe die Installation der Anwendung zu ermöglichen. Benutzer dieses Administratorimages sollten dann Updates auf die lokale Instanz der Anwendung anwenden, die sich auf ihrem Computer befindet. Dies sorgt dafür, dass Benutzer mit dem Administratorimage synchronisiert werden. Das Anwenden von Updates auf die Administratorinstallation wird aus den folgenden Gründen nicht empfohlen.

-   Die Größe und Latenz des Downloads, der für Benutzer erforderlich ist, um ein Update zu erhalten, wird im Vergleich zum Herunterladen eines Patches erhöht. Das gesamte aktualisierte Windows Installer-Paket und die Quelldateien müssen heruntergeladen, neu zwischenspeichert und neu installiert werden.
-   Benutzer können Anwendungen erst nach [Bedarf installieren](installation-on-demand.md) und von einer aktualisierten Administratorinstallation reparieren, wenn sie die Anwendung erneut zwischenspeichern und neu installieren.
-   Durch Anwenden eines Patches auf eine Administratorinstallation wird die digitale Signatur aus dem Paket entfernt. Ein Administrator muss das Paket kündigen. Weitere Informationen zur Verwendung digitaler Signaturen finden Sie unter [Digitale Signaturen und Windows Installer.](digital-signatures-and-windows-installer.md)
-   Viele binäre Patches zielen auf das RTM-Image der Anwendung ab und erfordern eine frühere Dateiversion. Die lokale Instanz einer Anwendung, die über eine aktualisierte Administratorinstallation installiert wurde, funktioniert möglicherweise nicht mit anderen Updates. Viele binäre Patchanwendungen können fehlschlagen.
-   Durch anwenden eines Patches auf eine Administratorinstallation werden die Quelldateien und die .msi Datei aktualisiert, aber das Netzwerkimage wird nicht mit Informationen zum Update gestempelt. Benutzer können nicht ermitteln, welche Updates sie von der Administratorinstallation erhalten haben. Dies macht es unmöglich, auf benutzerseitige Updates angewendete Sequenzupdates mit denen zu sequenzen, die bereits auf der Administratorimageseite angewendet wurden.
-   Patches, die auf eine Administratorinstallation angewendet werden, sind keine [deinstallationsfähigen Patches.](uninstallable-patches.md) Dadurch kann verhindert werden, dass sich der auf dem Computer des Benutzers zwischengespeicherte Paketcode von dem Paketcode bei der Administratorinstallation unterscheidet. Wenn sich der auf dem Computer des Benutzers zwischengespeicherte Paketcode von dem auf der Administratorinstallation unterscheidet, installieren Sie die Anwendung über die Administratorinstallation neu, und patchen Sie dann den Clientcomputer.
-   Wenn Sie kleine Updates durch Patchen eines administrativen Images anwenden möchten, befolgen Sie die Richtlinien, die im Thema [Anwenden kleiner Updates durch Patchen eines administrativen Images](applying-small-updates-by-patching-an-administrative-image.md)beschrieben werden.

## <a name="register-updates-to-run-with-elevated-privilege"></a>Registrieren Sie Updates für die Ausführung mit erhöhten Rechten.

Ab Windows Installer 3.0 ist es möglich, Patches auf eine Anwendung anzuwenden, die in einem pro Benutzer verwalteten Kontext installiert wurde, nachdem der Patch als mit erhöhten Rechten registriert wurde. Sie können keine Patches auf Anwendungen anwenden, die in einem benutzerbezogenen verwalteten Kontext mit Versionen von Windows Installer vor Version 3.0 installiert sind.

-   Verwenden Sie die [**SourceListAddSource-Methode**](patch-sourcelistaddsource.md) oder die [**MsiSourceListAddSourceEx-Funktion,**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) um ein Patchpaket mit erhöhten Rechten zu registrieren. Befolgen Sie die Richtlinien und Beispiele unter [Patching Per-User Managed Applications](patching-per-user-managed-applications.md).
-   Wenn Sie Windows Installer Version 4.0 unter Windows Vista ausführen, können Sie auch das Patchen der [Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md) verwenden, um es den Autoren von installationen von Windows Installer zu ermöglichen, digital signierte Patches zu identifizieren, die in Zukunft von Benutzern ohne Administratorrechte angewendet werden können. Dies ist nur bei der Installation von Paketen im [Installationskontext](installation-context.md) pro Computer (ALLUSERS=1) verfügbar.
-   Stellen Sie sicher, dass das Patchen mit den geringsten Rechten nicht deaktiviert wurde, indem Sie die [**MSIDISABLELUAPATCHING-Eigenschaft**](msidisableluapatching.md) oder die [DisableLUAPatching-Richtlinie](disableluapatching.md) festlegen.

## <a name="use-the-msipatchsequence-table-to-sequence-patches"></a>Verwenden Sie die MsiPatchSequence-Tabelle zum Sequenzen von Patches.

Fügen Sie eine [MsiPatchSequence-Tabelle](msipatchsequence-table.md) in Ihr Paket ein, und fügen Sie Informationen zur Patchsequenzierung hinzu. Ab Windows Installer Version 3.0 kann das Installationsprogramm die MsiPatchSequence-Tabelle verwenden, wenn [mehrere Patches installiert](installing-multiple-patches.md) werden, um die beste Patchanwendungssequenz zu ermitteln. Verwenden Sie die Richtlinien, die im Whitepaper [Patch sequencing in Windows Installer version 3.0 (Patchsequenzierung in Windows Installer Version 3.0)](https://www.microsoft.com/downloads/details.aspx?FamilyID=ad7ac91e-2493-4549-ae6f-bf5e007c12a3) beschrieben sind, um Patchfamilien zu definieren.

-   Geben Sie ggf. alle Patches als zu einer einzelnen Patchfamilie gehörend an. In vielen Fällen bietet eine einzelne Patchfamilie genügend Flexibilität zum Sequenzen von Patches. Die Komplexität der Erstellung steigt, wenn mehrere Patchfamilien verwendet werden. Weisen Sie der Patchfamilie einen aussagekräftigen Namen zu, und weisen Sie Sequenzwerte in dieser Patchfamilie zu, die sich im Laufe der Zeit erhöhen. Befolgen Sie das Beispiel für [mehrere Patches,](multiple-patching-example.md) um Patches in der Reihenfolge anzuwenden, in der sie ausgegeben wurden.
-   Verwenden Sie die [PatchSequence-Tabelle](patchsequence-table--patchwiz-dll-.md) in [Patchwiz.dll, ](patchwiz-dll.md) um die Informationen in der [MsiPatchSequence-Tabelle](msipatchsequence-table.md)zu generieren. Die Version von PATCHWIZ.DLL, die mit Windows Installer 3.0 veröffentlicht wurde, kann automatisch Patchsequenzierungsinformationen generieren. Weitere Informationen zum Hinzufügen eines neuen Patches finden Sie unter [Generieren von Patchsequenzinformationen.](generating-patch-sequence-information---patchwiz-dll-.md) Weitere Informationen zu Patchsequenzierungsszenarien finden Sie im Whitepaper [Patch Sequencing in Windows Installer Version 3.0](https://www.microsoft.com/downloads/details.aspx?FamilyID=ad7ac91e-2493-4549-ae6f-bf5e007c12a3).

## <a name="test-the-installation-package-thoroughly"></a>Testen Sie das Installationspaket gründlich.

Testen Sie, ob das Windows Installer-Paket ordnungsgemäß installiert, repariert und entfernt wurde. Sie können den Testprozess in die folgenden Teile unterteilen.

-   Installationstests: Testen Sie die Installation mit allen möglichen Kombinationen von Anwendungsfeatures. Testen Sie alle Installationstypen, einschließlich [Administrative Installation,](administrative-installation.md) [Rollbackinstallation](rollback-installation.md)und [Installation-On-Demand](installation-on-demand.md). Probieren Sie alle möglichen Installationsmethoden aus, z. B. das Klicken auf die .msi-Datei, [Befehlszeilenoptionen](command-line-options.md)und die Installation über die Systemsteuerung. Testen Sie, ob das Paket von Benutzern in allen möglichen Berechtigungskontexten installiert werden kann. Versuchen Sie, das Paket zu installieren, nachdem es mit allen möglichen Methoden bereitgestellt wurde. Aktivieren Sie [Windows Installer-Protokollierung](windows-installer-logging.md) für jeden Test, und beheben Sie alle Fehler, die im Installationsprogramm- und Ereignisprotokoll gefunden wurden.
-   Benutzeroberfläche Testing : Testen Sie das Paket bei der Installation mit allen möglichen [Benutzeroberflächenebenen.](user-interface-levels.md) Testen Sie das installierte Paket ohne Benutzeroberfläche und mit allen Informationen, die über die Benutzeroberfläche bereitgestellt werden. Stellen Sie sicher, dass die [Barrierefreiheit](accessibility.md) der Benutzeroberfläche und die Benutzeroberfläche für unterschiedliche Bildschirmauflösungen und Schriftgrade erwartungsgemäß funktionieren.
-   Wartungs- und Reparaturtests: Testen Sie, ob das Paket [Patches und Upgrades](patching-and-upgrades.md) verarbeiten kann, die durch ein [kleines Update,](small-updates.md) [ein kleineres Upgrade](minor-upgrades.md)und größere Upgrades bereitgestellt [werden.](major-upgrades.md) Schreiben Sie vor der Bereitstellung des Pakets ein Testupdate für jeden Typ, und versuchen Sie, es auf das ursprüngliche Paket anzuwenden.
-   Deinstallieren von Tests: Stellen Sie sicher, dass beim Entfernen des Pakets keine unnötigen Teile von sich selbst auf dem Computer des Benutzers zurückbleiben und dass nur informationen entfernt wurden, die zum Paket gehören. Starten Sie den Testcomputer nach der Deinstallation des Pakets neu, und überprüfen Sie die Integrität gängiger Systemtools und anderer Standardanwendungen. Testen Sie, ob das Paket von Benutzern in allen möglichen Berechtigungskontexten entfernt werden kann. Testen Sie alle Methoden, um das Paket zu entfernen, klicken Sie auf die datei .msi, testen Sie die [Befehlszeilenoptionen,](command-line-options.md)und entfernen Sie das Paket aus der Systemsteuerung. Aktivieren Sie [Windows Installer-Protokollierung](windows-installer-logging.md) für jeden Test, und beheben Sie alle Fehler, die im Installationsprogramm- und Ereignisprotokoll gefunden wurden.
-   Testen der Produktfunktionalität: Stellen Sie sicher, dass die Anwendung nach der Installation, Reparatur oder Entfernung des Pakets wie erwartet funktioniert.

## <a name="fix-all-validation-errors-before-deploying-a-new-or-revised-installation-package"></a>Beheben Sie alle Validierungsfehler, bevor Sie ein neues oder überarbeitetes Installationspaket bereitstellen.

Führen Sie [die Paketvalidierung](package-validation.md) für ein neues oder überarbeitetes Windows Installer-Paket aus, bevor Sie versuchen, es zum ersten Mal zu installieren. Bei der Überprüfung wird die Windows Installer-Datenbank auf Erstellungsfehler überprüft. Der Versuch, ein Paket zu installieren, das die Überprüfung nicht bestanden hat, kann das System des Benutzers beschädigen.

-   Sie können Ihr Paket mit [Orca.exe](orca-exe.md) oder [Msival2.exe](msival2-exe.md)überprüfen. Beide Tools werden mit dem Windows SDK bereitgestellt. Drittanbieter können auch das ICE-Überprüfungssystem in ihre Erstellungsumgebung integrieren.
-   Sie können den Standardsatz interner [Konsistenzauswertungen](internal-consistency-evaluators-ices.md) verwenden– ICEs, die in den CUB-Dateien enthalten sind, die mit dem SDK bereitgestellt werden. Alternativ können Sie die Überprüfung anpassen, indem [Sie einen ICE](building-an-ice.md) erstellen und der CUB-Datei hinzufügen.
-   Sie können die Evalcom2.dll verwenden, um [Validation Automation](validation-automation.md) für Installationspakete und Mergemodule zu implementieren.

## <a name="author-a-secure-installation"></a>Erstellen sie eine sichere Installation.

Befolgen Sie diese Richtlinien bei der Entwicklung Ihres Pakets, um eine sichere Umgebung während der Installation beizubehalten.

-   [Richtlinien für die Erstellung sicherer Installationen](guidelines-for-authoring-secure-installations.md)
-   [Richtlinien zum Sichern von Paketen auf gesperrten Computern](guidelines-for-securing-packages-on-locked-down-computers.md)
-   [Richtlinien zum Sichern benutzerdefinierter Aktionen](guidelines-for-securing-custom-actions.md)

## <a name="use-pmsihandle-instead-of-handle"></a>Verwenden von PMSIHANDLE anstelle von HANDLE

Die **PMSIHANDLE-Typvariablen** werden in msi.h definiert. Es wird empfohlen, dass Ihre Anwendung den **PMSIHANDLE-Typ** verwendet, da das Installationsprogramm **PMSIHANDLE-Objekte** schließt, sobald sie den Gültigkeitsbereich sprengen, während Ihre Anwendung **MSIHANDLE-Objekte** durch Aufrufen von [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle)schließen muss.

Wenn Sie z. B. Code wie den folgenden verwenden:

``` syntax
MSIHANDLE hRec = MsiCreateRecord(3);
```

Ändern Sie sie in:

``` syntax
PMSIHANDLE hRec = MsiCreateRecord(3);
```

 

 
