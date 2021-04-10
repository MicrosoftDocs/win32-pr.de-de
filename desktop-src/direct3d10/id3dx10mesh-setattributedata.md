---
description: Legen Sie die Attributdaten des Mesh fest.
ms.assetid: bcf7b1b3-b923-400a-8d12-5094f3844d8f
title: 'ID3DX10Mesh:: stattributedata-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 19d69f8747196d7b25c85cb04fb173adef193098
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219610"
---
# <a name="id3dx10meshsetattributedata-method"></a>ID3DX10Mesh:: stattributedata-Methode

Legen Sie die Attributdaten des Mesh fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetAttributeData(
  [in] const UINT *pData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* \[ in\]
</dt> <dd>

Typ: Konstante **[**uint**](../winprog/windows-data-types.md) \***

Die festzulegenden Attributdaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

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

 

 
