---
description: Konstanten, die verwendet werden, um die Priorität einer Ressource in SetPriority festzulegen.
ms.assetid: 98886349-883f-41c3-870b-e4a639977760
title: D3D9_RESOURCE_PRIORITY (D3d9types. h)
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
ms.openlocfilehash: 1ae5a54c7645db63b1023c3571f8181f4ee2daec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219465"
---
# <a name="d3d9_resource_priority"></a>D3d9- \_ Ressourcen \_ Priorität

Konstanten, die verwendet werden, um die Priorität einer Ressource in [**SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority)festzulegen.



| Konstante/Wert                                                                                                                                                                                                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3D9_RESOURCE_PRIORITY_MINIMUM"></span><span id="d3d9_resource_priority_minimum"></span><dl> <dt>**D3d9 \_ \_ \_ Minimale Ressourcen Priorität**</dt> <dt>0x28000000</dt> </dl> | Die Ressource hat die niedrigste mögliche Priorität. Diese Konstante markiert die Ressource als nicht verwendet und zum Entfernen. Die Ressource sollte entfernt werden, sobald eine andere Ressource den von der Ressource belegten Speicherplatz benötigt.<br/>                                                                                                                                                                                                              |
| <span id="D3D9_RESOURCE_PRIORITY_LOW"></span><span id="d3d9_resource_priority_low"></span><dl> <dt>**D3d9 \_ Ressourcen \_ Priorität \_ niedrig**</dt> <dt>0x50.000.000</dt> </dl>             | Die Ressource wird mit niedriger Priorität geplant. Die Platzierung der Ressource ist nicht wichtig, und das Betriebssystem führt nur wenig Arbeit aus, um einen Speicherort für die Ressource zu finden. Durch das Markieren einer Ressource mit niedriger Priorität können andere kritische Ressourcen den schnelleren Arbeitsspeicher belegen.<br/>                                                                                                                                                      |
| <span id="D3D9_RESOURCE_PRIORITY_NORMAL"></span><span id="d3d9_resource_priority_normal"></span><dl> <dt>**D3d9 \_ Ressourcen \_ Priorität \_ Normal**</dt> <dt>0x78000000</dt> </dl>    | Die Ressource wird mit normaler Priorität geplant. Die Platzierung der Ressource ist wichtig für die Leistung, aber Sie ist nicht entscheidend. Das Betriebssystem sollte versuchen, die Ressource, die als normal gekennzeichnet ist, am bevorzugten Speicherort der Ressource anstatt an eine Ressource mit niedriger Priorität zu platzieren. In der Regel werden Texturen als normal gekennzeichnet.<br/>                                                                                                     |
| <span id="D3D9_RESOURCE_PRIORITY_HIGH"></span><span id="d3d9_resource_priority_high"></span><dl> <dt>**D3d9 \_ Ressourcen \_ Priorität \_ hoch**</dt> <dt>0xA0000000</dt> </dl>          | Die Ressource wird mit hoher Priorität geplant. Die Platzierung der Ressource ist wichtig für die Leistung. Das Betriebssystem versucht immer, die Ressource, die im bevorzugten Speicherort der Ressource als hoch gekennzeichnet ist, anstelle einer Ressource mit niedriger Priorität oder normaler Priorität zu platzieren. In der Regel werden Renderziele als hoch markiert.<br/>                                                                                                         |
| <span id="D3D9_RESOURCE_PRIORITY_MAXIMUM"></span><span id="d3d9_resource_priority_maximum"></span><dl> <dt>**D3d9 \_ \_ \_ Maximale Ressourcen Priorität**</dt> <dt>0xc8000000</dt> </dl> | Die Ressource hat die maximal mögliche Priorität. Diese Konstante markiert die Priorität der Ressource als vorläufig. Eine vorläufig fixierte Ressource wird nur dann aus dem Arbeitsspeicher entfernt, wenn es keine andere Möglichkeit gibt, die Arbeitsspeicher Anforderung eines DMA-Puffers zu beheben. Das Betriebssystem versucht, einen DMA-Puffer auf seine Mindestgröße aufzuteilen und alle anderen Ressourcen, die nicht fixiert und nicht vorläufig fixiert werden, zu entfernen, bevor eine vorläufig fixierte Ressource entfernt wird. <br/> |



## <a name="remarks"></a>Bemerkungen

Werte, die nicht den maximalen Wert für die **d3d9- \_ Ressourcen \_ Priorität \_** und die **Maximale d3d9- \_ Ressourcen \_ Priorität \_** haben, werden vom Planer als Hinweise behandelt.

Sie können andere Prioritätsstufen als die zuvor in diesem Thema definierten Werte verwenden. Wenn Sie z. b. eine Ressource mit der Prioritätsstufe 0x78000001 markieren, wird angegeben, dass die Ressourcen Priorität etwas über dem normalen Wert liegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
