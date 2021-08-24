---
description: Die GetNPPPatternFilterFromBlob-Funktion ruft den Musterabbildfilter aus einem bestimmten BLOB ab.
ms.assetid: b17cde55-8abb-4699-960f-676cbbb24326
title: GetNPPPatternFilterFromBlob-Funktion (Netmon.h)
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
ms.openlocfilehash: f54be7ac5d5b7a443f967d0f6aa1b4737f798a9459833fc87f07f50328f824c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743890"
---
# <a name="getnpppatternfilterfromblob-function"></a>GetNPPPatternFilterFromBlob-Funktion

Die **GetNPPPatternFilterFromBlob-Funktion** ruft den Musterabbildfilter aus einem bestimmten BLOB ab.

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

*hBlob* \[ In\]
</dt> <dd>

Handle für das BLOB.

</dd> <dt>

*pExpression* \[ In\]
</dt> <dd>

Zeiger auf den Filterausdruck.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Handle für ein Fehlerblob, das angibt, wo im ursprünglichen BLOB der Fehler aufgetreten ist (sofern ein Fehler aufgetreten ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert eine NMERR-Funktion, die den Fehler angibt.

## <a name="remarks"></a>Hinweise

Die Filterinformationen für Musterein treffer werden in der **Config-Kategorie** des BLOB gespeichert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[SetNPPPatternFilterInBlob](setnpppatternfilterinblob.md)
</dt> <dt>

[GetBoolFromBlob](getboolfromblob.md)
</dt> <dt>

[GetClassIDFromBlob](getclassidfromblob.md)
</dt> <dt>

[GetDwordFromBlob](getdwordfromblob.md)
</dt> <dt>

[GetMacAddressFromBlob](getmacaddressfromblob.md)
</dt> <dt>

[GetNetworkInfoFromBlob](getnetworkinfofromblob.md)
</dt> <dt>

[GetNPPAddressFilterFromBlob](getnppaddressfilterfromblob.md)
</dt> <dt>

[GetNPPTriggerFromBlob](getnpptriggerfromblob.md)
</dt> <dt>

[GetStringFromBlob](getstringfromblob.md)
</dt> <dt>

[GetStringsFromBlob](getstringsfromblob.md)
</dt> </dl>

 

 




