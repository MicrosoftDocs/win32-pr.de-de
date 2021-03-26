---
title: Pufferanordnung
description: Eine Puffer Ressource ist in Kacheln mit 64 KB unterteilt, wobei ein Leerzeichen in der letzten Kachel leer ist, wenn die Größe kein Vielfaches von 64 KB ist.
ms.assetid: 979EFCF3-1FE1-412A-A19D-F1B1CF86423B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fafa009e554499822c90c8fb6c0c8f34e47f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858286"
---
# <a name="buffer-tiling"></a>Pufferanordnung

Eine [Puffer](overviews-direct3d-11-resources-buffers.md) Ressource ist in Kacheln mit 64 KB unterteilt, wobei ein Leerzeichen in der letzten Kachel leer ist, wenn die Größe kein Vielfaches von 64 KB ist.

Für strukturierte Puffer ist keine Einschränkung auf dem STRIDE erforderlich, um gekachelt zu werden. Aber mögliche Leistungsoptimierungen in der Hardware für die Verwendung von [**structuredbuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) können durch das Anordnen der Kacheln an erster Stelle geopfert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kacheln eines gekachelten Ressourcenbereichs](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 