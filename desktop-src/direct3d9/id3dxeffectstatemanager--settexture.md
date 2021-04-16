---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um eine Textur festzulegen.
ms.assetid: 971802f4-ea7a-4906-83b8-0cd83111716e
title: 'ID3DXEffectStateManager:: SetTexture-Methode (D3DX9Effect. h)'
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
ms.openlocfilehash: b395c19b65bb39b8328da24f727292f7dbe2a0f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530974"
---
# <a name="id3dxeffectstatemanagersettexture-method"></a>ID3DXEffectStateManager:: SetTexture-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um eine Textur festzulegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTexture(
  [in] DWORD                  Stage,
  [in] LPDIRECT3DBASETEXTURE9 pTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Stage* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Die Stufe, der die Textur zugewiesen wird. Dies ist der Indexwert in [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) oder [**IDirect3DDevice9:: settexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).

</dd> <dt>

*ptexture* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Ein Zeiger auf das Textur Objekt. Dabei kann es sich um einen beliebigen Direct3D-Textur Typen (Cube, Volume usw.) handeln. Siehe [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:

-   Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.
-   Der dynamische Effekt Zustands Aufrufe (z. b. [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)) schlägt fehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
