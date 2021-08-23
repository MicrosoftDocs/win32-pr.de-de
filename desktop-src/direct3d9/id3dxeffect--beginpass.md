---
description: Startet einen Durchlauf innerhalb der aktiven Technik.
ms.assetid: fbb2bf1c-e37a-4117-8c3c-5f5b6a267301
title: ID3DXEffect::BeginPass-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9013a67c2d4e0e9760167bc979ac05edd4879c5414ce5c9b9c55528baf3f6a18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987545"
---
# <a name="id3dxeffectbeginpass-method"></a>ID3DXEffect::BeginPass-Methode

Startet einen Durchlauf innerhalb der aktiven Technik.

## <a name="syntax"></a>Syntax


```C++
HRESULT BeginPass(
  [in] UINT Pass
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Übergeben* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Ein nullbasierter ganzzahliger Index in die Technik.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

Eine Anwendung legt einen aktiven Durchlauf (innerhalb einer aktiven Technik) im Effektsystem fest, indem **ID3DXEffect::BeginPass** aufgerufen wird. Eine Anwendung signalisiert das Ende des aktiven Durchlaufs, indem [**sie ID3DXEffect::EndPass**](id3dxeffect--endpass.md)aufruft. **ID3DXEffect::BeginPass** und **ID3DXEffect::EndPass** müssen in einem übereinstimmenden Paar innerhalb eines übereinstimmenden Paars von [**ID3DXEffect::Begin-**](id3dxeffect--begin.md) und [**ID3DXEffect::End-Aufrufen**](id3dxeffect--end.md) auftreten.

Wenn die Anwendung einen Effektzustand mithilfe einer der [**Effect::Setx-Methoden**](id3dxeffect.md) innerhalb eines **ID3DXEffect::BeginPass** / [**ID3DXEffect::EndPass-Abgleichspaars**](id3dxeffect--endpass.md) ändert, muss die Anwendung [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) aufrufen, um das Gerät mit den Zustandsänderungen zu aktualisieren. Wenn innerhalb eines **ID3DXEffect::BeginPass-** und **ID3DXEffect::EndPass-Paars** keine Zustandsänderungen auftreten, ist es nicht erforderlich, **ID3DXEffect::CommitChanges** aufzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
