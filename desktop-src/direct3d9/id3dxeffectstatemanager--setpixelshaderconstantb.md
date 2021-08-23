---
description: 'ID3DXEffectStateManager::SetPixelShaderConstantB-Methode: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von booleschen Vertexshaderkonstanten festzulegen.'
ms.assetid: ad4d9beb-fd34-4574-9787-61bd3bfaaaaa
title: ID3DXEffectStateManager::SetPixelShaderConstantB-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantB
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d293aff7faafe1451c73bc423cabdd3ceec2a1e5cfb6637075108f4862fd6ba3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893600"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstantb-method"></a>ID3DXEffectStateManager::SetPixelShaderConstantB-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von booleschen Vertex-Shaderkonstanten festzulegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPixelShaderConstantB(
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
-   Der Dynamische Effektzustandsaufruf (z.B. [**IDirect3DDevice9::SetPixelShaderConstantB)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)schlägt fehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
