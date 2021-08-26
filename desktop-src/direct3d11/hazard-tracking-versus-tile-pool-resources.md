---
title: Gefahrennachverfolgung im Vergleich mit den Kachelpoolressourcen
description: Bei nicht gekachelten Ressourcen kann Direct3D bestimmte Gefährdungsbedingungen während des Renderings verhindern, aber da die Risikonachverfolgung für gekachelte Ressourcen auf Kachelebene erfolgen würde, ist die Nachverfolgung von Gefährdungsbedingungen während des Renderns von gekachelten Ressourcen möglicherweise zu teuer.
ms.assetid: 4106BAB9-3E0C-48F1-B7E2-565A65DBC78F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b30feeba564371055ee4297c6795396173a46272f43ffe43af353b17abc0193
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952900"
---
# <a name="hazard-tracking-versus-tile-pool-resources"></a>Gefahrennachverfolgung im Vergleich mit den Kachelpoolressourcen

Bei nicht gekachelten Ressourcen kann Direct3D bestimmte Gefährdungsbedingungen während des Renderings verhindern, aber da die Risikonachverfolgung für gekachelte Ressourcen auf Kachelebene erfolgen würde, ist die Nachverfolgung von Gefährdungsbedingungen während des Renderns von gekachelten Ressourcen möglicherweise zu teuer.

Bei nicht gekachelten Ressourcen lässt die Runtime beispielsweise nicht zu, dass eine bestimmte SubResource gleichzeitig als Eingabe (z. B. ShaderResourceView) und als Ausgabe (z. B. RenderTargetView) gebunden wird. Wenn ein solcher Fall auftritt, entbindet die Laufzeit die Eingabe. Dieser Nachverfolgungsaufwand in der Laufzeit ist kostengünstig und erfolgt auf SubResource-Ebene. Einer der Vorteile dieses Nachverfolgungsaufwands besteht darin, die Wahrscheinlichkeit zu minimieren, dass Anwendungen versehentlich von der Ausführungsreihenfolge des Hardware-Shaders abhängig sind. Die Ausführungsreihenfolge des Hardware-Shaders kann variieren, wenn nicht auf einer bestimmten Grafikverarbeitungseinheit (GRAPHICS Processing Unit, GPU) und sicher über verschiedene GPUs hinweg.

Die Nachverfolgung, wie Ressourcen gebunden sind, kann für gekachelte Ressourcen zu teuer sein, da die Nachverfolgung auf Kachelebene erfolgt. Es treten neue Probleme auf, z. B. das mögliche Entfernen von Versuchen, in eine RenderTargetView zu rendern, wobei eine Kachel mehreren Bereichen auf der Oberfläche gleichzeitig zugeordnet ist. Wenn sich herausstellt, dass diese Risikonachverfolgung pro Kachel für die Laufzeit zu teuer ist, wäre dies im Idealfall zumindest eine Option in der Debugebene.

Eine Anwendung muss den Anzeigetreiber informieren, wenn sie einen Schreib- oder Lesevorgang für eine gekachelte Ressource ausgeführt hat, die auf den Kachelpoolspeicher verweist, auf den auch von separaten gekachelten Ressourcen in anstehenden Lese- oder Schreibvorgängen verwiesen wird, dass der erste Vorgang abgeschlossen werden soll, bevor die folgenden Vorgänge beginnen können. Weitere Informationen zu dieser Bedingung finden Sie unter [**ID3D11DeviceContext2::TiledResourceBarrier-Hinweise.**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnungen in einen Kachelpool](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




