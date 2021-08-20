---
description: Ruft einen Zeiger auf den Pool mit freigegebenen Parametern ab.
ms.assetid: 1e999fd5-76ef-43fa-8a77-ae6f2821f46d
title: ID3DXEffect::GetPool-Methode (D3DX9Effect.h)
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
ms.openlocfilehash: 0220b2864d6c668c2d4fbb71925da6452f6cc8661d0d931a379969418dfe7e19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118521226"
---
# <a name="id3dxeffectgetpool-method"></a>ID3DXEffect::GetPool-Methode

Ruft einen Zeiger auf den Pool mit freigegebenen Parametern ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPool(
  [out] LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppPool* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***

Zeiger auf ein [**ID3DXEffectPool-Objekt.**](id3dxeffectpool.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Diese Methode gibt immer den Wert S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Pools enthalten freigegebene Parameter zwischen Effekten. Weitere Informationen [finden Sie unter Klonen und Freigeben (Direct3D 9).](cloning-and-sharing.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




