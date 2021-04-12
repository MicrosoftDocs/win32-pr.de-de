---
description: Ruft den Scheitelpunkt Wert fester Funktion ab.
ms.assetid: 9b80c4b9-2e5b-4965-99b9-ad6c459ef413
title: 'ID3DXSkinInfo:: getf VF-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6d48cd9cea6efd6cb43e6da6877a7aaf42909c71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354067"
---
# <a name="id3dxskininfogetfvf-method"></a>ID3DXSkinInfo:: getf VF-Methode

Ruft den Scheitelpunkt Wert fester Funktion ab.

## <a name="syntax"></a>Syntax


```C++
DWORD GetFVF();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt die flexiblen Vertexformatcodes (FVF) zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode kann 0 zurückgeben, wenn das Vertex-Format nicht direkt einem FVF-Code zugeordnet werden kann. Dies geschieht bei einem Mesh, das aus einer Scheitelpunkt Deklaration erstellt wurde, die nicht die gleiche Reihenfolge und dieselben Elemente hat, die von den f

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo:: setf VF**](id3dxskininfo--setfvf.md)
</dt> </dl>

 

 
