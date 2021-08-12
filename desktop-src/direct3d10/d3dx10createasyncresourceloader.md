---
description: Erstellen Sie ein asynchrones Ressourcenlader.
ms.assetid: 1b3eb21c-4ba6-4910-b2f0-2ffa4ae50e47
title: D3DX10CreateAsyncResourceLoader-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncResourceLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: bedb3559ead576c074dafed526fc0ebfefebaf5c3e53a6559223af346e7f9c98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303455"
---
# <a name="d3dx10createasyncresourceloader-function"></a>D3DX10CreateAsyncResourceLoader-Funktion

Erstellen Sie ein asynchrones Ressourcenlader.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CreateAsyncResourceLoader(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSrcModule* \[ In\]
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle für das Ressourcenmodul. Verwenden [Sie die GetModuleHandle-Funktion,](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) um das Handle zu erhalten.

</dd> <dt>

*pSrcResource* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Name der Ressource in hSrcModule. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der Datentyp in LPCSTR auflösen.

</dd> <dt>

*ppDataLoader* \[ out\]
</dt> <dd>

Typ: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***

Die Adresse eines Zeigers auf den asynchronen Datenprozessor (siehe [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Async.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
