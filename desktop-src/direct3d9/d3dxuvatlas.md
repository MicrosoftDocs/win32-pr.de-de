---
description: Definiert Optionen zum Ausführen von geodätischen Entfernungsberechnungen beim Anpassen einer Textur an eine gekrümmte Oberfläche. Verwenden Sie dieses Flag, um beim Berechnen eines Texturat atlas zwischen hoher Qualität und schnellen Berechnungen zu wählen.
ms.assetid: 76649c57-e5ae-4e0d-a7ab-f56385a327c2
title: D3DXUVATLAS-Enumeration (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVATLAS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 1edcf2b1cbe2363f805bee1f5eb67f5558702ea9e163a865e1a6c51d6f5ed6ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523836"
---
# <a name="d3dxuvatlas-enumeration"></a>D3DXUVATLAS-Enumeration

Definiert Optionen zum Ausführen von geodätischen Entfernungsberechnungen beim Anpassen einer Textur an eine gekrümmte Oberfläche. Verwenden Sie dieses Flag, um beim Berechnen eines Texturat atlas zwischen hoher Qualität und schnellen Berechnungen zu wählen.

## <a name="syntax"></a>Syntax


```C++
typedef enum _D3DXUVATLAS { 
  D3DXUVATLAS_DEFAULT           = 1,
  D3DXUVATLAS_GEODESIC_FAST     = 2,
  D3DXUVATLAS_GEODESIC_QUALITY  = 3
} D3DXUVATLAS;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**D3DXUVATLAS \_ DEFAULT**
</dt> <dd>

Für Gitternetze mit mehr als 25.000 Gesichtern wird die schnelle geodasische Entfernungsmethode angewendet, während für Gitternetze mit weniger als 25.000 Gesichtern stattdessen die geodätische Entfernungsmethode höherer Qualität angewendet wird.

</dd> <dt>

<span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**D3DXUVATLAS \_ GEODESIC \_ FAST**
</dt> <dd>

Verwendet Näherungen, um die Diagrammgeschwindigkeit auf Kosten von zusätzlichen Stretchingdiagrammen oder mehr Diagrammen zu verbessern, die für das Gitternetz ausgegeben werden.

</dd> <dt>

<span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**D3DXUVATLAS \_ GEODESIC \_ QUALITY**
</dt> <dd>

Stellt Diagramme mit besserer Qualität bereit, erfordert jedoch mehr Zeit und Arbeitsspeicher als schnell.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




