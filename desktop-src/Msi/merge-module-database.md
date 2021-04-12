---
description: Die Datenbank eines Mergemoduls enthält alle Installations Eigenschaften und die Setup Logik für das Modul.
ms.assetid: 72e42392-54e6-4be8-9a43-04158552be3d
title: Modul Datenbank zusammenführen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74158e38d10b302c28520f6c1736e9cc6d823641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347158"
---
# <a name="merge-module-database"></a>Modul Datenbank zusammenführen

Die Datenbank eines Mergemoduls enthält alle Installations Eigenschaften und die Setup Logik für das Modul. Es handelt sich im Wesentlichen um eine vereinfachte [Installer-Datenbank](installer-database.md) oder MSI-Datei. Standard mäßige Mergemodul-Datenbankdateien werden durch eine MSM-Erweiterung angegeben. Eine Liste aller Datenbanktabellen, die in Mergemodulen vorhanden sein können, finden Sie unter [Merge Module Database Tables](merge-module-database-tables.md). Die folgenden Tabellen sind in der-Datenbank jeder MSM-Datei erforderlich:

[Komponente](component-table.md)

[Verzeichnis](directory-table.md)

[FeatureComponents](featurecomponents-table.md)

[File](file-table.md)

[ModuleSignature](modulesignature-table.md)

[Modulecomponents](modulecomponents-table.md)

Beachten Sie, dass die Komponenten "Component", "Directory", "FeatureComponents" und "file" auch in allen MSI-Dateien vorhanden sind. Eine mergemoduldatenbank enthält keine [Featuretabelle](feature-table.md) , sodass die MSM-Datei nicht allein installiert werden kann. Zum Installieren eines Mergemoduls muss es zuerst mithilfe eines Merge-Tools in einer MSI-Datei zusammengeführt werden.

Die [ModuleSignature-Tabelle](modulesignature-table.md) ist nur in MSI-Dateien vorhanden, die mit mindestens einer MSM-Datei zusammengeführt wurden. Wenn diese Tabelle in einer MSI-Datei vorhanden ist, enthält Sie einen Datensatz für jedes Mergemodul, das zuvor in der Installations Datenbank zusammengeführt wurde.

Mergemodule können optionale Mergemodule-Sequenz Tabellen enthalten. Diese Tabellen treten nur in MSM-Dateien auf. Wenn die MSM-Dateien in einer MSI-Datei zusammengeführt werden, ändern diese Tabellen die Aktions [*Sequenz Tabellen*](s-gly.md) der MSI-Datei.

Mergemodule können benutzerdefinierte Tabellen enthalten. Diese Tabellen werden von [benutzerdefinierten Aktionen](custom-actions.md) verwendet, die im Mergemodul definiert sind.

Mergemodule erfordern selten Benutzeroberflächen Tabellen. Diese Tabellen müssen nur in seltenen Fällen vorhanden sein, in denen das Mergemodul während der Installation Eingaben vom Benutzer erfordert. Weitere Informationen finden Sie unter [Erstellen von Benutzeroberflächen in Mergemodulen](authoring-user-interfaces-in-merge-modules.md).

 

 



