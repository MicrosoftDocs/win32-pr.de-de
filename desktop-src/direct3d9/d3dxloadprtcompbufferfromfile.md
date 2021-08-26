---
description: Lädt einen komprimierten PRT-Puffer (Precomputed Radiance Transfer), der auf dem Datenträger gespeichert wurde, in den Arbeitsspeicher.
ms.assetid: ea8bb0d6-f3ed-4ba0-ac87-02e9ac3ae15f
title: D3DXLoadPRTCompBufferFromFile-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTCompBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a05a5712961e8bf72f4eb67f7e644d0f41150b812800fc1c0bd9bca464e3f54f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027380"
---
# <a name="d3dxloadprtcompbufferfromfile-function"></a>D3DXLoadPRTCompBufferFromFile-Funktion

Lädt einen komprimierten PRT-Puffer (Precomputed Radiance Transfer), der auf dem Datenträger gespeichert wurde, in den Arbeitsspeicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXLoadPRTCompBufferFromFile(
  _In_    LPCSTR              pFileName,
  _Inout_ LPD3DXPRTCOMPBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFileName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Name der Datei, aus der die komprimierten Pufferdaten geladen werden.

</dd> <dt>

*ppBuffer* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***

Adresse eines Zeigers auf das [**Id3DXPRTCompBuffer-Ausgabeobjekt.**](id3dxprtcompbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXLoadPRTCompBufferFromFileW auflösen. Andernfalls wird der Funktionsaufruf in D3DXLoadPRTCompBufferFromFileA auflösen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Vorausberechnungsfunktionen für die Übertragung von Radiance](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
