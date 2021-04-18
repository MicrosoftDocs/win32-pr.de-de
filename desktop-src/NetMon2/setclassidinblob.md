---
description: Die setclassidinblob-Funktion legt den Wert der benannten Klassen Kennung eines BLOBs fest.
ms.assetid: d17dd48b-2e35-4c57-ba33-688180910b63
title: Setclassidinblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetClassIDInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: b617c39767038bac51d749a640ebcf2301e0c63f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351617"
---
# <a name="setclassidinblob-function"></a>Setclassidinblob-Funktion

Die **setclassidinblob** -Funktion legt den Wert der benannten Klassen Kennung eines BLOBs fest.

## <a name="syntax"></a>Syntax


```C++
DWORD SetClassIDInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const CLSID *pClsID
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

Zeiger auf den Namen des BLOB- **Besitzers** , der festgelegt wird.

</dd> <dt>

*pcategoryname* \[ in\]
</dt> <dd>

Zeiger auf den Namen der BLOB- **Kategorie** , die festgelegt wird.

</dd> <dt>

*ptagname* \[ in\]
</dt> <dd>

Zeiger auf den Namen des BLOB- **Tags** , der festgelegt wird.

</dd> <dt>

*pclsid* \[ in\]
</dt> <dd>

Zeiger auf den Klassen Bezeichner des festgelegten BLOBs.

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

[Getclassidfromblob](getclassidfromblob.md)
</dt> <dt>

[Setboolinblob](setboolinblob.md)
</dt> <dt>

[Setdwordinblob](setdwordinblob.md)
</dt> <dt>

[Setmacaddressinblob](setmacaddressinblob.md)
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

 

 




