---
description: Diese Dokumentation ist die primäre Quelle des Referenzmaterials für Windows Installer.
ms.assetid: dfbcc4b6-08bd-4b8a-b658-7010bd0b099c
title: Roadmap to Windows Installer Documentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad76621cf26e72bf277964609846c32e514b9cb73296bf27593111f84b92d037
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625910"
---
# <a name="roadmap-to-windows-installer-documentation"></a>Roadmap to Windows Installer Documentation

Diese Dokumentation ist die primäre Quelle des Referenzmaterials für Windows Installer. Sie enthält Informationen zu Installationspaketen und zum Installationsprogrammdienst. Darüber hinaus werden vollständige Beschreibungen der Anwendungsprogrammierschnittstelle (APPLICATION PROGRAMMING Interface, API) und der Elemente der Installer-Datenbank bereitgestellt. Diese Dokumentation enthält auch eine Erläuterung grundlegender Beispiele für Installations- und Updatepakete in [Windows Installer-Beispielen](windows-installer-examples.md).

Der [rollenbasierte Leitfaden zum Windows Installer-Dokumentation](role-based-guide-to-windows-installer-documentation.md) ist eine Alternative, die Lesern als Leitfaden zur Verfügung gestellt wird, die Links zu Themen bevorzugen, die nach professionellen Rollen und allgemeinen Aufgabenszenarien organisiert sind.

Informationen zu Windows Installer-Newsgroups finden Sie auch im [Thema: Andere Quellen von Windows Installer-Informationen.](other-sources-of-windows-installer-information.md)

Eine Liste der Tipps zur Verwendung des Windows Installers finden Sie unter [Windows Installer Best Practices](windows-installer-best-practices.md).

In der folgenden Liste werden die einzelnen Abschnitte der Dokumentation zum Installationsprogramm beschrieben.

