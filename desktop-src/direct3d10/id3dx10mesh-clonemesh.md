---
description: Erstellt ein neues Gitternetz und füllt es mit den Daten eines zuvor geladenen Gitternetzes auf.
ms.assetid: 2ce39982-abc0-444b-bc6f-24508f76fe31
title: ID3DX10Mesh::CloneMesh-Methode (D3DX10.h)
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
ms.openlocfilehash: 292522e47dbaf6937d871209006134e866e92fdeb27f6edba4f4f71f6d1fad14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409130"
---
# <a name="id3dx10meshclonemesh-method"></a>ID3DX10Mesh::CloneMesh-Methode

Erstellt ein neues Gitternetz und füllt es mit den Daten eines zuvor geladenen Gitternetzes auf.

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

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Erstellungsflags, die auf das neue Gitternetz angewendet werden sollen. Siehe [**D3DX10 \_ MESH**](d3dx10-mesh.md).

</dd> <dt>

*pPosSemantic* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Der semantische Name für die Positionsdaten.

</dd> <dt>

*pDesc* \[ In\]
</dt> <dd>

Typ: **const [**D3D10 \_ INPUT ELEMENT \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***

Array von D3D10 \_ INPUT \_ ELEMENT \_ DESC-Strukturen, das das Scheitelpunktformat für das zurückgegebene Gitternetz beschreibt. Siehe [**D3D10 \_ INPUT ELEMENT \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).

</dd> <dt>

*DeclCount* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der Elemente im pDesc-Array.

</dd> <dt>

*ppCloneMesh* \[ out\]
</dt> <dd>

Typ: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***

Das neue Gitternetz.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
