---
description: Mehrere Sprachmodule können Komponenten mit mehreren verschiedenen Sprachen als einzelne Verbunddatei bereitstellen.
ms.assetid: b3a0b635-49c7-4f95-b31f-6c8688466dd2
title: Mehrere Sprachzusammenführungsmodule
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17f32d219e1071cd431117919d3eb3f3361d30213f59a26f9ec2cdf2e81e591b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943421"
---
# <a name="multiple-language-merge-modules"></a>Mehrere Sprachzusammenführungsmodule

Mehrere Sprachmodule können Komponenten mit mehreren verschiedenen Sprachen als einzelne Verbunddatei bereitstellen. Der Entwurf und die Funktionalität mehrerer Sprachzusammenführungsmodule ähneln Den einzelnen Sprachmodulen. Ein Mergemodul mit mehreren Sprachen verfügt über mehrere Sprachen, die in der [**Vorlagenzusammenfassungseigenschaft**](template-summary.md) aufgeführt sind. Die Datenbank eines Mergemoduls mit mehreren Sprachen enthält alle Setupinformationen für mehrere Sprachen. Das MergeModule.CABInet-Schränk in einem Modul zum Zusammenführen mehrerer Sprachen enthält alle Dateien für alle unterstützten Sprachen.

Wenn Sie eine MSM-Datei mit mehreren Sprachen auf eine .msi Datei anwenden, müssen Sie nach der Zusammenführung die endgültige Sprache des Installationspakets angeben. Im Fall eines Mergemoduls in einer einzelnen Sprache listet die [Dateitabelle](file-table.md) des Mergemoduls jede Datei auf, die im MergeModule.CABinet-Schränke vorhanden ist. Bei einem Mergemodul mit mehreren Sprachen enthält MergeModule.CABinet alle Dateien für jede vom Modul unterstützte Sprache, aber nur die Teilmenge der Dateien für die endgültige Sprache wird in die Dateitabelle des Moduls aufgenommen. Das Mergetool muss sicherstellen, dass das Modul die Teilmenge der Informationen und Dateien bereitstellt, die für die angeforderte endgültige Sprache erforderlich sind.

Jedes Mergemodul verfügt über eine Standardsprache, die in der Spalte Sprache der [Tabelle ModuleSignature](modulesignature-table.md)angegeben ist. Die Standardsprache eines Mergemoduls wird auch als erste oder einzige Sprache in der [**Vorlagenzusammenfassungseigenschaft**](template-summary.md) angezeigt. Abhängig von der angeforderten endgültigen Sprache und der Standardsprache des Moduls kann das Mergetool Sprachtransformationen auf ein Modul mit mehreren Sprachzusammenführungen anwenden, sodass es in der angeforderten Sprache oder einer Näherung der angeforderten Sprache geöffnet werden kann. Die Sprachtransformationen werden in das Mergemodul eingebettet. Mergetools müssen Sprachtransformationen unter Einhaltung der folgenden allgemeinen Regeln anwenden:

-   Wenn die Standard- und endgültigen Sprachen identisch sind, kann das Modul ohne Sprachtransformationen zusammengeführt werden.
-   Wenn die Standardsprache 0 (ein sprachneutrales Modul) ist, kann das Modul ohne Sprachtransformationen zusammengeführt werden.
-   Wenn die endgültige Sprache nicht die Standardsprache ist, muss das Mergetool eine der im Modul eingebetteten Sprachtransformationen anwenden, um das Modul in die endgültige Sprache oder eine Näherung der endgültigen Sprache zu ändern.

Beispielsweise sind keine Sprachtransformationen erforderlich, wenn die endgültige Sprache 1033 (US-Englisch) und die Standardsprache des Moduls 1033 (US-Englisch), 0 (sprachneutral) oder 9 (generisches Englisch) ist.

Sprachtransformationen sind erforderlich, wenn die endgültige Sprache 1033 (US-Englisch) und die Standardsprache 1031 (Deutsch) ist. In diesem Fall kann das Mergetool zunächst das Modul für mehrere Sprachen nach einer eingebetteten Sprachtransformation in 1033 (US-Englisch) durchsuchen. Wenn dies nicht erfolgreich ist, kann nach einer Transformation in eine Sprache mit einer übereinstimmenden primären LANGID gesucht werden, auch wenn die sekundäre LANGID nicht übereinstimmt. Wenn das Tool z. B. keine Transformation in 1033 (Englisch in den USA) finden kann, sucht es nach einer Transformation in 9 (generisches Englisch). Wenn dies fehlschlägt, sucht das Mergetool nach einer Transformation in 0 (sprachneutral). Wenn all diese Suchvorgänge nach einer geeigneten Transformation fehlschlagen, kann das Modul nicht geöffnet werden.

Weitere Informationen finden Sie unter [Erstellen mehrerer Sprachzusammenführungsmodule.](authoring-multiple-language-merge-modules.md)

 

 