-   [Informationen zu Windows Installer](about-windows-installer.md) bietet eine Übersicht über die Funktionen und Vorteile des Installationsprogramms, z. B. Ankündigung, Installation bei Bedarf, Resilienz, Anpassung und Komponentenverwaltung. In diesem Abschnitt werden die Konzepte der Installationskomponenten und -features vorgestellt, die für das Verständnis der Organisation einer Installation durch das Installationsprogramm unerlässlich sind. Außerdem werden mehrere übergeordnete Themen zur Installation erläutert, z. B. Systemrichtlinie, Regeln für die Dateiversionsversionsierung und Rollbackinstallation.
-   [Mit Windows Installer](using-windows-installer.md) wird eine Vielzahl von Themen erläutert, z. B. eine Standardmethode zum Organisieren einer Anwendung in Komponenten, die das Installationsprogramm installieren oder vom Computer eines Benutzers entfernen kann. Herunterladen eines Installationspakets aus dem World Wide Web und verwenden komprimierte Quellimages.
-   Die Informationen in den [Abschnitten Neuerungen in Windows Installer](what-s-new-in-windows-installer.md) können verwendet werden, um neue Features zu identifizieren, die von früheren Versionen Windows Installers nicht unterstützt werden.
-   [Digitale Signaturen und Windows Installer](digital-signatures-and-windows-installer.md) beschreibt, wie digitale Signaturen mit Paketen, Transformationen, Patches, Mergemodulen und externen Cab-Dateien verwendet werden können.
-   [Assemblys](assemblies.md) erläutert, wie Windows Installer zum Installieren und Verwalten von Common Language-Laufzeit- und Win32-Assemblys verwendet wird.
-   [Benutzeroberfläche](user-interface.md) enthält Informationen über die Benutzeroberflächenfunktionen des Installationsprogramms. Obwohl das Installationsprogramm keine Benutzeroberfläche bereitstellt, kann ein Paketautor alle Daten und Logik beibehalten, die zum Ausführen einer vollständig interaktiven internen oder externen Benutzeroberfläche in der Installationsdatenbank erforderlich sind. Im Abschnitt Verweis werden Elemente der Benutzeroberfläche beschrieben, die in den Datenbanktabellen angegeben werden können, einschließlich Dialogfeldern, Steuerelementen und Steuerelementereignissen.
-   [Standardaktionen](standard-actions.md) erläutert die Standardaktionen, die vom Installationsprogramm in den Sequenztabellen zum Ausführen einer Installation verwendet werden. Diese Informationen sind in erster Linie für Paketentwickler bestimmt.
-   [Benutzerdefinierte Aktionen](custom-actions.md) beschreibt, wie zusätzliche Funktionen im Installationsprogramm erstellt werden. Benutzerdefinierte Aktionen ermöglichen es einem Autor eines Installationspakets, die Funktionen von Standardaktionen zu erweitern, indem ausführbare Dateien, Dynamic Link-Bibliotheken und Skripts eingeschlossen werden. Diese Informationen sind für Paketentwickler bestimmt, die Installationsfunktionen ausführen müssen, die nicht an anderer Stelle im Installationsprogramm gefunden wurden.
-   [Eigenschaften](properties.md) enthalten Informationen zu den Eigenschaften, die das Installationsprogramm während einer Installation verwendet. Die Abschnitte "About" und "Using" enthalten eine Übersicht über diese globalen Variablen, und jede Eigenschaft wird im Abschnitt Referenz beschrieben.
-   [Summary Information Stream](summary-information-stream.md) dokumentiert die Eigenschaften der Zusammenfassungsinformationen, die vom Installationsprogramm verwendet werden. Diese Informationen sind für alle Entwickler von Interesse.
-   [Patchen und Upgrades](patching-and-upgrades.md) erläutert die Verwendung des Installationsprogramms zum Ausführen von Dateiupdates, ILEEs, kleineren Updates, Produktupgrades und Patchen.
-   [In Transformationen](transforms.md) wird erläutert, wie eine Installationsdatenbank mithilfe einer Datenbanktransformation geändert oder angepasst wird und wie Transformationen generiert, geschützt und angewendet werden.
-   [Die Paketvalidierung](package-validation.md) erläutert die Verwendung interner Konsistenzauswertungen (Internal Consistency Evaluators, ICEs), um die interne Konsistenz von Installationspaketen zu testen, die sich in der Entwicklung befinden.
-   [Mergemodule](merge-modules.md) stellen einen Standard für den Entwurf von Mergemodulen dar. Auf diesen Standard sollten Entwickler folgen, die ihre eigenen Mergemodule erstellen, sowie von Entwicklern, die den Installer verwenden möchten, um freigegebenen Code für ihre Anwendungen bereitzustellen.
-   [Windows Installer unter 64-Bit-Betriebssystemen](windows-installer-on-64-bit-operating-systems.md) erläutert die Verwendung von Windows Installer zum Installieren und Verwalten von Installationskomponenten, die für die Ausführung unter 64-Bit-Betriebssystemen entwickelt wurden.
-   [Windows Installer-Beispiele](windows-installer-examples.md) enthält ein Schritt-für-Schritt-Beispiel zum Erstellen eines Installationspakets mit einer internen Benutzeroberfläche in [Ein Installationsbeispiel.](an-installation-example.md) Ein Beispiel für die Erstellung eines größeren Upgrades für ein vorhandenes Paket finden Sie unter Beispiel für [ein Upgrade.](an-upgrade-example.md) Informationen dazu, wie eine Anpassungstransformation Features deaktiviert und neue Ressourcen hinzufügt, finden Sie unter [Beispiel für eine Anpassungstransformation.](a-customization-transform-example.md) Ein Beispiel für das Erstellen eines Patchpakets, das ein kleines Update auf ein vorhandenes Installationspaket anwendet, finden Sie unter [A Small Update Patching Example](a-small-update-patching-example.md). Informationen zum Lokalisieren eines vorhandenen Installationspakets finden Sie unter [Ein Lokalisierungsbeispiel.](a-localization-example.md)
-   [Automation Interface](automation-interface.md) stellt Informationen für Entwickler bereit, die die Automatisierungsschnittstelle von Windows Installer verwenden möchten.
-   [Installer Functions](installer-functions.md) beschreibt Funktionsaufrufe an die Installer-API. Dies sind die Funktionen, die andere Anwendungen aufrufen, um auf die Installationsdienste zuzugreifen, um Anwendungen zu installieren, zu warten oder zu entfernen. Die Using-Abschnitte enthalten Diskussionen darüber, wie Sie Features anfordern, Installationen initiieren und fehlende Komponenten programmgesteuert neu installieren. Der Abschnitt Verweis ist das primäre Referenzmaterial für die Installer-Dienstfunktionen.
-   [Installationsprogrammdatenbank](installer-database.md) erläutert die Installationsdatenbank. Das Installationsprogramm speichert alle Logik und Daten, die für eine Installation in einer relationalen Datenbank in einer .msi-Datei erforderlich sind. Der Abschnitt Informationen bietet eine Übersicht mit Schemadiagrammen für die wichtigsten Funktionsgruppen von Tabellen der Datenbank. Im Abschnitt Using wird die Arbeit mit den wichtigsten dieser Tabellen erläutert. Diese Abschnitte enthalten Informationen, die für Entwickler wichtig sind, die Installationspakete erstellen oder Tools zum Erstellen von Paketen schreiben. Der Abschnitt Verweis enthält vollständiges Referenzmaterial für jede Datenbanktabelle. Dieser Abschnitt enthält auch den primären Verweis für jede datenbankfunktion. Die Datenbankfunktionen werden intern vom Installationsprogramm für den Zugriff auf die Datenbank verwendet und sind in erster Linie für Entwickler von Tools zum Erstellen von Installationspaketen von Interesse.

 

 



