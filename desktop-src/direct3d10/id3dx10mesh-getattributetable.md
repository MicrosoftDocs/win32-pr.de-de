---
description: 'ID3DX10Mesh::GetAttributeTable-Methode: Ruft entweder eine Attributtabelle für ein Gitternetz oder die Anzahl der einträge ab, die in einer Attributtabelle für ein Gitternetz gespeichert sind.'
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
ms.openlocfilehash: ce1f2464882bfdece8997aeea23f2bb42c276b3f6ce49b13cb242d517a522250
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540290"
---
# <a name="id3dx10meshgetattributetable-method"></a>ID3DX10Mesh::GetAttributeTable-Methode

Ruft entweder eine Attributtabelle für ein Gitternetz oder die Anzahl der Einträge ab, die in einer Attributtabelle für ein Gitternetz gespeichert sind.

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

Zeiger auf ein Array von D3DX10 \_ ATTRIBUTE \_ RANGE-Strukturen, das die Einträge in der Attributtabelle des Gitternetzes darstellt. Geben Sie **NULL** an, um den Wert für pAttribTableSize abzurufen.

</dd> <dt>

*pAttribTableSize* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Zeiger auf die Anzahl der in pAttribTable gespeicherten Einträge oder auf einen Wert, der mit der Anzahl von Einträgen gefüllt werden soll, die in der Attributtabelle für das Gitternetz gespeichert sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

## <a name="remarks"></a>Hinweise

Eine Attributtabelle wird verwendet, um Bereiche des Gitternetzes zu identifizieren, die mit unterschiedlichen Texturen, Renderzuständen, Materialien usw. gezeichnet werden müssen. Darüber hinaus kann die Anwendung die Attributtabelle verwenden, um Teile eines Gitternetzes auszublenden, indem beim Zeichnen des Rahmens kein angegebener Attributbezeichner gezeichnet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
