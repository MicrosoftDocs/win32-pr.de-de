---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von Vertex-Shader-Gleit Komma Konstanten festzulegen.
ms.assetid: 3a13040d-5d5a-4454-bf11-cda9653585c0
title: 'ID3DXEffectStateManager:: setvertexshaderconstantf-Methode (D3DX9Effect. h)'
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
ms.openlocfilehash: 378af983e0ed7ca1709ae8bb6cfe8615a481b3f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353380"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantf-method"></a>ID3DXEffectStateManager:: setvertexshaderconstantf-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von Vertex-Shader-Gleit Komma Konstanten festzulegen.

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

*Startregiester* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der null basierte Index des ersten Konstanten Registers.

</dd> <dt>

*pconstantdata* \[ vorgenommen\]
</dt> <dd>

Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***

Ein Array von Gleit Komma Konstanten.

</dd> <dt>

*Register count* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Anzahl der Register in pconstantdata.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:

-   Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.
-   Der dynamische Effekt Zustands Aufrufe (z. b. [**IDirect3DDevice9:: setvertexshaderconstantf**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)) schlägt fehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
