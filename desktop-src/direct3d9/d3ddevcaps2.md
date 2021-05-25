---
description: D3DDEVCAPS2-Treiberfunktionsflags.
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6296db9b338d5f9a8c8ede702a784baf1fdfd462
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343205"
---
# <a name="d3ddevcaps2"></a>D3DDEVCAPS2

D3DDEVCAPS2-Treiberfunktionsflags.



| \#Definieren                                        | BESCHREIBUNG                                                                                                                                                                                                               |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DDEVCAPS2 \_ ADAPTIVETESSRTPATCH                | Das Gerät unterstützt die adaptive Mosaikierung von RT-Patches.                                                                                                                                                                       |
| D3DDEVCAPS2 \_ ADAPTIVETESSNPATCH                 | Das Gerät unterstützt die adaptive Mosaikierung von N-Patches.                                                                                                                                                                       |
| D3DDEVCAPS2 \_ KANN \_ \_ STRETCHRECT AUS \_ TEXTUREN ZIEHEN.   | Das Gerät unterstützt [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) mithilfe einer Textur als Quelle.                                                                                                                       |
| D3DDEVCAPS2 \_ DMAPNPATCH                         | Das Gerät unterstützt Verschiebungszuordnungen für N-Patches.                                                                                                                                                                          |
| D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH               | Das Gerät unterstützt vorsampelte Verschiebungszuordnungen für N-Patches. Weitere Informationen zur Verschiebungszuordnung finden Sie unter [Verschiebungszuordnung (Direct3D 9).](displacement-mapping.md)                                           |
| D3DDEVCAPS2 \_ STREAMOFFSET                       | Das Gerät unterstützt Streamoffsets.                                                                                                                                                                                           |
| D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET | Mehrere Vertexelemente können denselben Offset in einem Stream gemeinsam nutzen, wenn D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET vom Gerät festgelegt wird und die Scheitelpunktdeklaration kein Element mit D3DDECLUSAGE \_ POSITIONT0 aufwies. |



 

## <a name="constant-information"></a>Konstante Informationen



| Anforderung                         | Wert           |
|--------------------------|------------|
| Header                   | d3d9caps.h |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Konstanten](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
