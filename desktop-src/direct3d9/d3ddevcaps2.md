---
description: D3DDEVCAPS2-treiberfunktionsflags.
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e774076f5ad93abf5ab1ffc343f573497592728f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214132"
---
# <a name="d3ddevcaps2"></a>D3DDEVCAPS2

D3DDEVCAPS2-treiberfunktionsflags.



|                                                 |                                                                                                                                                                                                                           |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definieren                                        | BESCHREIBUNG                                                                                                                                                                                                               |
| D3DDEVCAPS2 \_ adaptivetess-Patch                | Das Gerät unterstützt das adaptive Mosaik von RT-Patches.                                                                                                                                                                       |
| D3DDEVCAPS2 \_ adaptivetess npatch                 | Das Gerät unterstützt das adaptive Mosaik von N-Patches.                                                                                                                                                                       |
| D3DDEVCAPS2 \_ kann \_ \_ von \_ Texturen gestrebe werden.   | Das Gerät unterstützt [**stretchrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) mithilfe einer Textur als Quelle.                                                                                                                       |
| D3DDEVCAPS2 \_ dmapnpatch                         | Das Gerät unterstützt Verschiebungs Zuordnungen für N-Patches.                                                                                                                                                                          |
| D3DDEVCAPS2 \_ presampleddmapnpatch               | Das Gerät unterstützt die Verschiebungs Zuordnungen für N-Patches. Weitere Informationen zur Verschiebungs Zuordnung finden Sie unter [Verschiebungs Zuordnung (Direct3D 9)](displacement-mapping.md).                                           |
| D3DDEVCAPS2 \_ Streamoffset                       | Das Gerät unterstützt streamoffsets.                                                                                                                                                                                           |
| D3DDEVCAPS2 \_ vertexelementscansharestreamoffset | Mehrere Scheitelpunkt Elemente können denselben Offset in einem Datenstrom gemeinsam verwenden, wenn D3DDEVCAPS2 \_ vertexelementscansharestreamoffset vom Gerät festgelegt wird und die Vertexdeklaration kein Element mit D3DDECLUSAGE \_ POSITIONT0 enthält. |



 

## <a name="constant-information"></a>Konstante Informationen



|                          |            |
|--------------------------|------------|
| Header                   | d3d9caps. h |
| Mindestens Betriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
