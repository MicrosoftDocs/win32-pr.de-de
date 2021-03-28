---
title: Gefahrennachverfolgung im Vergleich mit den Kachelpoolressourcen
description: Bei nicht gekachelten Ressourcen kann Direct3D bestimmte Gefahren Bedingungen während des Renderings verhindern, aber da die gefährverfolgung auf Kachel Ebene für gekachelte Ressourcen erfolgen würde, kann das Nachverfolgen von Gefährdungs Zuständen beim Rendern von gekachelten Ressourcen zu teuer sein.
ms.assetid: 4106BAB9-3E0C-48F1-B7E2-565A65DBC78F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c75dcd11cb5e49f165105bd932854e36b37308cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388033"
---
# <a name="hazard-tracking-versus-tile-pool-resources"></a>Gefahrennachverfolgung im Vergleich mit den Kachelpoolressourcen

Bei nicht gekachelten Ressourcen kann Direct3D bestimmte Gefahren Bedingungen während des Renderings verhindern, aber da die gefährverfolgung auf Kachel Ebene für gekachelte Ressourcen erfolgen würde, kann das Nachverfolgen von Gefährdungs Zuständen beim Rendern von gekachelten Ressourcen zu teuer sein.

Beispielsweise lässt die Runtime für nicht gekachelte Ressourcen nicht zu, dass eine angegebene untergeordnete Quelle als Eingabe (z. b. eine shaderresourceview) und als Ausgabe (z. b. eine rendertargetview) gleichzeitig gebunden wird. Wenn ein solcher Fall auftritt, wird die Bindung der Eingabe von der Laufzeit entbindet. Dieser Überwachungs Aufwand in der Laufzeit ist kostengünstig und wird auf der Ebene der untergeordneten Quelle erreicht. Einer der Vorteile dieses nach Verfolgungs Aufwands besteht darin, die Wahrscheinlichkeit von Anwendungen zu minimieren, abhängig von der Reihenfolge der Hardware-Shader-Ausführung. Die Ausführungsreihenfolge der Hardware-Shader kann variieren, wenn Sie nicht auf einer bestimmten GPU (Graphics Processing Unit) und dann auf unterschiedlichen GPUs verteilt ist.

Die Nachverfolgung, wie Ressourcen gebunden werden, kann für gekachelte Ressourcen zu teuer sein, da die Nachverfolgung auf Kachel Ebene erfolgt. Es ergeben sich neue Probleme, z. b. das Überprüfen von versuchen, eine rendertargetview zu rendertargetview zu rendieren, und eine Kachel, die mehreren Bereichen in der Wenn sich herausstellt, dass die Nachverfolgung pro Kachel für die Laufzeit zu teuer ist, ist dies im Idealfall zumindest eine Option in der debugschicht.

Eine Anwendung muss den Anzeigetreiber Benachrichtigen, wenn Sie einen Schreib-oder Lesevorgang für eine gekachelte Ressource ausgegeben hat, die auf den Kachel Pool Speicher verweist, auf den auch von separaten gekachelten Ressourcen in anstehenden Lese-oder Schreibvorgängen verwiesen wird, bevor die folgenden Vorgänge beginnen können. Weitere Informationen zu dieser Bedingung finden Sie unter [**ID3D11DeviceContext2:: tiledresourcebarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) -Hinweise.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnungen in einen Kachelpool](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




