---
description: Windows Installer ist die empfohlene Lösung für die Installation und Einrichtung von Anwendungen unter Windows.
ms.assetid: 13f41020-5275-44cd-b26b-f45483700d8a
title: Rollenbasiertes Handbuch für Windows Installer-Dokumentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8a2138e963b6d29bd161df5e09144cf0cfd36b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041944"
---
# <a name="role-based-guide-to-windows-installer-documentation"></a>Rollenbasiertes Handbuch für Windows Installer-Dokumentation

Windows Installer ist die empfohlene Lösung für die Installation und Einrichtung von Anwendungen unter Windows. Daher sind einige der in diesem SDK enthaltenen Informationen für eine Vielzahl von Software Entwicklungs-und IT-Experten von Interesse. Dieser Abschnitt dient als Leitfaden für Leser, die lieber Links zu Themen finden, die nach professionellen Rollen und allgemeinen Aufgaben Szenarios organisiert sind. Da sich die Rollen zwischen Organisationen stark voneinander unterscheiden können, sollte die folgende Gruppierung nur als Leitfaden für einen Standort betrachtet werden, um mit der Suche nach den benötigten Informationen zu beginnen.

-   [Anwendungsentwickler](#application-developers)
-   [Setup Autoren](#setup-authors)
-   [IT-Fachleute](#it-professionals)
-   [Infrastruktur Entwickler](#infrastructure-developers)

Diese Dokumentation ist für Softwareentwickler gedacht, die Anwendungen erstellen möchten, die Windows Installer verwenden. Als Hauptquelle für das Referenzmaterial für das Installationsprogramm bietet das SDK Informationen zu Installationspaketen und zum Installerdienst. Es enthält umfassende Beschreibungen der Anwendungsprogrammierschnittstelle (Application Programming Interface, API) und der-Elemente der Installer-Datenbank.

Weitere Informationen finden Sie unter [andere Quellen mit Windows Installer-Informationen](other-sources-of-windows-installer-information.md).

## <a name="application-developers"></a>Anwendungsentwickler

Anwendungsentwickler erstellen Anwendungen, die die Windows Installer-Anwendungsprogrammierschnittstelle aufzurufen und Windows Installer-Pakete zur Laufzeit installieren. Der Windows Installer kann in einer Anwendung funktionieren, z. b. bei der Selbstreparatur und bei der Installation bei Bedarf. Anwendungsentwickler führen in der Regel folgende Aktionen aus:

-   Aktivieren Sie die Installation bei Bedarf von Anwendungen zur Laufzeit in einer anderen Anwendung.

    Weitere Informationen finden Sie unter

    -   [Verwenden von Installer-Funktionen](using-installer-functions.md)
    -   [Installationsfunktionsverweis](installer-function-reference.md)
    -   [Installation bei Bedarf](installation-on-demand.md)
    -   [Verwaltung von Komponenten](component-management.md)
    -   [Bearbeiten von Installationsprogramm Kombinationen](editing-installer-shortcuts.md)
    -   [**Oleadvtsupport (Eigenschaft)**](oleadvtsupport.md)
    -   [Platt Form Unterstützung für Ankündigungen](platform-support-of-advertisement.md)

-   Aktivieren Sie die Selbstreparatur von Anwendungen, indem Sie die Komponenten bei Bedarf zur Laufzeit neu installieren.

    Weitere Informationen finden Sie unter

    -   [Verwenden von Installer-Funktionen](using-installer-functions.md)
    -   [Installationsfunktionsverweis](installer-function-reference.md)
    -   [Resilienz](resiliency.md)
    -   [Quellen Resilienz](source-resiliency.md)
    -   [Suchen nach einer unterbrochenen Funktion oder Komponente](searching-for-a-broken-feature-or-component.md)
    -   [Ersetzen vorhandener Dateien](replacing-existing-files.md)

-   Anzeigen einer Benutzeroberfläche, um Benutzerinformationen und Konfigurationseinstellungen zu erfassen, wenn eine Anwendung zum ersten Mal installiert oder ausgeführt wird. Die Benutzeroberfläche muss vom Setup-Autor des Windows Installer Pakets hinzugefügt werden.

    Weitere Informationen finden Sie unter

    -   [Verwenden von Installer-Funktionen](using-installer-functions.md)
    -   [Initialisieren einer Anwendung](initializing-an-application.md)
    -   [Dialog Feld "FIRSTRUN"](firstrun-dialog.md)
    -   [Informationen zur Benutzeroberfläche](about-the-user-interface.md)

-   Erstellen Sie Anwendungen, die ein dereferenzierungsmodell verwenden, um auf Komponenten mit paralleler Funktionalität zu verweisen. Die qualifizierten Komponenten Kategorien müssen vom Setup Autor des Windows Installer Pakets hinzugefügt werden.

    Weitere Informationen finden Sie unter

    -   [Qualifizierte Komponenten](qualified-components.md)
    -   [Verwenden qualifizierter Komponenten](using-qualified-components.md)

-   Verwenden Sie private und parallele Assemblys, um Anwendungen zu isolieren und DLL-Konflikte zu verringern.

    Weitere Informationen finden Sie unter

    -   [Assemblys](assemblies.md)
    -   [Von Windows Installer geschriebene assemblyregistrierungsschlüssel](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Installieren von Win32-Assemblys für die parallele Freigabe unter Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
    -   [Installieren von Win32-Assemblys für die private Verwendung einer Anwendung unter Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)
    -   [MsiAssembly-Tabelle](msiassembly-table.md)
    -   [MsiAssemblyName-Tabelle](msiassemblyname-table.md)
    -   [**Msiproviabassembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)
    -   [**MsiWin32AssemblySupport-Eigenschaft**](msiwin32assemblysupport.md)
    -   [**MsiNetAssemblySupport (Eigenschaft)**](msinetassemblysupport.md)
    -   [**Isolierte Komponenten**](isolated-components.md)

-   Bereiten Sie die Anwendung vor, um Ihre eigenen umfassenden Upgrades zu installieren.

    Weitere Informationen finden Sie unter

    -   [Patchen und Upgrades](patching-and-upgrades.md)
    -   [Wichtige Upgrades](major-upgrades.md)
    -   [**UpgradeCode-Eigenschaft**](upgradecode.md)
    -   [**Verwenden von UpgradeCode**](using-an-upgradecode.md)
    -   [Verhindern, dass ein altes Paket über eine neuere Version installiert wird](preventing-an-old-package-from-installing-over-a-newer-version.md)

-   Bereiten Sie die Anwendung vor, um Ihre eigenen kleinen Upgrades, kleine Updates oder Korrekturen zu installieren.

    Weitere Informationen finden Sie unter

    -   [Patchen und Upgrades](patching-and-upgrades.md)
    -   [Kleine Updates](small-updates.md)
    -   [Kleinere Upgrades](minor-upgrades.md)

-   Organisieren Sie Anwendungs Ressourcen in Komponenten, die mit dem Windows Installer arbeiten können.

    Weitere Informationen finden Sie unter

    -   [Windows Installer Komponenten](windows-installer-components.md)
    -   [Arbeiten mit Features und Komponenten](working-with-features-and-components.md)
    -   [Verwenden transitiv Komponenten](using-transitive-components.md)
    -   [Was geschieht, wenn die Komponenten Regeln beschädigt sind?](what-happens-if-the-component-rules-are-broken.md)
    -   [Organisieren von Anwendungen in Komponenten](organizing-applications-into-components.md)
    -   [Isolierte Komponenten](isolated-components.md)
    -   [Qualifizierte Komponenten](qualified-components.md)

## <a name="setup-authors"></a>Setup Autoren

Setup Autoren erstellen Windows Installer Pakete (MSI-Dateien), die die Setup Logik und die erforderlichen Informationen zum Installieren einer Anwendung enthalten. In der Regel verwenden Sie Erstellungs Tools wie [Orca.exe](orca-exe.md) , um die Windows Installer Datenbank mit der Setup Logik und den Informationen aufzufüllen. In der Regel führen Setup Autoren folgende Aktionen aus:

-   Bestimmen Sie die Funktionalität, die mit verschiedenen Windows Installer Versionen verfügbar ist.

    Weitere Informationen finden Sie unter

    -   [Bestimmen der Windows Installer Version](determining-the-windows-installer-version.md)
    -   [Veröffentlichte Versionen von Windows Installer](released-versions-of-windows-installer.md)
    -   [Neues in Windows Installer](what-s-new-in-windows-installer.md)

-   Organisieren von Anwendungs Ressourcen in Windows Installer-Komponenten.

    Weitere Informationen finden Sie unter

    -   [Windows Installer Komponenten](windows-installer-components.md)
    -   [Organisieren von Anwendungen in Komponenten](organizing-applications-into-components.md)
    -   [Ändern des Komponenten Codes](changing-the-component-code.md)
    -   [Was geschieht, wenn die Komponenten Regeln beschädigt sind?](what-happens-if-the-component-rules-are-broken.md)
    -   [Windows Installer Beispiele](windows-installer-examples.md)

-   Verwenden Sie Windows Installer Paket Erstellungs Tools von Drittanbietern oder SDK-Tools wie [Orca.exe](orca-exe.md) , um eine Installations Datenbank aufzufüllen und ein Windows Installer Paket zu erstellen.

    Weitere Informationen finden Sie unter

    -   [Entwicklungs Tools für Windows Installer](windows-installer-development-tools.md)
    -   [Installationspaket, Informationen zur Installer-Datenbank](installation-package.md)
    -   [Dateierweiterungen Windows Installer](windows-installer-file-extensions.md)
    -   [Datenbanktabellen](database-tables.md)
    -   [Paket Codes](package-codes.md)
    -   [Erstellen eines großen Pakets](authoring-a-large-package.md)
    -   [Windows Installer auf 64-Bit-Betriebssystemen](windows-installer-on-64-bit-operating-systems.md)
    -   [Benennen von benutzerdefinierten Tabellen, Eigenschaften und Aktionen](naming-custom-tables-properties-and-actions.md)
    -   [OLE-Einschränkungen für Streams](ole-limitations-on-streams.md)
    -   [Spalten Definitions Format](column-definition-format.md)
    -   [Reduzieren der Größe einer MSI-Datei](reducing-the-size-of-an--msi-file.md)

-   Erstellen Sie die Windows Installer Datenbank, um Dateien zu installieren.

    Weitere Informationen finden Sie unter

    -   [Kern Tabellen Gruppe](core-tables-group.md)
    -   [Datei Tabellen Gruppe](file-tables-group.md)
    -   [Dateitabelle](file-table.md)
    -   [Dateisuche](file-searching.md)
    -   [Datei Kosten](file-costing.md)
    -   [Datei Installation](file-installation.md)
    -   [Begleit Dateien](companion-files.md)
    -   [Regeln für die Datei Versionsverwaltung](file-versioning-rules.md)
    -   [Standardmäßige Datei Versionsverwaltung](default-file-versioning.md)
    -   [Ersetzen vorhandener Dateien](replacing-existing-files.md)
    -   [Verwenden von Schränken und komprimierten Quellen](using-cabinets-and-compressed-sources.md)
    -   [Entfernen von gestrandeten Dateien](removing-stranded-files.md)
    -   [Installieren von permanenten Komponenten, Dateien, Schriftarten, Registrierungs Schlüsseln](installing-permanent-components-files-fonts-registry-keys.md)
    -   [Filesfpcatalog-Tabelle](filesfpcatalog-table.md)
    -   [Suchen nach einer Datei und Erstellen einer Eigenschaft mit dem Pfad der Datei](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
    -   [Suchen nach einem Verzeichnis und einer Datei im Verzeichnis](searching-for-a-directory-and-a-file-in-the-directory.md)
    -   [Windows Installer Beispiele](windows-installer-examples.md)

-   Erstellen Sie eine Windows Installer Datenbank, die eine Verzeichnisstruktur und Ordner installiert.

    Weitere Informationen finden Sie unter

    -   [Kern Tabellen Gruppe](core-tables-group.md)
    -   [Datei Tabellen Gruppe](file-tables-group.md)
    -   [Komponenten Tabelle](component-table.md)
    -   [Verzeichnis Tabelle](directory-table.md)
    -   [Verwenden der Verzeichnis Tabelle](using-the-directory-table.md)
    -   [Verwenden einer Verzeichnis Eigenschaft in einem Pfad](using-a-directory-property-in-a-path.md)
    -   [Eigenschaften von System Ordnern](property-reference.md)
    -   [Tabelle "Buildordner"](createfolder-table.md)
    -   [Lockberechtigungs Tabelle](lockpermissions-table.md)
    -   [Msilockpermissionsex-Tabelle](msilockpermissionsex-table.md)
    -   [Ändern des Zielspeicher Orts für ein Verzeichnis](changing-the-target-location-for-a-directory.md)
    -   [Windows Installer Beispiele](windows-installer-examples.md)

-   Erstellen Sie eine Windows Installer Datenbank, die Registrierungsschlüssel installiert.

    Weitere Informationen finden Sie unter

    -   [Kern Tabellen Gruppe](core-tables-group.md)
    -   [Registrierungs Tabellen Gruppe](registry-tables-group.md)
    -   [Registrierungs Tabelle](registry-table.md)
    -   [Ändern der Registrierung](modifying-the-registry.md)
    -   [Hinzufügen oder Entfernen von Registrierungs Schlüsseln zum Installieren oder Entfernen von Komponenten](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)
    -   [Hinzufügen und Entfernen einer Anwendung ohne Ablauf Verfolgung in der Registrierung](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [Installieren von permanenten Komponenten, Dateien, Schriftarten, Registrierungs Schlüsseln](installing-permanent-components-files-fonts-registry-keys.md)
    -   [Suchen nach vorhandenen Anwendungen, Dateien, Registrierungs Einträgen oder INI-Datei Einträgen](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
    -   [Suchen nach einem Registrierungs Eintrag und Erstellen einer Eigenschaft mit dem Wert der Registrierung](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)
    -   [Vom Windows Installer geschriebene assemblyregistrierungsschlüssel](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Registrierungsschlüssel deinstallieren](uninstall-registry-key.md)
    -   [Selfreg-Tabelle](selfreg-table.md)
    -   [Angeben der Reihenfolge der Selbstregistrierung](specifying-the-order-of-self-registration.md)
    -   [Windows Installer Beispiele](windows-installer-examples.md)

-   Erstellen Sie eine Windows Installer Datenbank, mit der Dienste installiert werden.

    Weitere Informationen finden Sie unter

    -   [Servicabstall-Tabelle](serviceinstall-table.md)
    -   [ServiceControl-Tabelle](servicecontrol-table.md)
    -   [Komponenten Tabelle](component-table.md)

-   Erstellen Sie eine Windows Installer Datenbank, mit der isolierte Komponenten oder COM-Komponenten installiert werden.

    Weitere Informationen finden Sie unter

    -   [Registrierungs Tabellen Gruppe](registry-tables-group.md)
    -   [Klassen Tabelle](class-table.md)
    -   [ComPlus-Tabelle](complus-table.md)
    -   [Isolierte Komponenten](isolated-components.md)
    -   [Verwenden isolierter Komponenten](using-isolated-components.md)
    -   [Installation isolierter Komponenten](installation-of-isolated-components.md)
    -   [Neuinstallation isolierter Komponenten](reinstallation-of-isolated-components.md)
    -   [Entfernen isolierter Komponenten](removal-of-isolated-components.md)
    -   [Installieren einer COM-Komponente an einem privaten Speicherort](installing-a-com-component-to-a-private-location.md)
    -   [Erstellen einer COM-Komponente in einem vorhandenen Paket](make-a-com-component-in-an-existing-package-private.md)
    -   [Installieren einer COM+-Anwendung mit der Windows Installer](installing-a-com--application-with-the-windows-installer.md)
    -   [Installieren einer nicht-COM-Komponente an einem privaten Speicherort](installing-a-non-com-component-to-a-private-location.md)
    -   [Erstellen einer nicht-COM-Komponente in einem vorhandenen Paket](make-a-non-com-component-in-an-existing-package-private.md)

-   Erstellen Sie eine Windows Installer Datenbank, die Assemblys installiert.

    Weitere Informationen finden Sie unter

    -   [MsiAssembly-Tabelle](msiassembly-table.md)
    -   [MsiAssemblyName-Tabelle](msiassemblyname-table.md)
    -   [Assemblys](assemblies.md)
    -   [Vom Windows Installer geschriebene assemblyregistrierungsschlüssel](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Installation von Win32-Assemblys](installation-of-win32-assemblies.md)

-   Erstellen Sie eine Windows Installer Datenbank, die ODBC-Treiber und-Konvertierer installiert.

    Weitere Informationen finden Sie unter

    -   [Odbingtribute-Tabelle](odbcattribute-table.md)
    -   [Odbcdriver-Tabelle](odbcdriver-table.md)
    -   [Odbctranslator-Tabelle](odbctranslator-table.md)
    -   [ODBCDatasource-Tabelle](odbcdatasource-table.md)
    -   [Odbcsourceattribute-Tabelle](odbcsourceattribute-table.md)

-   Erstellen Sie eine Windows Installer Datenbank, die MIME installiert.

    Weitere Informationen finden Sie unter

    -   [MIME-Tabelle](mime-table.md)
    -   [Erweiterungs Tabelle](extension-table.md)
    -   [Ändern der Registrierung](modifying-the-registry.md)

-   Erstellen Sie eine Windows Installer Datenbank, die Umgebungsvariablen installiert.

    Weitere Informationen finden Sie unter

    -   [Umgebungs Tabelle](environment-table.md)

-   Erstellen Sie eine Windows Installer Datenbank, die Verknüpfungen installiert.

    Weitere Informationen finden Sie unter

    -   [Verknüpfungs Tabelle](shortcut-table.md)
    -   [Msishortcutproperty-Tabelle](msishortcutproperty-table.md)
    -   [Bearbeiten von Installationsprogramm Kombinationen](editing-installer-shortcuts.md)
    -   [Windows Installer Beispiele](windows-installer-examples.md)

-   Erstellen Sie eine Windows Installer Datenbank, die mehrere Anwendungs Instanzen installiert.

    Weitere Informationen finden Sie unter

    -   [Installieren mehrerer Instanzen von Produkten und Patches](installing-multiple-instances-of-products-and-patches.md)
    -   [Erstellen mehrerer Instanzen mit instanztransformationen](authoring-multiple-instances-with-instance-transforms.md)
    -   [Installieren mehrerer Instanzen mit instanztransformationen](installing-multiple-instances-with-instance-transforms.md)

-   Geben Sie die Standardoptionen für die Funktionsauswahl an.

    Weitere Informationen finden Sie unter

    -   [Kern Tabellen Gruppe](core-tables-group.md)
    -   [Komponenten Tabelle](component-table.md)
    -   [Funktions Tabelle](feature-table.md)
    -   [FeatureComponents-Tabelle](featurecomponents-table.md)
    -   [Steuern von Funktionsauswahl Zuständen](controlling-feature-selection-states.md)
    -   [Eigenschaften von featureinstallationsoptionen](property-reference.md)

-   Geben Sie Bedingungen an, die erfüllt sein müssen, um eine Anwendung oder ausgewählte Komponenten zu installieren.

    Weitere Informationen finden Sie unter

    -   [Bedingungs Tabelle](condition-table.md)
    -   [LaunchCondition-Tabelle](launchcondition-table.md)
    -   [Komponenten Tabelle](component-table.md)
    -   [Verwenden von Eigenschaften in Bedingungs Anweisungen](using-properties-in-conditional-statements.md)
    -   [Syntax der bedingten Anweisung](conditional-statement-syntax.md)
    -   [Während des Entfernens auszuführende Aufbereitungs Aktionen](conditioning-actions-to-run-during-removal.md)
    -   [Beispiele für bedingte Anweisungs Syntax](examples-of-conditional-statement-syntax.md)

-   Erstellen Sie die Abfolge der Aktionen, die zum Installieren der Anwendung verwendet werden.

    Weitere Informationen finden Sie unter

    -   [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md)
    -   [Gruppe "Installationsprozedur Tabellen"](installation-procedure-tables-group.md)
    -   [Beispiel für eine detaillierte Sequenz Tabelle](sequence-table-detailed-example.md)
    -   [Aktionen mit Sequenz Einschränkungen](actions-with-sequencing-restrictions.md)
    -   [Aktionen ohne Sequenz Einschränkungen](actions-without-sequencing-restrictions.md)
    -   [Verwenden von Eigenschaften in Bedingungs Anweisungen](using-properties-in-conditional-statements.md)
    -   [Syntax der bedingten Anweisung](conditional-statement-syntax.md)
    -   [Beispiele für bedingte Anweisungs Syntax](examples-of-conditional-statement-syntax.md)
    -   [Während des Entfernens auszuführende Aufbereitungs Aktionen](conditioning-actions-to-run-during-removal.md)
    -   [Standard Aktionen](standard-actions.md)
    -   [Windows Installer Beispiele](windows-installer-examples.md)

-   Bereiten Sie das Installationspaket der Anwendung für zukünftige Upgrades der Anwendung durch den Windows Installer-Dienst vor.

    Weitere Informationen finden Sie unter

    -   [Patchen und Upgrades](patching-and-upgrades.md)
    -   [Vorbereiten einer Anwendung für zukünftige größere Upgrades](preparing-an-application-for-future-major-upgrades.md)
    -   [Verwenden von UpgradeCode](using-an-upgradecode.md)
    -   [Upgradetabelle](upgrade-table.md)
    -   [**UpgradeCode-Eigenschaft**](upgradecode.md)
    -   [Verhindern, dass ein altes Paket über eine neuere Version installiert wird](preventing-an-old-package-from-installing-over-a-newer-version.md)
    -   [Ändern des Produktcodes](changing-the-product-code.md)
    -   [Aktualisieren von Assemblys](updating-assemblies.md)
    -   [Windows Installer Beispiele](windows-installer-examples.md)

-   Problembehandlung bei Windows Installer Paketen in der Entwicklung.

    Weitere Informationen finden Sie unter

    -   [Paketvalidierung](package-validation.md)
    -   [Interne Konsistenz Auswertung-ICES](internal-consistency-evaluators-ices.md)
    -   [Windows Installer Protokollierung](windows-installer-logging.md)
    -   [Überprüfen der Installation von Features, Komponenten, Dateien](checking-the-installation-of-features-components-files.md)
    -   [Erstellen eines großen Pakets](authoring-a-large-package.md)
    -   [Wilogutl.exe](wilogutl-exe.md)
    -   [Entwicklungs Tools für Windows Installer](windows-installer-development-tools.md)
    -   [Validieren von Mergemodulen](validating-merge-modules.md)
    -   [Überprüfen einer Installations Datenbank](validating-an-installation-database.md)
    -   [Überprüfen eines Installations Upgrades](validating-an-installation-upgrade.md)
    -   [Suchen nach einer unterbrochenen Funktion oder Komponente](searching-for-a-broken-feature-or-component.md)
    -   [Windows Installer von Fehlermeldungen](windows-installer-error-messages.md)
    -   [Protokollierung von Neustart Anforderungen](logging-of-reboot-requests.md)

-   Stellen Sie eine sichere Einrichtung und Installation der Anwendung sicher.

    Weitere Informationen finden Sie unter

    -   [Richtlinien für das Erstellen von sicheren Installationen](guidelines-for-authoring-secure-installations.md)
    -   [Richtlinien zum Sichern von benutzerdefinierten Aktionen](guidelines-for-securing-custom-actions.md)
    -   [Sicherheit für benutzerdefinierte Aktionen](custom-action-security.md)
    -   [Richtlinien zum Sichern von Paketen auf gesperrten Computern](guidelines-for-securing-packages-on-locked-down-computers.md)
    -   [Erstellen einer vollständig überprüften signierten Installation mithilfe von Automation](authoring-a-fully-verified-signed-installation-using-automation.md)
    -   [URL-basiertes Windows Installer-Installationsbeispiel](a-url-based-windows-installer-installation-example.md)
    -   [Erstellen der Benutzeroberfläche für die Kenn Wort Eingabe](authoring-the-user-interface-for-password-input.md)
    -   [Digitale Signaturen und Windows Installer](digital-signatures-and-windows-installer.md)
    -   [Verwenden von Windows Installer mit UAC](using-windows-installer-with-uac.md)
    -   [Patching der Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md)
    -   [Msicert.exe](msicert-exe.md)
    -   [**AdminUser (Eigenschaft)**](adminuser.md)
    -   [**Privilegierte Eigenschaft**](privileged.md)
    -   [**Securecustomproperties (Eigenschaft)**](securecustomproperties.md)

-   Erstellen Sie eine Benutzeroberfläche, um Optionen zum Konfigurieren der Installation und zum Abrufen von Informationen vom Benutzer zum ausstehenden Installationsvorgang zu präsentieren.

    Weitere Informationen finden Sie unter

    -   [Informationen zur Benutzeroberfläche](about-the-user-interface.md)
    -   [Hinzufügen von Steuerelementen und Text](adding-controls-and-text.md)
    -   [Erstellen eines ProgressBar-Steuer Elements](authoring-a-progressbar-control.md)
    -   [Erstellen von Datenträger Aufforderungs Meldungen](authoring-disk-prompt-messages.md)
    -   [Erstellen einer bedingten "Bitte warten..." Meldungs Feld](authoring-a-conditional-please-wait-------message-box.md)
    -   [Anzeigen der Vorschau der Benutzeroberfläche](previewing-the-user-interface.md)
    -   [Hinzufügen von in einer Eigenschaft gespeicherten Text](adding-text-stored-in-a-property.md)
    -   [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

-   Erstellen Sie eine externe Benutzeroberfläche, um eine benutzerdefinierte Benutzeroberfläche zum Konfigurieren der Installation und zum Abrufen von Informationen vom Benutzer zum ausstehenden Installationsvorgang zu präsentieren.

    Weitere Informationen finden Sie unter

    -   [**Msiseeltexternalui**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
    -   [Überwachen einer Installation mithilfe von "msiabtexternaluirecord"](monitoring-an-installation-using-msisetexternaluirecord.md)
    -   [Windows Installer Meldungen werden verarbeitet.](parsing-windows-installer-messages.md)
    -   [Zurückgeben von Werten von einem externen Benutzeroberflächen Handler](returning-values-from-an-external-user-interface-handler.md)
    -   [installui- \_ Handler](/windows/desktop/api/Msi/nc-msi-installui_handlera)
    -   [Verarbeiten von Statusmeldungen mithilfe von "msieintexternalui"](handling-progress-messages-using-msisetexternalui.md)
    -   [Überwachen einer Installation mithilfe von "msieintexternalui"](monitoring-an-installation-using-msisetexternalui.md)

-   Festlegen von Informationen für die Anwendung **in "** Software" (ARP)

    Weitere Informationen finden Sie unter

    -   [Konfigurieren von "Programme hinzufügen/entfernen" mit Windows Installer](configuring-add-remove-programs-with-windows-installer.md)
    -   [Hinzufügen und Entfernen einer Anwendung ohne Ablauf Verfolgung in der Registrierung](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [Registrierungsschlüssel deinstallieren](uninstall-registry-key.md)

-   Schreiben Sie benutzerdefinierte Aktionen, um die Setup Logik zu behandeln, die von Windows Installer nicht System intern unterstützt wird.

    Weitere Informationen finden Sie unter

    -   [Benutzerdefinierte Aktionen](custom-actions.md)
    -   [Zusammenfassungs Liste aller benutzerdefinierten Aktions Typen](summary-list-of-all-custom-action-types.md)
    -   [Richtlinien zum Sichern von benutzerdefinierten Aktionen](guidelines-for-securing-custom-actions.md)
    -   [Referenz zu benutzerdefinierten Aktionen](custom-action-reference.md)
    -   [Verwenden einer benutzerdefinierten Aktion zum Erstellen von Benutzerkonten auf einem lokalen Computer](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [Verwenden einer benutzerdefinierten Aktion zum Starten einer installierten Datei am Ende der Installation](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
    -   [Zugreifen auf eine Datenbank oder eine Sitzung innerhalb einer benutzerdefinierten Aktion](accessing-a-database-or-session-from-inside-a-custom-action.md)
    -   [Zugreifen auf die aktuelle Installer-Sitzung innerhalb einer benutzerdefinierten Aktion](accessing-the-current-installer-session-from-inside-a-custom-action.md)
    -   [Ändern des System Status mithilfe einer benutzerdefinierten Aktion](changing-the-system-state-using-a-custom-action.md)

-   Bootstrap der Windows Installer auf den Computer eines Benutzers.

    Weitere Informationen finden Sie unter

    -   [Bootstrapping](bootstrapping.md)
    -   [Instmsi.exe](instmsi-exe.md)
    -   [Internetdownload-Bootstrapping](internet-download-bootstrapping.md)
    -   [Msistuff.exe](msistuff-exe.md)
    -   [URL-basiertes Windows Installer-Installationsbeispiel](a-url-based-windows-installer-installation-example.md)
    -   [Konfigurieren der Setup.exe Ressourcen](configuring-the-setup-exe-resources.md)
    -   [Herunterladen einer Installation aus dem Internet](downloading-an-installation-from-the-internet.md)

-   Beachten Sie Active Accessibility Richtlinien beim Schreiben von Windows Installer Paketen.

    Weitere Informationen finden Sie unter

    -   [Bedienungshilfen](accessibility.md)

-   Bereiten Sie die Internationalisierung eines Anwendungs Setups vor.

    Weitere Informationen finden Sie unter

    -   [Vorbereiten eines Windows Installer Pakets für die Lokalisierung](preparing-a-windows-installer-package-for-localization.md)
    -   [Lokalisieren eines Windows Installer Pakets](localizing-a-windows-installer-package.md)
    -   [Code Page Behandlung (Windows Installer)](code-page-handling-windows-installer-.md)
    -   [Hinzufügen lokalisierter Ressourcen](adding-localized-resources.md)
    -   [Beispiel für eine Lokalisierung](a-localization-example.md)
    -   [Lokalisieren von Fehler-und Aktions Text Tabellen](localizing-the-error-and-actiontext-tables.md)
    -   [Lokalisieren von Daten Bank Spalten](localizing-database-columns.md)
    -   [Erstellen einer Datenbank mit einer neutralen Codepage](creating-a-database-with-a-neutral-code-page.md)
    -   [Code Page Behandlung importierter und exportierter Tabellen](code-page-handling-of-imported-and-exported-tables.md)
    -   [Lokalisieren der von Dialogfeldern angezeigten Sprache](localizing-the-language-displayed-by-dialogs.md)
    -   [Importieren lokalisierter Fehler-und Aktions Text Tabellen](importing-localized-error-and-actiontext-tables.md)
    -   [Aktualisieren von productlanguage-und ProductCode-Eigenschaften](updating-productlanguage-and-productcode-properties.md)
    -   [Aktualisieren eines Zusammenfassungs Informationsdaten Stroms](updating-a-summary-information-stream.md)
    -   [Qualifizierte Komponenten](qualified-components.md)
    -   [UIText-Tabelle](uitext-table.md)
    -   [Verwalten von Sprache und Codepage](manage-language-and-codepage.md)
    -   [Die Codepage der Installations Datenbank wird überprüft.](checking-the-installation-database-code-page.md)

-   Erstellen Sie Windows Installer Pakete für 32-Bit-und 64-Bit-Plattformen.

    Weitere Informationen finden Sie unter

    -   [Windows Installer auf 64-Bit-Betriebssystemen](windows-installer-on-64-bit-operating-systems.md)
    -   [benutzerdefinierte 64-Bit-Aktionen](64-bit-custom-actions.md)
    -   [Verwenden von benutzerdefinierten 64-Bit-Aktionen](using-64-bit-custom-actions.md)
    -   [Verwenden von 64-Bit-Mergemodulen](using-64-bit-merge-modules.md)

-   Verteilen Sie freigegebene Windows Installer Komponenten und Setup Logik als Mergemodule neu.

    Weitere Informationen finden Sie unter

    -   [Mergemodule](merge-modules.md)
    -   [Erstellen einer sprach Transformation für ein Mergemodul mit mehreren Sprachen](authoring-a-language-transform-for-a-multiple-language-merge-module.md)
    -   [Anwenden eines konfigurierbaren Mergemoduls mit Anpassungen](applying-a-configurable-merge-module-with-customizations.md)

-   Planen oder Unterdrücken von Neustarts während einer Windows Installer Installation.

    Weitere Informationen finden Sie unter

    -   [System Neustarts](system-reboots.md)
    -   [Protokollierung von Neustart Anforderungen](logging-of-reboot-requests.md)

-   Erstellen Sie Updates oder Korrekturen für eine vorhandene Anwendung, indem Sie einen Patch erstellen.

    Weitere Informationen finden Sie unter

    -   [Erstellen eines kleinen Update-Patches](creating-a-small-update-patch.md)
    -   [Beispiel für ein kleines Update-Patching](a-small-update-patching-example.md)

-   Erstellen Sie ein Paket mit zwei Zweck, mit dem eine Anwendung entweder nur für den aktuellen Benutzer oder für alle Benutzer des Computers installiert werden können.

    Weitere Informationen finden Sie unter

    -   [Installations Kontext](installation-context.md)
    -   [Erstellung eines einzelnen Pakets](single-package-authoring.md)
    -   [Beispiel für eine einmalige Paket Erstellung](single-package-authoring-example.md)

-   Passen Sie die Dienste auf dem Computer mithilfe der Windows Installer an.

    Weitere Informationen finden Sie unter

    -   [Verwenden der Dienst Konfiguration](using-services-configuration.md)

-   Sichern Sie die Ressourcen auf dem Computer mithilfe der Windows Installer.

    Weitere Informationen finden Sie unter

    -   [Richtlinien für das Erstellen von sicheren Installationen](guidelines-for-authoring-secure-installations.md)
    -   [Sichern von Ressourcen](securing-resources-.md)

-   Listet alle auf dem Computer installierten Komponenten auf und ruft den Schlüssel Pfad für die Komponente ab.

    Weitere Informationen finden Sie unter

    -   [Auflisten von Komponenten](enumerating-components-.md)

-   Installieren Sie mehrere Pakete mithilfe der [*Transaktionsverarbeitung*](t-gly.md).

    Weitere Informationen finden Sie unter

    -   [Installationen mit mehreren Paketen](multiple-package-installations.md)

-   Betten Sie eine benutzerdefinierte Benutzeroberfläche in das Windows Installer-Paket ein.

    Weitere Informationen finden Sie unter

    -   [Verwenden der Benutzeroberfläche](using-the-user-interface.md)
    -   [Verwenden einer eingebetteten Benutzeroberfläche](using-an-embedded-ui.md)

## <a name="it-professionals"></a>IT-Fachleute

IT-Fachleute und Administratoren passen vorhandene Windows Installer Pakete an und stellen Sie bereit. Diese Benutzer Verpacken Setups für vorhandene Anwendungen in Windows Installer Installationspaketen und installieren und warten administrative Images von Windows Installer Installationen in Netzwerken.

-   Anpassen von Anwendungen und Setup durch das erzeugen und Anwenden von Windows Installer Transformationen

    Weitere Informationen finden Sie unter

    -   [Anpassung](customization.md)
    -   [Daten Bank Transformationen](database-transforms.md)
    -   [Beispiel für eine Anpassungs Transformation](a-customization-transform-example.md)
    -   [Zusammenführungen und Transformationen](merges-and-transforms.md)
    -   [Verwenden von Transformationen zum Hinzufügen von Ressourcen](using-transforms-to-add-resources.md)
    -   [Generieren einer Transformation](generate-a-transform.md)
    -   [Befehlszeilenoptionen](command-line-options.md)
    -   [Msitran.exe](msitran-exe.md)
    -   [Anwenden einer Transformation](apply-a-transform.md)
    -   [Anzeigen einer Transformation](view-a-transform.md)
    -   [Anzeigen von Unterschieden zwischen zwei Datenbanken](view-differences-between-two-databases.md)
    -   [Patchen von angepassten Anwendungen](patching-customized-applications.md)

-   Stellen Sie ein Windows Installer Installationspaket, ein Update oder einen Patch bereit.

    Weitere Informationen finden Sie unter

    -   [Installieren einer Anwendung](installing-an-application.md)
    -   [Patchen und Upgrades](patching-and-upgrades.md)
    -   [Transformationen](transforms.md)
    -   [Installieren eines Pakets mit erhöhten Rechten für einen nicht Administrator](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Anwenden von größeren Upgrades durch Patchen der lokalen Installation des Produkts](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)
    -   [Anwenden von größeren Upgrades durch Installieren des Produkts](applying-major-upgrades-by-installing-the-product.md)
    -   [Anwenden von kleinen Updates durch Patchen der lokalen Installation des Produkts](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [Anwenden von kleinen Updates durch Neuinstallation des Produkts](applying-small-updates-by-reinstalling-the-product.md)
    -   [Anwenden von kleinen Updates durch Patchen eines administrativen Abbilds](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Patchen von erst Installationen](patching-initial-installations.md)
    -   [Befehlszeilenoptionen](command-line-options.md)

-   Behandeln von Problemen mit Windows Installer Paketen

    Weitere Informationen finden Sie unter

    -   [Windows Installer Protokollierung](windows-installer-logging.md)
    -   [Überprüfen der Installation von Features, Komponenten, Dateien](checking-the-installation-of-features-components-files.md)
    -   [Wilogutl.exe](wilogutl-exe.md)
    -   [Suchen nach einer unterbrochenen Funktion oder Komponente](searching-for-a-broken-feature-or-component.md)
    -   [Windows Installer von Fehlermeldungen](windows-installer-error-messages.md)
    -   [Msicert.exe](msicert-exe.md)

-   Verwenden Sie Skripts zum Abfragen von Windows Installer Paketen, um Informationen zu einem Produkt zu finden und die Installation zu ändern.

    Weitere Informationen finden Sie unter

    -   [Automatisierungsschnittstelle](automation-interface.md)
    -   [Skript Beispiele für Windows Installer](windows-installer-scripting-examples.md)
    -   [Verwenden von Windows Installer mit WMI](using-windows-installer-with-wmi.md)

-   Erstellen und warten Sie administrative Installationen.

    Weitere Informationen finden Sie unter

    -   [Administrative Installation](administrative-installation.md)
    -   [Befehlszeilenoptionen](command-line-options.md)
    -   [**Adminproperties (Eigenschaft)**](adminproperties.md)
    -   [Anwenden von kleinen Updates durch Patchen eines administrativen Abbilds](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Anwenden eines Patchpakets auf eine administrative Installation](applying-a-patch-package-to-an-administrative-installation.md)
    -   [Aktions Ausführungsreihenfolge](action-execution-order.md)
    -   [**Isadminpackage (Eigenschaft)**](isadminpackage.md)
    -   [Reihenfolge der Eigenschafts Rangfolge](order-of-property-precedence.md)
    -   [**Adminproperties (Eigenschaft)**](adminproperties.md)

-   Stellen Sie eine Anwendung für alle Benutzer eines Computers oder nur für einen bestimmten Benutzer zur Verfügung.

    Weitere Informationen finden Sie unter

    -   [Installations Kontext](installation-context.md)
    -   [**ALLUSERS (Eigenschaft)**](allusers.md)

-   Verwenden Sie die Befehlszeile, um Pakete zu interpretieren, Produkte zu installieren und Funktions Optionen zu konfigurieren.

    Weitere Informationen finden Sie unter

    -   [Befehlszeilenoptionen](command-line-options.md)
    -   [Festlegen von Werten für öffentliche Eigenschaften in der Befehlszeile](setting-public-property-values-on-the-command-line.md)
    -   [Eigenschaften werden erhalten und festgelegt](getting-and-setting-properties.md)
    -   [Neuinstallieren eines Features oder einer Anwendung](reinstalling-a-feature-or-application.md)
    -   [Anwenden von kleinen Updates durch Patchen der lokalen Installation des Produkts](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [Anwenden von kleinen Updates durch Neuinstallation des Produkts](applying-small-updates-by-reinstalling-the-product.md)
    -   [Ändern des Zielspeicher Orts für ein Verzeichnis](changing-the-target-location-for-a-directory.md)
    -   [Anwenden von kleinen Updates durch Patchen eines administrativen Abbilds](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Anwenden von größeren Upgrades durch Installieren des Produkts](applying-major-upgrades-by-installing-the-product.md)
    -   [Konfigurations Eigenschaften](property-reference.md)
    -   [Eigenschaften von featureinstallationsoptionen](property-reference.md)

-   Arbeiten Sie mit der Richtlinie, um Zugriffsrechte und Berechtigungen zu verwalten.

    Weitere Informationen finden Sie unter

    -   [Computer Richtlinien](machine-policies.md),
    -   [Benutzerrichtlinien](user-policies.md)
    -   [Installieren eines Pakets mit erhöhten Rechten für einen nicht Administrator](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Ankündigen einer Per-User Anwendung, die mit erhöhten Rechten installiert werden soll](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [Verwenden einer benutzerdefinierten Aktion zum Erstellen von Benutzerkonten auf einem lokalen Computer](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [**AdminUser (Eigenschaft)**](adminuser.md)
    -   [**Privilegierte Eigenschaft**](privileged.md)
    -   [**Enableusercontrol (Eigenschaft)**](enableusercontrol.md)
    -   [**UserSID-Eigenschaft**](usersid.md)
    -   [**Securecustomproperties (Eigenschaft)**](securecustomproperties.md)

-   Installieren Sie mehrere Pakete mithilfe der [*Transaktionsverarbeitung*](t-gly.md).

    Weitere Informationen finden Sie unter

    -   [Installationen mit mehreren Paketen](multiple-package-installations.md)

-   Betten Sie eine benutzerdefinierte Benutzeroberfläche in ein Windows Installer Paket ein.

    Weitere Informationen finden Sie unter

    -   [Verwenden der Benutzeroberfläche](using-the-user-interface.md)
    -   [Verwenden einer eingebetteten Benutzeroberfläche](using-an-embedded-ui.md)

## <a name="infrastructure-developers"></a>Infrastruktur Entwickler

Infrastruktur Entwickler können einheitliche Plattformen für die Bereitstellung und Verwaltung von Software erstellen, die den Windows Installer-Dienst verwendet. Sie können die Windows Installer Programmierschnittstelle verwenden, um Anwendungen, Patches und Quellen auf einem System abzufragen, zu verwalten und zu verteilen.

-   Suchen, inventarisieren und Abfragen des Zustands, der Informationen und der Clients von Komponenten.

    Weitere Informationen finden Sie unter

    -   [Komponenten spezifische Funktionen](installer-function-reference.md)
    -   [System Status Funktionen](installer-function-reference.md)
    -   [Installer-Objekt](installer-object.md)
    -   [Product-Objekt](product-object.md)
    -   [Patch-Objekt](patch-object.md)

-   Inventarisieren Sie Informationen und den Status von Produkten und Features, und Fragen Sie Sie ab.

    Weitere Informationen finden Sie unter

    -   [Inventur Produkte und Patches](inventory-products-and-patches-.md)
    -   [System Status Funktionen](installer-function-reference.md)
    -   [Product Query-Funktionen](installer-function-reference.md)
    -   [Installer-Objekt](installer-object.md)
    -   [Product-Objekt](product-object.md)
    -   [Patch-Objekt](patch-object.md)

-   Verbessern Sie die Resilienz der Quelle, indem Sie die Windows Installer zum Inventarisieren, Abfragen und Ändern der Quell Liste von Anwendungen, Upgrades und Patches verwenden.

    Weitere Informationen finden Sie unter

    -   [**SourceList-Eigenschaft**](sourcelist.md)
    -   [**Quellen Resilienz**](source-resiliency.md)
    -   [Installations-und Konfigurationsfunktionen](installer-function-reference.md)
    -   [Installer-Objekt](installer-object.md)
    -   [Product-Objekt](product-object.md)
    -   [Patch-Objekt](patch-object.md)

-   Verbessern Sie die Resilienz der Quelle, indem Sie mithilfe der Windows Installer Medienquellen inventarisieren, Abfragen und ändern.

    Weitere Informationen finden Sie unter

    -   [**SourceList-Eigenschaft**](sourcelist.md)
    -   [Quellen Resilienz](source-resiliency.md)
    -   [Installations-und Konfigurationsfunktionen](installer-function-reference.md)
    -   [Product-Objekt](product-object.md)
    -   [Patch-Objekt](patch-object.md)

-   Inventarisieren Sie Informationen und den Status von Patches, um diese abzufragen.

    Weitere Informationen finden Sie unter

    -   [Inventur Produkte und Patches](inventory-products-and-patches-.md)
    -   [Installationsfunktionsverweis](installer-function-reference.md)
    -   [Patch-Objekt](patch-object.md)

-   Arbeiten Sie mit der Richtlinie, um Zugriffsrechte und Berechtigungen zu verwalten.

    Weitere Informationen finden Sie unter

    -   [Computer Richtlinien](machine-policies.md)
    -   [Benutzerrichtlinien](user-policies.md)
    -   [Installieren eines Pakets mit erhöhten Rechten für einen nicht Administrator](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Ankündigen einer Per-User Anwendung, die mit erhöhten Rechten installiert werden soll](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [Verwenden einer benutzerdefinierten Aktion zum Erstellen von Benutzerkonten auf einem lokalen Computer](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [**AdminUser (Eigenschaft)**](adminuser.md)
    -   [**Privilegierte Eigenschaft**](privileged.md)
    -   [**Enableusercontrol (Eigenschaft)**](enableusercontrol.md)
    -   [**UserSID-Eigenschaft**](usersid.md)
    -   [**Securecustomproperties (Eigenschaft)**](securecustomproperties.md)

 

 



