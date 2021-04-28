---
description: 'ID3DXEffectStateManager::SetVertexShaderConstantI-Methode: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von ganzzahligen Vertexshaderkonstanten festlegen zu können.'
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
ms.openlocfilehash: c129e3e01fe6fbae6ba7ede1b9ea8c4bee5338a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090398"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstanti-method"></a>ID3DXEffectStateManager::SetVertexShaderConstantI-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von ganzzahligen Vertex-Shaderkonstten festlegen zu können.

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

Der nullbasierte Index des ersten konstanten Registers.

</dd> <dt>

*pConstantData* \[ out\]
</dt> <dd>

Typ: **const [**INT**](../winprog/windows-data-types.md) \***

Ein Array von ganzzahligen Konstanten.

</dd> <dt>

*RegisterCount* \[ out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der Register in pConstantData.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Gerätestatus fehlschlägt, tritt eine der folgenden Bedingungen auf:

-   Die Auswirkung tritt während [**ID3DXEffect::BeginPass auf.**](id3dxeffect--beginpass.md)
-   Beim Dynamischen Effektzustandsaufruf (z. B. [**IDirect3DDevice9::SetVertexShaderConstantI)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)tritt ein Fehler auf.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
