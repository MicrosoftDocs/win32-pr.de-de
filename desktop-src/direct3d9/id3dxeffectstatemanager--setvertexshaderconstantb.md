---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von booleschen Scheitelpunkt Konstanten für Vertex-Shader festzulegen.
ms.assetid: 25fd0c68-11b5-4401-a2f8-86075ba3fa54
title: 'ID3DXEffectStateManager:: setvertexshaderconstantb-Methode (D3DX9Effect. h)'
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
ms.openlocfilehash: 1eaf68f27d477aee36bd7773488f34bad29db61d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351967"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantb-method"></a>ID3DXEffectStateManager:: setvertexshaderconstantb-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Array von booleschen Scheitelpunkt Konstanten für Vertex-Shader festzulegen.

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

*Startregiester* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der null basierte Index des ersten Konstanten Registers.

</dd> <dt>

*pconstantdata* \[ vorgenommen\]
</dt> <dd>

Typ: Konstante **[**bool**](../winprog/windows-data-types.md) \***

Ein Array von booleschen Konstanten.

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
-   Der dynamische Effekt Status-aufrufen (z. [**b. IDirect3DDevice9:: setvertexshaderconstantb**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)) schlägt fehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
