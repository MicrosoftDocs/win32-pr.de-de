---
title: D3DX11GetImageInfoFromFile-Funktion (D3DX11tex.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Hinweis Anstelle dieser Funktion wird empfohlen, die DirectXTex-Bibliothek GetMetadataFromXXXFile (wobei XXX WIC, DDS oder TGA ist) zu verwenden. WIC unterstützt DDS und TGA nicht. Von D3DX 9 unterstützte TGA als gängiges Art Source-Format für Spiele). Ruft Informationen zu einer bestimmten Bilddatei ab.
ms.assetid: 57768604-3672-49a0-8120-f09240b8fc98
keywords:
- D3DX11GetImageInfoFromFile-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ba5827c17428cf4e5b335d2a16b67d9c448099be38366a1e9f463ba83a4285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536074"
---
# <a name="d3dx11getimageinfofromfile-function"></a>D3DX11GetImageInfoFromFile-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

> [!Note]  
> Anstatt diese Funktion zu verwenden, empfiehlt es sich, die [DirectXTex-Bibliothek](https://github.com/Microsoft/DirectXTex) **GetMetadataFromXXXFile** (wobei XXX WIC, DDS oder TGA ist) zu verwenden. WIC unterstützt DDS und TGA nicht. Von D3DX 9 unterstützte TGA als gängiges Art Source-Format für Spiele).

 

Ruft Informationen zu einer bestimmten Bilddatei ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11GetImageInfoFromFile(
  _In_  LPCTSTR           pSrcFile,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSrcFile* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Dateiname des Bilds, zu dem Informationen abgerufen werden. Wenn UNICODE oder \_ UNICODE definiert sind, ist dieser Parametertyp LPCWSTR, andernfalls ist der Typ LPCSTR.

</dd> <dt>

*pPump* \[ In\]
</dt> <dd>

Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Optionale Threadpump, die zum asynchronen Laden der Informationen verwendet werden kann. Kann NULL **sein.** Siehe [**ID3DX11ThreadPump-Schnittstelle**](id3dx11threadpump.md).

</dd> <dt>

*pSrcInfo* \[ In\]
</dt> <dd>

Typ: **[ **D3DX11 \_ IMAGE \_ INFO**](d3dx11-image-info.md)\***

Zeiger auf eine [**D3DX11-BILDINFORMATION, \_ \_**](d3dx11-image-info.md) die mit der Beschreibung der Daten in der Quelldatei gefüllt werden soll.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Ein Zeiger auf den Rückgabewert. Kann NULL **sein.** Wenn *pPump* nicht **NULL ist,** muss *pHResult* ein gültiger Speicherort sein, bis die asynchrone Ausführung abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt sein: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Hinweise

Diese Funktion unterstützt sowohl Unicode- als auch ANSI-Zeichenfolgen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

