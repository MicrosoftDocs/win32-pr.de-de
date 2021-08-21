---
description: 'ID3DXEffectStateManager::SetVertexShaderConstantB-Methode: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von booleschen Vertexshader-Shaderkonstanten festzulegen.'
ms.assetid: 25fd0c68-11b5-4401-a2f8-86075ba3fa54
title: ID3DXEffectStateManager::SetVertexShaderConstantB-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantB
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0db8c141f16a14db57e5d6867a9894399bacf5a5cebb7c7e14a2592ea7f09bff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121436"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantb-method"></a>ID3DXEffectStateManager::SetVertexShaderConstantB-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von booleschen Vertex-Shaderkonstanten festzulegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetVertexShaderConstantB(
  [out]       UINT StartRegister,
  [out] const BOOL *pConstantData,
  [out]       UINT RegisterCount
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

Typ: **const [**BOOL**](../winprog/windows-data-types.md) \***

Ein Array von booleschen Konstanten.

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
-   Der Dynamische Effektzustandsaufruf (z.B. [**IDirect3DDevice9::SetVertexShaderConstantB)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)schlägt fehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
