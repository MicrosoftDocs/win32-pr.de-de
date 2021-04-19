---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den gerengerzustand festzulegen.
ms.assetid: a5a27e30-c141-44a4-b8d4-38c1d6076b2a
title: 'ID3DXEffectStateManager:: strenderstate-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetRenderState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 111ab8ff379d5b095500101674fc45b6a2b31bc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355028"
---
# <a name="id3dxeffectstatemanagersetrenderstate-method"></a>ID3DXEffectStateManager:: strenderstate-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den gerengerzustand festzulegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetRenderState(
  [in] D3DRENDERSTATETYPE State,
  [in] DWORD              Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Status* \[ in\]
</dt> <dd>

Typ: **[ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**

Der festzulegende Rendering-Zustand. [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)

</dd> <dt>

*Wert* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Der Wert des Rendering-Zustands. Siehe [Effekt Zustände (Direct3D 9)](effect-states.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:

-   Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.
-   Der Status des dynamischen Effekts (z. b. [**IDirect3DDevice9:: strenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) schlägt fehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
