---
description: Hier erhalten Sie eine Beschreibung des aktuellen Schriftartobjekts.
ms.assetid: f08beb35-351f-4087-a2db-097843463291
title: ID3DX10Font::GetDesc-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDesc
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d684a0bf485db441a0a6bf23cd36496cc13fdfe766eaa890682259b76b3800c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990440"
---
# <a name="id3dx10fontgetdesc-method"></a>ID3DX10Font::GetDesc-Methode

Hier erhalten Sie eine Beschreibung des aktuellen Schriftartobjekts.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDesc(
  [in] D3DX10_FONT_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDesc* \[ In\]
</dt> <dd>

Typ: **[ **D3DX10 \_ FONT \_ DESC**](d3dx10-font-desc.md)\***

Zeiger auf eine [**D3DX10 \_ FONT \_ DESC-Struktur,**](d3dx10-font-desc.md) die das Schriftartobjekt beschreibt. Wenn UNICODE definiert ist, wird ein Zeiger auf eine D3DX10FONT DESCW zurückgegeben. Andernfalls wird ein Zeiger auf eine \_ D3DX10FONT \_ DESCA zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Hinweise

Diese Methode beschreibt Unicode-Schriftartobjekte, wenn UNICODE definiert ist. Andernfalls wird GetDescA aufgerufen, das einen Zeiger auf die D3DX10FONT \_ DESCA-Struktur zurückgibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




