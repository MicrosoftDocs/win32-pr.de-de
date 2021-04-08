---
description: Die setmacaddressinblob-Funktion legt die angeforderte Mac-Adresse eines BLOBs fest.
ms.assetid: f44d0cec-ced7-4d2a-a58e-aeb476bfe800
title: Setmacaddressinblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetMacAddressInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 2183f5635dcdb15362a86a77ae2b3c109c71dbd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866699"
---
# <a name="setmacaddressinblob-function"></a>Setmacaddressinblob-Funktion

Die **setmacaddressinblob** -Funktion legt die angeforderte Mac-Adresse eines BLOBs fest.

## <a name="syntax"></a>Syntax


```C++
DWORD SetMacAddressInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const BYTE  *pMacAddress
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hblob* \[ in\]
</dt> <dd>

Handle für das festzulegende BLOB.

</dd> <dt>

*pownername* \[ in\]
</dt> <dd>

Zeiger auf den Namen des BLOB- **Besitzers** , der festgelegt wird.

</dd> <dt>

*pcategoryname* \[ in\]
</dt> <dd>

Zeiger auf den Namen der BLOB- **Kategorie** , die festgelegt wird.

</dd> <dt>

*ptagname* \[ in\]
</dt> <dd>

Zeiger auf den festzulegenden BLOB- **Tagnamen** .

</dd> <dt>

*pmacaddress* \[ in\]
</dt> <dd>

Ein Zeiger auf die Mac-Adresse des festgelegten BLOBs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Getmacaddressfromblob](getmacaddressfromblob.md)
</dt> <dt>

[Setboolinblob](setboolinblob.md)
</dt> <dt>

[Setclassidinblob](setclassidinblob.md)
</dt> <dt>

[Setdwordinblob](setdwordinblob.md)
</dt> <dt>

[Setnetworkinfoinblob](setnetworkinfoinblob.md)
</dt> <dt>

[Setnppaddressfilterinblob](setnppaddressfilterinblob.md)
</dt> <dt>

[Setnpppatternfilterinblob](setnpppatternfilterinblob.md)
</dt> <dt>

[Setnpptriggerinblob](setnpptriggerinblob.md)
</dt> <dt>

[Setstringinblob](setstringinblob.md)
</dt> </dl>

 

 




