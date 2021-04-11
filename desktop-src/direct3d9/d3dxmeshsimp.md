---
description: Gibt Vereinfachungs Optionen für ein Mesh an.
ms.assetid: f03170bd-7d2a-4839-9aec-c29426b95437
title: D3DXMESHSIMP-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHSIMP
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: faf4244d115076b6b04cd04697acf789172d9b11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132333"
---
# <a name="d3dxmeshsimp-enumeration"></a>D3DXMESHSIMP-Enumeration

Gibt Vereinfachungs Optionen für ein Mesh an.

## <a name="syntax"></a>Syntax


```C++
enum _D3DXMESHSIMP {
  D3DXMESHSIMP_VERTEX  = 1, 
  D3DXMESHSIMP_FACE    = 2 

};
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXMESHSIMP_VERTEX"></span><span id="d3dxmeshsimp_vertex"></span>**D3DXMESHSIMP \_ Scheitelpunkt**
</dt> <dd>

Das Mesh wird um die Anzahl der im MinValue-Parameter angegebenen Scheitel Punkte vereinfacht.

</dd> <dt>

<span id="D3DXMESHSIMP_FACE"></span><span id="d3dxmeshsimp_face"></span>**D3DXMESHSIMP \_**
</dt> <dd>

Das Mesh wird durch die Anzahl der im MinValue-Parameter angegebenen Gesichter vereinfacht.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXSimplifyMesh**](d3dxsimplifymesh.md)
</dt> </dl>

 

 




