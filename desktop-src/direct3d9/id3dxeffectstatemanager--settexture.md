---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um eine Textur festlegen zu können.
ms.assetid: 971802f4-ea7a-4906-83b8-0cd83111716e
title: ID3DXEffectStateManager::SetTexture-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 96ed2d8abfd7cb815292c81e6cc9feb2ae84c184cded3b5c5a808dbb4456598f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118521246"
---
# <a name="id3dxeffectstatemanagersettexture-method"></a>ID3DXEffectStateManager::SetTexture-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um eine Textur festlegen zu können.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTexture(
  [in] DWORD                  Stage,
  [in] LPDIRECT3DBASETEXTURE9 pTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Phase* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Die Stufe, der die Textur zugewiesen wird. Dies ist der Indexwert in [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) oder [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).

</dd> <dt>

*pTexture* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Ein Zeiger auf das Texturobjekt. Dies kann einer der Direct3D-Texturtypen (Cube, Volume usw.) sein. Siehe [**IDirect3DBaseTexture9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Gerätestatus fehlschlägt, tritt eine der folgenden Bedingungen auf:

-   Die Auswirkung tritt während [**ID3DXEffect::BeginPass auf.**](id3dxeffect--beginpass.md)
-   Der Dynamische Effektzustandsaufruf (z. B. [**IDirect3DDevice9::SetTexture)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)tritt ein Fehler auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
