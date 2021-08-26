---
description: Weitergeben von Zustandsänderungen, die innerhalb eines aktiven Durchlaufs an das Gerät auftreten, bevor das Rendering durchgeführt wird.
ms.assetid: 3a779b63-c106-4a81-afeb-82bd6e556de4
title: ID3DXEffect::CommitChanges-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CommitChanges
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5b81cd2674e08473358e031b827528121537264df11dba54c6a1f610ac054ee4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951760"
---
# <a name="id3dxeffectcommitchanges-method"></a>ID3DXEffect::CommitChanges-Methode

Weitergeben von Zustandsänderungen, die innerhalb eines aktiven Durchlaufs an das Gerät auftreten, bevor das Rendering durchgeführt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT CommitChanges();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

Wenn die Anwendung einen Effektzustand mithilfe einer der [**ID3DXEffect::Setx-Methoden**](id3dxeffect.md) innerhalb eines [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) / [**ID3DXEffect::EndPass-Abgleichspaars**](id3dxeffect--endpass.md) ändert, muss die Anwendung **ID3DXEffect::CommitChanges** vor einem DrawxPrimitive-Aufruf aufrufen, um Zustandsänderungen vor dem Rendern an das Gerät weiterzuleiten. Wenn innerhalb eines **ID3DXEffect::BeginPass-** und **ID3DXEffect::EndPass-Paars** keine Zustandsänderungen auftreten, ist es nicht erforderlich, **ID3DXEffect::CommitChanges** aufzurufen.

Dies unterscheidet sich bei allen freigegebenen Parametern in einem geklonten Effekt geringfügig. Wenn eine Technik für einen geklonten Effekt aktiv ist (d. h. wenn [**ID3DXEffect::Begin**](id3dxeffect--begin.md) aufgerufen wurde, aber [**ID3DXEffect::End**](id3dxeffect--end.md) nicht aufgerufen wurde), aktualisiert **ID3DXEffect::CommitChanges** Parameter, die nicht wie erwartet freigegeben werden. Um einen freigegebenen Parameter zu aktualisieren (nur für einen geklonten Effekt, dessen Technik aktiv ist), rufen Sie **ID3DXEffect::End** auf, um die Technik zu deaktivieren, und **ID3DXEffect::Begin,** um die Technik vor dem Aufruf von **ID3DXEffect::CommitChanges** erneut zu aktivieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




