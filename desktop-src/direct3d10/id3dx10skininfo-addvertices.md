---
description: Ordnen Sie Speicherplatz für zusätzliche Scheitelräume zu.
ms.assetid: dd6445ea-4754-4ba3-a264-59295325ee08
title: ID3DX10SkinInfo::AddVertices-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 232778cdec6c8ab1c4874c6dcef3cadb9b1492d12fe1d4d60d787a484a3425c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302466"
---
# <a name="id3dx10skininfoaddvertices-method"></a>ID3DX10SkinInfo::AddVertices-Methode

Ordnen Sie Speicherplatz für zusätzliche Scheitelräume zu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddVertices(
  [in] UINT Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anzahl* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der hinzuzufügenden Scheitelzeichen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn diese Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert E \_ OUTOFMEMORY sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
