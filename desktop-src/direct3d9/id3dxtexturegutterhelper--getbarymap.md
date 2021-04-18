---
description: Ruft texzentrische texzentrische Koordinaten ab.
ms.assetid: f380a37f-b9c1-4433-b1d6-e9feeca79b30
title: 'ID3DXTextureGutterHelper:: getbarymap-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 246117569b9106de18a31d08613146a3aa0d88c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355026"
---
# <a name="id3dxtexturegutterhelpergetbarymap-method"></a>ID3DXTextureGutterHelper:: getbarymap-Methode

Ruft texzentrische texzentrische Koordinaten ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetBaryMap(
  [in, out] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbarydata* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ein Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die die ersten beiden über die beiden texzentrischen Koordinaten jeder texenstruktur enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall

## <a name="remarks"></a>Bemerkungen

Die dritte barzentrierte Koordinate wird durch Folgendes angegeben:


```
    1 - ( pBaryData.x + pBaryData.y )
```



Barzentrierte Koordinaten werden immer in Bezug auf das von [**ID3DXTextureGutterHelper:: getfacemap**](id3dxtexturegutterhelper--getfacemap.md)zurückgegebene Dreieck angegeben.

Die von dieser Methode zurückgegebenen von dieser Methode zurückgegebenen, von dieser Methode zurückgegebenen Koordinaten sind nur gültig für gültige Texels (nicht Class 0). [**ID3DXTextureGutterHelper:: getguttermap**](id3dxtexturegutterhelper--getguttermap.md) gibt Werte ungleich 0 (null) für gültige Texels zurück.

[**Class 2 texeln**](id3dxtexturegutterhelper.md) werden dem nächstgelegenen Punkt auf dem Dreieck im textraum zugeordnet.

Die Anwendung muss pbarydata zuordnen und verwalten.

In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert. Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




