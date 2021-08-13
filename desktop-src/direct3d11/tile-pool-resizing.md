---
title: Ändern der Größe des Kachelpools
description: Verwenden Sie die ID3D11DeviceContext2 ResizeTilePool-API, um einen Kachelpool zu vergrößern, wenn die Anwendung mehr Arbeitssatz für die Zuordnung der gekachelten Ressourcen benötigt, oder um zu verkleinern, wenn weniger Speicherplatz erforderlich ist.
ms.assetid: 529E874E-650B-4BFD-97F6-E66E743564A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b91e3942e5da88c58c391f652a2b23a7b02513777060d78e86522b892da478
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119375810"
---
# <a name="tile-pool-resizing"></a>Ändern der Größe des Kachelpools

Verwenden Sie die [**ID3D11DeviceContext2::ResizeTilePool-API,**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) um einen Kachelpool zu vergrößern, wenn die Anwendung mehr Arbeitssatz für die Zuordnung der gekachelten Ressourcen benötigt, oder um zu verkleinern, wenn weniger Speicherplatz erforderlich ist. Eine weitere Option für Anwendungen ist das Zuordnen zusätzlicher Kachelpools für neue gekachelte Ressourcen. Wenn jedoch eine einzelne gekachelte Ressource mehr Speicherplatz benötigt, als ursprünglich im Kachelpool verfügbar ist, ist das Anwachsen des Kachelpools eine gute Option. Eine gekachelte Ressource kann nicht gleichzeitig Zuordnungen zu mehreren Kachelpools haben.

Wenn ein Kachelpool größer wird, werden zusätzliche Kacheln am Ende über eine oder mehrere neue Zuordnungen durch den Anzeigetreiber hinzugefügt. Diese Aufschlüsselung in Zuordnungen ist für die Anwendung nicht sichtbar. Der vorhandene Arbeitsspeicher im Kachelpool bleibt unverändert, und vorhandene kachelierte Ressourcenzuordnungen in diesem Speicher bleiben intakt.

Wenn ein Kachelpool verkleinert wird, werden Kacheln vom Ende entfernt. Kacheln werden sogar unterhalb der anfänglichen Zuordnungsgröße bis auf 0 entfernt, was bedeutet, dass neue Zuordnungen nicht über die neue Größe hinaus vorgenommen werden können. Vorhandene Zuordnungen über das Ende der neuen Größe hinaus bleiben jedoch intakt und können verwendet werden. Der Anzeigetreiber hält den Arbeitsspeicher so lange, wie Zuordnungen zu einem beliebigen Teil der Zuordnungen, die der Treiber für den Kachelpoolspeicher verwendet, erhalten bleiben. Wenn nach dem Verkleinern von Arbeitsspeicher beibehalten wurde, weil Kachelzuordnungen darauf zeigen und der Kachelpool erneut vergrößerbar wird (um eine beliebige Menge), wird der vorhandene Arbeitsspeicher zuerst wiederverwendet, bevor zusätzliche Zuordnungen auftreten, um die Größe des Vergrößerungsvorgang zu verarbeiten.

Um Arbeitsspeicher zu sparen, muss eine Anwendung nicht nur einen Kachelpool verkleinern, sondern auch vorhandene Zuordnungen nach dem Ende der neuen kleineren Kachelpoolgröße entfernen/neu zuordnen.

Das Verkleinern (und Entfernen von Zuordnungen) führt nicht unbedingt zu sofortigen Speichereinsparungen. Die Speicherzuweisung hängt davon ab, wie präzise die dem Anzeigetreiber zugrunde liegenden Zuordnungen für den Kachelpool sind. Wenn das Verkleinern ausreicht, damit eine Anzeigetreiberzuordnung nicht verwendet wird, kann der Anzeigetreiber sie wieder frei geben. Wenn ein Kachelpool größer wurde, führt das Verkleinern auf vorherige Größen (und das entfernen/neu zuordnende Kachelzuordnungen entsprechend) am wahrscheinlichsten zu Speichereinsparungen. Dies ist jedoch nicht garantiert, wenn die Größen nicht genau mit den zugrunde liegenden Zuordnungsgrößen, die vom Anzeigetreiber ausgewählt wurden, ausgerichtet sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnungen in einen Kachelpool](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




