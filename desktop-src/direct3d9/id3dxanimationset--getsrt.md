---
description: Ruft die Skalierungs-, Drehungs-und Übersetzungs Werte des Animations Satzes ab.
ms.assetid: 84fc56f3-15bf-4e27-ad06-57fab94f3a33
title: 'ID3DXAnimationSet:: getrt-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetSRT
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b70243dd9aa2f304d80eaff2e2cc7695dad43379
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355842"
---
# <a name="id3dxanimationsetgetsrt-method"></a>ID3DXAnimationSet:: gezrt-Methode

Ruft die Skalierungs-, Drehungs-und Übersetzungs Werte des Animations Satzes ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSRT(
  [in]  DOUBLE         PeriodicPosition,
  [in]  UINT           Animation,
  [out] D3DXVECTOR3    *pScale,
  [out] D3DXQUATERNION *pRotation,
  [out] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PeriodicPosition* \[ in\]
</dt> <dd>

Typ: **[ **Double**](../winprog/windows-data-types.md)**

Die Position des Animations Satzes. Die Position kann durch Aufrufen von [**ID3DXAnimationSet:: GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md)abgerufen werden.

</dd> <dt>

*Animation* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Animations Index.

</dd> <dt>

*pscale* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ein Zeiger auf den [**D3DXVECTOR3**](d3dxvector3.md) -Vektor, der die Skala des Animations Satzes beschreibt.

</dd> <dt>

*protation* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Ein Zeiger auf die [**D3DXQUATERNION**](d3dxquaternion.md) Quaternion, die die Drehung des Animations Satzes beschreibt.

</dd> <dt>

*ptranslation* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ein Zeiger auf den [**D3DXVECTOR3**](d3dxvector3.md) -Vektor, der die Übersetzung des Animations Satzes beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert. Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ . Andernfalls programmieren Sie die-Methode, um eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR**](./d3dxerr.md)zurückzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
