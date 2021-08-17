---
description: Hier erhalten Sie den Effektzustands-Manager.
ms.assetid: 4a09eb2a-2393-40b0-81b9-3c27998c2b77
title: ID3DXEffect::GetStateManager-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6700447485d83f2610149b809065ab02140a2e6cf068508b6571d5132844fb0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121641"
---
# <a name="id3dxeffectgetstatemanager-method"></a>ID3DXEffect::GetStateManager-Methode

Hier erhalten Sie den Effektzustands-Manager.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStateManager(
  [out] LPD3DXEFFECTSTATEMANAGER *ppManager
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppManager* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***

Gibt einen Zeiger auf den Zustands-Manager zurück. Siehe [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

Der [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) ist eine vom Benutzer implementierte Schnittstelle, die Rückrufe in eine Anwendung einfing, um den Gerätezustand von einem Effekt aus zu setzen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::SetStateManager**](id3dxeffect--setstatemanager.md)
</dt> </dl>

 

 




