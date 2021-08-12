---
description: Ruft einen Parameter oder eine Anmerkungsbeschreibung ab.
ms.assetid: fd54eb08-a7e4-4106-b0ed-49a4da7fcadc
title: ID3DXBaseEffect::GetParameterDesc-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8c60332909ef601d58cb624201bae6e1934a84699ead1227a5d8a83c2db64dc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118296703"
---
# <a name="id3dxbaseeffectgetparameterdesc-method"></a>ID3DXBaseEffect::GetParameterDesc-Methode

Ruft einen Parameter oder eine Anmerkungsbeschreibung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetParameterDesc(
  [in]  D3DXHANDLE         hParameter,
  [out] D3DXPARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hParameter* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Parameter- oder Anmerkungshand handle. Siehe [Handles (Direct3D 9).](handles.md)

</dd> <dt>

*pDesc* \[ out\]
</dt> <dd>

Typ: **[ **D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md)\***

Gibt eine Beschreibung des angegebenen Parameters oder der Anmerkung zurück. Siehe [**D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




