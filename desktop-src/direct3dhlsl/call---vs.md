---
title: call – vs
description: Führt einen Funktionsaufruf an die Anweisung aus, die mit der angegebenen Bezeichnung markiert ist. | call – vs
ms.assetid: 3c1ec529-1ee4-40d9-8ce5-f8e7a61fde9c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d2321224b10ca1f7822b19e48ebbb58c1e01c261720f64a8b39331fbceab75fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986890"
---
# <a name="call---vs"></a>call – vs

Führt einen Funktionsaufruf an die Anweisung aus, die mit der angegebenen Bezeichnung markiert ist.

## <a name="syntax"></a>Syntax



| call l\# |
|----------|



 

Wobei l \# eine Bezeichnung ist , im Gegensatz [zum](label---vs.md) Markieren des Anfangs der auf zu aufgerufenen Unterroutine.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Aufruf                   |      | x    | x    | x     | x    | x     |



 

Diese Anweisung führt Folgendes aus:

1.  Pushadresse der nächsten Anweisung an den Rückgabeadressenstapel.
2.  Setzen Sie die Ausführung über die anweisung fort, die durch die Bezeichnung markiert ist.

In Vertex-Shader 2 \_ 0 sind Schachtelungsaufrufe nicht zulässig.

In Vertexshader 2 x wird die Schachtelungstiefe durch das \_ StaticFlowControlDepth-Element der [**D3DVSHADERCAPS2 \_ 0-Struktur**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) eingeschränkt. Weitere Informationen finden Sie unter [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).

In Vertex-Shader 3 \_ 0 sind vier Ebenen der Aufrufschachtelung zulässig.

Nur Forward-Aufrufe sind zulässig. Dies bedeutet, dass sich die Position der Bezeichnung im Vertex-Shader hinter der Aufrufen-Anweisung befinden sollte, auf die sie verweisen.

Wenn eine Aufrufanweisung innerhalb der Schleife aufgerufen [wird...](loop---vs.md) [endloop-Block:](endloop---vs.md) Der Wert des [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) ist innerhalb der Unterroutine zugänglich.

Wenn eine Unterroutine auf das Schleifenzählerregister [(Loop Counter Register,](dx9-graphics-reference-asm-vs-registers-loop-counter.md) aL) außerhalb der Unterroutine verweisen, sollte jede Instanz des Aufrufs dieser Unterroutine von einer Schleife umgeben [sein...](loop---vs.md) [endloop-Block.](endloop---vs.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Anweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
