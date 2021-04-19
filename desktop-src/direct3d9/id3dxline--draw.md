---
description: Zeichnet einen Zeilen Streifen im Bildschirmbereich. Die Eingabe erfolgt in Form eines Arrays, das Punkte (of D3DXVECTOR2) im Zeilen Streifen definiert.
ms.assetid: 10ad5af5-fb57-46ef-a89f-7a05dcf58826
title: ID3DXLine::D RAW-Methode (D3dx9core. h)
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
ms.openlocfilehash: 0a7492fb2128e0d9ec402d5211c20d5569ceb506
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364004"
---
# <a name="id3dxlinedraw-method"></a>ID3DXLine::D RAW-Methode

Zeichnet einen Zeilen Streifen im Bildschirmbereich. Die Eingabe erfolgt in Form eines Arrays, das Punkte (of [**D3DXVECTOR2**](d3dxvector2.md)) im Zeilen Streifen definiert.

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

*pvertexlist* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***

Ein Array von Scheitel Punkten, die die Linie bilden. Siehe [**D3DXVECTOR2**](d3dxvector2.md).

</dd> <dt>

*dwvertexlistcount* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Scheitel Punkte in der Scheitelpunkt Liste.

</dd> <dt>

*Farbe* \[ in\]
</dt> <dd>

Typ: **[ **D3DCOLOR**](d3dcolor.md)**

Die Farbe der Linie. Siehe [**D3DCOLOR**](d3dcolor.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
