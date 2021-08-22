---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Licht zu setzen.
ms.assetid: 3b9b2cbd-79f5-4ea4-a47b-da23b091adfd
title: ID3DXEffectStateManager::SetLight-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetLight
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 83250450a0510949267ffd52f17e6e9013a646d40229efcf7d5bcc7a396e1b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119372080"
---
# <a name="id3dxeffectstatemanagersetlight-method"></a>ID3DXEffectStateManager::SetLight-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Licht zu setzen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetLight(
  [in]       DWORD     Index,
  [in] const D3DLight9 *pLight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Der nullbasierte Index des Lichts. Dies ist derselbe Index in [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).

</dd> <dt>

*pLight* \[ In\]
</dt> <dd>

Typ: **const [**D3DLight9**](d3dlight9.md) \***

Das light-Objekt. Siehe [**D3DLIGHT9**](d3dlight9.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Gerätestatus fehlschlägt, tritt eine der folgenden Bedingungen auf:

-   Die Auswirkung tritt während [**ID3DXEffect::BeginPass auf.**](id3dxeffect--beginpass.md)
-   Der Dynamische Effektzustandsaufruf (z. B. [**IDirect3DDevice9::SetLight)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)tritt ein Fehler auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
