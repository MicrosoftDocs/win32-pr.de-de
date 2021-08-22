---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um eine Transformation festlegen zu können.
ms.assetid: 5d886554-ddb6-4b8a-a7fd-453e94b9516f
title: ID3DXEffectStateManager::SetTransform-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTransform
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 48b9bb16bdcb145b94e94de61ed011bb9931982511ddfb8ac9076d047c01ad0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121466"
---
# <a name="id3dxeffectstatemanagersettransform-method"></a>ID3DXEffectStateManager::SetTransform-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um eine Transformation festlegen zu können.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTransform(
  [in]       D3DTRANSFORMSTATETYPE State,
  [in] const D3DMATRIX             *pMatrix
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Status* \[ In\]
</dt> <dd>

Typ: **[ **D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)**

Der Typ der Transformation, auf die die Matrix angewendet werden soll. Siehe [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md).

</dd> <dt>

*pMatrix* \[ In\]
</dt> <dd>

Typ: **const [**D3DMATRIX**](d3dmatrix.md) \***

Eine Transformationsmatrix. Siehe [**D3DMATRIX**](d3dmatrix.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Gerätestatus fehlschlägt, tritt eine der folgenden Bedingungen auf:

-   Die Auswirkung tritt während [**ID3DXEffect::BeginPass auf.**](id3dxeffect--beginpass.md)
-   Der Dynamische Effektzustandsaufruf (z. B. [**IDirect3DDevice9::SetTransform)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)tritt ein Fehler auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
