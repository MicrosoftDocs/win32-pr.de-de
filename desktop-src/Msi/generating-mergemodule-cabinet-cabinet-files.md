---
description: Jede Datei, die vom Mergemodul an das Ziel Installationspaket übermittelt wird, muss in einer CAB-Datei gespeichert werden, die als Stream in der MSM-Datei eingebettet ist. Der Name dieses CAB ist immer MergeModule.CABinet.
ms.assetid: 884df249-977e-4e8e-8978-15331a7c1d8a
title: Erstellen von MergeModule.CABinet-CAB-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a26eb9bb3daf92d81e21267b2f56706b74d9179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360650"
---
# <a name="generating-mergemodulecabinet-cabinet-files"></a>Erstellen von MergeModule.CABinet-CAB-Dateien

Jede Datei, die vom Mergemodul an das Ziel Installationspaket übermittelt wird, muss in einer CAB-Datei gespeichert werden, die als Stream in der MSM-Datei eingebettet ist. Der Name dieses CAB ist immer MergeModule.CABinet.

Die Namen der Dateien in MergeModule.CABinet müssen mit den primär Schlüsseln übereinstimmen, die in der [Dateitabelle](file-table.md) des Mergemoduls verwendet werden, und müssen der in [Benennen von primär Schlüsseln in mergemoduldatenbanken](naming-primary-keys-in-merge-module-databases.md)beschriebenen Konvention entsprechen.

Das Installationsprogramm überspringt zusätzliche Dateien, die in MergeModule.CABinet enthalten sind und nicht in der [Dateitabelle](file-table.md)des Mergemoduls aufgeführt sind. Die Sequenznummern von Dateien, die in der Dateitabelle angegeben sind, müssen nicht aufeinander folgen, aber Sie müssen derselben Reihenfolge wie die in MergeModule.CABinet gespeicherten Dateien entsprechen. Weitere Informationen finden Sie unter [Erstellen von Mergemodul-Datei Tabellen](authoring-merge-module-file-tables.md).

Dies bedeutet, dass eine einzelne CAB-Datei alle Dateien enthalten kann, die für ein Mergemodul erforderlich sind, um mehrere Sprachen zu unterstützen. Allen Sprachdateien können eindeutige Sequenznummern in der CAB-Datei zugewiesen werden. Anschließend kann eine sprach Transformation verwendet werden, um Dateien aus der Dateitabelle hinzuzufügen oder zu entfernen, um ein Mergemodul für eine bestimmte Sprache zu erhalten. Weitere Informationen finden Sie unter [Erstellen mehrerer sprachmergemodule](authoring-multiple-language-merge-modules.md).

MergeModule.CABinet kann dem Mergemodul hinzugefügt werden, indem eine temporäre [ \_ Streams-Tabelle](-streams-table.md)geöffnet wird. Beispielsweise kann das mit dem Windows Installer SDK bereitgestellte Tool Msidb.exe verwendet werden, um dem Mergemodul den MergeModule.CABinet hinzuzufügen. Weitere Informationen finden Sie unter [Einschließen einer CAB-Datei in eine-Installation](including-a-cabinet-file-in-an-installation.md).

 

 



