---
description: 'In diesem Abschnitt wird eine Liste mit Tipps aufgelistet, die mit der Haupt Windows Installer SDK-Dokumentation verknüpft sind, um Anwendungsentwicklern, Setup Autoren, IT-Experten und Infrastruktur Entwicklern zu helfen, bewährte Methoden für die Verwendung der Windows Installer zu ermitteln:'
ms.assetid: ff48d995-fe6f-4d1b-898d-67574ed3c5b7
title: Bewährte Methoden für Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ffaf6aae83afbe510f2b1eefc447e34754296ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042531"
---
# <a name="windows-installer-best-practices"></a>Bewährte Methoden für Windows Installer

In diesem Abschnitt wird eine Liste mit Tipps aufgelistet, die mit der Haupt Windows Installer SDK-Dokumentation verknüpft sind, um Anwendungsentwicklern, Setup Autoren, IT-Experten und Infrastruktur Entwicklern zu helfen, bewährte Methoden für die Verwendung der Windows Installer zu ermitteln:

-   [Aktualisieren Sie die Windows Installer Version.](#update-the-windows-installer-version)
-   [Erfüllen Sie die Zertifizierungsanforderungen für Windows-Logo.](#meet-the-windows-logo-certification-requirements)
-   [Bereiten Sie das Paket für die Lokalisierung vor.](#prepare-the-package-for-localization)
-   [Aktualisieren Sie Ihre Windows Installer Entwicklungs Tools und-Dokumentation.](#update-your-windows-installer-development-tools-and-documentation)
-   [Wenn Sie sich entschließen, eine Legacy-Setup Anwendung neu zu verpacken, befolgen Sie die bewährten Vorgehensweisen zum erneuten verpacken.](#if-you-decide-to-repackage-a-legacy-setup-application-follow-good-repackaging-practices)
-   [Versuchen Sie nicht, geschützte Ressourcen zu ersetzen.](#do-not-try-to-replace-protected-resources)
-   [Verlassen Sie sich nicht auf nicht kritische Ressourcen.](#do-not-depend-upon-non-critical-resources)
-   [Verwenden Sie die-API, um Windows Installer Konfigurationsinformationen abzurufen.](#use-the-api-to-retrieve-windows-installer-configuration-information)
-   [Organisieren Sie die Installation Ihrer Anwendung um Komponenten.](#organize-the-installation-of-your-application-around-components)
-   [Reduzieren Sie die Größe großer Windows Installer Pakete.](#reduce-the-size-of-large-windows-installer-packages)
-   [Wenn Sie benutzerdefinierte Aktionen verwenden, befolgen Sie bewährte Methoden für benutzerdefinierte Aktionen.](#if-you-use-custom-actions-follow-good-custom-action-practices)
-   [Befolgen Sie bei Verwendung von Assemblys gute assemblypraktiken.](#if-you-use-assemblies-follow-good-assembly-practices)
-   [Senden Sie keine gleichzeitigen Installationen.](#do-not-ship-concurrent-installations)
-   [Halten Sie die Paketnamen und Paket Codes konsistent.](#keep-package-names-and-package-codes-consistent)
-   [Verwenden Sie die Tabellen "selfreg" und "TypeLib" nicht.](#do-not-use-the-selfreg-and-typelib-tables)
-   [Stellen Sie die Option zur Installation ohne Benutzeroberfläche bereit.](#provide-the-option-to-install-without-a-user-interface)
-   [Vermeiden Sie die Verwendung der alwaysinstallerhöhten-Richtlinie.](#avoid-using-the-alwaysinstallelevated-policy)
-   [Aktivieren Sie die disablemedia-Richtlinie, um die nicht autorisierte Installation einzuschränken](#enable-the-disablemedia-policy-to-limit-unauthorized-installation)
-   [Sorgen Sie dafür, dass die ursprünglichen Paket Quelldateien sicher und für Benutzer verfügbar sind.](#keep-the-original-package-source-files-secure-and-available-to-users)
-   [Aktivieren Sie die ausführliche Protokollierung auf dem Computer des Benutzers bei der Problembehandlung.](#enable-verbose-logging-on-users-computer-when-troubleshooting-deployment)
-   [Bei der Installation bleibt der Computer des Benutzers in einem sauberen Zustand.](#uninstallation-leaves-the-users-computer-in-a-clean-state)
-   [Test Pakete für die Bereitstellung pro Benutzer und pro Computerinstallation.](#test-packages-for-both-per-user-and-per-machine-installation-deployment)
-   [Planen und testen Sie eine Wartungsstrategie, bevor Sie die Anwendung versenden.](#plan-and-test-a-servicing-strategy-before-shipping-the-application)
-   [Reduzieren Sie die Abhängigkeit von Updates auf den ursprünglichen Quellen.](#reduce-the-dependency-of-updates-upon-the-original-sources)
-   [Nicht servierbar-Mergemodule verteilen.](#do-not-distribute-unserviceable-merge-modules)
-   [Vermeiden Sie das Patchen administrativer Installationen.](#avoid-patching-administrative-installations)
-   [Registrieren von Updates, die mit erhöhten Rechten ausgeführt werden.](#register-updates-to-run-with-elevated-privilege)
-   [Verwenden Sie die msipatchsequence-Tabelle, um Patches zu sequenzieren.](#use-the-msipatchsequence-table-to-sequence-patches)
-   [Testen Sie das Installationspaket gründlich.](#test-the-installation-package-thoroughly)
-   [Beheben Sie alle Validierungs Fehler, bevor Sie ein neues oder überarbeitetes Installationspaket bereitstellen.](#fix-all-validation-errors-before-deploying-a-new-or-revised-installation-package)
-   [Erstellen Sie eine sichere Installation.](#author-a-secure-installation)
-   [Verwenden von "pmsihandle" anstelle von "handle"](#use-pmsihandle-instead-of-handle)

## <a name="update-the-windows-installer-version"></a>Aktualisieren Sie die Windows Installer Version.

-   Verwenden Sie Windows Installer 5,0 unter Windows Server 2008 R2 und Windows 7. Dies ist die Windows Installer Version, die mit dem Betriebssystem bereitgestellt wird.
-   Verwenden Sie Windows Installer 4,5 unter Windows Server 2008, Windows Server 2003 mit Service Pack 1 (SP1), Windows Vista mit Service Pack 1 (SP1) oder Windows XP mit Service Pack 2 (SP2). Informationen zum Abrufen der neuesten Windows Installer Version finden Sie unter [Windows Installer Redistributables](windows-installer-redistributables.md).
-   Verwenden Sie Windows Installer 3,1 unter Windows 2000 mit Service Pack 3 (SP3). Windows Installer Version 3,1 verfügt über Features, die eine bessere Anwendungs Wartung und das [Patchen](patching.md)ermöglichen.
-   Viele wichtige Features wurden mit Version 3,0 eingeführt und sind im Abschnitt [nicht unterstützt in Windows Installer Version 2,0](not-supported-in-windows-installer-version-2-0.md)aufgeführt. Installationspakete und Updates, die für Windows Installer 2,0 erstellt wurden, können mit Windows Installer 3,0 und höher installiert werden. Patchpakete, die die neuen, von Windows Installer 3,0 verwendeten Tabellen enthalten, können weiterhin mit früheren Versionen von Windows Installer angewendet werden, jedoch ohne die Windows Installer 3,0-Patchen-Funktionalität. Es ist auch möglich, Patches zu erstellen, die die Windows Installer 3,0 explizit benötigen, die von früheren Versionen von Windows Installer nicht angewendet werden können. Wenn ein Benutzer die Installerversion nicht aktualisieren kann, müssen Sie sicherstellen, dass die Anwendung oder das Update mit einem zukünftigen Update der Windows Installer kompatibel ist.
-   Eine Liste der Windows Installer Features, die von früheren Versionen von Windows Installer nicht unterstützt werden, finden Sie unter [What es New in Windows Installer](what-s-new-in-windows-installer.md).

## <a name="meet-the-windows-logo-certification-requirements"></a>Erfüllen Sie die Zertifizierungsanforderungen für Windows-Logo.

-   Auch wenn Sie nicht beabsichtigen, Ihre Anwendung an das Logo-Programm zu übermitteln, können Sie nach den Logo Zertifizierungsrichtlinien helfen, Ihr Windows Installer Paket zu verbessern. Eine Übersicht über die Logo-Anforderungen und Links zu bestimmten Logo Zertifizierungsprogrammen finden Sie unter [Windows Installer-und Logo-Anforderungen](windows-installer-and-logo-requirements.md).

## <a name="prepare-the-package-for-localization"></a>Bereiten Sie das Paket für die Lokalisierung vor.

-   Es empfiehlt sich, bei der Erstellung des ursprünglichen Installationspakets eine zukünftige Lokalisierung vorzubereiten. Sie können das empfohlene Paket Lokalisierungs Verfahren bei der [Lokalisierung eines Windows Installer Pakets](localizing-a-windows-installer-package.md)befolgen.

## <a name="update-your-windows-installer-development-tools-and-documentation"></a>Aktualisieren Sie Ihre Windows Installer Entwicklungs Tools und-Dokumentation.

-   Die [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md) sind nicht Verteil Bar, und Sie sollten nur die Versionen dieser Tools verwenden, die von Microsoft zur Verfügung stehen. Diese sind in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md) im Microsoft Windows Software Development Kit (SDK) verfügbar.
-   Mehrere unabhängige Softwarehersteller bieten Tools zum Erstellen oder Ändern von Windows Installer Paketen. Diese Tools können eine Paket Erstellungs Umgebung bereitstellen, die möglicherweise einfacher zu verwenden ist als die Tools, die im Windows Installer SDK bereitgestellt werden. Weitere Informationen zu diesen Tools finden Sie in den Informationsressourcen, die in [anderen Quellen Windows Installer Informationen](other-sources-of-windows-installer-information.md)erläutert werden.
-   Die Funktion zum Erstellen eines Pakets aus Textdateien ist für einige Entwickler möglicherweise intuitiver. Das WiX-Toolset (Windows Installer XML), das auf [SourceForge.net](https://sourceforge.net/projects/wix) verfügbar ist, erstellt Windows-Installationspakete aus XML-Quellcode.
-   Die Dokumentation im [Windows Installer SDK](./windows-installer-portal.md) , das in der MSDN-Online Bibliothek veröffentlicht wurde, wird am häufigsten aktualisiert.
-   Verwenden Sie die aktuelle Version von [Msizap.exe](msizap-exe.md) (Version 3.1.4000.2726 oder höher), die in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md) für Windows Vista oder höher verfügbar ist. Kleinere Versionen von Msizap.exe können Informationen zu allen Updates entfernen, die auf andere Anwendungen auf dem Computer des Benutzers angewendet wurden. Wenn diese Informationen entfernt werden, müssen diese anderen Anwendungen möglicherweise entfernt und erneut installiert werden, um weitere Updates zu erhalten.
-   Der Datenbanktabellen-Editor [Orca.exe](orca-exe.md) ist ein Datenbanktabellen-Editor zum Erstellen und Bearbeiten von Windows Installer Paketen und Mergemodulen. Es verfügt über eine grundlegende GUI-Schnittstelle, unterstützt jedoch die erweiterte Bearbeitung von Windows Installer- Auch wenn Sie als primäres Entwicklungs Tool eine andere Anwendung verwenden, finden Sie möglicherweise die Verwendung von Orca.exe die bei der Problembehandlung und beim Testen eines Pakets praktisch ist.
-   Weitere Informationen zu den aktuellen Windows Installer Informationen, die in Blogs, technischen Chats, Newsgroups, technischen Artikeln und Websites verfügbar sind, finden Sie unter [andere Quellen mit Windows Installer](other-sources-of-windows-installer-information.md) .

## <a name="if-you-decide-to-repackage-a-legacy-setup-application-follow-good-repackaging-practices"></a>Wenn Sie sich entschließen, eine Legacy-Setup Anwendung neu zu verpacken, befolgen Sie die bewährten Vorgehensweisen zum erneuten verpacken.

Viele Anwendungshersteller stellen systemeigene Windows Installer Pakete für die Installation oder deren Produkte bereit. Software, die eine vorhandene Legacy-Setup-Anwendung in ein Windows Installer Paket konvertiert, wird als Umverpackungs Tool bezeichnet. Im Whitepaper [schrittweise Anleitung zum Erstellen von Windows Installer Paketen und zum erneuten Verpacken von Software für die Windows Installer](https://www.microsoft.com/technet/prodtechnol/windows2000serv/howto/winstall.mspx) wird ein kommerziell verfügbares Tool zum erneuten Verpacken beschrieben. Das erneute Verpacken einer vorhandenen Setup Anwendung ist nicht die beste Entwicklungs Übung. Anwendungen, die von Anfang an entwickelt wurden, um Windows Installer Features zu nutzen, können Benutzern die Installation und den Betrieb erleichtern. Wenn Sie sich für die Verwendung einer Software zum erneuten Verpacken entscheiden, können Sie mithilfe der folgenden Verfahren ein besseres Windows Installer Paket erzielen.

-   Die Tools zum erneuten Verpacken konvertieren Legacy Installationen in ein Windows Installer Paket, indem ein Bild eines stagingsystems vor und nach der Installation erstellt wird. Alle Registrierungs Änderungen, Dateiänderungen oder Systemeinstellungen, die während des Aufzeichnungs Vorgangs auftreten, sind in der-Installation enthalten. Konfigurieren Sie die Hardware und die Software des Computers, der zum erneuten Verpacken der Installation verwendet wird, so nah wie möglich an das System des vorgesehenen Benutzers. Erstellen Sie ein separates Paket für jede andere Hardwarekonfiguration. Ernedas erneute Verpacken mithilfe eines sauberen stagingcomputers. Entfernen Sie alle nicht benötigten Anwendungen. Beendet alle unnötigen Prozesse. Schließen Sie alle nicht wichtigen Systemdienste.
-   Erstellen Sie immer eine Kopie der ursprünglichen Installation, bevor Sie mit der Arbeit beginnen. Arbeiten Sie immer an der Kopie. Beenden Sie einen Neuverpackungs nie, bevor Sie das Paket erstellt haben. Wenn das Paket vom Neuverpackungs beschädigt wird, verfügen Sie weiterhin über das Original.
-   Packen Sie Microsoft-Software Updates nicht erneut in ein Windows Installer Paket. Microsoft veröffentlicht Software Updates, z. b. Service Packs, als selbst extrahierende Dateien, die automatisch installiert werden. Diese Updates verwenden andere Installationsprogramme als die Windows Installer, um geschützte Windows-Ressourcen zu ersetzen, und können nicht in ein Windows Installer Paket konvertiert werden. Weitere Informationen zum Bereitstellen von Windows Service Packs finden Sie im Bereitstellungs Handbuch Service Pack in [Microsoft TechNet](https://technet.microsoft.com/).
-   Verwenden Sie kein Tool zum erneuten Verpacken, um ein Windows Installer Paket in ein neues Paket zu konvertieren. Der Windows Installer fügt dem System und den Anwendungs Ressourcen Konfigurationsinformationen hinzu. Wenn ein Tool zum erneuten Verpacken das System vor und nach der Installation vergleicht, interpretiert der Neuverpackungs die Konfigurationsinformationen als Teil der Anwendung. Dies schadet in der Regel der neu verpackten Anwendung. Verwenden Sie stattdessen [Anpassungs Transformationen](a-customization-transform-example.md) , um ein vorhandenes Windows Installer Paket zu ändern, oder erstellen Sie ein neues Paket. Anpassungs Transformationen können mithilfe des [Msitran.exe](msitran-exe.md) Tools erstellt werden.
-   Verwenden Sie kein Tool zum erneuten Verpacken, um mehrere Windows Installer Pakete in einem einzelnen Paket zu konsolidieren. Stattdessen können Sie das [Msistuff.exe](msistuff-exe.md) -Tool verwenden, um die ausführbare Datei Setup.exe Bootstrap so zu konfigurieren, dass die Pakete nacheinander installiert werden.
-   Legen Sie das Windows Installer Paket so fest, dass es vom Kunden problemlos angepasst werden kann. Globale Variablen, die während einer Installation von der Windows Installer verwendet werden, können mithilfe von öffentlichen [Eigenschaften](properties.md) oder [Anpassungs Transformationen](a-customization-transform-example.md)festgelegt werden. Stellen Sie eine Dokumentation zur Verwendung dieser Eigenschaften und praktischen Standardwerte für alle anpassbaren Werte bereit. Weitere Informationen zum erhalten und Festlegen von Eigenschaften finden [Sie unter Verwenden von Eigenschaften](using-properties.md). Ein Beispiel für eine Anpassungs Transformation finden Sie unter [Beispiel für eine Anpassungs Transformation](a-customization-transform-example.md).

## <a name="do-not-try-to-replace-protected-resources"></a>Versuchen Sie nicht, geschützte Ressourcen zu ersetzen.

Windows Installer Paketen sollten nicht versuchen, geschützte Ressourcen während der Installation oder des Updates zu ersetzen. Der Windows Installer entfernt oder ersetzt diese Ressourcen nicht, da Windows die Ersetzung wichtiger Systemdateien, Ordner und Registrierungsschlüssel verhindert. Der Schutz dieser Ressourcen verhindert Anwendungs-und Betriebssystem Fehler.

-   Bei Ausführung unter Windows Server 2008 oder Windows Vista überspringt das Windows Installer die Installation von Dateien oder Registrierungs Schlüsseln, die durch [Windows-Ressourcenschutz](../wfp/windows-resource-protection-portal.md) (WRP) geschützt sind, das Installationsprogramm gibt eine Warnung in die Protokolldatei ein und setzt den Rest der Installation ohne Fehler fort. Weitere Informationen finden [Sie unter Verwenden von Windows Installer und Windows-Ressourcenschutz](windows-resource-protection-on-windows-vista.md).
-   WRP ist der neue Name für den Windows-Datei Schutz (WFP). WRP schützt Registrierungsschlüssel und Ordner sowie wichtige Systemdateien. In Windows Server 2003, Windows XP und Windows 2000 konnte das Installationsprogramm die Datei von WFP installieren, wenn das Windows Installer eine durch WFP geschützte Datei gefunden hat. Weitere Informationen finden [Sie unter Verwenden von Windows Installer und Windows-Ressourcenschutz](windows-resource-protection-on-windows-vista.md).

## <a name="do-not-depend-upon-non-critical-resources"></a>Verlassen Sie sich nicht auf nicht kritische Ressourcen.

Die Installation oder Aktualisierung sollte aus folgenden Gründen nicht von der Installation nicht kritischer Ressourcen abhängen.

-   Benutzerdefinierte Aktionen können fehlschlagen, wenn Sie von einer Komponente abhängen, die zu einer Funktion gehört, die der Benutzer anstelle von installiert.
-   Benutzerdefinierte Aktionen, die vor der [InstallFinalize](installfinalize-action.md) -Aktion sequenziert werden, können fehlschlagen, wenn Sie von einer Komponente abhängen, die eine installierte Assembly enthält. Der Windows Installer committet Assemblys nicht in den globalen Assemblycache (GAC), bis die InstallFinalize-Aktion abgeschlossen ist.

## <a name="use-the-api-to-retrieve-windows-installer-configuration-information"></a>Verwenden Sie die-API, um Windows Installer Konfigurationsinformationen abzurufen.

Die Installation der Anwendung oder des Updates sollte nicht von direktem Zugriff auf Windows Installer Konfigurationsinformationen abhängen, die auf dem Computer gespeichert sind. Verwenden Sie stattdessen die Windows Installer-Anwendungsprogrammierschnittstelle zum Abrufen von Konfigurationsinformationen. Der Speicherort und das Format der Konfigurationsinformationen werden vom Windows Installer-Dienst verwaltet und können sich ändern.

-   Die Installations-und Konfigurationsfunktionen der Windows Installer-API werden in der [Installations Funktionsreferenz](installer-function-reference.md)beschrieben.
-   Die [Konfigurations Eigenschaften](property-reference.md) werden in der Eigenschaften Referenz beschrieben.
-   Die Automatisierungsmethoden und-Eigenschaften werden in der [Automatisierungs Schnittstellenreferenz](automation-interface-reference.md)beschrieben. Das Beispielskript WiLstPrd.vbs die eine Verbindung mit einem Installer-Objekt herstellt und registrierte Produkte und Produktinformationen auflistet. Weitere Informationen finden Sie unter [Auflisten von Produkten, Eigenschaften, Features und Komponenten](list-products-properties-features-and-components.md).

## <a name="organize-the-installation-of-your-application-around-components"></a>Organisieren Sie die Installation Ihrer Anwendung um Komponenten.

Der Windows Installer-Dienst installiert oder entfernt Sammlungen von Ressourcen, die als [Komponenten](windows-installer-components.md)bezeichnet werden. Da Komponenten im allgemeinen gemeinsam genutzt werden, muss der Autor eines Installationspakets den Regeln folgen, wenn die Komponenten eines Features oder einer Anwendung angegeben werden.

-   Befolgen Sie die Komponenten Regeln, wenn Sie [Anwendungen in Komponenten organisieren](organizing-applications-into-components.md) , um sicherzustellen, dass neue Komponenten oder neue Versionen von Komponenten installiert und entfernt werden können, ohne dass andere Anwendungen beschädigt werden. Sie können das unter [Definieren von Installationsprogramm Komponenten](defining-installer-components.md)beschriebene Verfahren befolgen.
-   Das Installationsprogramm verfolgt jede Komponente anhand der entsprechenden Komponenten-ID-GUID, die in der [Komponenten Tabelle](component-table.md)angegeben ist. Es ist von entscheidender Bedeutung für den Betrieb des Windows Installer Verweis Zählmechanismus, dass die Komponenten-ID-GUID korrekt ist. Befolgen Sie die Richtlinien zum [Ändern des Komponenten Codes](changing-the-component-code.md).
-   Wenn das Paket die Komponenten Regeln unterbrechen muss, achten Sie auf die möglichen Konsequenzen, und stellen Sie sicher, dass bei der Installation die Komponenten nie installiert werden, wo Sie möglicherweise Komponenten im System des Benutzers beschädigen. Weitere Informationen finden Sie unter [Was geschieht, wenn die Komponenten Regeln beschädigt sind?](what-happens-if-the-component-rules-are-broken.md).
-   Beachten Sie, wie das Windows Installer die [Regeln für die Datei Versions](file-versioning-rules.md) Verwaltung anwendet, wenn [vorhandene Dateien ersetzt](replacing-existing-files.md)werden. Der Windows Installer bestimmt zunächst, ob die Schlüsseldatei der Komponente bereits installiert ist, bevor versucht wird, die Dateien der Komponente zu installieren. Wenn das Installationsprogramm eine Datei mit dem gleichen Namen wie die Schlüsseldatei der Komponente findet, die am Ziel Speicherort installiert ist, vergleicht Sie die Version, das Datum und die Sprache der beiden Schlüsseldateien und verwendet Datei Versions Regeln, um zu bestimmen, ob die vom Paket bereitgestellte Komponente installiert werden soll. Wenn das Installationsprogramm feststellt, dass es die Komponentenbasis auf der Schlüsseldatei ersetzen muss, verwendet es die Datei Versions Regeln für jede installierte Datei, um zu bestimmen, ob die Datei ersetzt werden soll.

## <a name="reduce-the-size-of-large-windows-installer-packages"></a>Reduzieren Sie die Größe großer Windows Installer Pakete.

Sehr große Windows-Pakete benötigen Systemressourcen und können für Benutzer schwierig zu installieren sein. Es empfiehlt sich, die Größe von sehr großen Windows Installer Paketen mit den folgenden Methoden zu verringern.

-   Komprimieren Sie die Dateien in der Installation, und speichern Sie Sie in einer CAB-Datei. Das Installationsprogramm ermöglicht die Speicherung der CAB-Datei als separate externe Datei oder als Datenstream im MSI-Paket selbst. Weitere Informationen finden [Sie unter Verwenden von Schränken und komprimierten Quellen](using-cabinets-and-compressed-sources.md).
-   Entfernen Sie Speicherplatz in der MSI-Datei, indem Sie eine der Optionen verwenden, [die unter Reduzieren der Größe einer MSI-Datei](reducing-the-size-of-an--msi-file.md)erläutert werden.
-   Wenn das Windows Installer-Paket mehr als 32767 Dateien enthält, müssen Sie das Schema der Datenbank ändern. Weitere Informationen finden Sie unter [Erstellen eines großen Pakets](authoring-a-large-package.md).

## <a name="if-you-use-custom-actions-follow-good-custom-action-practices"></a>Wenn Sie benutzerdefinierte Aktionen verwenden, befolgen Sie bewährte Methoden für benutzerdefinierte Aktionen.

Der Windows Installer verfügt über viele integrierte [Standard Aktionen](standard-actions-reference.md) für die Installation und Wartung von Anwendungen. Entwickler sollten versuchen, sich auf die Standard Aktionen zu verlassen, anstatt ihre eigenen [benutzerdefinierten Aktionen](custom-actions.md)zu erstellen. Es gibt jedoch Situationen, in denen der Entwickler eines Installationspakets es zum Schreiben einer benutzerdefinierten Aktion findet.

-   Befolgen Sie die Richtlinien zum [Verwenden von benutzerdefinierten Aktionen](using-custom-actions.md).
-   Befolgen Sie die [Richtlinien zum Sichern von benutzerdefinierten Aktionen](guidelines-for-securing-custom-actions.md). Benutzerdefinierte Aktionen, die vertrauliche Informationen verwenden, sollten diese Informationen nicht in das Protokoll schreiben. Weitere Informationen finden Sie unter [Sicherheit für benutzerdefinierte Aktionen](custom-action-security.md).
-   Benutzerdefinierte Aktionen dürfen nicht versuchen, einen Einstiegspunkt für die System Wiederherstellung innerhalb einer benutzerdefinierten Aktion festzulegen. Weitere Informationen finden Sie [unter Festlegen eines Wiederherstellungs Punkts aus einer benutzerdefinierten Aktion](setting-a-restore-point-from-a-custom-action.md).
-   Gibt Fehlermeldungen von benutzerdefinierten Aktionen zurück und schreibt Sie in das Protokoll, um die Problembehandlung für benutzerdefinierte Aktionen zu vereinfachen Weitere Informationen finden Sie unter [Fehlermeldung benutzerdefinierte Aktionen](error-message-custom-actions.md) und [zurückgeben von Fehlermeldungen von benutzerdefinierten Aktionen](returning-error-messages-from-custom-actions.md).
-   Ändern Sie den Systemstatus nicht in eine sofortige benutzerdefinierte Aktion. Benutzerdefinierte Aktionen, die das System direkt ändern oder einen anderen Systemdienst aufzurufen, müssen bis zu dem Zeitpunkt verzögert werden, zu dem das Installationsskript ausgeführt wird. Jeder [benutzerdefinierten Aktion für die verzögerte Ausführung](deferred-execution-custom-actions.md) , die den Systemstatus ändert, muss eine [benutzerdefinierte Rollback-Aktion](rollback-custom-actions.md) voranstehen, um die Systemstatus Änderung bei einem Installations Rollback rückgängig zu machen. Weitere Informationen finden [Sie unter Ändern des System Status mithilfe einer benutzerdefinierten Aktion](changing-the-system-state-using-a-custom-action.md).
-   Benutzerdefinierte Aktionen, bei denen komplexe Installations Vorgänge ausgeführt werden, sollten eine [ausführbare Datei](executable-files.md) oder eine [Dynamic Link Library](dynamic-link-libraries.md)sein. Beschränken Sie die Verwendung von benutzerdefinierten Aktionen auf der Grundlage von [Skripts](scripts.md) auf einfache Installations Vorgänge.
-   Machen Sie die Details, die die benutzerdefinierte Aktion für das System durchführt, leicht für Systemadministratoren auffindbar. Fügen Sie die Details von Registrierungs Einträgen und Dateien, die von der benutzerdefinierten Aktion verwendet werden, in eine benutzerdefinierte Tabelle ein, und lassen Sie die benutzerdefinierte Aktion aus dieser Tabelle Dies wird anhand des Beispiels unter [Verwenden einer benutzerdefinierten Aktion zum Erstellen von Benutzerkonten auf einem lokalen Computer](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)veranschaulicht. Weitere Informationen zum Hinzufügen von benutzerdefinierten Tabellen zu einer Datenbank finden Sie unter [Arbeiten mit Abfragen](working-with-queries.md) und [Beispielen für Datenbankabfragen mithilfe von SQL und Skript](examples-of-database-queries-using-sql-and-script.md).
-   Bei benutzerdefinierten Aktionen sollte kein Dialogfeld angezeigt werden. Benutzerdefinierte Aktionen, für die eine Benutzeroberfläche erforderlich ist, können stattdessen die [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) -Funktion verwenden. Siehe [Senden von Nachrichten an Windows Installer mithilfe von "msiprocessmessage](sending-messages-to-windows-installer-using-msiprocessmessage.md)".
-   Benutzerdefinierte Aktionen dürfen keine Funktionen verwenden, die auf der Seite aufgelistet sind: Funktionen, die [nicht für benutzerdefinierte Aktionen verwendet](functions-not-for-use-in-custom-actions.md)werden können.
-   Wenn die Installation auf einem Terminal Server ausgeführt werden soll, testen Sie, ob alle benutzerdefinierten Aktionen auf einem Terminal Server ausgeführt werden können. Weitere Informationen finden Sie unter [**Terminalserver**](terminalserver.md) -Eigenschaft.
-   Um eine benutzerdefinierte Aktion auszuführen, wenn ein bestimmter Patch deinstalliert wird, muss die benutzerdefinierte Aktion entweder in der ursprünglichen Anwendung vorhanden sein oder sich in einem Patch für das Produkt befinden, das immer angewendet wird. Weitere Informationen finden Sie unter [Patch Uninstall Custom Actions](patch-uninstall-custom-actions.md).
-   Benutzerdefinierte Aktionen sollten die Benutzeroberflächen Ebene nicht als Bedingung für das Senden von Fehlermeldungen an das Installationsprogramm verwenden, da dies die Protokollierung und externe Nachrichten beeinträchtigen kann. Weitere Informationen finden Sie [unter Bestimmen der Benutzeroberflächen Ebene aus einer benutzerdefinierten Aktion](determining-ui-level-from-a-custom-action.md).
-   Verwenden Sie bedingte Anweisungen und [bedingte Anweisungs Syntax](conditional-statement-syntax.md) , um sicherzustellen, dass das Paket ordnungsgemäß benutzerdefinierte Aktionen ausführt, keine benutzerdefinierten Aktionen ausführt oder Alternative benutzerdefinierte Aktionen ausführt, wenn das Paket deinstalliert wird. Testen Sie, ob das Paket beim [Deinstallieren von benutzerdefinierten Aktionen](uninstalling-custom-actions.md)erwartungsgemäß funktioniert. Weitere Informationen finden [Sie unter während des Entfernens](conditioning-actions-to-run-during-removal.md) auszuführende Maßnahmen.
-   Wenn die Installation in der Lage sein muss, von Benutzern ohne Administratorrechte ausgeführt zu werden, testen Sie, um sicherzustellen, dass alle benutzerdefinierten Aktionen mit nicht Administratorrechten ausgeführt werden können. Benutzerdefinierte Aktionen erfordern erweiterte Berechtigungen, um Teile des Systems zu ändern, die Nichtbenutzer spezifisch sind. Der Installer kann benutzerdefinierte Aktionen mit erhöhten Rechten ausführen, wenn eine verwaltete Anwendung installiert wird oder wenn die System Richtlinie für erweiterte Berechtigungen angegeben wurde. Alle benutzerdefinierten Aktionen, für die erhöhte Rechte erforderlich sind, müssen die benutzerdefinierte Aktion "msidbcustomaction typeinscript" und "msidbcustomaction tytaoannehmen" [In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md) in den benutzerdefinierten Aktionstyp einschließen. Dies wird anhand des Beispiels unter [Verwenden einer benutzerdefinierten Aktion zum Erstellen von Benutzerkonten auf einem lokalen Computer](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)veranschaulicht.

## <a name="if-you-use-assemblies-follow-good-assembly-practices"></a>Befolgen Sie bei Verwendung von Assemblys gute assemblypraktiken.

Wenn das [Paket](assemblies.md)softwareupdateiassemblys verwendet, befolgen Sie die Richtlinien zum Hinzufügen von Assemblys [zu einem Paket](adding-assemblies-to-a-package.md), zum [Aktualisieren](updating-assemblies.md) [von](installing-and-removing-assemblies.md)Assemblys

## <a name="do-not-ship-concurrent-installations"></a>Senden Sie keine gleichzeitigen Installationen.

[Gleichzeitige Installationen](concurrent-installations.md), auch geschsted-Installationen genannt, installieren während einer aktuell ausgeführten Installation ein weiteres Windows Installer Paket. Die Verwendung gleichzeitiger Installationen ist keine bewährte Vorgehensweise, da Sie für Kunden schwierig zu bedienen sind. Das Patchen und Aktualisieren funktioniert möglicherweise nicht mit gleichzeitigen Installationen. Die empfohlene Alternative zur Verwendung gleichzeitiger Installationen besteht darin, stattdessen eine Setup Anwendung und einen externen Benutzeroberflächen Handler zu verwenden, um mehrere Windows Installer Pakete nacheinander zu installieren.

Weitere Informationen zur Verwendung eines externen UI-Handlers finden Sie unter über [Wachen einer Installation mithilfe von "msieintexternalui](monitoring-an-installation-using-msisetexternalui.md)". Weitere Informationen zum Verwenden eines Daten Satz basierten externen Handlers finden Sie unter über [Wachen einer Installation mithilfe von "msieintexternaluirecord](monitoring-an-installation-using-msisetexternaluirecord.md)".

Parallele Installationen werden manchmal in kontrollierten Unternehmensumgebungen verwendet, um Anwendungen zu installieren, die nicht für die Öffentlichkeit vorgesehen sind. Befolgen Sie diese Richtlinien, wenn Sie sich entscheiden, parallele Installationen zu verwenden.

-   Verwenden Sie keine gleichzeitigen Installationen zum Installieren oder Aktualisieren eines Versand Produkts.
-   Bei gleichzeitigen Installationen sollten keine Komponenten gemeinsam genutzt werden.
-   Eine administrative Installation sollte keine gleichzeitige Installation enthalten.
-   Integrierte progressbars sollten nicht mit gleichzeitigen Installationen verwendet werden.
-   Ressourcen, die angekündigt werden sollen, sollten nicht durch eine parallele Installation installiert werden.
-   Ein Paket, das eine parallele Installation einer Anwendung ausführt, sollte auch die gleichzeitige Anwendung deinstallieren, wenn das übergeordnete Produkt deinstalliert wird. Eine in der Systemsteuerung unter "Software" unter "Programme hinzufügen/entfernen" ist eine untergeordnete Installation im Kontext des übergeordneten Produkts vorhanden.

## <a name="keep-package-names-and-package-codes-consistent"></a>Halten Sie die Paketnamen und Paket Codes konsistent.

Der MSI-Datei kann ein beliebiger Name zugewiesen werden, der Benutzern hilft, das Paket zu identifizieren, aber der Name sollte nicht geändert werden, ohne dass auch der Produktcode geändert wird.

-   Geben Sie der MSI-Datei einen benutzerfreundlichen Namen, mit dem der Benutzer den Inhalt des Windows Installer Pakets identifizieren kann.
-   Der [Produktcode](product-codes.md) ist die Prinzipal Identifizierung einer Anwendung und muss sich ändern, wenn ein umfassendes Update der Anwendung vorhanden ist. Weitere Informationen finden Sie unter [**ProductCode**](productcode.md) und [Ändern des Produktcodes](changing-the-product-code.md). Das Ändern des Namens der MSI-Datei der Anwendung wird als umfassende Änderung angesehen und erfordert immer eine entsprechende Änderung des Produktcodes, um die Konsistenz zu gewährleisten.
-   Der [Paket Code](package-codes.md) ist der primäre Bezeichner, der vom Installer verwendet wird, um das richtige Paket für eine bestimmte Installation zu suchen und zu überprüfen. Keine zwei nonidentical. msi-Dateien sollten jemals denselben Paketcode aufweisen. Wenn ein Paket geändert wird, ohne den Paket Code zu ändern, verwendet das Installationsprogramm ggf. das neuere Paket nicht, wenn auf beide weiterhin für den Installer zugegriffen werden kann. Der Paketcode wird in der [**Zusammenfassungs Eigenschaft "Revisionsnummer**](revision-number-summary.md) " des [Zusammenfassungs Informationsdaten Stroms](summary-information-stream.md)gespeichert.
-   Beachten Sie, dass Buchstaben in Produktcode und Paket Code- [GUIDs](guid.md) alle Großbuchstaben sein müssen.

## <a name="do-not-use-the-selfreg-and-typelib-tables"></a>Verwenden Sie die Tabellen "selfreg" und "TypeLib" nicht.

-   Die Autoren von Installationspaketen werden dringend von der Verwendung der Selbstregistrierung und der Tabelle [selfreg](selfreg-table.md) abgeraten. Stattdessen sollten Sie Module registrieren, indem Sie eine oder mehrere Tabellen in der [Registrierungs Tabellen Gruppe](registry-tables-group.md)erstellen. Viele der Vorteile der Windows Installer gehen bei der Selbstregistrierung verloren, da in der Regel selbst Registrierungs Routinen wichtige Konfigurationsinformationen ausgeblendet werden. Eine Liste der Gründe für die Vermeidung der Selbstregistrierung finden Sie unter [selfreg Table](selfreg-table.md).
-   Autoren von Installationspaketen wird dringend empfohlen, die [typelib](typelib-table.md) -Tabelle zu verwenden. Anstatt die TypeLib-Tabelle zu verwenden, registrieren Sie Typbibliotheken mithilfe der [Registrierungs](registry-table.md) Tabelle. Wenn eine Installation mit der TypeLib-Tabelle fehlschlägt und ein Rollback ausgeführt werden muss, wird der Computer vom Rollback möglicherweise nicht in demselben Zustand wieder hergestellt, der vor dem Rollback vorhanden war.

## <a name="provide-the-option-to-install-without-a-user-interface"></a>Stellen Sie die Option zur Installation ohne Benutzeroberfläche bereit.

Administratoren bevorzugen häufig die Bereitstellung von Anwendungen innerhalb einer Corporation, ohne dass eine Benutzerinteraktion erforderlich ist. Es empfiehlt sich, die Anwendung für die Bereitstellung der Option zu aktivieren, die mit der [Benutzeroberflächen Ebene](user-interface-levels.md) "None" installiert wird.

-   Verwenden Sie [öffentliche Eigenschaften](public-properties.md) für Konfigurationsinformationen. Administratoren können diese Informationen über die Befehlszeile bereitstellen.
-   Es ist nicht erforderlich, dass die Installation von Informationen abhängig ist, die von der Benutzerinteraktion mit Dialogfeldern gesammelt wurden. Diese Informationen sind während einer automatischen Installation nicht verfügbar.
-   Der Computer des Benutzers wird während einer automatischen Installation nicht automatisch neu gestartet.
-   Administratoren können die [Ebene der Benutzeroberfläche](user-interface-levels.md) bei der Installation mithilfe der [Befehlszeilenoption](command-line-options.md) "/q" festlegen. Die Benutzeroberflächen Ebene kann auch Programm gesteuert mit einem [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)-Befehl festgelegt werden.

## <a name="avoid-using-the-alwaysinstallelevated-policy"></a>Vermeiden Sie die Verwendung der alwaysinstallerhöhten-Richtlinie.

Wenn die Richtlinie [alwaysinstallerhöhten](alwaysinstallelevated.md) nicht festgelegt ist, werden Anwendungen, die nicht vom Administrator verteilt werden, mit den Berechtigungen des Benutzers installiert, und nur verwaltete Anwendungen erhalten erhöhte Rechte. Durch Festlegen dieser Richtlinie wird Windows Installer angewiesen, System Berechtigungen zu verwenden, wenn die Anwendung auf dem System installiert wird. Diese Methode kann einen Computer mit einem Sicherheitsrisiko öffnen, denn wenn diese Richtlinie festgelegt ist, kann ein Benutzer, der nicht Administrator ist, Installationen mit [*erhöhten*](e-gly.md) Rechten ausführen und auf sichere Speicherorte auf dem Computer zugreifen. Es empfiehlt sich, eine andere Methode als die alwaysinstallerhöhten-Richtlinie zu verwenden, wenn Sie [ein Paket mit erhöhten Rechten für ein nicht-Administrator-](installing-a-package-with-elevated-privileges-for-a-non-admin.md) oder [Patching-Per-User verwaltete Anwendungen](patching-per-user-managed-applications.md)installieren.

## <a name="enable-the-disablemedia-policy-to-limit-unauthorized-installation"></a>Aktivieren Sie die disablemedia-Richtlinie, um die nicht autorisierte Installation einzuschränken

Die [disablemedia](disablemedia.md) -Richtlinie kann eine nicht autorisierte Installation von Anwendungen verhindern. Wenn diese Richtlinie aktiviert ist, können Benutzer und Administratoren, die eine Wartungs Installation eines Produkts ausführen, das Dialog Feld "Durchsuchen" nicht zum Durchsuchen von Medienquellen (z. b. CD-ROM) für die Quellen anderer installier barer Produkte verwenden. Das Durchsuchen anderer Produkte wird verhindert, unabhängig davon, ob die Installation mit erweiterten Berechtigungen erfolgt. Der Benutzer kann das Produkt weiterhin von einem Medium aus neu installieren, wenn der Benutzer über eine ordnungsgemäß bezeichnete Medienquelle verfügt.

## <a name="keep-the-original-package-source-files-secure-and-available-to-users"></a>Sorgen Sie dafür, dass die ursprünglichen Paket Quelldateien sicher und für Benutzer verfügbar sind.

In einigen Fällen ist die ursprüngliche Quelle des Windows Installer Pakets möglicherweise erforderlich, um eine Anwendung zu installieren, zu reparieren oder zu aktualisieren. Wenn das Installationsprogramm eine verfügbare Quelle nicht finden kann, wird der Benutzer aufgefordert, Medien bereitzustellen oder zu einem Netzwerk Speicherort zu wechseln, der die benötigten Quellen enthält. Es wird empfohlen, sicherzustellen, dass das Installationsprogramm über die benötigten Quellen verfügt, ohne dass der Benutzer dazu aufgefordert werden muss.

-   Verwenden Sie [digitale Signaturen und externe CAB-Dateien](digital-signatures-and-external-cabinet-files.md) , um sicherzustellen, dass die vom Installationsprogramm verwendeten Quellen sicher sind. Ein unkomprimiertes Quell Image, das an einem öffentlichen Speicherort gespeichert ist, ist nicht sicher.
-   Fügen Sie eine komplette Liste der Netzwerk-oder URL-Quell Pfade zum Installationspaket der Anwendung in die [**SourceList**](sourcelist.md) -Eigenschaft ein.
-   Verwenden Sie für den Quellpfad eine DFS-Freigabe (verteiltes Dateisystem).
-   Verwenden Sie die Windows Installer-API, um Quell Listen Informationen für Windows Installer Anwendungen und Patches abzurufen und zu ändern. Weitere Informationen finden Sie unter [Verwalten von Installations Quellen](managing-installation-sources.md).
-   Verwenden Sie die Methoden und Eigenschaften des [**Installerobjekts**](installer-object.md), des [**Product-Objekts**](product-object.md)und des [**Patch-Objekts**](patch-object.md) , um Quell Listen Informationen für Windows Installer Anwendungen und Patches abzurufen und zu ändern.
-   Beachten Sie die unter verhindern der Verwendung [des Zugriffs auf die ursprünglichen Installations Quell](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md) Punkte aufgeführten Punkte, um die Möglichkeit zu minimieren, dass Ihr Patch Zugriff auf die ursprünglichen Quellen benötigt.
-   Speichern Sie die Paket Quelldateien an einem Speicherort, bei dem es sich nicht um den temporären Ordner des Systems handelt. Windows Installer im temporären Ordner gespeicherten Quelldateien können Benutzern nicht mehr zur Verfügung stehen.

## <a name="enable-verbose-logging-on-users-computer-when-troubleshooting-deployment"></a>Aktivieren Sie die ausführliche Protokollierung auf dem Computer des Benutzers bei der Problembehandlung.

[Windows Installer Protokollierung](windows-installer-logging.md) schließt eine ausführliche Protokollierungs Option ein, die auf dem Computer eines Benutzers aktiviert werden kann. Die Informationen in einem ausführlichen Protokoll können bei der Problembehandlung Windows Installer Paket Bereitstellung hilfreich sein.

-   Sie können die ausführliche Protokollierung auf dem Computer des Benutzers aktivieren, indem Sie die [Befehlszeilenoptionen](command-line-options.md), die [**MsiLogging**](msilogging.md) -Eigenschaft, die [Protokollierungs Richtlinie](logging.md), die [**msienablelog**](/windows/desktop/api/Msi/nf-msi-msienableloga)und die [**EnableLog**](installer-enablelog.md) -Methode verwenden.
-   Eine sehr nützliche Ressource zum interpretieren Windows Installer Protokolldateien ist [Wilogutl.exe](wilogutl-exe.md). Dieses Tool unterstützt die Analyse von Protokolldateien und zeigt vorgeschlagene Lösungen für Fehler an, die in einer Protokolldatei gefunden werden.
-   Weitere Informationen zur Interpretation Windows Installer Protokolldateien finden Sie im Whitepaper auf der TechNet-Website: [Windows Installer: Vorteile und Implementierung für System Administratoren](https://www.microsoft.com/technet/prodtechnol/windows2000serv/maintain/featusability/winmsi.mspx).
-   Die Protokollierungs Option "ausführliche" sollte nur zur Problembehandlung verwendet werden und sollte nicht beibehalten werden, da dies negative Auswirkungen auf die Systemleistung und den Speicherplatz haben kann. Jedes Mal, wenn Sie das Tool "Software" in der Systemsteuerung verwenden, wird eine neue Datei erstellt.

## <a name="uninstallation-leaves-the-users-computer-in-a-clean-state"></a>Bei der Installation bleibt der Computer des Benutzers in einem sauberen Zustand.

Die Anwendungs Entfernung ist so wichtig wie die Installation. Wenn ein Windows Installer Paket deinstalliert wird, sollte es nicht nutzlose Teile von sich selbst auf dem Computer des Benutzers zurückbleiben.

-   Wenn eine Datei, die auf dem Computer des Benutzers entfernt worden sein soll, nach dem Ausführen einer Deinstallation weiterhin installiert ist, entfernt das Installationsprogramm möglicherweise nicht die Komponente, die die Datei enthält, aus einem oder mehreren der unter [Entfernen von Dateien](removing-stranded-files.md)mit den Dateien beschriebenen Gründen.
-   Wenn eine Anwendung registriert werden muss, erstellen Sie das Paket, um Registrierungsinformationen zu entfernen, wenn die Anwendung deinstalliert wird. Weitere Informationen finden Sie [unter Hinzufügen oder Entfernen von Registrierungs Schlüsseln für die Installation oder Entfernung von-Komponenten](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md). Wenn eine Anwendung nicht registriert ist, wird die Anwendung in der Systemsteuerung nicht in der Funktion "Software" aufgeführt und kann nicht mit dem Windows Installer verwaltet werden.
-   Wenn Sie eine Anwendung in der Systemsteuerung über das Feature "Software" ausblenden möchten und weiterhin den Windows Installer zur Verwaltung der Anwendung verwenden können, befolgen Sie die Anweisungen unter [Hinzufügen und Entfernen einer Anwendung und belassen der Registrierung in der Registrierung](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).
-   Benutzerdefinierte Aktionen sollten bei der Neuinstallation für die Durchführung von oder nicht erforderlich sein. Bei der Installation und Deinstallation müssen möglicherweise unterschiedliche benutzerdefinierte Aktionen ausgeführt werden.
-   Benutzerspezifische Anpassungs Informationen können in einer Textdatei auf dem Computer gespeichert werden. Dies hat den Vorteil, dass die Datei entfernt werden kann, wenn die Anwendung deinstalliert wird, auch wenn der Benutzer dieser Anpassung derzeit nicht angemeldet ist.

## <a name="test-packages-for-both-per-user-and-per-machine-installation-deployment"></a>Test Pakete für die Bereitstellung pro Benutzer und pro Computerinstallation.

Es empfiehlt sich, den Kunden zu ermöglichen, zu entscheiden, ob ein Paket für die Installation entweder im Computer-oder benutzerspezifischen [Installations Kontext](installation-context.md)bereitgestellt werden soll.

-   Berücksichtigen Sie, ob die Anwendung während des Entwicklungsprozesses nur für bestimmte Benutzer oder alle Benutzer des Computers verfügbar sein soll.
-   Überprüfen Sie, ob das Paket sowohl für die Installation pro Benutzer als auch für Computer spezifische Installations Kontexte ordnungsgemäß funktioniert.
-   Sorgen Sie dafür, dass das Paket problemlos anpassbar ist, und lassen Sie Kunden entscheiden, ob Sie Sie pro Benutzer oder pro Computer bereitstellen.

## <a name="plan-and-test-a-servicing-strategy-before-shipping-the-application"></a>Planen und testen Sie eine Wartungsstrategie, bevor Sie die Anwendung versenden.

Sie sollten entscheiden, wie Sie die Anwendung bereitstellen möchten, bevor Sie die Anwendung zum ersten Mal bereitstellen.

-   Beachten Sie die Aktualisierungs Typen, die Sie für die spätere Verwendung Ihrer Anwendung erwarten. Der Windows Installer stellt drei Arten von Updates bereit: [kleine Updates](small-updates.md), [kleinere](minor-upgrades.md)Upgrades und [größere Upgrades](major-upgrades.md). Die Unterschiede zwischen diesen werden im Thema [Patching und Upgrades](patching-and-upgrades.md) beschrieben.
-   Bevor Sie Ihre Anwendung versenden, testen Sie, ob Sie nach der Wartung mit den einzelnen Update Typen erwartungsgemäß funktioniert.

## <a name="reduce-the-dependency-of-updates-upon-the-original-sources"></a>Reduzieren Sie die Abhängigkeit von Updates auf den ursprünglichen Quellen.

Wenn die ursprünglichen Quelldateien erforderlich sind, um Ihre Anwendung zu aktualisieren, kann dies die Wartung der Anwendung erschweren. Die folgenden Methoden können dabei helfen, die Abhängigkeit von Updates auf den ursprünglichen Quellen zu verringern.

-   Verwenden Sie zum Aktualisieren der Baselineversion der Anwendung einen [*Delta Patch*](d-gly.md) , z. b. die RTM-Version und die Service Pack Versionen. Befolgen Sie die Richtlinien für die Verwendung von Delta Patches, die im Thema: [verringern der Patchgröße](reducing-patch-size.md)beschrieben werden.
-   Befolgen Sie die Empfehlungen im Thema: [verhindern, dass ein Patch Zugriff auf die ursprüngliche Installationsquelle erfordert](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md).

## <a name="do-not-distribute-unserviceable-merge-modules"></a>Nicht servierbar-Mergemodule verteilen.

Anwendungen sollten nicht von [Mergemodulen](merge-modules.md) für die Installation der-Komponente abhängen, wenn sich der Besitzer des Mergemoduls und der Besitzer der Anwendung unterscheiden. Dies kann das bedienen der Anwendung erschweren, da beide Besitzer koordinieren müssen, um die Anwendung oder das Modul zu aktualisieren. Ohne alle Anwendungen zu kennen, die das Mergemodul verwendet haben, kann der Besitzer der Anwendung das Mergemodul nicht aktualisieren, ohne zu riskieren, dass das Update möglicherweise nicht mit einer anderen Anwendung kompatibel ist. Der Besitzer des Mergemoduls verfügt über keine direkte Methode zum Aktualisieren von Windows Installer Paketen, auf denen das Mergemodul bereits installiert ist.

-   Es empfiehlt sich, den Benutzern die erforderlichen Komponenten als weitere Windows Installer-Installation bereitzustellen.

## <a name="avoid-patching-administrative-installations"></a>Vermeiden Sie das Patchen administrativer Installationen.

Stellen Sie in einem Netzwerk eine [Administrative Installation](administrative-installation.md) des ursprünglichen Windows Installer Pakets Ihrer Anwendung bereit, um Mitgliedern einer Arbeitsgruppe die Installation der Anwendung zu ermöglichen. Benutzer dieses administrativen Abbilds sollten dann Updates auf die lokale Instanz der Anwendung auf dem Computer anwenden. Dies sorgt dafür, dass die Benutzer mit dem administrativen Abbild synchronisiert werden. Das Anwenden von Updates auf die administrative Installation wird aus den folgenden Gründen nicht empfohlen.

-   Die Größe und Latenz des Downloads, die für Benutzer zum Abrufen eines Updates erforderlich sind, wird im Vergleich zum Herunterladen eines Patches erweitert. Das gesamte aktualisierte Windows Installer Paket und die Quelldateien müssen heruntergeladen, wiederholt und neu installiert werden.
-   Benutzer können die [Installation nach Bedarf](installation-on-demand.md) nicht durchlaufen und Anwendungen von einer aktualisierten administrativen Installation reparieren, bis Sie die Anwendung wiederholen und erneut installieren.
-   Wenn Sie einen Patch auf eine administrative Installation anwenden, wird die digitale Signatur aus dem Paket entfernt. Ein Administrator muss das Paket zurückziehen. Weitere Informationen zur Verwendung digitaler Signaturen finden Sie unter [digitale Signaturen und Windows Installer](digital-signatures-and-windows-installer.md).
-   Viele binäre Patches Zielen auf das RTM-Image der Anwendung ab und erfordern eine vorherige Dateiversion. Die lokale Instanz einer Anwendung, die über eine aktualisierte administrative Installation installiert wurde, funktioniert möglicherweise nicht mit anderen Updates. Viele binäre patchanwendungen können fehlschlagen.
-   Wenn Sie einen Patch auf eine administrative Installation anwenden, werden die Quelldateien und die MSI-Datei aktualisiert, aber das Netzwerk Image wird nicht mit Informationen über das Update versehen. Benutzer können nicht ermitteln, welche Updates von der administrativen Installation empfangen wurden. Dadurch ist es unmöglich, auf der Benutzerseite angewendete Updates mit denjenigen zu sequenzieren, die bereits auf dem Administrator Image angewendet wurden.
-   Patches, die auf eine administrative Installation angewendet werden, sind keine nicht [installierbaren Patches](uninstallable-patches.md). Dadurch kann verhindert werden, dass sich der auf dem Computer des Benutzers zwischengespeicherte Paketcode von dem Paket Code bei der administrativen Installation unterscheidet. Wenn sich der Paket Code, der auf dem Computer des Benutzers zwischengespeichert ist, von dem auf dem Computer des Benutzers unterscheidet, installieren Sie die Anwendung über die administrative Installation neu, und Patchen Sie dann den Client Computer.
-   Wenn Sie sich dazu entschließen, kleine Updates durch das Patchen eines administrativen Abbilds anzuwenden, befolgen Sie die im Thema: [anwenden kleiner Updates durch Patchen eines administrativen Abbilds](applying-small-updates-by-patching-an-administrative-image.md)beschriebenen Richtlinien.

## <a name="register-updates-to-run-with-elevated-privilege"></a>Registrieren von Updates, die mit erhöhten Rechten ausgeführt werden.

Ab Windows Installer 3,0 ist es möglich, Patches auf eine Anwendung anzuwenden, die in einem Benutzer verwalteten Kontext installiert wurde, nachdem der Patch als erweiterte Berechtigungen registriert wurde. Patches können nicht auf Anwendungen angewendet werden, die in einem pro Benutzer verwalteten Kontext unter Verwendung von Versionen von Windows Installer vor Version 3,0 installiert sind.

-   Verwenden Sie die [**sourcelistaddsource**](patch-sourcelistaddsource.md) -Methode oder die [**msisourcelistaddsourceex**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) -Funktion, um ein Patchpaket mit erhöhten Rechten zu registrieren. Befolgen Sie die Richtlinien und Beispiele für das [Patchen Per-User verwaltete Anwendungen](patching-per-user-managed-applications.md).
-   Wenn Sie Windows Installer Version 4,0 unter Windows Vista ausführen, können Sie auch das [Patchen der Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md) verwenden, um den Autoren von Windows Installer Installationen die Identifizierung Digital signierter Patches zu ermöglichen, die in Zukunft von Benutzern ohne Administratorrechte angewendet werden können. Dies ist nur bei der Installation von Paketen im [Installations Kontext](installation-context.md) pro Computer (ALLUSERS = 1) verfügbar.
-   Stellen Sie sicher, dass Patchen mit geringsten Rechten nicht deaktiviert wurde, indem Sie die [**msidisableluapatching**](msidisableluapatching.md) -Eigenschaft oder die [disableluapatching](disableluapatching.md) -Richtlinie festlegen.

## <a name="use-the-msipatchsequence-table-to-sequence-patches"></a>Verwenden Sie die msipatchsequence-Tabelle, um Patches zu sequenzieren.

Fügen Sie eine [msipatchsequence-Tabelle](msipatchsequence-table.md) in das Paket ein, und fügen Sie patchsequenzierungs Informationen hinzu. Ab Windows Installer Version 3,0 kann das Installationsprogramm die msipatchsequence-Tabelle verwenden, wenn [mehrere Patches installiert](installing-multiple-patches.md) werden, um die beste patchanwendungssequenz zu ermitteln. Verwenden Sie die Richtlinien, die im Whitepaper [Patch-Sequenzierung in Windows Installer Version 3,0](https://www.microsoft.com/downloads/details.aspx?FamilyID=ad7ac91e-2493-4549-ae6f-bf5e007c12a3) beschrieben werden, um patchfamilien zu definieren.

-   Wenn Sie praktisch sind, geben Sie alle Patches als zu einer einzelnen patchfamilie gehörenden an. In vielen Fällen bietet eine einzige patchfamilie genügend Flexibilität, um Patches zu sequenzieren. Die Komplexität der Erstellung erhöht sich, wenn mehrere patchfamilien verwendet werden. Weisen Sie der patchfamilie einen aussagekräftigen Namen zu, und weisen Sie der patchfamilie Sequenzwerte zu, die sich im Laufe der Zeit vergrößern. Befolgen Sie das Beispiel für das [mehrfache Patchen](multiple-patching-example.md) , um Patches in der Reihenfolge anzuwenden, in der Sie ausgestellt wurden.
-   Verwenden Sie die [patchsequence-Tabelle](patchsequence-table--patchwiz-dll-.md) in [Patchwiz.dll](patchwiz-dll.md) , um die Informationen in der [msipatchsequence-Tabelle](msipatchsequence-table.md)zu generieren. Die Version von PATCHWIZ.DLL, die mit Windows Installer 3,0 veröffentlicht wurde, kann automatisch patchsequenzierungs Informationen generieren. Weitere Informationen zum Hinzufügen eines neuen Patches finden Sie unter [Erstellen von Patchsequenzinformationen](generating-patch-sequence-information---patchwiz-dll-.md). Weitere Informationen zu Szenarien für die Patchsequenzierung finden Sie im Whitepaper: [Patchsequenzierung in Windows Installer Version 3,0](https://www.microsoft.com/downloads/details.aspx?FamilyID=ad7ac91e-2493-4549-ae6f-bf5e007c12a3).

## <a name="test-the-installation-package-thoroughly"></a>Testen Sie das Installationspaket gründlich.

Testen Sie die ordnungsgemäße Installation, Reparatur und Löschung Ihres Windows Installer Pakets. Sie können den Testprozess in folgende Teile aufteilen.

-   Installations Tests: Testen Sie die Installation mit allen möglichen Kombinationen von Anwendungs Features. Testen Sie alle Installationstypen, einschließlich [administrativer Installation](administrative-installation.md), [Rollback-Installation](rollback-installation.md)und [Installation nach Bedarf](installation-on-demand.md). Probieren Sie alle möglichen Installationsmethoden aus, und klicken Sie auf die MSI-Datei, die [Befehlszeilenoptionen](command-line-options.md)und die Installation über die Systemsteuerung. Testen Sie, ob das Paket von Benutzern in allen möglichen Berechtigungs Kontexten installiert werden kann. Versuchen Sie, das Paket zu installieren, nachdem es mit allen möglichen Methoden bereitgestellt wurde. Aktivieren Sie [Windows Installer Protokollierung](windows-installer-logging.md) für jeden Test, und beheben Sie alle Fehler, die im Installationsprotokoll und im Ereignisprotokoll gefunden werden.
-   Testen der Benutzeroberfläche: Testen Sie das Paket, wenn es mit allen möglichen [Benutzeroberflächen Ebenen](user-interface-levels.md)installiert ist. Testen Sie das installierte Paket ohne Benutzeroberfläche und mit allen Informationen, die über die Benutzeroberfläche bereitgestellt werden. Stellen Sie sicher, [dass der Zugriff auf die](accessibility.md) Benutzeroberfläche und die Benutzeroberfläche für verschiedene Bildschirmauflösungen und Schriftgrößen erwartungsgemäß funktioniert.
-   Wartung und Reparatur testen: Testen Sie, ob das Paket [Patches und Upgrades](patching-and-upgrades.md) verarbeiten kann, die von einem [kleinen Update](small-updates.md), einem [geringfügigen Upgrade](minor-upgrades.md)und [großen Upgrades](major-upgrades.md)geliefert werden. Schreiben Sie vor dem Bereitstellen des Pakets ein Test Update für jeden Typ, und wenden Sie es auf das ursprüngliche Paket an.
-   Tests deinstallieren: Vergewissern Sie sich, dass beim Entfernen des Pakets keine nutzbaren Teile von sich selbst auf dem Computer des Benutzers liegen und nur die Informationen entfernt wurden, die zum Paket gehören. Starten Sie den Testcomputer neu, nachdem Sie das Paket deinstalliert haben, und überprüfen Sie die Integrität der allgemeinen System Tools und anderer Standardanwendungen. Testen Sie, ob das Paket von Benutzern in allen möglichen Berechtigungs Kontexten entfernt werden kann. Testen Sie alle Methoden, um das Paket zu entfernen, klicken Sie auf die MSI-Datei, verwenden Sie die [Befehlszeilenoptionen](command-line-options.md), und entfernen Sie das Paket aus der Systemsteuerung. Aktivieren Sie [Windows Installer Protokollierung](windows-installer-logging.md) für jeden Test, und beheben Sie alle Fehler, die im Installationsprotokoll und im Ereignisprotokoll gefunden werden.
-   Testen von Produktfunktionen: Stellen Sie sicher, dass die Anwendung nach dem installieren, reparieren oder Entfernen des Pakets erwartungsgemäß funktioniert.

## <a name="fix-all-validation-errors-before-deploying-a-new-or-revised-installation-package"></a>Beheben Sie alle Validierungs Fehler, bevor Sie ein neues oder überarbeitetes Installationspaket bereitstellen.

Führen Sie die [Paket](package-validation.md) Überprüfung für ein neues oder überarbeitetes Windows Installer Paket aus, bevor Sie es zum ersten Mal installieren. Die Überprüfung überprüft die Windows Installer Datenbank auf Erstellungs Fehler. Wenn Sie versuchen, ein Paket zu installieren, das die Überprüfung nicht besteht, kann das System des Benutzers beschädigt werden.

-   Sie können das Paket mit [Orca.exe](orca-exe.md) oder [Msival2.exe](msival2-exe.md)validieren. Beide Tools werden mit dem Windows SDK bereitgestellt. Drittanbieter können auch das Ice-Validierungssystem in Ihre Erstellungs Umgebung integrieren.
-   Sie können den Standardsatz [interner Konsistenz Evaluatoren-ICES](internal-consistency-evaluators-ices.md) verwenden, die in den Cub-Dateien enthalten sind, die mit dem SDK bereitgestellt werden, oder die Validierung anpassen, indem Sie [ein Eis aufbauen](building-an-ice.md) und es der CUB-Datei hinzufügen.
-   Sie können den Evalcom2.dll verwenden, um die [Validierungs Automatisierung](validation-automation.md) für Installationspakete und Mergemodule zu implementieren.

## <a name="author-a-secure-installation"></a>Erstellen Sie eine sichere Installation.

Befolgen Sie diese Richtlinien, wenn Sie Ihr Paket entwickeln, um bei der Installation eine sichere Umgebung zu gewährleisten.

-   [Richtlinien für das Erstellen von sicheren Installationen](guidelines-for-authoring-secure-installations.md)
-   [Richtlinien zum Sichern von Paketen auf gesperrten Computern](guidelines-for-securing-packages-on-locked-down-computers.md)
-   [Richtlinien zum Sichern von benutzerdefinierten Aktionen](guidelines-for-securing-custom-actions.md)

## <a name="use-pmsihandle-instead-of-handle"></a>Verwenden von "pmsihandle" anstelle von "handle"

Die **pmsihandle** -Typvariablen sind in "MSI. h" definiert. Es wird empfohlen, dass Ihre Anwendung den **pmsihandle** -Typ verwendet, da das Installationsprogramm **pmsihandle** -Objekte schließt, wenn Sie den Gültigkeitsbereich verlassen, während die Anwendung **msihandle** -Objekte durch Aufrufen von [**msiclosehandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle)schließen muss.

Wenn Sie z. b. Code wie den folgenden verwenden:

``` syntax
MSIHANDLE hRec = MsiCreateRecord(3);
```

Ändern Sie ihn in:

``` syntax
PMSIHANDLE hRec = MsiCreateRecord(3);
```

 

 
