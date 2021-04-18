---
description: Diese Dokumentation ist die Hauptquelle für das Referenzmaterial für Windows Installer.
ms.assetid: dfbcc4b6-08bd-4b8a-b658-7010bd0b099c
title: Roadmap zur Windows Installer Dokumentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 324d626eb5dd201a47c16613c5de598fcd13052d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368197"
---
# <a name="roadmap-to-windows-installer-documentation"></a>Roadmap zur Windows Installer Dokumentation

Diese Dokumentation ist die Hauptquelle für das Referenzmaterial für Windows Installer. Es enthält Informationen zu Installationspaketen und zum Installations Dienst. Außerdem werden umfassende Beschreibungen der Anwendungsprogrammierschnittstelle (Application Programming Interface, API) und der Elemente der Installer-Datenbank bereitgestellt. In dieser Dokumentation finden Sie auch grundlegende Beispiele für Installations-und Update Pakete in [Windows Installer Beispielen](windows-installer-examples.md).

Das [rollenbasierte Handbuch zu Windows Installer-Dokumentation](role-based-guide-to-windows-installer-documentation.md) ist eine Alternative, die als Leitfaden für Leser bereitgestellt wird, die es vorziehen, Links zu Themen anzuzeigen, die nach professionellen Rollen und allgemeinen Aufgaben Szenarios organisiert sind.

Weitere Informationen zu Windows Installer Newsgroups finden Sie unter dem Thema: [andere Quellen mit Windows Installer Informationen](other-sources-of-windows-installer-information.md).

Eine Liste mit Tipps zur Verwendung der Windows Installer finden Sie unter [Windows Installer bewährten Methoden](windows-installer-best-practices.md).

In der folgenden Liste werden die einzelnen Abschnitte der installerdokumentation beschrieben.

