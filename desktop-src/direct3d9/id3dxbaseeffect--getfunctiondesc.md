---
description: Ruft eine Funktionsbeschreibung ab.
ms.assetid: a1a0ccf4-2428-4e60-9af0-07dc2132a367
title: ID3DXBaseEffect::GetFunctionDesc-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b8f74715b163b3d197f62274c6aa6bf52ae872254db9df8225e061dc54900964
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893720"
---
# <a name="id3dxbaseeffectgetfunctiondesc-method"></a>ID3DXBaseEffect::GetFunctionDesc-Methode

Ruft eine Funktionsbeschreibung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFunctionDesc(
  [in]  D3DXHANDLE        hFunction,
  [out] D3DXFUNCTION_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFunction* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Funktionshand handle. Siehe [Handles (Direct3D 9).](handles.md)

</dd> <dt>

*pDesc* \[ out\]
</dt> <dd>

Typ: **[ **D3DXFUNCTION \_ DESC**](d3dxfunction-desc.md)\***

Gibt eine Beschreibung der Funktion zurück. Siehe [**D3DXFUNCTION \_ DESC**](d3dxfunction-desc.md).

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

 

 




