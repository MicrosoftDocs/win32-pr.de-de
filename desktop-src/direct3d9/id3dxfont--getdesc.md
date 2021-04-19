---
description: Ruft eine Beschreibung des aktuellen Schriftart Objekts ab. Getdescw und getdesca sind mit dieser Methode identisch, mit dem Unterschied, dass ein Zeiger an eine D3DXFONT- \_ oder D3DXFONT-DeScA-Struktur zurückgegeben wird \_ .
ms.assetid: 21bcd3e0-3659-4d64-959a-0f2d65850cb1
title: 'ID3DXFont:: getdesc-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3310971e360fb9994a30d62349d3e7e4b764c7d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355806"
---
# <a name="id3dxfontgetdesc-method"></a>ID3DXFont:: getdesc-Methode

Ruft eine Beschreibung des aktuellen Schriftart Objekts ab. Getdescw und getdesca sind mit dieser Methode identisch, mit dem Unterschied, dass ein Zeiger an eine [**D3DXFONT \_**](d3dxfont-desc.md) -oder **D3DXFONT- \_ DeScA** -Struktur zurückgegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDesc(
  [out] D3DXFONT_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PDE SC* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **D3DXFONT \_ DESC**](d3dxfont-desc.md)\***

Zeiger auf eine [**D3DXFONT \_**](d3dxfont-desc.md) -Struktur, die das Schriftart Objekt beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.

## <a name="remarks"></a>Bemerkungen

Diese Methode beschreibt Unicode-Schriftart Objekte, wenn Unicode definiert ist. Andernfalls wird getdesca aufgerufen, wodurch ein Zeiger auf die [**D3DXFONT \_ DeScA**](d3dxfont-desc.md) -Struktur zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 




