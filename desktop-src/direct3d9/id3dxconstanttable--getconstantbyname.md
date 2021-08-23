---
description: 'ID3DXConstantTable::GetConstantByName-Methode: Ruft eine Konstante ab, indem deren Name nachgesehen wird.'
ms.assetid: 785a2d4f-6391-4419-a0b8-d8244a03ceae
title: ID3DXConstantTable::GetConstantByName-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 25458c14ee4d1d78388edb072fd80061778902e8cca476beaf7071c5f59aea9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675580"
---
# <a name="id3dxconstanttablegetconstantbyname-method"></a>ID3DXConstantTable::GetConstantByName-Methode

Ruft eine Konstante ab, indem deren Name nach gesucht wird.

## <a name="syntax"></a>Syntax


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hConstant* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für die übergeordnete Datenstruktur. Wenn die Konstante ein Parameter der obersten Ebene ist (es gibt keine übergeordnete Datenstruktur), verwenden Sie **NULL**.

</dd> <dt>

*pName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Name der Konstante.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt einen eindeutigen Bezeichner für die Konstante zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
