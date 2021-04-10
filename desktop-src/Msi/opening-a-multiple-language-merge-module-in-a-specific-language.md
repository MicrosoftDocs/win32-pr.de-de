---
description: Wenn Sie ein Modul in eine Installations Datenbank zusammenführen, gibt es zwei wichtige Sprachen.
ms.assetid: e815854f-a379-497a-ae37-b13de39dd516
title: Öffnen eines Multiple-Language Merge-Moduls in einer bestimmten Sprache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b552c41d7696b29a86987d027e00ef4cb19bbb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041868"
---
# <a name="opening-a-multiple-language-merge-module-in-a-specific-language"></a>Öffnen eines Multiple-Language Merge-Moduls in einer bestimmten Sprache

Wenn Sie ein Modul in eine Installations Datenbank zusammenführen, gibt es zwei wichtige Sprachen. Die erste ist die Sprache des Ziel Installationspakets, das von [**productlanguage**](productlanguage.md) in der [Eigenschaften Tabelle](property-table.md)angegeben wird. Die zweite ist die Sprache des Mergemoduls, das in der Spalte Sprache der [Tabelle ModuleSignature](modulesignature-table.md)angezeigt wird.

Die Sprache des Installationspakets kann vom Mergetool an das Modul übermittelt werden, wenn das Paket für einen Mergevorgang geöffnet wird. Manchmal kann es jedoch notwendig sein, die Sprache des Ziels zu ignorieren und anzufordern, dass das Modul in einer anderen Sprache geöffnet werden soll, z. b. in einem englischen Paket, das sowohl die englischen als auch die deutschen Ressourcen aus dem Modul installiert.

Beim Öffnen eines Moduls mit einer sprach Anforderung überprüft das Mergetool die angeforderte Sprache auf die Sprachen, die in der Spalte Sprache der [Tabelle ModuleSignature](modulesignature-table.md)angegeben sind.

Der folgende Prozess wird verwendet, um zu bestimmen, welche Sprache verwendet werden soll.

**So bestimmen Sie die zu verwendende Sprache**

1.  Wenn die Sprache in der [ModuleSignature-Tabelle](modulesignature-table.md) gleich oder allgemeiner als die angeforderte Sprache ist, wird das Modul geöffnet.
2.  Wenn das Modul die angeforderte Sprache genau unterstützt, wird diese Sprache verwendet.
3.  Wenn das Modul die Sprachgruppe der angeforderten Sprache unterstützt, beispielsweise 9, wenn 1033 angefordert wurde, aber in Schritt 2 nicht gefunden wurde.
4.  Überprüfen Sie, ob eine sprach Transformation vorhanden ist, durch die das Modul in neutral geändert wird.
5.  Wenn keiner der vorherigen Schritte erfolgreich ausgeführt wurde, wird die angeforderte Sprache vom Modul nicht unterstützt, und die Zusammenführung schlägt fehl.

 

 



