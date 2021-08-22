---
description: 'Auf Cluster kann aus zwei verschiedenen Perspektiven verwiesen werden: innerhalb der Datei und auf dem Volume.'
ms.assetid: 8e999524-4fe9-49b0-8b59-081fa7a42c72
title: Cluster und Blöcke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce987dc5c8afea842d6c92196474f88d17c36d2011995a2d760b83bfc1e5a644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119533840"
---
# <a name="clusters-and-extents"></a>Cluster und Blöcke

Auf Cluster kann aus zwei verschiedenen Perspektiven verwiesen werden: innerhalb der Datei und auf dem Volume. Jeder Cluster in einer Datei verfügt über eine *virtuelle Clusternummer (Virtual Cluster Number,* VCN), die den relativen Offset vom Anfang der Datei darstellt. Wenn beispielsweise versucht wird, die doppelte Größe eines Clusters zu erreichen, gefolgt von einem Lese-, werden Daten zurückgegeben, die am dritten VCN beginnen. Eine *logische Clusternummer (LOGICAL Cluster Number,* LCN) beschreibt den Offset eines Clusters von einem beliebigen Punkt innerhalb des Volumes. LCNs sollten nur als Ordnungszahlen oder relative Zahlen behandelt werden. Es gibt keine garantierte Zuordnung logischer Cluster zu physischen Festplattenlaufwerksektoren.

Ein *Extent* ist eine Ausführung zusammenhängender Cluster. Angenommen, eine Datei, die aus 30 Clustern besteht, wird in zwei Blöcken aufgezeichnet. Der erste Blöcke kann aus fünf zusammenhängenden Clustern bestehen, der andere aus den verbleibenden 25 Clustern.

Es gibt keine Garantie für eine Beziehung auf dem Datenträger in einem beliebigen anderen Umfang. Beispielsweise kann der erste Extent einen höheren LCN als ein nachfolgender Extent haben.

 

 



