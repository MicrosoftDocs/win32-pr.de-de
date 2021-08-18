---
description: 'D3DX10GetImageInfoFromFile-Funktion: Ruft Informationen zu einer bestimmten Bilddatei ab.'
ms.assetid: 59bdce45-82d9-42da-b847-a29ca71919b5
title: D3DX10GetImageInfoFromFile-Funktion (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 49a1643e97ad4b177f2bc2e18d4e11f660ceab1fa1ab5293c1ab88dc2236334c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540919"
---
# <a name="d3dx10getimageinfofromfile-function"></a>D3DX10GetImageInfoFromFile-Funktion

Ruft Informationen zu einer bestimmten Bilddatei ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10GetImageInfoFromFile(
  _In_  LPCTSTR           pSrcFile,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSrcFile* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Dateiname des Bilds, zu dem Informationen abgerufen werden sollen. Wenn UNICODE oder \_ UNICODE definiert ist, ist dieser Parametertyp LPCWSTR, andernfalls LPCSTR.

</dd> <dt>

*pPump* \[ In\]
</dt> <dd>

Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Optionale Threadpumpe, die zum asynchronen Laden der Informationen verwendet werden kann. Kann **NULL** sein. Siehe [**ID3DX10ThreadPump.**](id3dx10threadpump.md)

</dd> <dt>

*pSrcInfo* \[ In\]
</dt> <dd>

Typ: **[ **D3DX10 \_ IMAGE \_ INFO**](d3dx10-image-info.md)\***

Zeiger auf eine D3DX10 \_ IMAGE \_ INFO-Struktur, die mit der Beschreibung der Daten in der Quelldatei gefüllt werden soll.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Ein Zeiger auf den Rückgabewert. Kann **NULL** sein. Wenn *pPump* nicht **NULL** ist, muss *pHResult* ein gültiger Speicherort sein, bis die asynchrone Ausführung abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt sein: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Hinweise

Diese Funktion unterstützt sowohl Unicode- als auch ANSI-Zeichenfolgen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Texturfunktionen in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
