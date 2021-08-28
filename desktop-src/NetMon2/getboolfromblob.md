---
description: Ruft einen benannten booleschen Wert aus einem BLOB ab.
ms.assetid: 26acfd2a-5b17-47ad-8f7b-7793174a13c3
title: GetBoolFromBlob-Funktion (Netmon.h)
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
ms.openlocfilehash: ec9f5333e3f85f92b30d52689288c971ca04437df647a7a7e5fe89379e06533e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743920"
---
# <a name="getboolfromblob-function"></a>GetBoolFromBlob-Funktion

Die **GetBoolFromBlob-Funktion** ruft einen benannten booleschen Wert aus einem BLOB ab.

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

*hBlob* \[ In\]
</dt> <dd>

Ein Handle für ein BLOB.

</dd> <dt>

*pOwnerName* \[ In\]
</dt> <dd>

Ein Zeiger auf den Namen des BLOB-Besitzers.

</dd> <dt>

*pCategoryName* \[ In\]
</dt> <dd>

Ein Zeiger auf den Blobkategorienamen.

</dd> <dt>

*pTagName* \[ In\]
</dt> <dd>

Ein Zeiger auf den Namen des BLOB-Tags.

</dd> <dt>

*pBool* \[ out\]
</dt> <dd>

Zeiger auf den booleschen Wert des BLOB.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein NMERR-Wert, der den Fehler beschreibt.

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

[SetBoolInBlob](setboolinblob.md)
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

[GetNPPPatternFilterFromBlob](getnpppatternfilterfromblob.md)
</dt> <dt>

[GetNPPTriggerFromBlob](getnpptriggerfromblob.md)
</dt> <dt>

[GetStringFromBlob](getstringfromblob.md)
</dt> <dt>

[GetStringsFromBlob](getstringsfromblob.md)
</dt> </dl>

 

 




