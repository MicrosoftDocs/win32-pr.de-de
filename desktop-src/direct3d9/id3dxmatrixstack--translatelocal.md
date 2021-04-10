---
description: Bestimmt das Produkt der berechneten Übersetzungs Matrix, die durch die angegebenen Faktoren (x, y und z) und die aktuelle Matrix bestimmt wird.
ms.assetid: d4752a6c-2114-4016-a69f-dcc561d2c76b
title: 'ID3DXMATRIXStack:: translatelocal-Methode (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.TranslateLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 784e623ae47dfece9b395d423437fb6ce661b223
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219594"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx9mathh"></a>ID3DXMATRIXStack:: translatelocal-Methode (D3dx9math. h)

Bestimmt das Produkt der berechneten Übersetzungs Matrix, die durch die angegebenen Faktoren (x, y und z) und die aktuelle Matrix bestimmt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT TranslateLocal(
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

Der Übersetzungs Faktor in der x-Richtung.

</dd> <dt>

*j* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der Übersetzungs Faktor in y-Richtung.

</dd> <dt>

*z* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der Übersetzungs Faktor in der z-Richtung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode wird die aktuelle Matrix mit der berechneten Übersetzungs Matrix Links multipliziert (die Transformation ist der lokale Ursprung des Objekts).


```
    
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
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

[**ID3DXMATRIXStack:: Translation**](id3dxmatrixstack--translate.md)
</dt> </dl>

 

 
