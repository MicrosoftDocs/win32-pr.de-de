---
description: Legt den BLOB-Trigger fest.
ms.assetid: 88bfd5cd-f563-4d0c-81a3-54a846805b87
title: Setnpptriggerinblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPTriggerInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 05b8bb3f7f95dc3246ef10f3945b9ab0868550cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214743"
---
# <a name="setnpptriggerinblob-function"></a>Setnpptriggerinblob-Funktion

Die **setnpptriggerinblob** -Funktion legt den BLOB-Trigger fest.

## <a name="syntax"></a>Syntax


```C++
DWORD SetNPPTriggerInBlob(
  _In_  HBLOB     hBlob,
  _In_  LPTRIGGER pTrigger,
  _Out_ HBLOB     hErrorBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hblob* \[ in\]
</dt> <dd>

Das Handle für das BLOB.

</dd> <dt>

*p-Auslösung* \[ in\]
</dt> <dd>

Ein Zeiger auf den Wert des Auslösers.

</dd> <dt>

*herrorblob* \[ vorgenommen\]
</dt> <dd>

Das Handle für ein fehlerblob, das angibt, wo der Fehler im ursprünglichen BLOB aufgetreten ist (sofern vorhanden).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.

## <a name="remarks"></a>Bemerkungen

Diese auslöserdaten werden in der **Trigger** -Kategorie des BLOBs gespeichert.

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

[Getnpptriggerfromblob](getnpptriggerfromblob.md)
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

[Setnppaddressfilterinblob](setnppaddressfilterinblob.md)
</dt> <dt>

[Setnpppatternfilterinblob](setnpppatternfilterinblob.md)
</dt> <dt>

[Setstringinblob](setstringinblob.md)
</dt> </dl>

 

 




