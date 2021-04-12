---
description: Lädt in den Arbeitsspeicher eines komprimierten PRT-Puffers (preberechneten Radiance Transfer), der auf dem Datenträger gespeichert wurde.
ms.assetid: ea8bb0d6-f3ed-4ba0-ac87-02e9ac3ae15f
title: D3DXLoadPRTCompBufferFromFile-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: 505fca7d8cb2426a49a2992c249ba45b5b7afd11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355816"
---
# <a name="d3dxloadprtcompbufferfromfile-function"></a>D3DXLoadPRTCompBufferFromFile-Funktion

Lädt in den Arbeitsspeicher eines komprimierten PRT-Puffers (preberechneten Radiance Transfer), der auf dem Datenträger gespeichert wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXLoadPRTCompBufferFromFile(
  _In_    LPCSTR              pFileName,
  _Inout_ LPD3DXPRTCOMPBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfilename* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Der Name der Datei, aus der die komprimierten Puffer Daten geladen werden sollen.

</dd> <dt>

*ppbuffer* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***

Adresse eines Zeigers auf das Output [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Die Compilereinstellung bestimmt auch die Funktions Version. Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXLoadPRTCompBufferFromFileW aufgelöst. Andernfalls wird der Funktions aufrufin D3DXLoadPRTCompBufferFromFileA aufgelöst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Voraus berechnete Strahlungs Übertragungsfunktionen](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
