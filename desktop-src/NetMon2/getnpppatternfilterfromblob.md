---
description: Die getnpppatternfilterfromblob-Funktion Ruft den Muster Übereinstimmungs Filter aus einem bestimmten BLOB ab.
ms.assetid: b17cde55-8abb-4699-960f-676cbbb24326
title: Getnpppatternfilterfromblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPPatternFilterFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5758c53fe21231d300058a9168e556e9f9ceaa43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750081"
---
# <a name="getnpppatternfilterfromblob-function"></a>Getnpppatternfilterfromblob-Funktion

Die **getnpppatternfilterfromblob** -Funktion Ruft den Muster Übereinstimmungs Filter aus einem bestimmten BLOB ab.

## <a name="syntax"></a>Syntax


```C++
DWORD GetNPPPatternFilterFromBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hblob* \[ in\]
</dt> <dd>

Handle für das BLOB.

</dd> <dt>

*pexpression* \[ in\]
</dt> <dd>

Zeiger auf den Filter Ausdruck.

</dd> <dt>

*herrorblob* \[ vorgenommen\]
</dt> <dd>

Handle für ein fehlerblob, das angibt, wo der Fehler im ursprünglichen BLOB aufgetreten ist (falls vorhanden).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr, der den Fehler angibt.

## <a name="remarks"></a>Bemerkungen

Die Filter Informationen für die Muster Übereinstimmung werden in der Kategorie **config** des BLOBs gespeichert.

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

[Setnpppatternfilterinblob](setnpppatternfilterinblob.md)
</dt> <dt>

[Getboolfromblob](getboolfromblob.md)
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

[Getnpptriggerfromblob](getnpptriggerfromblob.md)
</dt> <dt>

[Getstringfromblob](getstringfromblob.md)
</dt> <dt>

[Getstringsfromblob](getstringsfromblob.md)
</dt> </dl>

 

 




