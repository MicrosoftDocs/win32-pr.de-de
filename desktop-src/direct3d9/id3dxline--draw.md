---
description: Zeichnet einen Linienstreifen im Bildschirmbereich. Die Eingabe erfolgt in Form eines Arrays, das Punkte (von D3DXVECTOR2) auf dem Zeilenstreifen definiert.
ms.assetid: 10ad5af5-fb57-46ef-a89f-7a05dcf58826
title: ID3DXLine::D raw-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3cb8d55efffb58afefd7c42a6105131da83c48e1731b9d814d5af73f8c3f4f41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987350"
---
# <a name="id3dxlinedraw-method"></a>ID3DXLine::D raw-Methode

Zeichnet einen Linienstreifen im Bildschirmbereich. Die Eingabe erfolgt in Form eines Arrays, das Punkte (von [**D3DXVECTOR2**](d3dxvector2.md)) auf dem Zeilenstreifen definiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT Draw(
  [in] const D3DXVECTOR2 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVertexList* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Array von Scheitelpunkten, aus denen die Linie besteht. Siehe [**D3DXVECTOR2.**](d3dxvector2.md)

</dd> <dt>

*dwVertexListCount* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Scheitelpunkte in der Scheitelpunktliste.

</dd> <dt>

*Farbe* \[ In\]
</dt> <dd>

Typ: **[ **D3DCOLOR**](d3dcolor.md)**

Farbe der Linie. Siehe [**D3DCOLOR**](d3dcolor.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
