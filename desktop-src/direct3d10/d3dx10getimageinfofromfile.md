---
description: Ruft Informationen zu einer angegebenen Bilddatei ab.
ms.assetid: 59bdce45-82d9-42da-b847-a29ca71919b5
title: D3DX10GetImageInfoFromFile-Funktion (D3DX10Tex. h)
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
ms.openlocfilehash: 836d2e18b5c1c48bbe64d0026e97f8ebc5a066ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370395"
---
# <a name="d3dx10getimageinfofromfile-function"></a>D3DX10GetImageInfoFromFile-Funktion

Ruft Informationen zu einer angegebenen Bilddatei ab.

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

*psrcfile* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Dateiname des Bilds, über das Informationen abgerufen werden sollen. Wenn Unicode oder \_ Unicode definiert ist, ist dieser Parametertyp LPCWSTR; andernfalls lautet der Typ LPCSTR.

</dd> <dt>

*ppump* \[ in\]
</dt> <dd>

Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Optionales threadpump, das verwendet werden kann, um die Informationen asynchron zu laden. Kann **null** sein. Siehe [**ID3DX10ThreadPump**](id3dx10threadpump.md).

</dd> <dt>

*psrcinfo* \[ in\]
</dt> <dd>

Type: **[ **d3dx10 \_ Image \_ Info**](d3dx10-image-info.md)\***

Zeiger auf eine d3dx10 \_ Image \_ Info-Struktur, die mit der Beschreibung der Daten in der Quelldatei aufgefüllt werden soll.

</dd> <dt>

*phresult* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Ein Zeiger auf den Rückgabewert. Kann **null** sein. Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DERR \_ invalidcall

## <a name="remarks"></a>Bemerkungen

Diese Funktion unterstützt sowohl Unicode-als auch ANSI-Zeichen folgen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Textur Funktionen in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
