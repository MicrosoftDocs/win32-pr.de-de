---
description: Jede Datei, die vom Mergemodul an das Zielinstallationspaket übermittelt wird, muss in einer Schränkdatei gespeichert werden, die als Stream in der MSM-Datei eingebettet ist. Der Name dieser Schränkung ist immer MergeModule.CABinet.
ms.assetid: 884df249-977e-4e8e-8978-15331a7c1d8a
title: Generieren MergeModule.CABinet-Schränkdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 962cf46b95db1fe186878d23a7cc7fcd1b91d3b2d202a85741eee7ef1c2bc7e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649648"
---
# <a name="generating-mergemodulecabinet-cabinet-files"></a>Generieren MergeModule.CABinet-Schränkdateien

Jede Datei, die vom Mergemodul an das Zielinstallationspaket übermittelt wird, muss in einer Schränkdatei gespeichert werden, die als Stream in der MSM-Datei eingebettet ist. Der Name dieser Schränkung ist immer MergeModule.CABinet.

Die Namen der Dateien in MergeModule.CABinet müssen mit den Primärschlüsseln übereinstimmen, die in der [File-Tabelle](file-table.md) des Mergemoduls verwendet werden, und die unter Naming Primary Keys in Merge Module Databases beschriebene [Konvention einhalten.](naming-primary-keys-in-merge-module-databases.md)

Das Installationsprogramm überspringt zusätzliche Dateien, die in MergeModule.CABinet enthalten sind und nicht in der File-Tabelle des [Mergemoduls aufgeführt sind.](file-table.md) Die Sequenznummern von Dateien, die in der Tabelle File angegeben sind, müssen nicht aufeinander folgen, müssen jedoch der gleichen Reihenfolge folgen wie die dateien, die in MergeModule.CABgespeichert sind. Weitere Informationen finden Sie unter [Erstellen von Mergemodul-Dateitabellen.](authoring-merge-module-file-tables.md)

Dies bedeutet, dass eine einzelne Schränkdatei alle Dateien enthalten kann, die für ein Mergemodul zur Unterstützung mehrerer Sprachen erforderlich sind. Alle Sprachdateien können eindeutige Sequenznummern im Schränk erhalten. Anschließend kann eine Sprachtransformation zum Hinzufügen oder Entfernen von Dateien aus der Tabelle Datei verwendet werden, um ein Mergemodul für eine bestimmte Sprache zu erhalten. Weitere Informationen finden Sie unter [Erstellen mehrerer Sprachzusammenführungsmodule.](authoring-multiple-language-merge-modules.md)

MergeModule.CABinet kann dem Mergemodul hinzugefügt werden, indem eine temporäre Tabelle [ \_ Streams wird.](-streams-table.md) Beispielsweise kann das tool-Msidb.exe, das mit dem Windows Installer SDK bereitgestellt wird, verwendet werden, um das MergeModule.CABinet dem Mergemodul hinzuzufügen. Weitere Informationen finden Sie unter [Including a Cabinet File in an Installation](including-a-cabinet-file-in-an-installation.md).

 

 



