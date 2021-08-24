---
description: Ruft eine Beschreibung des aktuellen Schriftartobjekts ab. GetDescW und GetDescA sind mit dieser Methode identisch, mit der Ausnahme, dass ein Zeiger auf eine D3DXFONT DESCW- bzw. \_ D3DXFONT \_ DESCA-Struktur zurückgegeben wird.
ms.assetid: 21bcd3e0-3659-4d64-959a-0f2d65850cb1
title: ID3DXFont::GetDesc-Methode (D3dx9core.h)
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
ms.openlocfilehash: a2961c69e47bb46eaf782e8f5d4dbfe0be2d82a49f00f98c36b1ee7b141e962b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675430"
---
# <a name="id3dxfontgetdesc-method"></a>ID3DXFont::GetDesc-Methode

Ruft eine Beschreibung des aktuellen Schriftartobjekts ab. GetDescW und GetDescA sind mit dieser Methode identisch, mit der Ausnahme, dass ein Zeiger auf eine [**D3DXFONT \_ DESCW-**](d3dxfont-desc.md) bzw. **D3DXFONT \_ DESCA-Struktur** zurückgegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDesc(
  [out] D3DXFONT_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDesc* \[ out\]
</dt> <dd>

Typ: **[ **D3DXFONT \_ DESC**](d3dxfont-desc.md)\***

Zeiger auf eine [**D3DXFONT \_ DESC-Struktur,**](d3dxfont-desc.md) die das Schriftartobjekt beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Hinweise

Diese Methode beschreibt Unicode-Schriftartobjekte, wenn UNICODE definiert ist. Andernfalls wird GetDescA aufgerufen, das einen Zeiger auf die [**D3DXFONT \_ DESCA-Struktur**](d3dxfont-desc.md) zurückgibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 




