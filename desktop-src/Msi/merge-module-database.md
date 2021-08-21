---
description: Die Datenbank eines Mergemoduls enthält alle Installationseigenschaften und die Setuplogik für das Modul.
ms.assetid: 72e42392-54e6-4be8-9a43-04158552be3d
title: Merge Module Database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb75614218e7464879f62ea1527245e36d65d1dc14f19a9b82a13a893997f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804602"
---
# <a name="merge-module-database"></a>Merge Module Database

Die Datenbank eines Mergemoduls enthält alle Installationseigenschaften und die Setuplogik für das Modul. Es handelt sich im Wesentlichen um eine vereinfachte [Installationsdatenbank](installer-database.md) oder .msi Datei. Standard-Mergemodul-Datenbankdateien werden durch eine MSM-Erweiterung angegeben. Eine Liste aller Datenbanktabellen, die in Mergemodulen vorhanden sein können, finden Sie unter [Merge Module Database Tables](merge-module-database-tables.md). Die folgenden Tabellen sind in der Datenbank jeder MSM-Datei erforderlich:

[Komponente](component-table.md)

[Verzeichnis](directory-table.md)

[FeatureComponents](featurecomponents-table.md)

[File](file-table.md)

[Modulesignature](modulesignature-table.md)

[ModuleComponents](modulecomponents-table.md)

Beachten Sie, dass die Tabellen Component, Directory, FeatureComponents und File auch in allen .msi-Dateien vorhanden sind. Eine Mergemoduldatenbank enthält keine [Featuretabelle,](feature-table.md) sodass die MSM-Datei nicht allein installiert werden kann. Um ein Mergemodul zu installieren, muss es zuerst mithilfe eines Mergetools in einer .msi-Datei zusammengeführt werden.

Die [Tabelle ModuleSignature](modulesignature-table.md) ist nur in .msi Dateien vorhanden, die mit mindestens einer MSM-Datei zusammengeführt wurden. Wenn diese Tabelle in einer .msi-Datei vorhanden ist, enthält sie einen Datensatz für jedes Mergemodul, das zuvor mit der Installationsdatenbank zusammengeführt wurde.

Mergemodule können optionale MergeModule Sequence-Tabellen enthalten. Diese Tabellen treten nur in MSM-Dateien auf. Wenn die MSM-Dateien in eine .msi Datei zusammengeführt werden, ändern diese Tabellen die [*Aktionssequenztabellen*](s-gly.md) der .msi Datei.

Mergemodule können benutzerdefinierte Tabellen enthalten. Diese Tabellen werden von [benutzerdefinierten Aktionen](custom-actions.md) verwendet, die im Mergemodul definiert sind.

Mergemodule erfordern selten Benutzeroberflächentabellen. Diese Tabellen müssen nur in seltenen Fällen vorhanden sein, in denen das Mergemodul während der Installation Eingaben vom Benutzer erfordert. Weitere Informationen finden Sie unter [Erstellen von Benutzeroberflächen in Mergemodulen.](authoring-user-interfaces-in-merge-modules.md)

 

 



