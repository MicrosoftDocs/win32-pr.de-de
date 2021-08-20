---
description: Die folgenden Abschnitte enthalten ein Beispiel für die Erstellung eines Upgradepakets für die anwendung, die unter Ein Installationsbeispiel beschrieben wird.
ms.assetid: 233302ea-abc3-4879-b868-425f2b10e02e
title: Ein Upgradebeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a148c8d66c09ae2ce033d3ad2440040734a2b1301b2e9e1b9bb1b79e44beb06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066350"
---
# <a name="an-upgrade-example"></a>Ein Upgradebeispiel

In den folgenden Abschnitten wird ein Beispiel für die Erstellung eines Upgradepakets für die Anwendung dargestellt, die unter [Ein Installationsbeispiel beschrieben ist.](an-installation-example.md) Ein Beispiel für eine minimale Benutzeroberfläche für dieses Beispiel finden Sie im [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) als Datei Uisample.msi. Wenn Sie über das SDK verfügen, haben Sie Zugriff auf alle Tools und Daten, die zum Reproduzieren des Beispielinstallationspakets, der Benutzeroberfläche und des Beispielupgradepakets erforderlich sind.

Dieses Beispiel veranschaulicht das Erstellen eines Windows Installer-Pakets, das das hypothetische Produkt MNP2000 auf ein neues Produkt namens MNP2001 aktualisiert. Das Beispiel für ein Upgradepaket wendet ein größeres Upgrade auf das Produkt an, das eine Änderung des Produktcodes erfordert. Weitere Informationen zu wichtigen Upgrades finden Sie im Thema [Hauptupgrades](major-upgrades.md) im Abschnitt [Patchen und Upgrades.](patching-and-upgrades.md)

Das Beispielupgradepaket enthält die folgenden Spezifikationen:

-   Um dieses Upgrade auf MNP2001 zu erhalten, muss ein Benutzer zuvor die Versionen 1.0 bis 1.4 (einschließlich) der englischen Sprache MNP2000 mithilfe des Windows-Installers installiert haben.
-   Wenn ein Benutzer versucht, das Upgradepaket zu installieren, durchsucht die Upgradefunktion von Windows Installer den Computer des Benutzers nach Allen Produkten, die für das Upgrade qualifiziert sind.
-   Windows Das Installationsprogramm migriert alle Featureeinstellungen des ursprünglichen Produkts zum aktualisierten Produkt.
-   Das Installationsprogramm entfernt alle veralteten Features vom Computer des Benutzers.
-   Das Installationsprogramm installiert alle neuen Features, die zum Upgrade gehören.
-   Durch eine Deinstallation des Upgradepakets wird das Produkt vom Computer des Benutzers entfernt, und die frühere Version des Produkts wird nicht wiederhergestellt.
-   Mit dem Beispielupgrade werden Verknüpfungen zu neuen Dateien und Features aktualisiert.

    [Planen eines größeren Upgrades](planning-a-major-upgrade.md)

    [Importieren der Ursprünglichen Installationsdatenbank](importing-original-installation-database.md)

    [Aktualisieren der Verzeichnisstruktur für ein Upgrade](updating-directory-structure-for-an-upgrade.md)

    [Aktualisieren von Dateien und Dateiattributen für ein Upgrade](updating-files-and-file-attributes-for-an-upgrade.md)

    [Aktualisieren von Komponenten für ein Upgrade](updating-components-for-an-upgrade.md)

    [Aktualisieren von Features für ein Upgrade](updating-features-for-an-upgrade.md)

    [Aktualisieren von Verknüpfungen für ein Upgrade](updating-shortcuts-for-an-upgrade.md)

    [Aktualisieren der Upgradetabelle für ein Upgrade](updating-upgrade-table-for-an-upgrade.md)

    [Aktualisieren von Eigenschaften für ein Upgrade](updating-properties-for-an-upgrade.md)

    [Aktualisieren von Sequenztabellen für ein Upgrade](updating-sequence-tables-for-an-upgrade.md)

    [Aktualisieren von Zusammenfassungsinformationen für ein Upgrade](updating-summary-information-for-an-upgrade.md)

    [Überprüfen eines Installationsupgrades](validating-an-installation-upgrade.md)

 

 



