---
description: Konstanten, die verwendet werden, um die Priorität einer Ressource in SetPriority festzulegen.
ms.assetid: 98886349-883f-41c3-870b-e4a639977760
title: D3D9_RESOURCE_PRIORITY (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D9_RESOURCE_PRIORITY_MINIMUM
- D3D9_RESOURCE_PRIORITY_LOW
- D3D9_RESOURCE_PRIORITY_NORMAL
- D3D9_RESOURCE_PRIORITY_HIGH
- D3D9_RESOURCE_PRIORITY_MAXIMUM
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 367d50292b283cc7a0dcdef42b2e2c270099e314dc61c8d590e7ef2a1091a4f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751330"
---
# <a name="d3d9_resource_priority"></a>\_D3D9-RESSOURCENPRIORITÄT \_

Konstanten, die zum Festlegen der Priorität einer Ressource in [**SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority)verwendet werden.



| Konstante/Wert                                                                                                                                                                                                                                                                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3D9_RESOURCE_PRIORITY_MINIMUM"></span><span id="d3d9_resource_priority_minimum"></span><dl> <dt>**D3D9 \_ \_ \_ RESOURCE PRIORITY MINIMUM**</dt> <dt>0x28000000</dt> </dl> | Die Ressource hat die niedrigste mögliche Priorität. Diese Konstante markiert die Ressource als nicht verwendet und für die Eviction. Die Ressource sollte entfernt werden, sobald eine andere Ressource den Speicherplatz benötigt, den die Ressource belegt.<br/>                                                                                                                                                                                                              |
| <span id="D3D9_RESOURCE_PRIORITY_LOW"></span><span id="d3d9_resource_priority_low"></span><dl> <dt>**D3D9 \_ \_ \_ RESOURCE PRIORITY LOW**</dt> <dt>0x50000000</dt> </dl>             | Die Ressource wird mit niedriger Priorität geplant. Die Platzierung der Ressource ist nicht entscheidend, und das Betriebssystem führt minimale Arbeit aus, um einen Speicherort für die Ressource zu finden. Durch das Markieren einer Ressource als niedrige Priorität können andere kritischere Ressourcen den schnelleren Arbeitsspeicher belegen.<br/>                                                                                                                                                      |
| <span id="D3D9_RESOURCE_PRIORITY_NORMAL"></span><span id="d3d9_resource_priority_normal"></span><dl> <dt>**D3D9 \_ \_RESSOURCENPRIORITÄT \_ NORMAL**</dt> <dt>0x78000000</dt> </dl>    | Die Ressource wird mit normaler Priorität geplant. Die Platzierung der Ressource ist für die Leistung wichtig, aber nicht wichtig. Das Betriebssystem sollte versuchen, die als normal markierte Ressource anstelle einer Ressource mit niedriger Priorität am bevorzugten Speicherort der Ressource zu platzieren. In der Regel werden Texturen als normal markiert.<br/>                                                                                                     |
| <span id="D3D9_RESOURCE_PRIORITY_HIGH"></span><span id="d3d9_resource_priority_high"></span><dl> <dt>**D3D9 \_ \_ \_ RESOURCE PRIORITY HIGH**</dt> <dt>0xa0000000</dt> </dl>          | Die Ressource wird mit hoher Priorität geplant. Die Platzierung der Ressource ist für die Leistung von entscheidender Bedeutung. Das Betriebssystem versucht immer, die Ressource, die als hoch markiert ist, am bevorzugten Standort der Ressource anstelle einer Ressource mit niedriger oder normaler Priorität zu platzieren. In der Regel werden Renderziele als hoch markiert.<br/>                                                                                                         |
| <span id="D3D9_RESOURCE_PRIORITY_MAXIMUM"></span><span id="d3d9_resource_priority_maximum"></span><dl> <dt>**D3D9 \_ \_MAXIMALE \_ RESSOURCENPRIORITÄT**</dt> <dt>0xc8000000</dt> </dl> | Die Ressource hat die maximal mögliche Priorität. Diese Konstante markiert die Priorität der Ressource als soft-pinned. Eine soft-pinned-Ressource wird nur dann aus dem Arbeitsspeicher entfernt, wenn es keine andere Möglichkeit gibt, die Arbeitsspeicheranforderung eines DMA-Puffers zu beheben. Das Betriebssystem versucht, einen DMA-Puffer auf seine mindeste Größe aufzuteilen und alle anderen Ressourcen zu trennen, die nicht angeheftet und nicht soft angeheftet sind, bevor eine soft-pinned-Ressource entfernt wird. <br/> |



## <a name="remarks"></a>Hinweise

Andere Werte als **D3D9 \_ RESOURCE \_ PRIORITY \_ MINIMUM** und **D3D9 \_ RESOURCE PRIORITY \_ \_ MAXIMUM** werden vom Planer als Hinweise behandelt.

Sie können andere Prioritätsebenen als die zuvor in diesem Thema definierten Werte verwenden. Das Markieren einer Ressource mit der Prioritätsstufe 0x78000001 gibt beispielsweise an, dass die Ressourcenpriorität leicht über dem normalen Wert liegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
