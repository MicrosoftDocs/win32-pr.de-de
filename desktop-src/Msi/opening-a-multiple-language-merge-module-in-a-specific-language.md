---
description: Beim Zusammenführen eines Moduls in einer Installationsdatenbank gibt es zwei wichtige Sprachen.
ms.assetid: e815854f-a379-497a-ae37-b13de39dd516
title: Öffnen eines Multiple-Language Mergemoduls in einer bestimmten Sprache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc4dd46009f0cbe4f8c0f2cfd8b4f5dcd2caf91c7987ece7b3b032f61d9161ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942871"
---
# <a name="opening-a-multiple-language-merge-module-in-a-specific-language"></a>Öffnen eines Multiple-Language Mergemoduls in einer bestimmten Sprache

Beim Zusammenführen eines Moduls in einer Installationsdatenbank gibt es zwei wichtige Sprachen. Die erste ist die Sprache des Zielinstallationspakets, das von [**ProductLanguage**](productlanguage.md) in der [Eigenschaftentabelle angegeben wird.](property-table.md) Die zweite ist die Sprache des Mergemoduls, das in der Spalte Sprache der [ModuleSignature-Tabelle angezeigt wird.](modulesignature-table.md)

Die Sprache des Installationspakets kann vom Mergetool an das Modul übergeben werden, wenn das Paket für einen Merge geöffnet wird. Manchmal kann es jedoch erforderlich sein, die Sprache des Ziels zu ignorieren und an fordern, dass das Modul in einer anderen Sprache geöffnet wird, z. B. in einem englischen Paket, das sowohl die englischen als auch die deutschen Ressourcen aus dem Modul installiert.

Beim Öffnen eines Moduls mit einer Sprachanforderung überprüft das Mergetool die angeforderte Sprache mit den Sprachen, die in der Spalte Sprache der [ModuleSignature-Tabelle angegeben sind.](modulesignature-table.md)

Der folgende Prozess wird verwendet, um zu bestimmen, welche Sprache verwendet werden soll.

**So bestimmen Sie, welche Sprache verwendet werden soll**

1.  Wenn die Sprache in der [ModuleSignature-Tabelle](modulesignature-table.md) gleich oder allgemeiner als die angeforderte Sprache ist, wird das Modul geöffnet.
2.  Wenn das Modul die genaue angeforderte Sprache unterstützt, wird diese Sprache verwendet.
3.  Wenn das Modul die Sprachgruppe der von dieser Sprachgruppe angeforderten Sprache unterstützt, überprüfen Sie beispielsweise 9, ob 1033 angefordert, aber in Schritt 2 nicht gefunden wurde.
4.  Überprüfen Sie, ob es eine Sprachtransformation gibt, die das Modul in neutral ändert.
5.  Wenn keiner der vorherigen Schritte erfolgreich ist, unterstützt das Modul die angeforderte Sprache nicht, und die Zusammenführung schlägt fehl.

 

 