-   [Informationen zu Windows Installer](about-windows-installer.md) bietet einen Überblick über die installerfunktionen und-Vorteile, z. b. Werbung, Installation nach Bedarf, Resilienz, Anpassung und Komponenten Verwaltung. In diesem Abschnitt werden die Konzepte der Installer-Komponenten und-Features vorgestellt, die für das Verständnis der Installation einer-Installation durch das Installationsprogramm erforderlich sind. Außerdem werden mehrere allgemeine Themen zur Installation erläutert, wie z. b. System Richtlinien, Regeln für die Datei Versionsverwaltung und Rollback-Installation.
-   Die [Verwendung von Windows Installer](using-windows-installer.md) erläutert eine Vielzahl von Themen, z. b. eine Standardmethode zum Organisieren einer Anwendung in Komponenten, die das Installationsprogramm auf dem Computer eines Benutzers installieren oder entfernen kann. Herunterladen eines Installationspakets vom World Wide Web; und mit komprimierten Quell Images.
-   Die Informationen in den Abschnitten [Neuerungen in Windows Installer](what-s-new-in-windows-installer.md) können verwendet werden, um neue Features zu identifizieren, die von früheren Windows Installer Versionen nicht unterstützt werden.
-   [Digitale Signaturen und Windows Installer](digital-signatures-and-windows-installer.md) beschreiben, wie digitale Signaturen mit Paketen, Transformationen, Patches, Mergemodulen und externen CAB-Dateien verwendet werden können.
-   Assemblys [erläutert die](assemblies.md) Verwendung von Windows Installer zum Installieren und Verwalten von Common Language Run Time und Win32-Assemblys.
-   Die [Benutzeroberfläche](user-interface.md) enthält Informationen zu den Funktionen der Benutzeroberfläche des Installers. Obwohl das Installationsprogramm keine Benutzeroberfläche bereitstellt, kann ein Paket Autor alle Daten und die erforderliche Logik zum Ausführen einer vollständig interaktiven internen oder externen Benutzeroberfläche in der Installations Datenbank beibehalten. Im Referenz Abschnitt werden die Elemente der Benutzeroberfläche beschrieben, die in den Datenbanktabellen spezifizierbar sind, einschließlich Dialogfeldern, Steuerelementen und Steuerelement Ereignissen.
-   [Standard Aktionen](standard-actions.md) erläutert die Standard Aktionen, die vom Installationsprogramm in den Sequenz Tabellen verwendet werden, um eine Installation durchzuführen. Diese Informationen sind in erster Linie für Paket Entwickler vorgesehen.
-   [Benutzerdefinierte Aktionen](custom-actions.md) beschreiben, wie zusätzliche Funktionen im Installer erstellt werden. Benutzerdefinierte Aktionen ermöglichen einem Autor eines Installationspakets, die Funktionen von Standard Aktionen zu erweitern, indem Sie ausführbare Dateien, Dynamic Link Libraries und Skripts einschließen. Diese Informationen sind für Paket Entwickler gedacht, die Installationsfunktionen ausführen müssen, die an anderer Stelle im Installationsprogramm nicht gefunden wurden.
-   [Eigenschaften](properties.md) enthält Informationen zu den Eigenschaften, die vom Installationsprogramm während einer Installation verwendet werden. Die Abschnitte "about" und "using" bieten einen Überblick über diese globalen Variablen, und jede Eigenschaft wird im Abschnitt "Referenz" beschrieben.
-   [Zusammenfassungs Datenstrom](summary-information-stream.md) dokumentiert die Eigenschaften der Zusammenfassungs Informationen, die vom Installationsprogramm verwendet werden. Diese Informationen sind für alle Entwickler von Interesse.
-   Bei [Patching und Upgrades](patching-and-upgrades.md) wird die Verwendung des Installationsprogramms zum Ausführen von Datei Updates, QFEs, geringfügigen Updates, Produkt Upgrades und Patches erläutert.
-   [Transformationen](transforms.md) erläutert das ändern oder Anpassen einer Installations Datenbank mithilfe einer Daten Bank Transformation und das generieren, sichern und Anwenden von Transformationen.
-   Bei der [Paket](package-validation.md) Überprüfung wird die Verwendung interner Konsistenz Evaluatoren (ICES) zum Testen der internen Konsistenz von Installationspaketen erläutert, die sich in der Entwicklung befinden.
-   [Mergemodule](merge-modules.md) stellen einen Standard für das Entwerfen von Mergemodulen dar. Dieser Standard sollte von Entwicklern befolgt werden, die sowohl eigene Mergemodule als auch von Entwicklern erstellen, die das Installationsprogramm verwenden möchten, um freigegebenen Code für Ihre Anwendungen bereitzustellen.
-   [Windows Installer auf 64-Bit-Betriebssystemen](windows-installer-on-64-bit-operating-systems.md) erläutert, wie Sie mithilfe von Windows Installer Installationsprogramm Komponenten installieren und verwalten, die auf 64-Bit-Betriebssystemen ausgeführt werden.
-   [Windows Installer Beispiele](windows-installer-examples.md) beinhalten ein schrittweises Beispiel für das Erstellen eines Installationspakets mit einer internen Benutzeroberfläche in [einem Installations Beispiel](an-installation-example.md). Ein Beispiel für die Erstellung eines größeren Upgrades für ein vorhandenes Paket finden Sie in [einem upgradebeispiel](an-upgrade-example.md). Informationen dazu, wie eine Anpassungs Transformation Funktionen deaktiviert und neue Ressourcen hinzufügt, finden Sie unter [Beispiel für eine Anpassungs Transformation](a-customization-transform-example.md). Ein Beispiel für das Erstellen eines Patchpakets, das ein kleines Update auf ein vorhandenes Installationspaket anwendet, finden Sie unter [Beispiel für ein kleines Update-Patching](a-small-update-patching-example.md). Informationen zum Lokalisieren eines vorhandenen Installer-Pakets finden Sie unter [Beispiel für eine Lokalisierung](a-localization-example.md).
-   [Automation Interface](automation-interface.md) bietet Entwicklern Informationen, die die Automatisierungsschnittstelle von Windows Installer verwenden möchten.
-   [Installer-Funktionen](installer-functions.md) beschreiben Funktionsaufrufe der Installer-API. Dies sind die Funktionen, die andere Anwendungen aufrufen, um auf die Installer-Dienste zuzugreifen, um Anwendungen zu installieren, zu warten oder zu entfernen. Die using-Abschnitte enthalten Diskussionen darüber, wie Sie Features anfordern, Installationen initiieren und fehlende Komponenten Programm gesteuert neu installieren. Der Referenz Abschnitt ist das primäre Referenzmaterial für die Funktionen des Installations Dienstanbieter.
-   Die [Installer-Datenbank](installer-database.md) erläutert die-Installations Datenbank. Das Installationsprogramm speichert sämtliche Logik und Daten, die für eine Installation in einer relationalen Datenbank, die sich in einer MSI-Datei befindet, benötigt. Der Abschnitt about bietet einen Überblick über Schema Diagramme für die wichtigsten funktionalen Gruppen von Tabellen der-Datenbank. Der Abschnitt using erläutert das Arbeiten mit den wichtigsten dieser Tabellen. Diese Abschnitte enthalten Informationen, die für Entwickler, die Installationspakete erstellen, oder für das Schreiben von Paket Erstellungs Tools erforderlich sind. Der Referenz Abschnitt enthält das komplette Referenzmaterial für jede Datenbanktabelle. Dieser Abschnitt enthält auch den primären Verweis für jede der Datenbankfunktionen. Die Datenbankfunktionen werden intern vom Installationsprogramm für den Zugriff auf die Datenbank verwendet und sind hauptsächlich für Entwickler der Installer-Paket Erstellungs Tools von Interesse.

 

 



