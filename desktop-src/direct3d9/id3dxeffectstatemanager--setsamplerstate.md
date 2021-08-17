---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen Sampler festlegen zu können.
ms.assetid: 1e19e8cd-341d-4372-9182-8b3c82155407
title: ID3DXEffectStateManager::SetSamplerState-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetSamplerState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0227335c2110590439873b965b2d1393a42dd575bf530ce83aae5228547fda26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121476"
---
# <a name="id3dxeffectstatemanagersetsamplerstate-method"></a>ID3DXEffectStateManager::SetSamplerState-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen Sampler festlegen zu können.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSamplerState(
  [in] DWORD               Sampler,
  [in] D3DSAMPLERSTATETYPE Type,
  [in] DWORD               Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sampler* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Die nullbasierte Samplernummer.

</dd> <dt>

*Typ* \[ In\]
</dt> <dd>

Typ: **[ **D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)**

Identifiziert den Samplerzustand, der die Filterung, Adressierung oder Die Rahmenfarbe angeben kann. Siehe [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md).

</dd> <dt>

*Wert* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Ein Wert aus einem der Samplerzustandstypen in Type.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Gerätestatus fehlschlägt, tritt eine der folgenden Bedingungen auf:

-   Die Auswirkung tritt während [**ID3DXEffect::BeginPass auf.**](id3dxeffect--beginpass.md)
-   Der Dynamische Effektzustandsaufruf (z. B. [**IDirect3DDevice9::SetSamplerState)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)tritt ein Fehler auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
