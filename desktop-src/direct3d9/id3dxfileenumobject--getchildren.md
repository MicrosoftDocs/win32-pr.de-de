---
description: Ruft die Anzahl der untergeordneten Objekte in diesem Dateidatenobjekt ab.
ms.assetid: 4409819f-a346-40b1-8e12-86e8128ece47
title: ID3DXFileEnumObject::GetChildren-Methode (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChildren
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 857a52692fe0ef2390628f0d838129e6e00d1202e7615577f1e2e20b2ce74268
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121406"
---
# <a name="id3dxfileenumobjectgetchildren-method"></a>ID3DXFileEnumObject::GetChildren-Methode

Ruft die Anzahl der untergeordneten Objekte in diesem Dateidatenobjekt ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetChildren(
  [in] SIZE_T *puiChildren
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*puiChildren* \[ In\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)\***

Adresse eines Zeigers zum Empfangen der Anzahl der untergeordneten Objekte in diesem Dateidatenobjekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, wird der folgende Wert zurückgegeben: D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
