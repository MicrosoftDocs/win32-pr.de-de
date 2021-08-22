---
description: Windows Das Installationsprogramm ist die empfohlene Lösung für die Installation und Einrichtung von Anwendungen auf Windows.
ms.assetid: 13f41020-5275-44cd-b26b-f45483700d8a
title: Dokumentation zum rollenbasierten Leitfaden zum Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f886050f3bb0256f6f0f993e613be940cee9cd2fe748b2d17b5dc0f0f84a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625862"
---
# <a name="role-based-guide-to-windows-installer-documentation"></a>Dokumentation zum rollenbasierten Leitfaden zum Windows Installer

Windows Das Installationsprogramm ist die empfohlene Lösung für die Installation und Einrichtung von Anwendungen auf Windows. Daher sind einige der in diesem SDK enthaltenen Informationen für eine Vielzahl von Softwareentwicklungs- und IT-Experten von Interesse. Dieser Abschnitt wird als Leitfaden für Leser bereitgestellt, die lieber Links zu Themen anzeigen möchten, die nach professionellen Rollen und allgemeinen Aufgabenszenarien organisiert sind. Da sich Rollen zwischen Organisationen stark unterscheiden können, sollte die folgende Gruppierung nur als Leitfaden für einen Standort betrachtet werden, um mit der Suche nach den benötigten Informationen zu beginnen.

