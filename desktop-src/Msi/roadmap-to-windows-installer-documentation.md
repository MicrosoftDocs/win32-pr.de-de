---
description: Diese Dokumentation ist die primäre Quelle für Referenzmaterial für Windows Installer.
ms.assetid: dfbcc4b6-08bd-4b8a-b658-7010bd0b099c
title: Roadmap für Windows Installer-Dokumentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad76621cf26e72bf277964609846c32e514b9cb73296bf27593111f84b92d037
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625910"
---
# <a name="roadmap-to-windows-installer-documentation"></a>Roadmap für Windows Installer-Dokumentation

Diese Dokumentation ist die primäre Quelle für Referenzmaterial für Windows Installer. Sie enthält Informationen zu Installationspaketen und zum Installationsprogrammdienst. Sie enthält auch vollständige Beschreibungen der Anwendungsprogrammierschnittstelle (API) und der Elemente der Installer-Datenbank. Diese Dokumentation enthält auch eine Erörterung grundlegender Beispiele für Installations- und Updatepakete in Windows [Installer-Beispielen.](windows-installer-examples.md)

Der [rollenbasierte Leitfaden](role-based-guide-to-windows-installer-documentation.md) zur Dokumentation Windows Installer ist eine Alternative, die lesern zur Verfügung gestellt wird, die lieber Links zu Themen sehen möchten, die nach professionellen Rollen und allgemeinen Aufgabenszenarien organisiert sind.

Weitere Informationen zu Windows Installer-Newsgroups finden Sie auch im Thema: [Other Sources of Windows Installer Information](other-sources-of-windows-installer-information.md).

Eine Liste der Tipps zur Verwendung des Windows Installers finden Sie unter [Windows Installer Best Practices](windows-installer-best-practices.md).

In der folgenden Liste werden die einzelnen Abschnitte der Installationsdokumentation beschrieben.

