---
title: Pufferanordnung
description: Eine Pufferressource ist in Kacheln mit 64 KB unterteilt, mit einem leeren Platz auf der letzten Kachel, wenn die Größe nicht ein Vielfaches von 64 KB ist.
ms.assetid: 979EFCF3-1FE1-412A-A19D-F1B1CF86423B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36352f492efb88bf220035d737b5767ef086e74ab91ffb4228d7734f838425b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734242"
---
# <a name="buffer-tiling"></a>Pufferanordnung

Eine [Pufferressource](overviews-direct3d-11-resources-buffers.md) ist in Kacheln mit 64 KB unterteilt, mit einem leeren Platz auf der letzten Kachel, wenn die Größe nicht ein Vielfaches von 64 KB ist.

Strukturierte Puffer dürfen keine Einschränkung für den Schritt haben, um gekachelt zu werden. Mögliche Leistungsoptimierungen in der Hardware für die Verwendung [**von StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) können jedoch verflert werden, indem sie von Anfang an gekachelt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kacheln des Bereichs einer gekachelten Ressource](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 