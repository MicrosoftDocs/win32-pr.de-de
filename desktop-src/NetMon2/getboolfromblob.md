---
description: Ruft einen benannten booleschen Wert aus einem BLOB ab.
ms.assetid: 26acfd2a-5b17-47ad-8f7b-7793174a13c3
title: Getboolfromblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBoolFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e09a35f71181343cd401b3288c2b2c74a46f677b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346275"
---
# <a name="getboolfromblob-function"></a>Getboolfromblob-Funktion

Mit der **getboolfromblob** -Funktion wird ein benannter boolescher Wert aus einem BLOB abgerufen.

## <a name="syntax"></a>Syntax


```C++
DWORD GetBoolFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       BOOL  *pBool
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hblob* \[ in\]
</dt> <dd>

Ein Handle für ein BLOB.

</dd> <dt>

*pownername* \[ in\]
</dt> <dd>

Ein Zeiger auf den Namen des BLOB-Besitzers.

</dd> <dt>

*pcategoryname* \[ in\]
</dt> <dd>

Ein Zeiger auf den BLOB-Kategoriename.

</dd> <dt>

*ptagname* \[ in\]
</dt> <dd>

Ein Zeiger auf den BLOB-Tagnamen.

</dd> <dt>

*pbool* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den booleschen Wert des BLOBs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler beschreibt.

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

[Setboolinblob](setboolinblob.md)
</dt> <dt>

[Getclassidfromblob](getclassidfromblob.md)
</dt> <dt>

[Getdwordfromblob](getdwordfromblob.md)
</dt> <dt>

[Getmacaddressfromblob](getmacaddressfromblob.md)
</dt> <dt>

[Getnetworkinfofromblob](getnetworkinfofromblob.md)
</dt> <dt>

[Getnppaddressfilterfromblob](getnppaddressfilterfromblob.md)
</dt> <dt>

[Getnpppatternfilterfromblob](getnpppatternfilterfromblob.md)
</dt> <dt>

[Getnpptriggerfromblob](getnpptriggerfromblob.md)
</dt> <dt>

[Getstringfromblob](getstringfromblob.md)
</dt> <dt>

[Getstringsfromblob](getstringsfromblob.md)
</dt> </dl>

 

 




