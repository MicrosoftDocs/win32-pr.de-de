---
description: Zugreifen auf die vertexbeschreibung, die an D3DX10CreateMesh übermittelt wurde. In der Scheitelpunkt Beschreibung wird das Layout der Vertex-Puffer des Netzes beschrieben.
ms.assetid: e4a4a98a-e131-414c-ad98-21288ff0c61b
title: 'ID3DX10Mesh:: getvertexdescription-Methode (d3dx10. h)'
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
ms.openlocfilehash: 01888ea83f43e37951b48e03916f18af1ec6ddb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961613"
---
# <a name="id3dx10meshgetvertexdescription-method"></a>ID3DX10Mesh:: getvertexdescription-Methode

Zugreifen auf die vertexbeschreibung, die an [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md)übermittelt wurde. In der Scheitelpunkt Beschreibung wird das Layout der Vertex-Puffer des Netzes beschrieben.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVertexDescription(
  [out] const D3D10_INPUT_ELEMENT_DESC **ppDesc,
  [in]        UINT                     *pDeclCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PPDE SC* \[ vorgenommen\]
</dt> <dd>

Type: **Konstanten [**d3d10 input \_ - \_ Element \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \* \***

Array von Eingabe Elementen, das das Layout der Vertex-Puffer des Netzes beschreibt. Weitere Informationen finden Sie unter [**d3d10 \_ input \_ Element \_ ensc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).

</dd> <dt>

*pdeclcount* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Die Anzahl der Eingabeelemente in PPDE SC.

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

 

 
