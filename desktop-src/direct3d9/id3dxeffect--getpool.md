---
description: Ruft einen Zeiger auf den Pool von freigegebenen Parametern ab.
ms.assetid: 1e999fd5-76ef-43fa-8a77-ae6f2821f46d
title: 'ID3DXEffect:: getpool-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetPool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 18a35e9bc0a596cb88da6d4c1faf10941fbce8a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961564"
---
# <a name="id3dxeffectgetpool-method"></a>ID3DXEffect:: getpool-Methode

Ruft einen Zeiger auf den Pool von freigegebenen Parametern ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPool(
  [out] LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pppool* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***

Zeiger auf ein [**ID3DXEffectPool**](id3dxeffectpool.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Diese Methode gibt immer den Wert S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Pools enthalten freigegebene Parameter zwischen Effekten. Weitere Informationen finden Sie unter [Klonen und freigeben (Direct3D 9)](cloning-and-sharing.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




