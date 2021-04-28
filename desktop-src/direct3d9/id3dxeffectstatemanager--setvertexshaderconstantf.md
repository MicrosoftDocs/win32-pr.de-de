---
description: 'ID3DXEffectStateManager::SetVertexShaderConstantF-Methode: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von Vertexshader-Gleitkommakonstanten festzulegen.'
ms.assetid: 3a13040d-5d5a-4454-bf11-cda9653585c0
title: ID3DXEffectStateManager::SetVertexShaderConstantF-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ffbad3c695758a0388baf8161c322c1ff423699b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090388"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantf-method"></a>ID3DXEffectStateManager::SetVertexShaderConstantF-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von Vertex-Shader-Gleitkommakonstanten festzulegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetVertexShaderConstantF(
  [out]       UINT  StartRegister,
  [out] const FLOAT *pConstantData,
  [out]       UINT  RegisterCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StartRegister* \[ out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Der nullbasierte Index des ersten Konstantenregisters.

</dd> <dt>

*pConstantData* \[ out\]
</dt> <dd>

Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Ein Array von Gleitkommakonstanten.

</dd> <dt>

*RegisterCount* \[ out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der Register in pConstantData.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Gerätezustands fehlschlägt, tritt eine der folgenden Schritte auf:

-   Die Auswirkung schlägt während [**id3DXEffect::BeginPass**](id3dxeffect--beginpass.md)fehl.
-   Der Dynamische Effektzustandsaufruf (z.B. [**IDirect3DDevice9::SetVertexShaderConstantF)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)schlägt fehl.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
