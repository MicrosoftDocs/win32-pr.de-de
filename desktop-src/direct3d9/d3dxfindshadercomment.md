---
description: Durchsucht einen Shader nach einem bestimmten Kommentar. Der Kommentar wird durch einen vierstelligen Code (FOURCC) im ersten DWORD des Kommentars identifiziert.
ms.assetid: 86ab8330-fd48-4d14-835c-92399c6c8a38
title: D3DXFindShaderComment-Funktion (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFindShaderComment
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 07ff15b77866732f7a2dcab814e1ccf84d5344f640d83300af874e162485879b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096055"
---
# <a name="d3dxfindshadercomment-function"></a>D3DXFindShaderComment-Funktion

Durchsucht einen Shader nach einem bestimmten Kommentar. Der Kommentar wird durch einen vierstelligen Code (FOURCC) im ersten DWORD des Kommentars identifiziert.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXFindShaderComment(
  _In_  const DWORD   *pFunction,
  _In_        DWORD   FourCC,
  _In_        LPCVOID *ppData,
  _Out_       UINT    *pSizeInBytes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFunction* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf den DWORD-Stream der Shaderfunktion.

</dd> <dt>

*FourCC* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

FOURCC-Code, der den Kommentarblock identifiziert. Weitere Informationen finden Sie unter [FourCC-Formate.](d3dformat.md)

</dd> <dt>

*ppData* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)\***

Gibt einen Zeiger auf die Kommentardaten zurück (ohne Kommentartoken und FOURCC-Code). Dieser Wert kann **NULL** sein.

</dd> <dt>

*pSizeInBytes* \[ out\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Gibt die Größe der Kommentardaten in Bytes zurück. Dieser Wert kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn der Kommentar nicht gefunden wird und kein anderer Fehler aufgetreten ist, wird S \_ FALSE zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shaderfunktionen](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
