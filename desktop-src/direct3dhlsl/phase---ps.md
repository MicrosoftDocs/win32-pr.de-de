---
title: phase – ps
description: Die Phasesanweisung markiert den Übergang zwischen Phase 1 und Phase 2. Wenn keine Phasesanweisung vorhanden ist, wird der gesamte Shader so ausgeführt, als ob es sich um einen Shader der Phase 2 handelt.
ms.assetid: e0e89425-dc8e-489f-a0d1-3eefbfd09178
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aac29792274a36ad4bb7266ffa02d0ea5d2bb1b6cec8efe2db213e9b0dd4890b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118088693"
---
# <a name="phase---ps"></a>phase – ps

Die Phasesanweisung markiert den Übergang zwischen Phase 1 und Phase 2. Wenn keine Phasesanweisung vorhanden ist, wird der gesamte Shader so ausgeführt, als ob es sich um einen Shader der Phase 2 handelt.

Diese Anweisung gilt nur für Version 1 \_ 4.

## <a name="syntax"></a>Syntax


```
phase
```



## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| phase                 |      |      |      | x    |      |      |       |      |       |



 

Shaderanweisungen, die vor der Phasesanweisung auftreten, sind Anweisungen in Phase 1. Alle anderen Anweisungen sind Anweisungen in Phase 2. Durch zwei Phasen für Anweisungen wird die maximale Anzahl von Anweisungen pro Shader erhöht.

Der vorübergehende Nebeneffekt des [Phasenübergangs](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) ist, dass die Alphakomponente temporärer Register während des Übergangs nicht beibehalten wird. Anders ausgedrückt: Die Alphakomponente muss nach der Phasesanweisung erneut initialisiert werden.

## <a name="example"></a>Beispiel

In diesem Beispiel wird gezeigt, wie Anweisungen als Anweisungen in Phase 1 oder Phase 2 innerhalb eines Shaders gruppiert werden.

Die Phasenanweisung wird auch häufig als Phasenmarker bezeichnet, da sie den Übergang zwischen Phase 1- und 2-Anweisungen markiert. Wenn der Phasenmarker in einem Shader der Version 1 mit 4 Pixeln nicht vorhanden ist, wird der Shader so ausgeführt, als würde er \_ in Phase 2 ausgeführt. Dies ist wichtig, da es Unterschiede zwischen den Anweisungen in Phase 1 und 2 und der Registrierung der Verfügbarkeit gibt. Die Unterschiede werden im gesamten Referenzabschnitt beschrieben.


```
ps_1_4
  // Add phase 1 instructions here

phase
  // Add phase 2 instructions here
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




