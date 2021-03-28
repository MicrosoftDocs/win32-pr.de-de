---
title: Phase-PS
description: Die Phasen Anweisung markiert den Übergang Zwischenphase 1 und Phase 2. Wenn keine Phasen Anweisung vorhanden ist, wird der gesamte Shader so ausgeführt, als handele es sich um einen Shader der Phase 2.
ms.assetid: e0e89425-dc8e-489f-a0d1-3eefbfd09178
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e9a16b01e186de5645ffe65e003ebbe6defca2d5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038361"
---
# <a name="phase---ps"></a>Phase-PS

Die Phasen Anweisung markiert den Übergang Zwischenphase 1 und Phase 2. Wenn keine Phasen Anweisung vorhanden ist, wird der gesamte Shader so ausgeführt, als handele es sich um einen Shader der Phase 2.

Diese Anweisung gilt nur für Version 1 \_ 4.

## <a name="syntax"></a>Syntax


```
phase
```



## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| phase                 |      |      |      | x    |      |      |       |      |       |



 

Shaderanweisungen, die vor der Phasen Anweisung erfolgen, sind Anweisungen der Phase 1. Alle anderen Anweisungen sind Anweisungen der Phase 2. Wenn Sie zwei Phasen für Anweisungen haben, wird die maximale Anzahl von Anweisungen pro Shader angehoben.

Der unglückliche Nebeneffekt des Phasenübergangs besteht darin, dass die Alpha Komponente von [temporären Registern](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) nicht über den Übergang hinweg beibehalten wird. Das heißt, die Alpha Komponente muss nach der Phasen Anweisung erneut initialisiert werden.

## <a name="example"></a>Beispiel

In diesem Beispiel wird gezeigt, wie Sie Anweisungen in Phase 1 oder in Phase 2 in einem Shader gruppieren.

Die Phasen Anweisung wird auch als Phasen Marker bezeichnet, da Sie den Übergang zwischen den Anweisungen in Phase 1 und 2 markiert. Wenn in einem \_ Pixelshader der Version 1 4 der Phasen Marker nicht vorhanden ist, wird der Shader so ausgeführt, als ob er in Phase 2 ausgeführt wird. Dies ist wichtig, da es Unterschiede zwischen den Anweisungen in Phase 1 und 2 gibt und die Verfügbarkeit registriert ist. Die Unterschiede werden im gesamten Referenz Abschnitt vermerkt.


```
ps_1_4
  // Add phase 1 instructions here

phase
  // Add phase 2 instructions here
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




