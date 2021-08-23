---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den Texturphasenzustand festlegen zu können.
ms.assetid: cc86a483-ccf0-400d-b14d-ab55a3cf4b98
title: ID3DXEffectStateManager::SetTextureStageState-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTextureStageState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5a74642d97532020679749d54924f4ab4052100d638d2bbd902b7b721fc75610
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520985"
---
# <a name="id3dxeffectstatemanagersettexturestagestate-method"></a>ID3DXEffectStateManager::SetTextureStageState-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den Texturphasenzustand festlegen zu können.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTextureStageState(
  [in] DWORD                    Stage,
  [in] D3DTEXTURESTAGESTATETYPE Type,
  [in] DWORD                    Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Phase* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Die Stufe, der die Textur zugewiesen ist. Dies ist der Indexwert in [**IDirect3DDevice9::SetTexture**](/windows/desktop/api) oder [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).

</dd> <dt>

*Typ* \[ In\]
</dt> <dd>

Typ: **[ **D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)**

Definiert den Typ des Vorgangs, der von einer Texturphase durchgeführt wird. Siehe [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).

</dd> <dt>

*Wert* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kann entweder ein Vorgang ([**D3DTEXTUREOP**](./d3dtextureop.md)) oder ein Argumentwert ([D3DTA](d3dta.md)) sein, je nachdem, was für Type ausgewählt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Gerätestatus fehlschlägt, tritt eine der folgenden Bedingungen auf:

-   Die Auswirkung tritt während [**ID3DXEffect::BeginPass auf.**](id3dxeffect--beginpass.md)
-   Der Dynamische Effektzustandsaufruf (z. B. [**IDirect3DDevice9::SetTextureStageState)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)tritt ein Fehler auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
