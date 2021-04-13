---
description: Ruft die Namen aller Netzwerk-DDE-Freigaben ab, die im Kontext des aufrufenden Prozesses als vertrauenswürdig eingestuft werden.
ms.assetid: 8e2323a4-0c27-44e6-9598-08a3c1a88bd3
title: Nddebug-ShareEnum-Funktion (nddecoapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeTrustedShareEnum
- NDdeTrustedShareEnumA
- NDdeTrustedShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: caa3f7c20b95243e03c0c6025d1ff32d60443ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348248"
---
# <a name="nddetrustedshareenum-function"></a>Nddebug-ShareEnum-Funktion

\[Network DDE wird nicht mehr unterstützt. Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]

Ruft die Namen aller Netzwerk-DDE-Freigaben ab, die im Kontext des aufrufenden Prozesses als vertrauenswürdig eingestuft werden.

## <a name="syntax"></a>Syntax


```C++
UINT NDdeTrustedShareEnum(
  _In_  LPTSTR  lpszServer,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnEntriesRead,
  _Out_ LPDWORD lpcbTotalAvailable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszserver* \[ in\]
</dt> <dd>

Der Name des Servers, auf dem sich die DSDM befindet.

</dd> <dt>

*Nlevel* \[ in\]
</dt> <dd>

Reserviert. Dieser Parameter muss NULL sein.

</dd> <dt>

*lpBuffer* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Liste der vertrauenswürdigen DDE-Freigaben empfängt. Die Liste der vertrauenswürdigen DDE-Freigaben wird als Sequenz von durch Null getrennten Zeichen folgen zurückgegeben, die mit einem doppelten NULL-Zeichen am Ende beendet werden. Dieser Parameter kann **NULL** sein. Wenn der *lpBuffer* **null** ist, gibt die DSDM die Größe des Puffers zurück, der zum Speichern der Liste der Freigaben im Feld *lpcbtotalavailable* erforderlich ist.

</dd> <dt>

*cbubsize* \[ in\]
</dt> <dd>

Die Größe des *lpBuffer* -Puffers in Bytes. Dieser Parameter muss NULL sein, wenn *lpBuffer* **null** ist.

</dd> <dt>

*lpnentriesread* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Gesamtzahl der aufzuzählenden vertrauenswürdigen Freigaben empfängt. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*lpcbtotalavailable* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Gesamtzahl der Bytes empfängt, die zum Speichern der Liste vertrauenswürdiger DDE-Freigaben benötigt werden. Dieser Parameter darf nicht **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert "ndde \_ No \_ Error".

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch den Aufruf von [**nddegeterrorstring**](nddegeterrorstring.md)in eine Text Fehlermeldung übersetzt werden kann. Wenn der *lpBuffer* -Parameter **null** ist, wird ndde \_ buf \_ zu \_ klein zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Ndde API. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ndde API. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Nddebug-shareenumw** (Unicode) und **nddebug-shareenuma** (ANSI)<br/>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über das Netzwerk dynamischer Datenaustausch](network-dynamic-data-exchange.md)
</dt> <dt>

[Network DDE-Funktionen](network-dde-functions.md)
</dt> </dl>

 

 




