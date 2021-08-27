---
description: Wenn ein Modul mehrere Sprachen unterstützt, können Sie es mehrmals in derselben Windows Installer-Datenbank zusammenführen, aber stellen Sie sicher, dass jeder Merge eine andere Sprache verwendet.
ms.assetid: 816b1f52-1ca2-4332-9a9b-462ea372c3bb
title: Mehrfaches Zusammenführen eines Moduls mit mehreren Sprachen mit demselben Paket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23a96f3830b2caa4069eddc69b0b68de1deff35d00c5b4fdb81d4d21d4355bd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129260"
---
# <a name="merging-a-multiple-language-module-into-the-same-package-multiple-times"></a>Mehrfaches Zusammenführen eines Moduls mit mehreren Sprachen mit demselben Paket

Wenn ein Modul mehrere Sprachen unterstützt, können Sie es mehrmals in derselben Windows Installer-Datenbank zusammenführen, aber stellen Sie sicher, dass jeder Merge eine andere Sprache verwendet. Fordern Sie vor jeder Zusammenführung eine andere Sprache vom Modul an. Die resultierende .msi Datenbank verfügt dann über einen Datensatz in der [Tabelle ModuleSignature](modulesignature-table.md) für jede Zusammenführung des Moduls. Komponenten, die von sprachen gemeinsam verwendet werden, sind nur einmal in der [Komponententabelle](component-table.md)vorhanden, sind jedoch jeder Sprache in der [ModuleComponents-Tabelle](modulecomponents-table.md)zugeordnet.

Wenn mehrere Sprachen eines Moduls in demselben Paket zusammengeführt werden, muss jede Zusammenführung die gleichen Einschränkungen auf Codepages erfüllen wie einzelsprachige Module. Die Module dürfen keine Zeichenfolgen in verschiedenen Codepages enthalten.

Wenn Sie ein Modul mehrmals in einer einzelnen .msi Datei zusammenführen, müssen Sie möglicherweise die Reihenfolge der Dateien in der [Dateitabelle](file-table.md) ändern, um die vorhandenen .cab aus dem Modul direkt in Ihrer Installation zu verwenden. Die Reihenfolge der Dateien in der Dateitabelle muss mit der Reihenfolge der Dateien im .cab übereinstimmen. Beim mehrmaligen Zusammenführen eines Moduls mit einer Installationsdatenbank kann die Sequenz geändert werden, da dateien, die von den Sprachen gemeinsam verwendet werden, möglicherweise bereits aus einer vorherigen Zusammenführung im Modul vorhanden sind und eine andere relative Sequenznummer aufweisen.

 

 



