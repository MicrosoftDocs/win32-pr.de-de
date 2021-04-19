---
description: Projiziert eine in einer cubemap dargestellte Funktion in sphärischen Harmonics.
ms.assetid: de8bc4bd-cb29-44ab-8806-33d3ffd10a7b
title: D3DX10SHProjectCubeMap-Funktion (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SHProjectCubeMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fd991e2207f1ad556d9f9b5e648e296b857e884b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353366"
---
# <a name="d3dx10shprojectcubemap-function"></a>D3DX10SHProjectCubeMap-Funktion

Projiziert eine in einer cubemap dargestellte Funktion in sphärischen Harmonics.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10SHProjectCubeMap(
   UINT            Order,
   ID3D10Texture2D *pCubeMap,
   FLOAT           *pROut,
   FLOAT           *pGOut,
   FLOAT           *pBOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Order* 
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Reihenfolge der SH-Auswertung, generiert Order ^ 2-coefs, Grad ist Order-1.

</dd> <dt>

*pcubemap* 
</dt> <dd>

Typ: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Cubemap, die in sphärischen Harmoniken projiziert wird. Siehe [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d).

</dd> <dt>

*Proxy* 
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Ausgabe SH-Vektor für rot.

</dd> <dt>

*pgout* 
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Ausgabe SH-Vektor für grün.

</dd> <dt>

*pbout* 
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Ausgabe SH-Vektor für blau.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