-   [Anwendungsentwickler](#application-developers)
-   [Setupautoren](#setup-authors)
-   [IT-Fachleute](#it-professionals)
-   [Infrastrukturentwickler](#infrastructure-developers)

Diese Dokumentation richtet sich an Softwareentwickler, die Anwendungen erstellen möchten, die Windows Installer verwenden. Als primäre Quelle des Referenzmaterials für das Installationsprogramm stellt das SDK Informationen zu Installationspaketen und dem Installationsprogrammdienst bereit. Sie enthält vollständige Beschreibungen der Anwendungsprogrammierschnittstelle (Application Programming Interface, API) und der Elemente der Installer-Datenbank.

Weitere Informationen finden Sie unter [Andere Quellen von Windows Installer-Informationen.](other-sources-of-windows-installer-information.md)

## <a name="application-developers"></a>Anwendungsentwickler

Anwendungsentwickler erstellen Anwendungen, die die Windows Installer-Anwendungsprogrammierschnittstelle aufrufen und Windows Installationspakete zur Laufzeit installieren. Der Windows Installer kann in einer Anwendung arbeiten, z. B. selbstreparatur und installation-on-demand. In der Regel gehen Anwendungsentwickler wie folgt vor:

-   Aktivieren Sie die bedarfsorientierte Installation von Anwendungen zur Laufzeit innerhalb einer anderen Anwendung.

    Weitere Informationen finden Sie unter

    -   [Verwenden von Installerfunktionen](using-installer-functions.md)
    -   [Referenz zur Installerfunktion](installer-function-reference.md)
    -   [Installation bei Bedarf](installation-on-demand.md)
    -   [Verwaltung von Komponenten](component-management.md)
    -   [Bearbeiten von Installerverknüpfungen](editing-installer-shortcuts.md)
    -   [**OLEAdvtSupport-Eigenschaft**](oleadvtsupport.md)
    -   [Plattformunterstützung von Ankündigungen](platform-support-of-advertisement.md)

-   Aktivieren Sie die Selbstreparatur von Anwendungen, indem Sie Komponenten zur Laufzeit nach Bedarf neu installieren.

    Weitere Informationen finden Sie unter

    -   [Verwenden von Installerfunktionen](using-installer-functions.md)
    -   [Referenz zur Installerfunktion](installer-function-reference.md)
    -   [Resilienz](resiliency.md)
    -   [Quellresilienz](source-resiliency.md)
    -   [Suchen nach einem fehlerhaften Feature oder einer fehlerhaften Komponente](searching-for-a-broken-feature-or-component.md)
    -   [Ersetzen vorhandener Dateien](replacing-existing-files.md)

-   Zeigen Sie eine Benutzeroberfläche zum Sammeln von Benutzerinformationen und Konfigurationseinstellungen an, wenn eine Anwendung zum ersten Mal installiert oder ausgeführt wird. Die Benutzeroberfläche muss vom Setupautor des Windows Installer-Pakets hinzugefügt werden.

    Weitere Informationen finden Sie unter

    -   [Verwenden von Installerfunktionen](using-installer-functions.md)
    -   [Initialisieren einer Anwendung](initializing-an-application.md)
    -   [Dialogfeld "Erste Ausführen"](firstrun-dialog.md)
    -   [Informationen zum Benutzeroberfläche](about-the-user-interface.md)

-   Erstellen Sie Anwendungen, die ein Dereferenzierungsmodell verwenden, um auf Komponenten mit paralleler Funktionalität zu verweisen. Die qualifizierten Komponentenkategorien müssen vom Setupautor des Windows Installer-Pakets hinzugefügt werden.

    Weitere Informationen finden Sie unter

    -   [Qualifizierte Komponenten](qualified-components.md)
    -   [Verwenden von qualifizierten Komponenten](using-qualified-components.md)

-   Verwenden Sie private und nebeneinanderstehende Assemblys, um Anwendungen zu isolieren und DLL-Konflikte zu reduzieren.

    Weitere Informationen finden Sie unter

    -   [Assemblys](assemblies.md)
    -   [Von Windows Installer geschriebene Assemblyregistrierungsschlüssel](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Installieren von Win32-Assemblys für die seitenseitige Freigabe auf Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
    -   [Installieren von Win32-Assemblys für die private Verwendung einer Anwendung auf Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)
    -   [MsiAssembly-Tabelle](msiassembly-table.md)
    -   [MsiAssemblyName-Tabelle](msiassemblyname-table.md)
    -   [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)
    -   [**MsiWin32AssemblySupport-Eigenschaft**](msiwin32assemblysupport.md)
    -   [**MsiNetAssemblySupport-Eigenschaft**](msinetassemblysupport.md)
    -   [**Isolierte Komponenten**](isolated-components.md)

-   Bereiten Sie die Anwendung auf die Installation eigener umfassender Hauptupgrades vor.

    Weitere Informationen finden Sie unter

    -   [Patchen und Upgrades](patching-and-upgrades.md)
    -   [Hauptupgrades](major-upgrades.md)
    -   [**UpgradeCode-Eigenschaft**](upgradecode.md)
    -   [**Verwenden eines UpgradeCodes**](using-an-upgradecode.md)
    -   [Verhindern der Installation eines alten Pakets über eine neuere Version](preventing-an-old-package-from-installing-over-a-newer-version.md)

-   Bereiten Sie die Anwendung auf die Installation ihrer eigenen kleineren Upgrades, kleinen Updates oder Fehlerbehebungen vor.

    Weitere Informationen finden Sie unter

    -   [Patchen und Upgrades](patching-and-upgrades.md)
    -   [Kleine Updates](small-updates.md)
    -   [Kleinere Upgrades](minor-upgrades.md)

-   Organisieren Sie Anwendungsressourcen in Komponenten, die mit dem Windows Installer verwendet werden können.

    Weitere Informationen finden Sie unter

    -   [Windows Installer-Komponenten](windows-installer-components.md)
    -   [Arbeiten mit Features und Komponenten](working-with-features-and-components.md)
    -   [Verwenden transitiver Komponenten](using-transitive-components.md)
    -   [Was geschieht, wenn die Komponentenregeln fehlerhaft sind?](what-happens-if-the-component-rules-are-broken.md)
    -   [Organisieren von Anwendungen in Komponenten](organizing-applications-into-components.md)
    -   [Isolierte Komponenten](isolated-components.md)
    -   [Qualifizierte Komponenten](qualified-components.md)

## <a name="setup-authors"></a>Setupautoren

Setupautoren erstellen Windows Installer-Pakete (.msi-Dateien), die die Setuplogik und informationen enthalten, die zum Installieren einer Anwendung erforderlich sind. Sie verwenden in der Regel Erstellungstools wie [Orca.exe,](orca-exe.md) um die Windows Installer-Datenbank mit der Setuplogik und den Informationen aufzufüllen. Setupautoren gehen in der Regel wie folgt vor:

-   Ermitteln Sie die Funktionalität, die mit verschiedenen Versionen des Windows Installers verfügbar ist.

    Weitere Informationen finden Sie unter

    -   [Bestimmen der Windows Installer-Version](determining-the-windows-installer-version.md)
    -   [Veröffentlichte Versionen des Windows Installers](released-versions-of-windows-installer.md)
    -   [Neuerungen in Windows Installer](what-s-new-in-windows-installer.md)

-   Organisieren Sie Anwendungsressourcen in Windows Installer-Komponenten.

    Weitere Informationen finden Sie unter

    -   [Windows Installer-Komponenten](windows-installer-components.md)
    -   [Organisieren von Anwendungen in Komponenten](organizing-applications-into-components.md)
    -   [Ändern des Komponentencodes](changing-the-component-code.md)
    -   [Was geschieht, wenn die Komponentenregeln fehlerhaft sind?](what-happens-if-the-component-rules-are-broken.md)
    -   [Windows Beispiele für Installationsprogramme](windows-installer-examples.md)

-   Verwenden Sie Windows Installer-Paketerstellungstools von Drittanbietern oder SDK-Tools wie [Orca.exe,](orca-exe.md) um eine Installationsdatenbank aufzufüllen und ein Windows Installer-Paket zu erstellen.

    Weitere Informationen finden Sie unter

    -   [Windows Installationsentwicklungstools](windows-installer-development-tools.md)
    -   [Installationspaket, Informationen zur Installer-Datenbank](installation-package.md)
    -   [Windows Installer-Dateierweiterungen](windows-installer-file-extensions.md)
    -   [Datenbanktabellen](database-tables.md)
    -   [Paketcodes](package-codes.md)
    -   [Erstellen eines großen Pakets](authoring-a-large-package.md)
    -   [Windows Installationsprogramm unter 64-Bit-Betriebssystemen](windows-installer-on-64-bit-operating-systems.md)
    -   [Benennen von benutzerdefinierten Tabellen, Eigenschaften und Aktionen](naming-custom-tables-properties-and-actions.md)
    -   [OLE-Einschränkungen für Streams](ole-limitations-on-streams.md)
    -   [Spaltendefinitionsformat](column-definition-format.md)
    -   [Reduzieren der Größe einer .msi-Datei](reducing-the-size-of-an--msi-file.md)

-   Erstellen Sie die Windows Installer-Datenbank, um Dateien zu installieren.

    Weitere Informationen finden Sie unter

    -   [Gruppe "Kerntabellen"](core-tables-group.md)
    -   [Dateitabellengruppe](file-tables-group.md)
    -   [Dateitabelle](file-table.md)
    -   [Dateisuche](file-searching.md)
    -   [Dateikosten](file-costing.md)
    -   [Dateiinstallation](file-installation.md)
    -   [Begleitdateien](companion-files.md)
    -   [Regeln für die Dateiversionsierung](file-versioning-rules.md)
    -   [Standarddateiversionsierung](default-file-versioning.md)
    -   [Ersetzen vorhandener Dateien](replacing-existing-files.md)
    -   [Verwenden von Schränken und komprimierten Quellen](using-cabinets-and-compressed-sources.md)
    -   [Entfernen von hängenden Dateien](removing-stranded-files.md)
    -   [Installieren von permanenten Komponenten, Dateien, Schriftarten, Registrierungsschlüsseln](installing-permanent-components-files-fonts-registry-keys.md)
    -   [FileSFPCatalog-Tabelle](filesfpcatalog-table.md)
    -   [Suchen nach einer Datei und Erstellen einer Eigenschaft, die den Pfad der Datei enthält](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
    -   [Suchen nach einem Verzeichnis und einer Datei im Verzeichnis](searching-for-a-directory-and-a-file-in-the-directory.md)
    -   [Windows Beispiele für Installationsprogramme](windows-installer-examples.md)

-   Erstellen Sie eine Windows Installer-Datenbank, die eine Verzeichnisstruktur und Ordner installiert.

    Weitere Informationen finden Sie unter

    -   [Gruppe "Kerntabellen"](core-tables-group.md)
    -   [Dateitabellengruppe](file-tables-group.md)
    -   [Komponententabelle](component-table.md)
    -   [Verzeichnistabelle](directory-table.md)
    -   [Verwenden der Verzeichnistabelle](using-the-directory-table.md)
    -   [Verwenden einer Verzeichniseigenschaft in einem Pfad](using-a-directory-property-in-a-path.md)
    -   [Systemordnereigenschaften](property-reference.md)
    -   [CreateFolder-Tabelle](createfolder-table.md)
    -   [LockPermissions-Tabelle](lockpermissions-table.md)
    -   [MsiLockPermissionsEx-Tabelle](msilockpermissionsex-table.md)
    -   [Ändern des Zielspeicherorts für ein Verzeichnis](changing-the-target-location-for-a-directory.md)
    -   [Windows Beispiele für Installationsprogramme](windows-installer-examples.md)

-   Erstellen Sie eine Windows Installer-Datenbank, die Registrierungsschlüssel installiert.

    Weitere Informationen finden Sie unter

    -   [Gruppe "Kerntabellen"](core-tables-group.md)
    -   [Registrierungstabellengruppe](registry-tables-group.md)
    -   [Registrierungstabelle](registry-table.md)
    -   [Ändern der Registrierung](modifying-the-registry.md)
    -   [Hinzufügen oder Entfernen von Registrierungsschlüsseln bei der Installation oder Entfernung von Komponenten](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)
    -   [Hinzufügen und Entfernen einer Anwendung und Verlassen einer Ablaufverfolgung in der Registrierung](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [Installieren von permanenten Komponenten, Dateien, Schriftarten, Registrierungsschlüsseln](installing-permanent-components-files-fonts-registry-keys.md)
    -   [Suchen nach vorhandenen Anwendungen, Dateien, Registrierungseinträgen oder .ini Dateieinträgen](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
    -   [Suchen nach einem Registrierungseintrag und Erstellen einer Eigenschaft mit dem Wert der Registrierung](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)
    -   [Vom Windows Installer geschriebene Assemblyregistrierungsschlüssel](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Deinstallieren des Registrierungsschlüssels](uninstall-registry-key.md)
    -   [SelfReg-Tabelle](selfreg-table.md)
    -   [Angeben der Reihenfolge der Selbstregistrierung](specifying-the-order-of-self-registration.md)
    -   [Windows Beispiele für Installationsprogramme](windows-installer-examples.md)

-   Erstellen Sie eine Windows Installer-Datenbank, die Dienste installiert.

    Weitere Informationen finden Sie unter

    -   [ServiceInstall-Tabelle](serviceinstall-table.md)
    -   [ServiceControl-Tabelle](servicecontrol-table.md)
    -   [Komponententabelle](component-table.md)

-   Erstellen Sie eine Windows Installer-Datenbank, die isolierte Komponenten oder COM-Komponenten installiert.

    Weitere Informationen finden Sie unter

    -   [Registrierungstabellengruppe](registry-tables-group.md)
    -   [Klassentabelle](class-table.md)
    -   [Complus-Tabelle](complus-table.md)
    -   [Isolierte Komponenten](isolated-components.md)
    -   [Verwenden isolierter Komponenten](using-isolated-components.md)
    -   [Installation isolierter Komponenten](installation-of-isolated-components.md)
    -   [Neuinstallation isolierter Komponenten](reinstallation-of-isolated-components.md)
    -   [Entfernen isolierter Komponenten](removal-of-isolated-components.md)
    -   [Installieren einer COM-Komponente an einem privaten Speicherort](installing-a-com-component-to-a-private-location.md)
    -   [Erstellen einer COM-Komponente in einem vorhandenen Paket als privat](make-a-com-component-in-an-existing-package-private.md)
    -   [Installieren einer COM+-Anwendung mit dem Windows Installer](installing-a-com--application-with-the-windows-installer.md)
    -   [Installieren einer Nicht-COM-Komponente an einem privaten Speicherort](installing-a-non-com-component-to-a-private-location.md)
    -   [Erstellen einer Nicht-COM-Komponente in einem vorhandenen Paket als privat](make-a-non-com-component-in-an-existing-package-private.md)

-   Erstellen Sie eine Windows Installer-Datenbank, die Assemblys installiert.

    Weitere Informationen finden Sie unter

    -   [MsiAssembly-Tabelle](msiassembly-table.md)
    -   [MsiAssemblyName-Tabelle](msiassemblyname-table.md)
    -   [Assemblys](assemblies.md)
    -   [Vom Windows Installer geschriebene Assemblyregistrierungsschlüssel](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Installation von Win32-Assemblys](installation-of-win32-assemblies.md)

-   Erstellen Sie eine Windows Installer-Datenbank, die ODBC-Treiber und -Translator installiert.

    Weitere Informationen finden Sie unter

    -   [ODBCAttribute-Tabelle](odbcattribute-table.md)
    -   [ODBCDriver-Tabelle](odbcdriver-table.md)
    -   [ODBCTranslator-Tabelle](odbctranslator-table.md)
    -   [ODBCDataSource-Tabelle](odbcdatasource-table.md)
    -   [ODBCSourceAttribute-Tabelle](odbcsourceattribute-table.md)

-   Erstellen Sie eine Windows Installer-Datenbank, die MIME installiert.

    Weitere Informationen finden Sie unter

    -   [MIME-Tabelle](mime-table.md)
    -   [Erweiterungstabelle](extension-table.md)
    -   [Ändern der Registrierung](modifying-the-registry.md)

-   Erstellen Sie eine Windows Installer-Datenbank, die Umgebungsvariablen installiert.

    Weitere Informationen finden Sie unter

    -   [Umgebungstabelle](environment-table.md)

-   Erstellen Sie eine Windows Installer-Datenbank, die Verknüpfungen installiert.

    Weitere Informationen finden Sie unter

    -   [Verknüpfungstabelle](shortcut-table.md)
    -   [MsiShortcutProperty-Tabelle](msishortcutproperty-table.md)
    -   [Bearbeiten von Installerverknüpfungen](editing-installer-shortcuts.md)
    -   [Windows Beispiele für Installationsprogramme](windows-installer-examples.md)

-   Erstellen Sie eine Windows Installer-Datenbank, die mehrere Instanzen von Anwendungen installiert.

    Weitere Informationen finden Sie unter

    -   [Installieren mehrerer Instanzen von Produkten und Patches](installing-multiple-instances-of-products-and-patches.md)
    -   [Erstellen mehrerer Instanzen mit Instanztransformationen](authoring-multiple-instances-with-instance-transforms.md)
    -   [Installieren mehrerer Instanzen mit Instanztransformationen](installing-multiple-instances-with-instance-transforms.md)

-   Geben Sie standardfunktionsauswahlzustände und -optionen an.

    Weitere Informationen finden Sie unter

    -   [Gruppe "Kerntabellen"](core-tables-group.md)
    -   [Komponententabelle](component-table.md)
    -   [Featuretabelle](feature-table.md)
    -   [Tabelle "FeatureComponents"](featurecomponents-table.md)
    -   [Steuern von Funktionsauswahlzuständen](controlling-feature-selection-states.md)
    -   [Eigenschaften der Featureinstallationsoptionen](property-reference.md)

-   Geben Sie Bedingungen an, die erfüllt sein müssen, um eine Anwendung oder ausgewählte Komponenten zu installieren.

    Weitere Informationen finden Sie unter

    -   [Bedingungstabelle](condition-table.md)
    -   [LaunchCondition-Tabelle](launchcondition-table.md)
    -   [Komponententabelle](component-table.md)
    -   [Verwenden von Eigenschaften in bedingten Anweisungen](using-properties-in-conditional-statements.md)
    -   [Syntax der bedingten Anweisung](conditional-statement-syntax.md)
    -   [Durchführen von Aktionen, die während des Entfernens ausgeführt werden sollen](conditioning-actions-to-run-during-removal.md)
    -   [Beispiele für die Syntax der bedingten Anweisung](examples-of-conditional-statement-syntax.md)

-   Erstellen Sie die Sequenz der Aktionen, die zum Installieren der Anwendung verwendet werden.

    Weitere Informationen finden Sie unter

    -   [Verwenden einer Sequenztabelle](using-a-sequence-table.md)
    -   [Gruppe "Tabellen für Installationsprozedur"](installation-procedure-tables-group.md)
    -   [Detailliertes Beispiel für die Sequenztabelle](sequence-table-detailed-example.md)
    -   [Aktionen mit Sequenzeinschränkungen](actions-with-sequencing-restrictions.md)
    -   [Aktionen ohne Sequenzierungseinschränkungen](actions-without-sequencing-restrictions.md)
    -   [Verwenden von Eigenschaften in bedingten Anweisungen](using-properties-in-conditional-statements.md)
    -   [Syntax der bedingten Anweisung](conditional-statement-syntax.md)
    -   [Beispiele für die Syntax der bedingten Anweisung](examples-of-conditional-statement-syntax.md)
    -   [Durchführen von Aktionen, die während des Entfernens ausgeführt werden sollen](conditioning-actions-to-run-during-removal.md)
    -   [Standardaktionen](standard-actions.md)
    -   [Windows Beispiele für Installationsprogramme](windows-installer-examples.md)

-   Bereiten Sie das Installationspaket der Anwendung für zukünftige Upgrades der Anwendung durch den Windows Installer-Dienst vor.

    Weitere Informationen finden Sie unter

    -   [Patchen und Upgrades](patching-and-upgrades.md)
    -   [Vorbereiten einer Anwendung für zukünftige größere Upgrades](preparing-an-application-for-future-major-upgrades.md)
    -   [Verwenden eines UpgradeCodes](using-an-upgradecode.md)
    -   [Upgradetabelle](upgrade-table.md)
    -   [**UpgradeCode-Eigenschaft**](upgradecode.md)
    -   [Verhindern der Installation eines alten Pakets über eine neuere Version](preventing-an-old-package-from-installing-over-a-newer-version.md)
    -   [Ändern des Produktcodes](changing-the-product-code.md)
    -   [Aktualisieren von Assemblys](updating-assemblies.md)
    -   [Windows Beispiele für Installationsprogramme](windows-installer-examples.md)

-   Problembehandlung bei Windows Installer-Paketen in der Entwicklung.

    Weitere Informationen finden Sie unter

    -   [Paketvalidierung](package-validation.md)
    -   [Interne Konsistenzauswertungen – ICEs](internal-consistency-evaluators-ices.md)
    -   [Windows Installerprotokollierung](windows-installer-logging.md)
    -   [Überprüfen der Installation von Features, Komponenten und Dateien](checking-the-installation-of-features-components-files.md)
    -   [Erstellen eines großen Pakets](authoring-a-large-package.md)
    -   [Wilogutl.exe](wilogutl-exe.md)
    -   [Windows Installationsentwicklungstools](windows-installer-development-tools.md)
    -   [Überprüfen von Mergemodulen](validating-merge-modules.md)
    -   [Überprüfen einer Installationsdatenbank](validating-an-installation-database.md)
    -   [Überprüfen eines Installationsupgrades](validating-an-installation-upgrade.md)
    -   [Suchen nach einem fehlerhaften Feature oder einer fehlerhaften Komponente](searching-for-a-broken-feature-or-component.md)
    -   [Windows Fehlermeldungen des Installationsprogramms](windows-installer-error-messages.md)
    -   [Protokollierung von Neustartanforderungen](logging-of-reboot-requests.md)

-   Stellen Sie sicher, dass die Anwendung sicher eingerichtet und installiert wird.

    Weitere Informationen finden Sie unter

    -   [Richtlinien für die Erstellung sicherer Installationen](guidelines-for-authoring-secure-installations.md)
    -   [Richtlinien zum Sichern benutzerdefinierter Aktionen](guidelines-for-securing-custom-actions.md)
    -   [Benutzerdefinierte Aktionssicherheit](custom-action-security.md)
    -   [Richtlinien zum Sichern von Paketen auf gesperrten Computern](guidelines-for-securing-packages-on-locked-down-computers.md)
    -   [Erstellen einer vollständig überprüften signierten Installation mithilfe von Automation](authoring-a-fully-verified-signed-installation-using-automation.md)
    -   [URL-basiertes Windows Installer-Installationsbeispiel](a-url-based-windows-installer-installation-example.md)
    -   [Erstellen der Benutzeroberfläche für die Kennworteingabe](authoring-the-user-interface-for-password-input.md)
    -   [Installationsprogramm für digitale Signaturen und Windows](digital-signatures-and-windows-installer.md)
    -   [Verwenden Windows Installers mit UAC](using-windows-installer-with-uac.md)
    -   [Patchen der Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md)
    -   [Msicert.exe](msicert-exe.md)
    -   [**AdminUser-Eigenschaft**](adminuser.md)
    -   [**Privilegierte Eigenschaft**](privileged.md)
    -   [**SecureCustomProperties-Eigenschaft**](securecustomproperties.md)

-   Erstellen Sie eine Benutzeroberfläche, um Optionen zum Konfigurieren der Installation und Abrufen von Informationen über den ausstehenden Installationsvorgang vom Benutzer anzuzeigen.

    Weitere Informationen finden Sie unter

    -   [Informationen zum Benutzeroberfläche](about-the-user-interface.md)
    -   [Hinzufügen von Steuerelementen und Text](adding-controls-and-text.md)
    -   [Erstellen eines ProgressBar-Steuerelements](authoring-a-progressbar-control.md)
    -   [Erstellen von Datenträgereingabeaufforderungsmeldungen](authoring-disk-prompt-messages.md)
    -   [Erstellen einer bedingten "Please Wait . . "." Meldungsfeld](authoring-a-conditional-please-wait-------message-box.md)
    -   [Vorschau der Benutzeroberfläche](previewing-the-user-interface.md)
    -   [Hinzufügen von in einer Eigenschaft gespeicherten Text](adding-text-stored-in-a-property.md)
    -   [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

-   Erstellen Sie eine externe Benutzeroberfläche, um eine benutzerdefinierte Benutzeroberfläche zum Konfigurieren der Installation und Abrufen von Informationen über den ausstehenden Installationsvorgang vom Benutzer zu präsentieren.

    Weitere Informationen finden Sie unter

    -   [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
    -   [Überwachen einer Installation mit msiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md)
    -   [Analysieren von Windows Installer-Meldungen](parsing-windows-installer-messages.md)
    -   [Zurückgeben von Werten aus einem externen Benutzeroberfläche Handler](returning-values-from-an-external-user-interface-handler.md)
    -   [\_INSTALLUI-HANDLER](/windows/desktop/api/Msi/nc-msi-installui_handlera)
    -   [Verarbeiten von Statusmeldungen mithilfe von MsiSetExternalUI](handling-progress-messages-using-msisetexternalui.md)
    -   [Überwachen einer Installation mithilfe von MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md)

-   Legen Sie informationen für die Anwendung unter **Software (Add/Remove Programs,** ARP.) fest.

    Weitere Informationen finden Sie unter

    -   [Konfigurieren von "Programme hinzufügen/entfernen" mit Windows Installer](configuring-add-remove-programs-with-windows-installer.md)
    -   [Hinzufügen und Entfernen einer Anwendung und Verlassen einer Ablaufverfolgung in der Registrierung](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [Deinstallieren des Registrierungsschlüssels](uninstall-registry-key.md)

-   Schreiben Sie benutzerdefinierte Aktionen, um Setuplogik zu verarbeiten, die nicht nativ von Windows Installer unterstützt wird.

    Weitere Informationen finden Sie unter

    -   [Benutzerdefinierte Aktionen](custom-actions.md)
    -   [Zusammenfassungsliste aller benutzerdefinierten Aktionstypen](summary-list-of-all-custom-action-types.md)
    -   [Richtlinien zum Sichern benutzerdefinierter Aktionen](guidelines-for-securing-custom-actions.md)
    -   [Referenz zu benutzerdefinierten Aktionen](custom-action-reference.md)
    -   [Verwenden einer benutzerdefinierten Aktion zum Erstellen von Benutzerkonten auf einem lokalen Computer](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [Verwenden einer benutzerdefinierten Aktion zum Starten einer installierten Datei am Ende der Installation](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
    -   [Zugreifen auf eine Datenbank oder Sitzung über eine benutzerdefinierte Aktion](accessing-a-database-or-session-from-inside-a-custom-action.md)
    -   [Zugreifen auf die aktuelle Installersitzung aus einer benutzerdefinierten Aktion](accessing-the-current-installer-session-from-inside-a-custom-action.md)
    -   [Ändern des Systemstatus mithilfe einer benutzerdefinierten Aktion](changing-the-system-state-using-a-custom-action.md)

-   Starten Sie den Windows Installer auf den Computer eines Benutzers.

    Weitere Informationen finden Sie unter

    -   [Bootstrapping](bootstrapping.md)
    -   [Instmsi.exe](instmsi-exe.md)
    -   [Internetdownload-Bootstrapping](internet-download-bootstrapping.md)
    -   [Msistuff.exe](msistuff-exe.md)
    -   [URL-basiertes Windows Installer-Installationsbeispiel](a-url-based-windows-installer-installation-example.md)
    -   [Konfigurieren der Setup.exe-Ressourcen](configuring-the-setup-exe-resources.md)
    -   [Herunterladen einer Installation aus dem Internet](downloading-an-installation-from-the-internet.md)

-   Befolgen Sie beim Schreiben Windows Installer-Pakete Active Accessibility Richtlinien.

    Weitere Informationen finden Sie unter

    -   [Bedienungshilfen](accessibility.md)

-   Bereiten Sie sich auf die Internationalisierung eines Anwendungssetups vor.

    Weitere Informationen finden Sie unter

    -   [Vorbereiten eines Windows Installer-Pakets für die Lokalisierung](preparing-a-windows-installer-package-for-localization.md)von ,
    -   [Lokalisieren eines Windows Installer-Pakets](localizing-a-windows-installer-package.md)
    -   [Codepagebehandlung (Windows Installer)](code-page-handling-windows-installer-.md)
    -   [Hinzufügen lokalisierter Ressourcen](adding-localized-resources.md)
    -   [Ein Lokalisierungsbeispiel](a-localization-example.md)
    -   [Lokalisieren der Fehler- und ActionText-Tabellen](localizing-the-error-and-actiontext-tables.md)
    -   [Lokalisieren von Datenbankspalten](localizing-database-columns.md)
    -   [Erstellen einer Datenbank mit einer neutralen Codepage](creating-a-database-with-a-neutral-code-page.md)
    -   [Codepagebehandlung von importierten und exportierten Tabellen](code-page-handling-of-imported-and-exported-tables.md)
    -   [Lokalisieren der von Dialogen angezeigten Sprache](localizing-the-language-displayed-by-dialogs.md)
    -   [Importieren lokalisierter Fehler- und ActionText-Tabellen](importing-localized-error-and-actiontext-tables.md)
    -   [Aktualisieren der Eigenschaften "ProductLanguage" und "ProductCode"](updating-productlanguage-and-productcode-properties.md)
    -   [Aktualisieren eines Zusammenfassungsinformationsdatenstroms](updating-a-summary-information-stream.md)
    -   [Qualifizierte Komponenten](qualified-components.md)
    -   [UIText-Tabelle](uitext-table.md)
    -   [Verwalten von Sprache und Codepage](manage-language-and-codepage.md)
    -   [Überprüfen der Codepage der Installationsdatenbank](checking-the-installation-database-code-page.md)

-   Erstellen Sie Windows Installer-Pakete für 32-Bit- und 64-Bit-Plattformen.

    Weitere Informationen finden Sie unter

    -   [Windows Installationsprogramm unter 64-Bit-Betriebssystemen](windows-installer-on-64-bit-operating-systems.md)
    -   [Benutzerdefinierte 64-Bit-Aktionen](64-bit-custom-actions.md)
    -   [Verwenden von benutzerdefinierten 64-Bit-Aktionen](using-64-bit-custom-actions.md)
    -   [Verwenden von 64-Bit-Mergemodulen](using-64-bit-merge-modules.md)

-   Verteilen Sie freigegebene Windows Installer-Komponenten neu, und richten Sie logik als Mergemodule ein.

    Weitere Informationen finden Sie unter

    -   [Zusammenführen von Modulen](merge-modules.md)
    -   [Erstellen einer Sprachtransformation für ein Modul zum Zusammenführen mehrerer Sprachen](authoring-a-language-transform-for-a-multiple-language-merge-module.md)
    -   [Anwenden eines konfigurierbaren Mergemoduls mit Anpassungen](applying-a-configurable-merge-module-with-customizations.md)

-   Planen oder unterdrücken Sie Neustarts während einer installation Windows Installers.

    Weitere Informationen finden Sie unter

    -   [Systemneustarts](system-reboots.md)
    -   [Protokollierung von Neustartanforderungen](logging-of-reboot-requests.md)

-   Erstellen Sie Updates oder Fehlerbehebungen für eine vorhandene Anwendung, indem Sie einen Patch erstellen.

    Weitere Informationen finden Sie unter

    -   [Erstellen eines kleinen Updatepatches](creating-a-small-update-patch.md)
    -   [Beispiel für kleine Updatepatches](a-small-update-patching-example.md)

-   Erstellen Sie ein Dual-Purpose-Paket, das eine Anwendung entweder nur für den aktuellen Benutzer oder für alle Benutzer des Computers installieren kann.

    Weitere Informationen finden Sie unter

    -   [Installationskontext](installation-context.md)
    -   [Erstellen einzelner Pakete](single-package-authoring.md)
    -   [Beispiel für die Erstellung einzelner Pakete](single-package-authoring-example.md)

-   Passen Sie Dienste auf dem Computer mithilfe des Windows Installers an.

    Weitere Informationen finden Sie unter

    -   [Verwenden der Dienstkonfiguration](using-services-configuration.md)

-   Sichern Sie Ressourcen auf dem Computer mithilfe des Windows Installers.

    Weitere Informationen finden Sie unter

    -   [Richtlinien für die Erstellung sicherer Installationen](guidelines-for-authoring-secure-installations.md)
    -   [Sichern von Ressourcen](securing-resources-.md)

-   Aufzählen aller auf dem Computer installierten Komponenten und Abrufen des Schlüsselpfads für die Komponente.

    Weitere Informationen finden Sie unter

    -   [Aufzählen von Komponenten](enumerating-components-.md)

-   Installieren Sie mehrere Pakete mithilfe der [*Transaktionsverarbeitung.*](t-gly.md)

    Weitere Informationen finden Sie unter

    -   [Installationen mit mehreren Paketen](multiple-package-installations.md)

-   Betten Sie eine benutzerdefinierte Benutzeroberfläche in das paket Windows Installer ein.

    Weitere Informationen finden Sie unter

    -   [Verwenden der Benutzeroberfläche](using-the-user-interface.md)
    -   [Verwenden einer eingebetteten Benutzeroberfläche](using-an-embedded-ui.md)

## <a name="it-professionals"></a>IT-Fachleute

IT-Experten und Administratoren passen vorhandene Windows Installer-Pakete an und stellen sie bereit. Diese Benutzer packen Setups für vorhandene Anwendungen in Windows Installer-Installationspakete um und installieren und verwalten Administrative Images von Windows Installer-Installationen in Netzwerken.

-   Anpassen von Anwendungen und Setup durch Generieren und Anwenden Windows Installer-Transformationen

    Weitere Informationen finden Sie unter

    -   [Anpassung](customization.md)
    -   [Datenbanktransformationen](database-transforms.md)
    -   [Beispiel für eine Anpassungstransformation](a-customization-transform-example.md)
    -   [Zusammenführungen und Transformationen](merges-and-transforms.md)
    -   [Verwenden von Transformationen zum Hinzufügen von Ressourcen](using-transforms-to-add-resources.md)
    -   [Generieren einer Transformation](generate-a-transform.md)
    -   [Befehlszeilenoptionen](command-line-options.md)
    -   [Msitran.exe](msitran-exe.md)
    -   [Anwenden einer Transformation](apply-a-transform.md)
    -   [Anzeigen einer Transformation](view-a-transform.md)
    -   [Anzeigen der Unterschiede zwischen zwei Datenbanken](view-differences-between-two-databases.md)
    -   [Patchen von benutzerdefinierten Anwendungen](patching-customized-applications.md)

-   Stellen Sie ein Windows Installer-Installationspaket, -Update oder -Patch zur Bereitstellung.

    Weitere Informationen finden Sie unter

    -   [Installieren einer Anwendung](installing-an-application.md)
    -   [Patchen und Upgrades](patching-and-upgrades.md)
    -   [Transformationen](transforms.md)
    -   [Installieren eines Pakets mit erhöhten Rechten für einen Nicht-Administrator](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Anwenden wichtiger Upgrades durch Patchen der lokalen Installation des Produkts](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)
    -   [Anwenden wichtiger Upgrades durch Installieren des Produkts](applying-major-upgrades-by-installing-the-product.md)
    -   [Anwenden kleiner Updates durch Patchen der lokalen Installation des Produkts](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [Anwenden kleiner Updates durch Neuinstallation des Produkts](applying-small-updates-by-reinstalling-the-product.md)
    -   [Anwenden kleiner Updates durch Patchen eines administrativen Images](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Patchen von Erstinstallationen](patching-initial-installations.md)
    -   [Befehlszeilenoptionen](command-line-options.md)

-   Problembehandlung Windows Installer-Paketen.

    Weitere Informationen finden Sie unter

    -   [Windows Protokollierung des Installationsprogramms](windows-installer-logging.md)
    -   [Überprüfen der Installation von Features, Komponenten, Dateien](checking-the-installation-of-features-components-files.md)
    -   [Wilogutl.exe](wilogutl-exe.md)
    -   [Suchen nach einem fehlerhaften Feature oder einer fehlerhaften Komponente](searching-for-a-broken-feature-or-component.md)
    -   [Windows Fehlermeldungen des Installationsprogramms](windows-installer-error-messages.md)
    -   [Msicert.exe](msicert-exe.md)

-   Verwenden Sie Skripts, um Windows Installer-Pakete nach Informationen zu einem Produkt zu abfragen und die Installation zu ändern.

    Weitere Informationen finden Sie unter

    -   [Automatisierungsschnittstelle](automation-interface.md)
    -   [Windows Skriptbeispiele für Installer](windows-installer-scripting-examples.md)
    -   [Verwenden Windows Installers mit WMI](using-windows-installer-with-wmi.md)

-   Erstellen und Verwalten von Administratorinstallationen.

    Weitere Informationen finden Sie unter

    -   [Administratorinstallation](administrative-installation.md)
    -   [Befehlszeilenoptionen](command-line-options.md)
    -   [**AdminProperties-Eigenschaft**](adminproperties.md)
    -   [Anwenden kleiner Updates durch Patchen eines administrativen Images](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Anwenden eines Patchpakets auf eine Administratorinstallation](applying-a-patch-package-to-an-administrative-installation.md)
    -   [Reihenfolge der Aktionsausführung](action-execution-order.md)
    -   [**IsAdminPackage-Eigenschaft**](isadminpackage.md)
    -   [Rangfolge der Eigenschaften](order-of-property-precedence.md)
    -   [**AdminProperties-Eigenschaft**](adminproperties.md)

-   Stellen Sie eine Anwendung nur für alle Benutzer eines Computers oder für einen angegebenen Benutzer zur Verfügung.

    Weitere Informationen finden Sie unter

    -   [Installationskontext](installation-context.md)
    -   [**ALLUSERS-Eigenschaft**](allusers.md)

-   Interpretieren von Paketen, Installieren von Produkten und Konfigurieren von Featureoptionen über eine Befehlszeile

    Weitere Informationen finden Sie unter

    -   [Befehlszeilenoptionen](command-line-options.md)
    -   [Festlegen von öffentlichen Eigenschaftswerten in der Befehlszeile](setting-public-property-values-on-the-command-line.md)
    -   [Abrufen und Festlegen von Eigenschaften](getting-and-setting-properties.md)
    -   [Erneutes Installieren eines Features oder einer Anwendung](reinstalling-a-feature-or-application.md)
    -   [Anwenden kleiner Updates durch Patchen der lokalen Installation des Produkts](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [Anwenden kleiner Updates durch Neuinstallation des Produkts](applying-small-updates-by-reinstalling-the-product.md)
    -   [Ändern des Zielspeicherorts für ein Verzeichnis](changing-the-target-location-for-a-directory.md)
    -   [Anwenden kleiner Updates durch Patchen eines administrativen Images](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Anwenden wichtiger Upgrades durch Installieren des Produkts](applying-major-upgrades-by-installing-the-product.md)
    -   [Konfigurationseigenschaften](property-reference.md)
    -   [Eigenschaften der Featureinstallationsoptionen](property-reference.md)

-   Arbeiten Sie mit Richtlinien, um Zugriffsrechte und Berechtigungen zu verwalten.

    Weitere Informationen finden Sie unter

    -   [Computerrichtlinien](machine-policies.md),
    -   [Benutzerrichtlinien,](user-policies.md)
    -   [Installieren eines Pakets mit erhöhten Rechten für einen Nicht-Administrator](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Anwerten Per-User Anwendung, die mit erhöhten Rechten installiert werden soll](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [Verwenden einer benutzerdefinierten Aktion zum Erstellen von Benutzerkonten auf einem lokalen Computer](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [**AdminUser-Eigenschaft**](adminuser.md)
    -   [**Privileged Property**](privileged.md)
    -   [**EnableUserControl-Eigenschaft**](enableusercontrol.md)
    -   [**UserSID-Eigenschaft**](usersid.md)
    -   [**SecureCustomProperties-Eigenschaft**](securecustomproperties.md)

-   Installieren Sie mehrere Pakete mithilfe [*der Transaktionsverarbeitung.*](t-gly.md)

    Weitere Informationen finden Sie unter

    -   [Installationen mit mehreren Paketen](multiple-package-installations.md)

-   Betten Sie eine benutzerdefinierte Benutzeroberfläche in ein Windows Installer-Paket ein.

    Weitere Informationen finden Sie unter

    -   [Verwenden der Benutzeroberfläche](using-the-user-interface.md)
    -   [Verwenden einer eingebetteten Benutzeroberfläche](using-an-embedded-ui.md)

## <a name="infrastructure-developers"></a>Infrastrukturentwickler

Infrastrukturentwickler können einheitliche Plattformen für die Bereitstellung und Verwaltung von Software erstellen, die den Windows Installer-Dienst verwendet. Sie können die Programmierschnittstelle Windows Installer verwenden, um Anwendungen, Patches und Quellen auf einem System abfragen, verwalten und verteilen zu können.

-   Suchen, Inventarisieren und Abfragen des Zustands, der Informationen und der Clients von Komponenten.

    Weitere Informationen finden Sie unter

    -   [Komponentenspezifische Funktionen](installer-function-reference.md)
    -   [Systemstatusfunktionen](installer-function-reference.md)
    -   [Installer-Objekt](installer-object.md)
    -   [Product-Objekt](product-object.md)
    -   [Patch-Objekt](patch-object.md)

-   Inventarisierung und Abfrage von Informationen und des Status von Produkten und Features.

    Weitere Informationen finden Sie unter

    -   [Inventarisierung von Produkten und Patches](inventory-products-and-patches-.md)
    -   [Systemstatusfunktionen](installer-function-reference.md)
    -   [Produktabfragefunktionen](installer-function-reference.md)
    -   [Installer-Objekt](installer-object.md)
    -   [Product-Objekt](product-object.md)
    -   [Patch-Objekt](patch-object.md)

-   Verbessern Sie die Quellresilienz, indem Sie den Windows Installer verwenden, um die Quellliste von Anwendungen, Upgrades und Patches zu inventar, abfragen und zu ändern.

    Weitere Informationen finden Sie unter

    -   [**SOURCELIST-Eigenschaft**](sourcelist.md)
    -   [**Quellresilienz**](source-resiliency.md)
    -   [Installations- und Konfigurationsfunktionen](installer-function-reference.md)
    -   [Installer-Objekt](installer-object.md)
    -   [Product-Objekt](product-object.md)
    -   [Patch-Objekt](patch-object.md)

-   Verbessern Sie die Resilienz der Quelle, indem Sie den Windows Installer verwenden, um Medienquellen zu inventarisieren, abzufragen und zu ändern.

    Weitere Informationen finden Sie unter

    -   [**SOURCELIST-Eigenschaft**](sourcelist.md)
    -   [Quellresilienz](source-resiliency.md)
    -   [Installations- und Konfigurationsfunktionen](installer-function-reference.md)
    -   [Product-Objekt](product-object.md)
    -   [Patch-Objekt](patch-object.md)

-   Inventarisieren und Abfragen von Informationen und des Status von Patches.

    Weitere Informationen finden Sie unter

    -   [Inventurprodukte und Patches](inventory-products-and-patches-.md)
    -   [Referenz zur Installerfunktion](installer-function-reference.md)
    -   [Patch-Objekt](patch-object.md)

-   Arbeiten Sie mit Richtlinien, um Zugriffsrechte und Berechtigungen zu verwalten.

    Weitere Informationen finden Sie unter

    -   [Computerrichtlinien](machine-policies.md)
    -   [Benutzerrichtlinien](user-policies.md)
    -   [Installieren eines Pakets mit erhöhten Rechten für einen Nichtadministrator](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Ananzeigen einer zu installierenden Per-User-Anwendung mit erhöhten Rechten](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [Verwenden einer benutzerdefinierten Aktion zum Erstellen von Benutzerkonten auf einem lokalen Computer](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [**AdminUser-Eigenschaft**](adminuser.md)
    -   [**Privileged Property**](privileged.md)
    -   [**EnableUserControl-Eigenschaft**](enableusercontrol.md)
    -   [**UserSID-Eigenschaft**](usersid.md)
    -   [**SecureCustomProperties-Eigenschaft**](securecustomproperties.md)

 

 



