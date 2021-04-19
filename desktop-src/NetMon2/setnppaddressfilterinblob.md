---
description: Die setnppaddressfilterinblob-Funktion legt den angegebenen Adress Filter im BLOB fest.
ms.assetid: bdd1482d-8be0-4999-9a7a-16b0400412fb
title: Setnppaddressfilterinblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPAddressFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 39e8a85599fa63b1320d707f648731a195dbb48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352747"
---
# <a name="setnppaddressfilterinblob-function"></a>Setnppaddressfilterinblob-Funktion

Die **setnppaddressfilterinblob** -Funktion legt den angegebenen Adress Filter im BLOB fest.

## <a name="syntax"></a>Syntax


```C++
DWORD SetNPPAddressFilterInBlob(
  _In_ HBLOB          hBlob,
  _In_ LPADDRESSTABLE pAddressTable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hblob* \[ in\]
</dt> <dd>

Handle für ein BLOB.

</dd> <dt>

*padresssstable* \[ in\]
</dt> <dd>

Ein Zeiger auf eine- [**adressstabile**](addresstable.md) -Struktur, die die vom Benutzer zugeordnete Adress Tabelle definiert.

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

[Getnppaddressfilterfromblob](getnppaddressfilterfromblob.md)
</dt> <dt>

[Setboolinblob](setboolinblob.md)
</dt> <dt>

[Setclassidinblob](setclassidinblob.md)
</dt> <dt>

[Setdwordinblob](setdwordinblob.md)
</dt> <dt>

[Setmacaddressinblob](setmacaddressinblob.md)
</dt> <dt>

[Setnetworkinfoinblob](setnetworkinfoinblob.md)
</dt> <dt>

[Setnpppatternfilterinblob](setnpppatternfilterinblob.md)
</dt> <dt>

[Setnpptriggerinblob](setnpptriggerinblob.md)
</dt> <dt>

[Setstringinblob](setstringinblob.md)
</dt> </dl>

 

 




