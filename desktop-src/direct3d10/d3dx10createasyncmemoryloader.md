---
description: Erstellen Sie ein asynchrones Speicherladeprogramm.
ms.assetid: 92177390-cb09-445e-9828-806a23ef91b5
title: D3DX10CreateAsyncMemoryLoader-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncMemoryLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 897977147157c754c0f0da1c68e5e64b3fa64ea792c573c1f901aca6aec433fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989230"
---
# <a name="d3dx10createasyncmemoryloader-function"></a>D3DX10CreateAsyncMemoryLoader-Funktion

Erstellen Sie ein asynchrones Speicherladeprogramm.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CreateAsyncMemoryLoader(
  _In_  LPCVOID           pData,
  _In_  SIZE_T            cbData,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Zeiger auf die Daten.

</dd> <dt>

*cbData* \[ In\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Größe der Daten.

</dd> <dt>

*ppDataLoader* \[ out\]
</dt> <dd>

Typ: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***

Die Adresse eines Zeigers auf den asynchronen Datenprozessor (siehe [**ID3DX10DataProcessor-Schnittstelle).**](id3dx10dataprocessor.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Async.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
