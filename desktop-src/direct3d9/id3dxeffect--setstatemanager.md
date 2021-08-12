---
description: Legen Sie den Effektzustands-Manager fest.
ms.assetid: 87409687-03f1-4593-ae58-3a8ba08e592b
title: ID3DXEffect::SetStateManager-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 06b6a7404f664e8ec18247b2eda57c5097cd575a3556853bfe8a9eb67705d071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295903"
---
# <a name="id3dxeffectsetstatemanager-method"></a>ID3DXEffect::SetStateManager-Methode

Legen Sie den Effektzustands-Manager fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetStateManager(
  [in] LPD3DXEFFECTSTATEMANAGER pManager
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pManager* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)**

Ein Zeiger auf den Zustands-Manager. Siehe [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

Der [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) ist eine vom Benutzer implementierte Schnittstelle, die Rückrufe in eine Anwendung überfingt, um den Gerätezustand von einem Effekt aus zu setzen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::GetStateManager**](id3dxeffect--getstatemanager.md)
</dt> </dl>

 

 




