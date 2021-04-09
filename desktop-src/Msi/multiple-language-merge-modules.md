---
description: Mehrere Sprachmodule können Komponenten mit verschiedenen Sprachen als einzelne Verbund Datei bereitstellen.
ms.assetid: b3a0b635-49c7-4f95-b31f-6c8688466dd2
title: Mehrere Language Merge-Module
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d414cce484022bf81647110ac032d0db270d383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959388"
---
# <a name="multiple-language-merge-modules"></a>Mehrere Language Merge-Module

Mehrere Sprachmodule können Komponenten mit verschiedenen Sprachen als einzelne Verbund Datei bereitstellen. Der Entwurf und die Funktionalität mehrerer sprachmergemodule ähneln einzelnen Sprachmodulen. Ein Mergemodul für mehrere Sprachen verfügt über mehr als eine Sprache, die in der [**Vorlagen Zusammenfassungs**](template-summary.md) Eigenschaft aufgeführt ist. Die Datenbank eines Mergemoduls mit mehreren Sprachen enthält alle Setup Informationen für mehrere Sprachen. Der MergeModule.CABinet-CAB innerhalb eines Mergemoduls mit mehreren Sprachen enthält alle Dateien für alle unterstützten Sprachen.

Wenn Sie eine MSM-Datei mit mehreren Sprachen auf eine MSI-Datei anwenden, müssen Sie nach dem Merge die endgültige Sprache des Installationspakets angeben. Im Fall eines Moduls mit einer einzelnen Sprache führt die [Dateitabelle](file-table.md) des Merge-Moduls alle Dateien auf, die in der MergeModule.CABinet-CAB-Datei vorhanden sind. Bei einem Mergemodul mit mehreren Sprachen enthält MergeModule.CABinet alle Dateien für jede Sprache, die vom Modul unterstützt wird, aber nur die Teilmenge der Dateien für die endgültige Sprache wird in die Dateitabelle des Moduls geleitet. Das Merge-Tool muss sicherstellen, dass das Modul die Teilmenge der für die angeforderte endgültige Sprache erforderlichen Informationen und Dateien bereitstellt.

Jedes Mergemodul verfügt über eine Standardsprache, die in der Language-Spalte der [ModuleSignature-Tabelle](modulesignature-table.md)angegeben ist. Die Standardsprache eines Mergemoduls wird auch als erste oder einzige Sprache in der [**Template Summary**](template-summary.md) -Eigenschaft angezeigt. Abhängig von der angeforderten endgültigen Sprache und der Standardsprache des Moduls kann das Mergetool sprach Transformationen auf ein Modul mit mehreren Sprachen anwenden, sodass es in der angeforderten Sprache oder in einer Näherung der angeforderten Sprache geöffnet werden kann. Die sprach Transformationen sind innerhalb des Mergemoduls eingebettet. In den Merge-Tools müssen sprach Transformationen gemäß den folgenden allgemeinen Regeln angewendet werden:

-   Wenn die Standard-und die endgültige Sprache identisch sind, kann das Modul ohne sprach Transformationen zusammengeführt werden.
-   Wenn die Standardsprache 0 (ein sprach neutrales Modul) ist, kann das Modul ohne sprach Transformationen zusammengeführt werden.
-   Wenn die endgültige Sprache nicht die Standardsprache ist, muss das Merge-Tool eine der in das Modul eingebetteten sprach Transformationen anwenden, um das Modul in die endgültige Sprache oder eine Näherung der endgültigen Sprache zu ändern.

Beispielsweise sind keine sprach Transformationen erforderlich, wenn die endgültige Sprache 1033 (US-Englisch) ist und die Standardsprache des Moduls 1033 (US-Englisch), 0 (Sprachneutral) oder 9 (generisches Englisch) ist.

Sprach Transformationen sind erforderlich, wenn die endgültige Sprache 1033 (US-Englisch) und die Standardsprache 1031 (Deutsch) ist. In diesem Fall kann das Mergetool zuerst das Modul Multiple Language für eine eingebettete sprach Transformation in 1033 (US-Englisch) durchsuchen. Wenn dies fehlschlägt, wird möglicherweise eine Transformation in eine Sprache mit einer entsprechenden primären langid durchsucht, auch wenn die sekundäre langid nicht übereinstimmt. Wenn das Tool z. b. eine Transformation in 1033 (US-Englisch) nicht finden kann, sucht es nach einer Transformation in 9 (generisches Englisch). Wenn dies nicht gelingt, sucht das Merge-Tool nach einer Transformation in 0 (Sprachneutral). Wenn alle diese Suchvorgänge nach einer passenden Transformation fehlschlagen, kann das Modul nicht geöffnet werden.

Weitere Informationen finden Sie unter [Erstellen mehrerer sprachmergemodule](authoring-multiple-language-merge-modules.md).

 

 



