---
description: Wenn ein Modul in einer Datenbank zusammengeführt wird, die über eine andere Standardsprache verfügt, muss das Mergetool möglicherweise eine Sprachtransformation auf das Modul anwenden, um die endgültige Sprache bereitstellen zu können. Weitere Informationen finden Sie unter Multiple Language Merge Modules.
ms.assetid: 51e8774e-f358-423f-a283-ad7beeabbbdb
title: Erstellen einer Sprachtransformation für ein Mergemodul für mehrere Sprachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf9a9c2294d310959bcd82f13010c88eb513e40ad4536c4dbca61e50d260873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078060"
---
# <a name="authoring-a-language-transform-for-a-multiple-language-merge-module"></a>Erstellen einer Sprachtransformation für ein Mergemodul für mehrere Sprachen

Wenn ein Modul in einer Datenbank zusammengeführt wird, die über eine andere Standardsprache verfügt, muss das Mergetool möglicherweise eine Sprachtransformation auf das Modul anwenden, um die endgültige Sprache bereitstellen zu können. Weitere Informationen finden Sie unter [Multiple Language Merge Modules](multiple-language-merge-modules.md).

Die Sprachtransformationen werden in der MSM-Datei des Moduls gespeichert und müssen den Namen und das Format Haben: MergeModule.Lang \# \# \# \# . Stellt \# \# \# \# die bis zu vierstellige [LANGID](localizing-the-error-and-actiontext-tables.md) der endgültigen Sprache dar. Beispiel: MergeModule.Lang1033, MergeModule.Lang9 und MergeModule.Lang0 für Transformationen in US-Englisch, Englisch (Weltweit) und sprachneutral. Diese sind identisch mit [eingebetteten Transformationen,](embedded-transforms.md) und Sie können sie substorages in der MSM-Datei hinzufügen.

Die Sprachtransformation sollte Folgendes tun:

-   Ändern Sie die Standardsprache in der Spalte Sprache der [Tabelle ModuleSignature](modulesignature-table.md) in die neue Sprache des Moduls.
-   Ändern Sie die Standardsprache in der Spalte Sprache der [Tabelle ModuleComponents](modulecomponents-table.md) in die neue Sprache des Moduls. Die Transformation kann Zeilen zu dieser Tabelle hinzufügen oder daraus entfernen.
-   Ändern Sie bei Bedarf die Sprache in der Spalte RequiredLanguage, oder fügen Sie der [ModuleDependency-Tabelle Zeilen hinzu, oder löschen Sie sie.](moduledependency-table.md)
-   Ändern Sie bei Bedarf die Sprache in der Spalte ExcludedLanguage, oder fügen Sie der [ModuleExclusion-Tabelle Zeilen hinzu, oder löschen Sie sie.](moduleexclusion-table.md)
-   Die Transformation kann alle gültigen Transformationsvorgänge für das Modul ausführen, einschließlich des Hinzufügens oder Entfernens von Komponenten, Dateien, Registrierungseinträgen oder Aktionen.

Beachten Sie, dass das Anwenden einer Sprachtransformation beim Öffnen des Moduls nicht die Standardsprache oder die vom Modul unterstützten Sprachen ändert, sondern nur die Sprache ändert, die angefordert wird. Daher ändert [**sich die Eigenschaft**](template-summary.md) Vorlagenzusammenfassung nicht. Sie sollte bereits alle sprachen auflisten, die vom Modul mit der zuerst aufgeführten Standardsprache unterstützt werden.

Alle Dateien, die von allen möglichen Sprachtransformationen benötigt werden, werden in der Regel in einer einzelnen im Modul enthaltenen Datei gespeichert. Da es nicht praktikabel [ist,](file-table.md)diese Schränkdatei durch die Sprachtransformation zu ändern, ist es am besten, eine globale Dateisequenz in der Schränkdatei, der Dateitabelle und der Sprachtransformation zu verwenden. Weitere Informationen finden Sie unter Ordering the File Sequence in the CAB of a Multiple Language Merge Module (Reihenfolge der Dateisequenz in der [CAB eines Multiple Language Merge-Moduls).](ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module.md)

 

 



