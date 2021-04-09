---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen Vertex-Shader festzulegen.
ms.assetid: 8f3d3be3-c073-441d-a318-6d2cd5e7aca5
title: 'ID3DXEffectStateManager:: setvertexshader-Methode (D3DX9Effect. h)'
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
ms.openlocfilehash: 9fd25158f2aa6ab0a22d6226e8e709c3b498b0e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870159"
---
# <a name="id3dxeffectstatemanagersetvertexshader-method"></a>ID3DXEffectStateManager:: setvertexshader-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen Vertex-Shader festzulegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetVertexShader(
  [in] LPDIRECT3DVERTEXSHADER9 pShader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pshader* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)**

Ein Zeiger auf ein Vertex-Shader-Objekt. Siehe [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:

-   Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.
-   Der dynamische Effekt Zustands Aufrufe (z. b. [**IDirect3DDevice9:: setvertexshader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)) schlägt fehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
