---
description: Ruft einen Zeiger auf ein Array konstanter Beschreibungen in der Konstantentabelle ab.
ms.assetid: bd407fd6-b1cc-4197-ae98-1c2ca74d2ad0
title: ID3DXConstantTable::GetConstantDesc-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8462ccfbbf306da08c67d460584a470d82301a5bda5f95a1ad09b2062702ee62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607210"
---
# <a name="id3dxconstanttablegetconstantdesc-method"></a>ID3DXConstantTable::GetConstantDesc-Methode

Ruft einen Zeiger auf ein Array konstanter Beschreibungen in der Konstantentabelle ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hConstant* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für eine Konstante. Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).

</dd> <dt>

*pDesc* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)\***

Gibt einen Zeiger auf ein Array von Beschreibungen zurück. Siehe [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md).

</dd> <dt>

*pCount* \[ in, out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Die bereitgestellte Eingabe muss die maximale Größe des Arrays sein. Die Ausgabe ist die Anzahl der Elemente, die im Array aufgefüllt werden, wenn die Funktion zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

**ID3DXConstantTable::GetConstantDesc** gibt manchmal einen [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md) mit der \_ Registeranzahl 0 zurück. Dies geschieht, wenn eine Konstante in mehr als einem Registersatz angezeigt wird, aber kein Speicherplatz \_ in diesem Registersatz zugeordnet ist.

Da ein Sampler in einer konstanten Tabelle mehr als einmal angezeigt werden kann, kann diese Methode ein Array von Beschreibungen zurückgeben, die jeweils einen anderen Registerindex haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> <dt>

[**ID3DXConstantTable::GetDesc**](id3dxconstanttable--getdesc.md)
</dt> </dl>

 

 
