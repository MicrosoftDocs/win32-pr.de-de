---
description: Durchsucht einen Shader nach einem bestimmten Kommentar. Der Kommentar wird durch einen vierstelligen Code (FourCC) im ersten DWORD-Wert des Kommentars identifiziert.
ms.assetid: 86ab8330-fd48-4d14-835c-92399c6c8a38
title: D3DXFindShaderComment-Funktion (D3DX9Shader. h)
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
ms.openlocfilehash: 394c72bcf7076075318cd664cf56bbb464d7e3cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367367"
---
# <a name="d3dxfindshadercomment-function"></a>D3DXFindShaderComment-Funktion

Durchsucht einen Shader nach einem bestimmten Kommentar. Der Kommentar wird durch einen vierstelligen Code (FourCC) im ersten DWORD-Wert des Kommentars identifiziert.

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

*pfunction* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf den DWORD-Datenstrom der Shader-Funktion.

</dd> <dt>

*FourCC* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

FourCC-Code, der den Kommentar Block identifiziert. Siehe [FourCC-Formate](d3dformat.md).

</dd> <dt>

*ppData* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)\***

Gibt einen Zeiger auf die Kommentar Daten zurück (ohne das Kommentar Token und den FourCC-Code). Dieser Wert kann **null** sein.

</dd> <dt>

*psizin Bytes* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Gibt die Größe der Kommentar Daten in Bytes zurück. Dieser Wert kann **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn der Kommentar nicht gefunden wird und kein anderer Fehler aufgetreten ist, wird S \_ false zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Shaderfunktionen](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
