---
title: callvs
description: Führt einen Funktions Aufrufder Anweisung aus, die mit der angegebenen Bezeichnung gekennzeichnet ist. | callvs
ms.assetid: 3c1ec529-1ee4-40d9-8ce5-f8e7a61fde9c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c797e7ef6745f5710752fe059d2a2ff1f94a8aa3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961528"
---
# <a name="call---vs"></a>callvs

Führt einen Funktions Aufrufder Anweisung aus, die mit der angegebenen Bezeichnung gekennzeichnet ist.

## <a name="syntax"></a>Syntax



| l anrufen\# |
|----------|



 

Where l \# ist eine [Bezeichnung-vs](label---vs.md) , die den Anfang der aufzurufenden Unterroutine kennzeichnet.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| Aufruf                   |      | x    | x    | x     | x    | x     |



 

Diese Anweisung führt Folgendes aus:

1.  Die pushadresse der nächsten Anweisung in den Rückgabe Adress Stapel.
2.  Setzen Sie die Ausführung mit der von der Bezeichnung markierten Anweisung fort.

In Vertex-Shader 2 \_ 0 sind Verschachtelungs Aufrufe nicht zulässig.

In Vertex Shader 2 \_ x wird die Schachtelungs Tiefe durch das staticflowcontroltiefe-Element der [**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) -Struktur eingeschränkt. Weitere Informationen finden Sie unter [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).

In Vertex-Shader 3 0 sind vier Ebenen der Schachtelungs Schachtelung \_ zulässig.

Nur vorwärts Aufrufe sind zulässig. Dies bedeutet, dass der Speicherort der Bezeichnung innerhalb des Vertex-Shaders nach der Anweisung zum Aufrufen der Anweisung liegen muss.

Wenn eine Aufruf Anweisung innerhalb einer [Schleife](loop---vs.md)aufgerufen wird... [ENDLOOP](endloop---vs.md) -Block: auf den Wert des [Schleifen zählungs Leistungs Zählers](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) kann innerhalb der Unterroutine zugegriffen werden.

Wenn eine Unterroutine auf das Schleifen- [Counter-Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) verweist, das sich außerhalb der Unterroutine befindet, sollte jede Instanz des Aufrufes dieser Unterroutine von einer [Schleife](loop---vs.md)umgeben werden... [ENDLOOP](endloop---vs.md) -Block.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
