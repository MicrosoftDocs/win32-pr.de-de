---
description: 'D3DX10GetImageInfoFromResource-Funktion: Ruft Informationen zu einem bestimmten Bild in einer Ressource ab.'
ms.assetid: d413d887-77e0-43cc-a30e-67c3c40772f0
title: D3DX10GetImageInfoFromResource-Funktion (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: af4dea966b63549c4bcef913175c6c97e1c49d73e3d5694cfcd0f7b6c8170497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989160"
---
# <a name="d3dx10getimageinfofromresource-function"></a>D3DX10GetImageInfoFromResource-Funktion

Ruft Informationen zu einem bestimmten Bild in einer Ressource ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSrcModule* \[ In\]
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

Modul, in das die Ressource geladen wird. Legen Sie diesen Parameter auf **NULL fest,** um das Modul anzugeben, das dem Image zugeordnet ist, das das Betriebssystem zum Erstellen des aktuellen Prozesses verwendet hat.

</dd> <dt>

*pSrcResource* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Dateinamen angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der Datentyp in LPCSTR auflösen. Siehe Hinweise.

</dd> <dt>

*pPump* \[ In\]
</dt> <dd>

Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Optionale Threadpump, die zum asynchronen Laden der Informationen verwendet werden kann. Kann NULL **sein.** Siehe [**ID3DX10ThreadPump**](id3dx10threadpump.md).

</dd> <dt>

*pSrcInfo* \[ In\]
</dt> <dd>

Typ: **[ **D3DX10 \_ IMAGE \_ INFO**](d3dx10-image-info.md)\***

Zeiger auf eine D3DX10 IMAGE INFO-Struktur, die mit der Beschreibung der Daten \_ \_ in der Quelldatei gefüllt werden soll.

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

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DX10GetImageInfoFromResourceW auflösen. Andernfalls wird der Funktionsaufruf in D3DX10GetImageInfoFromResourceA auflösen, da ANSI-Zeichenfolgen verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Texturfunktionen in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
