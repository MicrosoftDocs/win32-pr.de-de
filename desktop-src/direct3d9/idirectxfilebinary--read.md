---
description: Liest die Binärdaten. Veraltet.
ms.assetid: 530552c5-bf05-4e86-836d-d25161832c6d
title: IDirectXFileBinary::Read-Methode (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.Read
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 2e0c926580df3471ae314d2c6127b38bf3c2231946010a0ab58500125edc6f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728986"
---
# <a name="idirectxfilebinaryread-method"></a>IDirectXFileBinary::Read-Methode

Liest die Binärdaten. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT Read(
  [out] LPVOID  pvData,
  [in]  DWORD   cbSize,
  [out] LPDWORD pcbRead
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvData* \[ out\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Zeiger auf den Puffer, der die gelesenen Daten empfängt.

</dd> <dt>

*cbSize* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Größe des Puffers, auf den pvData zeigt, in Bytes.

</dd> <dt>

*read* \[ out\]
</dt> <dd>

Typ: **[ **LPDWORD**](../winprog/windows-data-types.md)**

Zeiger auf die Anzahl der tatsächlich gelesenen Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert DXFILE \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREDATA.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDirectXFileBinary](idirectxfilebinary.md)
</dt> </dl>

 

 
