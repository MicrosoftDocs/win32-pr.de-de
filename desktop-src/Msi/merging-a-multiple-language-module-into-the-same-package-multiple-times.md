---
description: Wenn ein Modul mehrere Sprachen unterstützt, können Sie es mehrmals in dieselbe Windows Installer Datenbank zusammenführen, aber stellen Sie sicher, dass für jede Zusammenführung eine andere Sprache verwendet wird.
ms.assetid: 816b1f52-1ca2-4332-9a9b-462ea372c3bb
title: Mehrmals Zusammenführen eines Moduls mit mehreren Sprachen in demselben Paket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52552a68643d52c6aad97ed666b7dc1ae4043fd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363286"
---
# <a name="merging-a-multiple-language-module-into-the-same-package-multiple-times"></a>Mehrmals Zusammenführen eines Moduls mit mehreren Sprachen in demselben Paket

Wenn ein Modul mehrere Sprachen unterstützt, können Sie es mehrmals in dieselbe Windows Installer Datenbank zusammenführen, aber stellen Sie sicher, dass für jede Zusammenführung eine andere Sprache verwendet wird. Fordern Sie vor jeder Zusammenführung eine andere Sprache vom Modul an. Die resultierende MSI-Datenbank hat dann einen Datensatz in der [Tabelle ModuleSignature](modulesignature-table.md) für jede Zusammenführung des Moduls. Komponenten, die von Sprachen gemeinsam genutzt werden, sind nur einmal in der [Component-Tabelle](component-table.md)vorhanden, sind aber jeder Sprache in der [modulecomponents-Tabelle](modulecomponents-table.md)zugeordnet.

Wenn Sie mehrere Sprachen eines Moduls in dasselbe Paket zusammenführen, muss jede Zusammenführung dieselben Einschränkungen für Codepages wie einzelne Sprachmodule erfüllen. Die Module können keine Zeichen folgen in unterschiedlichen Codepages enthalten.

Wenn Sie ein Modul mehrmals in eine MSI-Datei zusammenführen, müssen Sie ggf. die Reihenfolge der Dateien in der [Dateitabelle](file-table.md) so ändern, dass die vorhandene CAB-Datei direkt in der Installation von dem Modul verwendet wird. Die Reihenfolge der Dateien in der Dateitabelle muss mit der Reihenfolge der Dateien in der CAB-Datei identisch sein. Wenn Sie ein Modul mehrmals in eine Installations Datenbank zusammenführen, kann die Sequenz geändert werden, da Dateien, die von den Sprachen gemeinsam genutzt werden, möglicherweise bereits aus einer vorherigen Zusammenführung im Modul vorhanden sind und eine andere relative Sequenznummer aufweisen.

 

 



