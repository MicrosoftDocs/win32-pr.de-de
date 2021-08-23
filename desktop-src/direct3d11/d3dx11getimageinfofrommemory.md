---
title: D3DX11GetImageInfoFromMemory-Funktion (D3DX11tex.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt. Hinweis Anstelle dieser Funktion wird empfohlen, die DirectXTex-Bibliothek GetMetadataFromXXXMemory (wobei XXX WIC, DDS oder TGA ist) zu verwenden. WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Art-Source-Format für Spiele). Abrufen von Informationen zu einem Image, das bereits in den Arbeitsspeicher geladen wurde.
ms.assetid: b13192fa-4235-4c38-ba46-e14ffab2f653
keywords:
- D3DX11GetImageInfoFromMemory-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64db94fd0827e1168c599c3a4b959da097faaf43231943d323a19917e18a8b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124705"
---
# <a name="d3dx11getimageinfofrommemory-function"></a>D3DX11GetImageInfoFromMemory-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt.

 

> [!Note]  
> Anstatt diese Funktion zu verwenden, wird empfohlen, die [DirectXTex-Bibliothek](https://github.com/Microsoft/DirectXTex) **GetMetadataFromXXXMemory** zu verwenden (wobei XXX WIC, DDS oder TGA ist. WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Art-Source-Format für Spiele).

 

Abrufen von Informationen zu einem Image, das bereits in den Arbeitsspeicher geladen wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11GetImageInfoFromMemory(
  _In_  LPCVOID           pSrcData,
  _In_  SIZE_T            SrcDataSize,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSrcData* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**

Zeiger auf das Bild im Arbeitsspeicher.

</dd> <dt>

*SrcDataSize* \[ In\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

Größe des Bilds im Arbeitsspeicher in Bytes.

</dd> <dt>

*pPump* \[ In\]
</dt> <dd>

Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Optionale Threadpumpe, die zum asynchronen Laden der Informationen verwendet werden kann. Kann **NULL** sein. Siehe [**ID3DX11ThreadPump-Schnittstelle.**](id3dx11threadpump.md)

</dd> <dt>

*pSrcInfo* \[ In\]
</dt> <dd>

Typ: **[ **D3DX11 \_ IMAGE \_ INFO**](d3dx11-image-info.md)\***

Informationen zum Bild im Arbeitsspeicher.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Ein Zeiger auf den Rückgabewert. Kann **NULL** sein. Wenn *pPump* nicht **NULL** ist, muss *pHResult* ein gültiger Speicherort sein, bis die asynchrone Ausführung abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 11-Rückgabecodes aufgeführten](d3d11-graphics-reference-returnvalues.md)Werte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

