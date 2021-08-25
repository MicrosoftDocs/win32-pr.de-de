---
description: 'ID3DXEffectStateManager::SetVertexShaderConstantI-Methode: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von ganzzahligen Vertexshaderkonstanten festzulegen.'
ms.assetid: 0035c97a-1b17-4665-9032-7b3b9a9d2cff
title: ID3DXEffectStateManager::SetVertexShaderConstantI-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantI
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 949f2cb23e15e3cfb99fcb6880795cfbd6019a8c858198b23bb9db6508714d44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856690"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstanti-method"></a>ID3DXEffectStateManager::SetVertexShaderConstantI-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von ganzzahligen Vertex-Shaderkonstanten festzulegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetVertexShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
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

Typ: **const [**INT**](../winprog/windows-data-types.md) \***

Ein Array ganzzahliger Konstanten.

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
-   Der Dynamische Effektzustandsaufruf (z.B. [**IDirect3DDevice9::SetVertexShaderConstantI)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)schlägt fehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
