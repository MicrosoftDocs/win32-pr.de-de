---
description: In den folgenden Abschnitten finden Sie ein Beispiel für die Erstellung eines upgradepakets für die Anwendung, die in einem Installations Beispiel beschrieben wird.
ms.assetid: 233302ea-abc3-4879-b868-425f2b10e02e
title: Ein upgradebeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1e19173a98f3ddee49c19d0ec10aca7994e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362425"
---
# <a name="an-upgrade-example"></a>Ein upgradebeispiel

In den folgenden Abschnitten finden Sie ein Beispiel für die Erstellung eines upgradepakets für die Anwendung, die in [einem Installations Beispiel](an-installation-example.md)beschrieben wird. Ein Beispiel für eine minimale Benutzeroberfläche für dieses Beispiel wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md) als Datei Uisample.msi bereitgestellt. Wenn Sie über das SDK verfügen, haben Sie Zugriff auf alle Tools und Daten, die für die Reproduktion des Beispiel Installationspakets, der Benutzeroberfläche und des beispielupgradepakets erforderlich sind.

In diesem Beispiel wird veranschaulicht, wie ein Windows Installer Paket erstellt wird, das das hypothetische Product MNP2000 auf ein neues Produkt mit dem Namen MNP2001 aktualisiert. Das Upgradepaket für das Beispiel wendet ein großes Upgrade auf das Produkt an, das das Ändern des Produktcodes erfordert. Weitere Informationen zu größeren Upgrades finden Sie im Thema zu den [wichtigsten Upgrades](major-upgrades.md) im Abschnitt " [Patching und Upgrades](patching-and-upgrades.md) ".

Das Beispiel Aktualisierungs Paket verfügt über die folgenden Spezifikationen:

-   Um dieses Upgrade auf MNP2001 zu qualifizieren, muss ein Benutzer die Versionen 1,0 bis 1,4 (einschließlich) der englischen Sprache MNP2000 mit Windows Installer installiert haben.
-   Wenn ein Benutzer versucht, das Upgradepaket zu installieren, durchsucht die upgradefunktion von Windows Installer den Computer des Benutzers nach allen Produkten, die für das Upgrade qualifiziert sind.
-   Windows Installer migriert alle der Funktionseinstellungen des ursprünglichen Produkts zu dem aktualisierten Produkt.
-   Das Installationsprogramm entfernt alle veralteten Features vom Computer des Benutzers.
-   Das Installationsprogramm installiert alle neuen Features, die zum Upgrade gehören.
-   Durch eine Deinstallation des upgradepakets wird das Produkt auf dem Computer des Benutzers entfernt, und die frühere Version des Produkts wird nicht wieder hergestellt.
-   Das Beispiel Upgrade aktualisiert Verknüpfungen zu neuen Dateien und Features.

    [Planen eines größeren Upgrades](planning-a-major-upgrade.md)

    [Importieren der ursprünglichen Installations Datenbank](importing-original-installation-database.md)

    [Aktualisieren der Verzeichnisstruktur für ein Upgrade](updating-directory-structure-for-an-upgrade.md)

    [Aktualisieren von Dateien und Dateiattributen für ein Upgrade](updating-files-and-file-attributes-for-an-upgrade.md)

    [Aktualisieren von Komponenten für ein Upgrade](updating-components-for-an-upgrade.md)

    [Aktualisieren von Features für ein Upgrade](updating-features-for-an-upgrade.md)

    [Aktualisieren von Verknüpfungen für ein Upgrade](updating-shortcuts-for-an-upgrade.md)

    [Aktualisieren der upgradetabelle für ein Upgrade](updating-upgrade-table-for-an-upgrade.md)

    [Aktualisieren von Eigenschaften für ein Upgrade](updating-properties-for-an-upgrade.md)

    [Aktualisieren von Sequenz Tabellen für ein Upgrade](updating-sequence-tables-for-an-upgrade.md)

    [Aktualisieren von Zusammenfassungs Informationen für ein Upgrade](updating-summary-information-for-an-upgrade.md)

    [Überprüfen eines Installations Upgrades](validating-an-installation-upgrade.md)

 

 



