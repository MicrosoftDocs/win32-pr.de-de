---
title: Ändern der Größe des Kachelpools
description: Verwenden Sie die ID3D11DeviceContext2 resizetilepool-API, um einen Kachel Pool zu vergrößern, wenn für die Anwendung mehr Arbeits Sätze benötigt werden, damit die gekachelten Ressourcen darauf zuordnet werden.
ms.assetid: 529E874E-650B-4BFD-97F6-E66E743564A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86368da46f7c2219f42b5ecbc122b79fee19e72c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855552"
---
# <a name="tile-pool-resizing"></a>Ändern der Größe des Kachelpools

Verwenden Sie die [**ID3D11DeviceContext2:: resizetilepool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) -API, um einen Kachel Pool zu vergrößern, wenn für die Anwendung mehr Arbeits Sätze benötigt werden, damit die gekachelten Ressourcen darauf zuordnet werden. Eine weitere Option für Anwendungen besteht darin, zusätzliche Kachel Pools für neue Kachel Ressourcen zuzuordnen. Wenn jedoch eine einzelne Kachel Ressource mehr Speicherplatz benötigt, als in Ihrem Kachel Pool anfänglich verfügbar ist, ist das Vergrößern des Kachel Pools eine gute Option. Eine gekachelte Ressource kann nicht gleichzeitig Zuordnungen in mehrere Kachel Pools haben.

Wenn ein Kachel Pool vergrößert wird, werden am Ende zusätzliche Kacheln über eine oder mehrere neue Zuordnungen durch den Anzeigetreiber hinzugefügt. Diese Aufteilung in Zuordnungen ist für die Anwendung nicht sichtbar. Vorhandener Arbeitsspeicher im Kachel Pool bleibt unverändert, und vorhandene gekachelte Ressourcen Zuordnungen in diesen Arbeitsspeicher bleiben intakt.

Wenn ein Kachel Pool verkleinert wird, werden die Kacheln vom Ende entfernt. Kacheln werden sogar unterhalb der anfänglichen Zuordnungs Größe (bis zu 0) entfernt, was bedeutet, dass neue Zuordnungen nicht über die neue Größe hinaus erfolgen können. Vorhandene Zuordnungen hinter dem Ende der neuen Größe bleiben jedoch intakt und können nutzbar sein. Der Anzeigetreiber behält den Arbeitsspeicher so lange bei, wie Zuordnungen zu beliebigen Teilen der Zuordnungen, die der Treiber für den Speicher des Kachel Pools verwendet, verbleibt. Wenn nach der Verkleinerung der Arbeitsspeicher nicht mehr aktiv ist, weil Kachel Zuordnungen darauf zeigen und der Kachel Pool wieder vergrößert wird (durch einen beliebigen Betrag), wird der vorhandene Speicher zuerst wieder verwendet, bevor zusätzliche Zuordnungen vorhanden sind, um die Größe des Anfügevorgangs zu verarbeiten.

Um Speicherplatz zu sparen, muss eine Anwendung nicht nur einen Kachel Pool verkleinern, sondern auch vorhandene Zuordnungen nach dem Ende der neuen kleineren Kachel Poolgröße entfernen bzw. neu zuordnen.

Das Verkleinern (und Entfernen von Zuordnungen) führt nicht unbedingt zu sofortiger Speicherersparnis. Die Freigabe des Arbeitsspeichers hängt von der Granularität der zugrunde liegenden Zuordnungen des Anzeige Treibers für den Kachel Pool ab. Wenn der Verkleinerungs Vorgang ausreichend ist, um eine Anzeigetreiber Zuordnung nicht verwendeter zu machen, kann der Anzeigetreiber ihn freigeben. Wenn ein Kachel Pool vergrößert wurde, ist es wahrscheinlich, dass eine Verkleinerung auf vorherige Größen (und das Entfernen/Neuzuordnen von Kachel Zuordnungen) in der Regel zu Speicher Einsparungen führen. Dies ist jedoch nicht garantiert, wenn die Größen nicht genau mit den zugrunde liegenden Zuordnungs Größen übereinstimmen, die vom Anzeigetreiber ausgewählt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnungen in einen Kachelpool](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




