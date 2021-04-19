---
description: Definiert Optionen zum Ausführen von geodäschen Entfernungs Berechnungen, wenn eine Textur an eine gekrümmte Oberfläche angepasst wird. Verwenden Sie dieses Flag, um beim Berechnen eines Textur Atlas zwischen hochwertigen und schnellen Berechnungen zu wählen.
ms.assetid: 76649c57-e5ae-4e0d-a7ab-f56385a327c2
title: D3DXUVATLAS-Enumeration (D3dx9mesh. h)
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
ms.openlocfilehash: 64cc116199b688fc9dcd8d6fbf331d85da508948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355799"
---
# <a name="d3dxuvatlas-enumeration"></a>D3DXUVATLAS-Enumeration

Definiert Optionen zum Ausführen von geodäschen Entfernungs Berechnungen, wenn eine Textur an eine gekrümmte Oberfläche angepasst wird. Verwenden Sie dieses Flag, um beim Berechnen eines Textur Atlas zwischen hochwertigen und schnellen Berechnungen zu wählen.

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

<span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**D3DXUVATLAS \_ Standard**
</dt> <dd>

Für Netzen mit mehr als 25 KB wird die schnelle geodasic-Entfernungs Methode angewendet, während für Netzen mit weniger als 25 KB die Entfernungs Methode für höhere Qualität auf Sie angewendet wird.

</dd> <dt>

<span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**D3DXUVATLAS \_ Geodesic \_ fast**
</dt> <dd>

Verwendet Näherungs Werte, um die Diagramm Geschwindigkeit zu verbessern, indem zusätzliche Stretch oder mehr Diagramme für das Mesh ausgegeben werden.

</dd> <dt>

<span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**D3DXUVATLAS \_ Geodesic- \_ Qualität**
</dt> <dd>

Bietet bessere Qualitäts Diagramme, erfordert jedoch mehr Zeit und Arbeitsspeicher als schnell.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




