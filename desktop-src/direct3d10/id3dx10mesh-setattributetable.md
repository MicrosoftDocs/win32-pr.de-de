---
description: Legt die Attribut Tabelle für ein Mesh und die Anzahl der in der Tabelle gespeicherten Einträge fest.
ms.assetid: 629fd31b-d88a-4650-82ed-ab7c40690986
title: ID3DX10Mesh::-Methode (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 808349b3f7456ebf3f8e1c3a7f9fdf2236db4beb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219609"
---
# <a name="id3dx10meshsetattributetable-method"></a>ID3DX10Mesh::-Methode

Legt die Attribut Tabelle für ein Mesh und die Anzahl der in der Tabelle gespeicherten Einträge fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetAttributeTable(
  [in] const D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in]       UINT                   cAttribTableSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pattribtable* \[ in\]
</dt> <dd>

Type: **Konstanten [**d3dx10 \_ Attribut \_ Bereich**](d3dx10-attribute-range.md) \***

Ein Zeiger auf ein Array von d3dx10- \_ Attribut \_ Bereichs Strukturen, die die Einträge in der Tabelle des Mesh-Attributs darstellen.

</dd> <dt>

"" "" "".  \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl von Attributen in der Tabelle "Mesh-Attribut".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="remarks"></a>Bemerkungen

Wenn eine Anwendung die Informationen in einer Attribut Tabelle nachverfolgt und die Tabelle als Ergebnis von Änderungen an Attributen oder Gesichtern neu anordnet, ermöglicht diese Methode der Anwendung, die Attribut Tabellen zu aktualisieren, anstatt ID3DX10Mesh:: optimiert erneut aufzurufende.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
