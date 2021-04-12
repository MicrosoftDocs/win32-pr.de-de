---
description: Skalieren Sie die aktuelle Matrix über den Objekt Ursprung.
ms.assetid: fe71da67-c8c9-4c78-9055-9bc3cadc0780
title: 'ID3DXMATRIXStack:: scalelocal-Methode (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.ScaleLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05b188e3f1b0322225584bc0ef7c194c52ef949f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219461"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx9mathh"></a>ID3DXMATRIXStack:: scalelocal-Methode (D3dx9math. h)

Skalieren Sie die aktuelle Matrix über den Objekt Ursprung.

## <a name="syntax"></a>Syntax


```C++
HRESULT ScaleLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*x* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Die Skalierungs Komponente in der x-Richtung.

</dd> <dt>

*j* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Die Skalierungs Komponente in der y-Richtung.

</dd> <dt>

*z* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Die Skalierungs Komponente in der z-Richtung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.

## <a name="remarks"></a>Bemerkungen

Diese Methode multipliziert die aktuelle Matrix Links mit der berechneten Skalierungs Matrix. Die Transformation ist der lokale Ursprung des Objekts.


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack:: Scale**](id3dxmatrixstack--scale.md)
</dt> </dl>

 

 
