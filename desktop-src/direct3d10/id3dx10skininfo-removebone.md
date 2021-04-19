---
description: Entfernt einen Knochen.
ms.assetid: efb88108-5c76-47c8-b8ce-1ba29cb18ba4
title: 'ID3DX10SkinInfo:: removebone-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemoveBone
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 49fd24c5661bbedb7fb839171fa4a835f07e446a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367370"
---
# <a name="id3dx10skininforemovebone-method"></a>ID3DX10SkinInfo:: removebone-Methode

Entfernt einen Knochen.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveBone(
  [in] UINT Index
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Ein Index, der angibt, welcher zu entfernende Knochen Muss zwischen 0 und dem von [**ID3DX10SkinInfo:: getnumbones**](id3dx10skininfo-getnumbones.md)zurückgegebenen Wert liegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: E \_ invalidArg.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
