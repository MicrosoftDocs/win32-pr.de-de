---
description: Optionen zum Schweißen von Vertices.
ms.assetid: e73af63d-ed02-4fbc-8386-e8a40b0465ea
title: D3DXWELDEPSILONSFLAGS-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXWELDEPSILONSFLAGS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 9e67c8b0f0bf93c9da181a5bba9a694525bd9819
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355037"
---
# <a name="d3dxweldepsilonsflags-enumeration"></a>D3DXWELDEPSILONSFLAGS-Enumeration

Optionen zum Schweißen von Vertices.

## <a name="syntax"></a>Syntax


```C++
enum _D3DXWELDEPSILONSFLAGS {
  D3DXWELDEPSILONS_WELDALL              = 1, 
  D3DXWELDEPSILONS_WELDPARTIALMATCHES   = 2, 
  D3DXWELDEPSILONS_DONOTREMOVEVERTICES  = 4, 
  D3DXWELDEPSILONS_DONOTSPLIT           = 8 

};
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**D3DXWELDEPSILONS \_ weldall**
</dt> <dd>

Alle Scheitel Punkte, die sich am selben Speicherort befinden, werden verbunden. Durch die Verwendung dieses Flags wird ein Epsilon-Vergleich zwischen Scheitelpunkt Komponenten vermieden.

</dd> <dt>

<span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**D3DXWELDEPSILONS \_ weldpartialmatches**
</dt> <dd>

Wenn eine bestimmte Scheitelpunkt Komponente innerhalb von Epsilon liegt, ändern Sie teilweise übereinstimmende Scheitel Punkte, sodass beide Komponenten identisch sind. Wenn alle Komponenten gleich sind, entfernen Sie eine der Scheitel Punkte.

</dd> <dt>

<span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**D3DXWELDEPSILONS \_ donotrevevertices**
</dt> <dd>

Weist das Schweißen an, nur Änderungen an Scheitel Punkten zu ermöglichen und nicht zu entfernen. Dieses Flag ist nur gültig, wenn D3DXWELDEPSILONS \_ weldpartialmatches festgelegt ist. Es ist hilfreich, die Scheitel Punkte so zu ändern, dass Sie gleich sind, aber nicht, um Vertices zu entfernen.

</dd> <dt>

<span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**D3DXWELDEPSILONS \_ donotsplit**
</dt> <dd>

Weist das Schweißen an, Vertices nicht zu teilen, die sich in separaten Attribut Gruppen befinden. Wenn die [**ID3DXMesh:: optimiert**](id3dxmesh--optimize.md) -Methode mit dem D3DXMESHOPT \_ attrsort-Flag aufgerufen wird, wird das D3DXMESHOPT \_ donotsplit-Flag ebenfalls festgelegt. Durch Festlegen dieses Flags kann die Verarbeitung von Software Scheitel Punkten verlangsamt werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXWeldVertices**](d3dxweldvertices.md)
</dt> </dl>

 

 




