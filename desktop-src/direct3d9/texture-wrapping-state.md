---
description: Die Renderzustände "D3DRS WRAP0" bis "D3DRS WRAP7" ermöglichen und deaktivieren das U- und V-Wrapping für verschiedene Texturen in der \_ \_ Multitexture-Kaskadierung des Geräts.
ms.assetid: c584eee6-1187-4741-b3af-4bd79d93be77
title: Texturumbruchzustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55f6c90e31d6571d99e8a0d56ac8804eb1bc18452c9e151d2812a049af3b611c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092038"
---
# <a name="texture-wrapping-state-direct3d-9"></a>Texturumbruchzustand (Direct3D 9)

Die Renderzustände "D3DRS WRAP0" bis "D3DRS WRAP7" ermöglichen und deaktivieren das U- und V-Wrapping für verschiedene Texturen in der \_ \_ Multitexture-Kaskadierung des Geräts. Sie können diese Renderzustände auf eine Kombination der Flags D3DWRAPCOORD \_ 0, D3DWRAPCOORD \_ 1, D3DWRAPCOORD 2 und \_ D3DWRAPCOORD 3 festlegen, um das Umschließen in der ersten, zweiten, dritten und vierten Richtung der \_ Textur zu ermöglichen. Verwenden Sie den Wert 0 (null), um das Umschließen vollständig zu deaktivieren. Texturumbruch ist für alle Texturphasen standardmäßig in alle Richtungen deaktiviert.

Eine konzeptionelle Übersicht finden Sie unter [Texturumbruch (Direct3D 9).](texture-wrapping.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Renderzustände](render-states.md)
</dt> </dl>

 

 



