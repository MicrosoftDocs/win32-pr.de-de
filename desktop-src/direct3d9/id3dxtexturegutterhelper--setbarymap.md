---
description: Legt texzentrische texse-Koordinaten fest.
ms.assetid: 6c7c74aa-71a3-45aa-9b18-6409fbd63bda
title: 'ID3DXTextureGutterHelper:: setbarymap-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e3de61913041a4e59e075ea42dacc308c1ce5f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219658"
---
# <a name="id3dxtexturegutterhelpersetbarymap-method"></a>ID3DXTextureGutterHelper:: setbarymap-Methode

Legt texzentrische texse-Koordinaten fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetBaryMap(
  [in] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbarydata* \[ in\]
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



Die Eingabe von Text zentrierten Koordinaten für diese Methode ist nur gültig für gültige Texels (Non-Class 0). [**ID3DXTextureGutterHelper:: getguttermap**](id3dxtexturegutterhelper--getguttermap.md) gibt Werte ungleich 0 (null) für gültige Texels zurück.

In den Scheitel Punkten des Dreiecks wird ein Punkt innerhalb eines Dreiecks definiert. Eine ausführlichere Beschreibung von baryzentrischen Koordinaten finden Sie in [der Beschreibung von mathworld in der Beschreibung der baryzentrierten Koordinaten](http://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




