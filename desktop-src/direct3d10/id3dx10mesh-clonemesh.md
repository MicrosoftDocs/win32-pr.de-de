---
description: Erstellt ein neues Mesh und füllt es mit den Daten eines zuvor geladenen Mesh.
ms.assetid: 2ce39982-abc0-444b-bc6f-24508f76fe31
title: 'ID3DX10Mesh:: clonemesh-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CloneMesh
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0f007475ea9f6aeaa6dc0c01bbd721c4a5103adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363161"
---
# <a name="id3dx10meshclonemesh-method"></a>ID3DX10Mesh:: clonemesh-Methode

Erstellt ein neues Mesh und füllt es mit den Daten eines zuvor geladenen Mesh.

## <a name="syntax"></a>Syntax


```C++
HRESULT CloneMesh(
  [in]        UINT                     Flags,
  [in]        LPCSTR                   pPosSemantic,
  [in]  const D3D10_INPUT_ELEMENT_DESC *pDesc,
  [in]        UINT                     DeclCount,
  [out]       ID3DX10Mesh              **ppCloneMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Erstellungsflags, die auf das neue Mesh angewendet werden sollen. Siehe [**d3dx10 \_ Mesh**](d3dx10-mesh.md).

</dd> <dt>

*ppossemantic* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Der semantische Name der Positionsdaten.

</dd> <dt>

*PDE SC* \[ in\]
</dt> <dd>

Type: **Konstanten [**d3d10 \_ input- \_ Element \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***

Array von d3d10 \_ input- \_ Element- \_ DESC-Strukturen, das das Vertex-Format für das zurückgegebene Mesh beschreibt. Weitere Informationen finden Sie unter [**d3d10 \_ input \_ Element \_ ensc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).

</dd> <dt>

*Declcount* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Anzahl der Elemente im PDE-Array.

</dd> <dt>

*ppclonemesh* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***

Das neue Mesh.

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

 

 
