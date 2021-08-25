---
description: Ruft die Größe der Binärdaten ab. Veraltet.
ms.assetid: 99a74043-ce87-4545-961f-dade54e77735
title: IDirectXFileBinary::GetSize-Methode (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetSize
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 1af59f6a32d163275df02d1469ba4777bf5c5152535c2df52fcf7d7c40218e2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846940"
---
# <a name="idirectxfilebinarygetsize-method"></a>IDirectXFileBinary::GetSize-Methode

Ruft die Größe der Binärdaten ab. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSize(
  [out] DWORD *pcbSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*layoutSize* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf die zurückgegebene Größe der Binärdaten in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert DXFILE \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert DXFILEERR \_ BADVALUE sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IDirectXFileBinary](idirectxfilebinary.md)
</dt> </dl>

 

 
