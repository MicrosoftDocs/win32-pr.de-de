---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen Vertex-Shader festlegen zu können.
ms.assetid: 8f3d3be3-c073-441d-a318-6d2cd5e7aca5
title: ID3DXEffectStateManager::SetVertexShader-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5f52daf5174608985b18140d2e6efde849f0bd6292c00584ece3453cca33ebf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520922"
---
# <a name="id3dxeffectstatemanagersetvertexshader-method"></a>ID3DXEffectStateManager::SetVertexShader-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen Vertex-Shader festlegen zu können.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetVertexShader(
  [in] LPDIRECT3DVERTEXSHADER9 pShader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pShader* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)**

Ein Zeiger auf ein Vertex-Shaderobjekt. Siehe [**IDirect3DVertexShader9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Gerätestatus fehlschlägt, tritt eine der folgenden Bedingungen auf:

-   Die Auswirkung tritt während [**ID3DXEffect::BeginPass auf.**](id3dxeffect--beginpass.md)
-   Der Dynamische Effektzustandsaufruf (z. B. [**IDirect3DDevice9::SetVertexShader)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)tritt ein Fehler auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
