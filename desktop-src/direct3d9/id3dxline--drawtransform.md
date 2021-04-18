---
description: Zeichnet einen Zeilen Streifen im Bildschirmbereich mit einer angegebenen Eingabe Transformationsmatrix.
ms.assetid: 869dc705-8162-4cd9-ac6a-c0ce32f430c3
title: ID3DXLine::D rawtransform-Methode (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.DrawTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 52407a8c92e626f8fe4d2df817017f81806cbae9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354405"
---
# <a name="id3dxlinedrawtransform-method"></a>ID3DXLine::D rawtransform-Methode

Zeichnet einen Zeilen Streifen im Bildschirmbereich mit einer angegebenen Eingabe Transformationsmatrix.

## <a name="syntax"></a>Syntax


```C++
HRESULT DrawTransform(
  [in] const D3DXVECTOR3 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in] const D3DXMATRIX  *pTransform,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvertexlist* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Ein Array von Scheitel Punkten, die die Linie bilden. Siehe [**D3DXVECTOR3**](d3dxvector3.md).

</dd> <dt>

*dwvertexlistcount* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Scheitel Punkte in der Scheitelpunkt Liste.

</dd> <dt>

*ptransform* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***

Eine Formel für Skalierung, Drehung und Übersetzung (SRT) zum Transformieren der Punkte. Siehe [**D3DXMATRIX**](d3dxmatrix.md). Wenn diese Matrix eine Projektions Matrix ist, werden alle gezeichneten Zeilen mit einem perspektivischen stippling-Muster gezeichnet. Oder Sie können die Scheitel Punkte transformieren und [**ID3DXLine::D RAW**](id3dxline--draw.md) verwenden, um die Linie mit einem nicht Perspektiven-korrekten Stippel Muster zu zeichnen.

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

 

 
