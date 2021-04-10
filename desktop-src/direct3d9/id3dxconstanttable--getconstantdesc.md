---
description: Ruft einen Zeiger auf ein Array konstanter Beschreibungen in der Konstanten Tabelle ab.
ms.assetid: bd407fd6-b1cc-4197-ae98-1c2ca74d2ad0
title: 'ID3DXConstantTable:: getconstantdesc-Methode (D3DX9Shader. h)'
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
ms.openlocfilehash: e5574c72fabd7561da0c60c903ae815faaebbfd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961624"
---
# <a name="id3dxconstanttablegetconstantdesc-method"></a>ID3DXConstantTable:: getconstantdesc-Methode

Ruft einen Zeiger auf ein Array konstanter Beschreibungen in der Konstanten Tabelle ab.

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

*hconstant* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für eine Konstante. Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).

</dd> <dt>

*PDE SC* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)\***

Gibt einen Zeiger auf ein Array von Beschreibungen zurück. Weitere Informationen finden Sie unter [**D3DXCONSTANT \_**](d3dxconstant-desc.md).

</dd> <dt>

*pcount* \[ in, out\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Die angegebene Eingabe muss die maximale Größe des Arrays sein. Bei der Ausgabe handelt es sich um die Anzahl der Elemente, die im Array aufgefüllt werden, wenn die Funktion zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="remarks"></a>Bemerkungen

**ID3DXConstantTable:: getconstantdesc** gibt manchmal einen [**D3DXCONSTANT- \_**](d3dxconstant-desc.md) Wert mit \_ der Register Anzahl 0 zurück. Dies geschieht, wenn eine Konstante in mehr als einem Register \_ Satz enthalten ist, aber keinen Platz in diesem zugeordneten Register Satz hat.

Da ein Sampler mehrmals in einer Konstanten Tabelle vorkommen kann, kann diese Methode ein Array von Beschreibungen zurückgeben, von denen jedes einen anderen Registrierungs Index hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> <dt>

[**ID3DXConstantTable:: getdebug**](id3dxconstanttable--getdesc.md)
</dt> </dl>

 

 