-   [Informationen Windows Installer](about-windows-installer.md) bietet eine Übersicht über die Funktionen und Vorteile des Installationsprogramms, z. B. Ankündigung, Installation bei Bedarf, Resilienz, Anpassung und Komponentenverwaltung. In diesem Abschnitt werden die Konzepte von Installerkomponenten und -features erläutert, die für das Verständnis der Installationsprogrammierung von entscheidender Bedeutung sind. Darüber hinaus werden mehrere themenorientierte Themen zur Installation erläutert, z. B. Systemrichtlinie, Dateiversionsregeln und Rollbackinstallation.
-   [Mit Windows Installer](using-windows-installer.md) werden verschiedene Themen behandelt, z. B. eine Standardmethode zum Organisieren einer Anwendung in Komponenten, die das Installationsprogramm installieren oder vom Computer eines Benutzers entfernen kann. Herunterladen eines Installationspakets aus dem World Wide Web; und verwenden komprimierte Quellbilder.
-   Die Informationen in den Abschnitten Neues [in Windows Installer](what-s-new-in-windows-installer.md) können verwendet werden, um neue Features zu identifizieren, die von früheren Versionen Windows Installer nicht unterstützt werden.
-   [Digital Signatures und Windows Installer](digital-signatures-and-windows-installer.md) beschreibt, wie digitale Signaturen mit Paketen, Transformationen, Patches, Mergemodulen und externen Schränkendateien verwendet werden können.
-   [Assemblys](assemblies.md) erläutert die Verwendung des Windows Installers zum Installieren und Verwalten von Common Language Run Time und Win32-Assemblys.
-   [Benutzeroberfläche](user-interface.md) enthält Informationen zu den Benutzeroberflächenfunktionen des Installationsprogramms. Obwohl das Installationsprogramm keine Benutzeroberfläche bietet, kann ein Paketautor alle Daten und Logik behalten, die zum Ausführen einer vollständig interaktiven internen oder externen Benutzeroberfläche in der Installationsdatenbank erforderlich sind. Im Abschnitt Referenz werden Elemente der Benutzeroberfläche beschrieben, die in den Datenbanktabellen angegeben werden können, einschließlich Dialogfeldern, Steuerelementen und Steuerelementereignissen.
-   [Standardaktionen](standard-actions.md) erläutert die Standardaktionen, die vom Installationsprogramm in den Sequenztabellen zum Ausführen einer Installation verwendet werden. Diese Informationen sind in erster Linie für Paketentwickler bestimmt.
-   [Benutzerdefinierte Aktionen](custom-actions.md) beschreibt, wie zusätzliche Funktionen im Installationsprogramm erstellt werden. Benutzerdefinierte Aktionen ermöglichen es einem Autor eines Installationspakets, die Funktionen von Standardaktionen zu erweitern, indem ausführbare Dateien, Dynamic Link-Bibliotheken und Skripts verwendet werden. Diese Informationen sind für Paketentwickler bestimmt, die Installationsfunktionen ausführen müssen, die nicht an anderer Stelle im Installationsprogramm gefunden werden.
-   [Eigenschaften](properties.md) enthalten Informationen zu den Eigenschaften, die das Installationsprogramm während einer Installation verwendet. Die Abschnitte About und Using (Informationen und Verwendung) geben einen Überblick über diese globalen Variablen, und jede Eigenschaft wird im Abschnitt Referenz beschrieben.
-   [Zusammenfassungsinformationsstream](summary-information-stream.md) dokumentiert die Eigenschaften der Zusammenfassungsinformationen, die vom Installationsprogramm verwendet werden. Diese Informationen sind für alle Entwickler von Interesse.
-   [Patchen und Upgrades erläutert](patching-and-upgrades.md) die Verwendung des Installationsprogramms zum Ausführen von Dateiupdates, QFEs, kleineren Updates, Produktupgrades und Patchen.
-   [In Transformationen](transforms.md) wird erläutert, wie Eine Installationsdatenbank mithilfe einer Datenbanktransformation geändert oder angepasst wird und wie Transformationen generiert, geschützt und angewendet werden.
-   [Bei der](package-validation.md) Paketvalidierung wird erläutert, wie interne Konsistenzauswertungen (Internal Consistency Evaluators, ICEs) verwendet werden, um die interne Konsistenz von Installationspaketen zu testen, die sich in der Entwicklung befinden.
-   [Mergemodule](merge-modules.md) stellen einen Standard für den Entwurf von Mergemodulen vor. Dieser Standard sollte von Entwicklern befolgt werden, die ihre eigenen Mergemodule erstellen, sowie von Entwicklern, die das Installationsprogramm verwenden möchten, um freigegebenen Code an ihre Anwendungen zu liefern.
-   [Windows Installer unter 64-Bit-Betriebssystemen](windows-installer-on-64-bit-operating-systems.md) wird erläutert, wie sie den Windows-Installer verwenden, um Installationskomponenten zu installieren und zu verwalten, die für die Ausführung unter 64-Bit-Betriebssystemen entwickelt wurden.
-   [Windows Installer-Beispiele](windows-installer-examples.md) enthält ein schritt-für-Schritt-Beispiel zum Erstellen eines Installationspakets mit einer internen Benutzeroberfläche in [Einem Installationsbeispiel.](an-installation-example.md) Ein Beispiel für die Erstellung eines größeren Upgrades für ein vorhandenes Paket finden Sie unter [Ein Upgradebeispiel.](an-upgrade-example.md) Informationen dazu, wie eine Anpassungstransformation Funktionen deaktiviert und neue Ressourcen hinzufügt, finden Sie unter [Beispiel für eine Anpassungstransformation.](a-customization-transform-example.md) Ein Beispiel für die Erstellung eines Patchpakets, mit dem ein kleines Update auf ein vorhandenes Installationspaket angewendet wird, finden Sie unter Beispiel für ein kleines [Updatepatching.](a-small-update-patching-example.md) Informationen zum Lokalisieren eines vorhandenen Installationspakets finden Sie unter [Ein Lokalisierungsbeispiel.](a-localization-example.md)
-   [Automation Interface](automation-interface.md) stellt Informationen für Entwickler bereit, die die Automatisierungsschnittstelle des Windows verwenden möchten.
-   [Installer Functions](installer-functions.md) beschreibt Funktionsaufrufe an die Installer-API. Dies sind die Funktionen, die andere Anwendungen aufrufen, um auf die Installationsdienste zu zugreifen, um Anwendungen zu installieren, zu verwalten oder zu entfernen. In den Abschnitten Using (Verwenden) wird erläutert, wie Sie Features anfordern, Installationen initiieren und fehlende Komponenten programmgesteuert neu installieren. Der Abschnitt Referenz ist das primäre Referenzmaterial für die Funktionen des Installerdiensts.
-   [Installationsprogrammdatenbank](installer-database.md) erläutert die Installationsdatenbank. Das Installationsprogramm speichert die logik- und daten, die für eine Installation in einer relationalen Datenbank erforderlich sind, die sich in einer .msi befindet. Der Abschnitt About bietet eine Übersicht mit Schemadiagrammen für die wichtigsten Funktionsgruppen von Tabellen der Datenbank. Im Abschnitt Using wird das Arbeiten mit den wichtigsten dieser Tabellen erläutert. Diese Abschnitte enthalten Informationen, die für Entwickler wichtig sind, die Installationspakete erstellen oder Paketerstellungstools schreiben. Der Abschnitt Verweis enthält vollständiges Referenzmaterial für jede Datenbanktabelle. Dieser Abschnitt enthält auch den primären Verweis für jede der Datenbankfunktionen. Die Datenbankfunktionen werden intern vom Installationsprogramm für den Zugriff auf die Datenbank verwendet und sind in erster Linie für Entwickler von Tools zum Erstellen von Installationspaketen von Interesse.

 

 



