---
description: Mit der getclassidfromblob-Funktion wird ein benannter klassenbezeichnerwert aus einem BLOB abgerufen.
ms.assetid: fef29a42-ccd3-4655-958c-d150e5bcd0d7
title: Getclassidfromblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetClassIDFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 70122422c47a986058322ca8d17082093e02a4b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128344"
---
# <a name="getclassidfromblob-function"></a>Getclassidfromblob-Funktion

Mit der **getclassidfromblob** -Funktion wird ein benannter klassenbezeichnerwert aus einem BLOB abgerufen.

## <a name="syntax"></a>Syntax


```C++
DWORD GetClassIDFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       CLSID *pClsID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hblob* \[ in\]
</dt> <dd>

Handle für ein BLOB.

</dd> <dt>

*pownername* \[ in\]
</dt> <dd>

Zeiger auf den Namen des BLOB-Besitzers.

</dd> <dt>

*pcategoryname* \[ in\]
</dt> <dd>

Zeiger auf den BLOB-Kategoriename.

</dd> <dt>

*ptagname* \[ in\]
</dt> <dd>

Zeiger auf den BLOB-Tagnamen.

</dd> <dt>

*pclsid* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den BLOB-Klassen Bezeichner.

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

[Setclassidinblob](setclassidinblob.md)
</dt> <dt>

[Getboolfromblob](getboolfromblob.md)
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

 

 




