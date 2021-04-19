---
description: Die setnetworkinfoinblob-Funktion füllt die networkinfo-Struktur im BLOB auf.
ms.assetid: 1a511c26-2fa7-4fe4-a5a9-23188c59bc34
title: Setnetworkinfoinblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNetworkInfoInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a0019bfaf802b5d4dc80d73e75affa3c50d95de1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353599"
---
# <a name="setnetworkinfoinblob-function"></a>Setnetworkinfoinblob-Funktion

Die **setnetworkinfoinblob** -Funktion füllt die **networkinfo** -Struktur im BLOB auf.

## <a name="syntax"></a>Syntax


```C++
DWORD SetNetworkInfoInBlob(
  _In_ HBLOB         hBlob,
  _In_ LPNETWORKINFO lpNetworkInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hblob* \[ in\]
</dt> <dd>

Handle für ein BLOB.

</dd> <dt>

*lpnetworkinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf die vom Benutzer zugewiesene [networkinfo](networkinfo.md) -Struktur, die die Funktion ausfüllt.

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

[Getnetworkinfofromblob](getnetworkinfofromblob.md)
</dt> <dt>

[Setboolinblob](setboolinblob.md)
</dt> <dt>

[Setclassidinblob](setclassidinblob.md)
</dt> <dt>

[Setdwordinblob](setdwordinblob.md)
</dt> <dt>

[Setmacaddressinblob](setmacaddressinblob.md)
</dt> <dt>

[Setnppaddressfilterinblob](setnppaddressfilterinblob.md)
</dt> <dt>

[Setnpppatternfilterinblob](setnpppatternfilterinblob.md)
</dt> <dt>

[Setnpptriggerinblob](setnpptriggerinblob.md)
</dt> <dt>

[Setstringinblob](setstringinblob.md)
</dt> </dl>

 

 




