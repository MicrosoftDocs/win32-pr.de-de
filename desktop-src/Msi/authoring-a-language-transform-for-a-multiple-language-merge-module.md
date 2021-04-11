---
description: Wenn ein Modul in einer-Datenbank mit einer anderen Standardsprache zusammengeführt wird, muss das Mergetool möglicherweise eine sprach Transformation auf das Modul anwenden, um die endgültige Sprache bereitzustellen. Weitere Informationen finden Sie unter mehrere sprachmergemodule.
ms.assetid: 51e8774e-f358-423f-a283-ad7beeabbbdb
title: Erstellen einer sprach Transformation für ein Mergemodul mit mehreren Sprachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970c8908ddbf89e31f0fc7a415358bb887f0838e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215713"
---
# <a name="authoring-a-language-transform-for-a-multiple-language-merge-module"></a>Erstellen einer sprach Transformation für ein Mergemodul mit mehreren Sprachen

Wenn ein Modul in einer-Datenbank mit einer anderen Standardsprache zusammengeführt wird, muss das Mergetool möglicherweise eine sprach Transformation auf das Modul anwenden, um die endgültige Sprache bereitzustellen. Weitere Informationen finden Sie unter [mehrere sprachmergemodule](multiple-language-merge-modules.md).

Die sprach Transformationen werden in der MSM-Datei des Moduls gespeichert und müssen den Namen und das Format aufweisen: Mergemodule. lang \# \# \# \# . \# \# \# \# Stellt die bis zu vierstellige [LangID](localizing-the-error-and-actiontext-tables.md) der endgültigen Sprache dar. Beispiel: Mergemodule. Lang1033, Mergemodule. Lang9 und Mergemodule. Lang0 für Transformationen in Englisch, Deutsch, Englisch und sprachneutral. Diese sind identisch mit [eingebetteten Transformationen](embedded-transforms.md) , und Sie können Sie unter Speicher in der MSM-Datei hinzufügen.

Die sprach Transformation sollte folgende Aktionen ausführen:

-   Ändern Sie die Standardsprache in der Spalte Sprache der [Tabelle ModuleSignature](modulesignature-table.md) in die neue Sprache des Moduls.
-   Ändern Sie die Standardsprache in der Spalte Sprache der [Tabelle modulecomponents](modulecomponents-table.md) in die neue Sprache des Moduls. Die Transformation kann Zeilen aus dieser Tabelle hinzufügen oder daraus entfernen.
-   Ändern Sie ggf. die Sprache in der Spalte "Requirements-language", oder fügen Sie der [Tabelle "moduledepend](moduledependency-table.md)" Zeilen hinzu, oder löschen Sie Sie.
-   Ändern Sie ggf. die Sprache in der Spalte "excludlanguage", oder fügen Sie der Tabelle " [moduleausschluss](moduleexclusion-table.md)" Zeilen hinzu, oder löschen Sie Sie.
-   Die Transformation kann beliebige gültige Transformations Vorgänge für das Modul ausführen, einschließlich hinzufügen oder Entfernen von Komponenten, Dateien, Registrierungs Einträgen oder Aktionen.

Beachten Sie, dass durch das Anwenden einer sprach Transformation beim Öffnen des Moduls die Standardsprache oder die vom Modul unterstützten Sprachen nicht geändert werden, sondern nur die angeforderte Sprache geändert wird. Daher ändert sich die [**Vorlagen Zusammenfassungs**](template-summary.md) Eigenschaft nicht, Sie sollte bereits alle vom Modul unterstützten Sprachen mit der Standardsprache auflisten, die zuerst aufgeführt wird.

Alle Dateien, die von allen möglichen sprach Transformationen benötigt werden, werden im Allgemeinen in einer einzelnen CAB-Datei gespeichert, die im Modul enthalten ist. Da es nicht praktikabel ist, dass die sprach Transformation diese CAB-Datei ändert, empfiehlt es sich, eine globale Datei Sequenz in der CAB-Datei, der [Dateitabelle](file-table.md)und der sprach Transformation zu verwenden. Weitere Informationen finden Sie unter [Anordnen der Datei Sequenz im CAB eines Moduls mit mehreren Sprachen](ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module.md) .

 

 



