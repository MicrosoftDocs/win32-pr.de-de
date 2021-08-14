---
description: Greifen Sie auf die Scheitelpunktbeschreibung zu, die an D3DX10CreateMesh übergeben wird. Die Scheitelpunktbeschreibung beschreibt das Layout der Scheitelpunktpuffer des Gitters.
ms.assetid: e4a4a98a-e131-414c-ad98-21288ff0c61b
title: ID3DX10Mesh::GetVertexDescription-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexDescription
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5857b5162cf351a235d9cbecd2e457030820485d37e9aa49062a63b196f95900
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540226"
---
# <a name="id3dx10meshgetvertexdescription-method"></a>ID3DX10Mesh::GetVertexDescription-Methode

Greifen Sie auf die Scheitelpunktbeschreibung zu, die [**an D3DX10CreateMesh übergeben wird.**](d3d10-d3dx10createmesh.md) Die Scheitelpunktbeschreibung beschreibt das Layout der Scheitelpunktpuffer des Gitters.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVertexDescription(
  [out] const D3D10_INPUT_ELEMENT_DESC **ppDesc,
  [in]        UINT                     *pDeclCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppDesc* \[ out\]
</dt> <dd>

Typ: **const [**D3D10 \_ INPUT ELEMENT \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \* \***

Ein Array von Eingabeelementen, die das Layout der Scheitelpunktpuffer des Gitters beschreiben. Siehe [**D3D10 \_ INPUT ELEMENT \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).

</dd> <dt>

*pDeclCount* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Die Anzahl der Eingabeelemente in ppDesc.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

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

 

 
