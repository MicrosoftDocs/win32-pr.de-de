---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den Renderzustand festzulegen.
ms.assetid: a5a27e30-c141-44a4-b8d4-38c1d6076b2a
title: ID3DXEffectStateManager::SetRenderState-Methode (D3DX9Effect.h)
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
ms.openlocfilehash: c7d34dae1d0789b80d896b72be7e35420daf587986ac2725e880b81597b15e88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119459620"
---
# <a name="id3dxeffectstatemanagersetrenderstate-method"></a>ID3DXEffectStateManager::SetRenderState-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den Renderzustand festzulegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetRenderState(
  [in] D3DRENDERSTATETYPE State,
  [in] DWORD              Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Status* \[ In\]
</dt> <dd>

Typ: **[ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**

Der festzulegende Renderzustand. [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)

</dd> <dt>

*Wert* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Der Renderzustandswert. Weitere Informationen finden Sie unter [Effect States (Direct3D 9) (Effektzustände (Direct3D 9)).](effect-states.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Gerätezustands fehlschlägt, tritt eine der folgenden Schritte auf:

-   Die Auswirkung schlägt während [**id3DXEffect::BeginPass**](id3dxeffect--beginpass.md)fehl.
-   Der Aufruf des Dynamischen Effektzustands (z.B. [**IDirect3DDevice9::SetRenderState)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)schlägt fehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
