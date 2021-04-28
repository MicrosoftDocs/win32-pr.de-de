---
description: 'ID3DX10Mesh::GetAttributeTable-Methode: Ruft entweder eine Attributtabelle für ein Gitternetz oder die Anzahl von Einträgen ab, die in einer Attributtabelle für ein Gitternetz gespeichert sind.'
ms.assetid: cee49eba-c113-49f5-a702-c366401f1f2d
title: ID3DX10Mesh::GetAttributeTable-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e7fc503af1a290b27fea81d0c2aba6b84393323b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083988"
---
# <a name="id3dx10meshgetattributetable-method"></a>ID3DX10Mesh::GetAttributeTable-Methode

Ruft entweder eine Attributtabelle für ein Gitternetz oder die Anzahl von Einträgen ab, die in einer Attributtabelle für ein Gitternetz gespeichert sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAttributeTable(
  [in] D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in] UINT                   *pAttribTableSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAttribTable* \[ In\]
</dt> <dd>

Typ: **[ **D3DX10-ATTRIBUTBEREICH \_ \_**](d3dx10-attribute-range.md)\***

Zeiger auf ein Array von D3DX10 ATTRIBUTE RANGE-Strukturen, die die Einträge \_ in der \_ Attributtabelle des Gitters darstellen. Geben **Sie NULL** an, um den Wert für pAttribTableSize abzurufen.

</dd> <dt>

*pAttribTableSize* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Zeiger auf die Anzahl der in pAttribTable gespeicherten Einträge oder auf einen Wert, der mit der Anzahl von Einträgen aufgefüllt werden soll, die in der Attributtabelle für das Gitternetz gespeichert sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Bemerkungen

Eine Attributtabelle wird verwendet, um Bereiche des Gitters zu identifizieren, die mit unterschiedlichen Texturen, Renderzuständen, Materialien und so weiter gezeichnet werden müssen. Darüber hinaus kann die Anwendung die Attributtabelle verwenden, um Teile eines Gitters auszublenden, indem beim Zeichnen des Rahmens kein angegebener Attributbezeichner gezeichnunget wird.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
