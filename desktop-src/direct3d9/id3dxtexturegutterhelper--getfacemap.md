---
description: Ruft den Index der Gitterfläche ab, zu der jeder textexgehört.
ms.assetid: 3eb3461c-4e16-4c89-9ca9-fc9c6b5638c7
title: 'ID3DXTextureGutterHelper:: getfacemap-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8164ec35c3b3596914577287ecc6b9285142fca8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367455"
---
# <a name="id3dxtexturegutterhelpergetfacemap-method"></a>ID3DXTextureGutterHelper:: getfacemap-Methode

Ruft den Index der Gitterfläche ab, zu der jeder textexgehört.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfacedata* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Zeiger auf den Index der Mesh-Seite, zu der jeder textexgehört.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall

## <a name="remarks"></a>Bemerkungen

Die von dieser Methode zurückgegebenen mesface-Daten sind nur für gültige Texels (Non-Class 0) gültig. [**ID3DXTextureGutterHelper:: getguttermap**](id3dxtexturegutterhelper--getguttermap.md) gibt Werte ungleich 0 (null) für gültige Texels (nicht Klassen 0) zurück.

Bei [**Klasse 2 texeln**](id3dxtexturegutterhelper.md)ruft diese Methode das nächste Gesicht ab.

Die Anwendung muss pfacedata zuordnen und verwalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
