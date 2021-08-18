---
description: Erstellen Sie ein asynchrones Dateiladeprogramm.
ms.assetid: 1b79fba5-e7f0-4160-9cec-ffea94f84fde
title: D3DX10CreateAsyncFileLoader-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncFileLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: cfb30de406843831745ab56ced1f3dc0552536ea4a8d45c7f3da4ae078e036e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753390"
---
# <a name="d3dx10createasyncfileloader-function"></a>D3DX10CreateAsyncFileLoader-Funktion

Erstellen Sie ein asynchrones Dateiladeprogramm.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CreateAsyncFileLoader(
  _In_  LPCTSTR           pFileName,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFileName* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Der Name der zu ladenden Datei. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der Datentyp in LPCSTR aufgelöst.

</dd> <dt>

*ppDataLoader* \[ out\]
</dt> <dd>

Typ: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***

Adresse eines Zeigers auf das asynchrone Datenladeprogramm (siehe [**ID3DX10DataLoader-Schnittstelle).**](id3dx10dataloader.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Async.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
