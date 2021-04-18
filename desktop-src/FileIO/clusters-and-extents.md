---
description: 'Auf Cluster kann aus zwei unterschiedlichen Perspektiven verwiesen werden: innerhalb der Datei und auf dem Volume.'
ms.assetid: 8e999524-4fe9-49b0-8b59-081fa7a42c72
title: Cluster und Blöcke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6b379e0dbc4f70ccf001f0be0517e25c0c99a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358933"
---
# <a name="clusters-and-extents"></a>Cluster und Blöcke

Auf Cluster kann aus zwei unterschiedlichen Perspektiven verwiesen werden: innerhalb der Datei und auf dem Volume. Jeder Cluster in einer Datei verfügt über eine *Virtuelle Cluster Nummer* (VCN), bei der es sich um den relativen Offset vom Anfang der Datei handelt. Beispielsweise gibt eine Suche nach einer doppelten Größe eines Clusters, gefolgt von einem Lesevorgang, Daten ab der dritten VCN zurück. In einer *logischen Cluster Nummer* (LCN) wird der Offset eines Clusters von einem beliebigen Punkt innerhalb des Volumes beschrieben. Lcns sollte nur als Ordinalzahl oder relative Zahlen behandelt werden. Es gibt keine garantierte Zuordnung logischer Cluster zu physischen Festplatten Laufwerken.

Ein *Block ist eine* Zusammenführung zusammenhängender Cluster. Nehmen wir beispielsweise an, eine Datei, die aus 30 Clustern besteht, wird in zwei Blöcken aufgezeichnet. Der erste Block besteht möglicherweise aus fünf zusammenhängenden Clustern, den anderen verbleibenden 25 Clustern.

Es gibt keine Garantie für eine Beziehung auf dem Datenträger in einem beliebigen Bereich in einem anderen Block. Der erste Block kann beispielsweise eine höhere LCN als nachfolgende Werte aufweisen.

 

 



