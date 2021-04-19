---
description: Ruft die Liste der verfügbaren DDE-Freigaben ab.
ms.assetid: ce5aeddd-d9d1-40a2-a807-1a9c9f98f171
title: Ndde ShareEnum-Funktion (nddecoapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareEnum
- NDdeShareEnumA
- NDdeShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 8bfa4884b88e72cb9a3b64bebf58af53cdc1047e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359196"
---
# <a name="nddeshareenum-function"></a>Ndde ShareEnum-Funktion

\[Network DDE wird nicht mehr unterstützt. Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]

Ruft die Liste der verfügbaren DDE-Freigaben ab.

## <a name="syntax"></a>Syntax


```C++
UINT NDdeShareEnum(
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

Ein Zeiger auf einen Puffer, der die Liste der DDE-Freigaben empfängt. Die Liste der DDE-Freigaben wird als Sequenz von durch Null getrennten Zeichen folgen gespeichert, die mit einem doppelten NULL-Zeichen am Ende beendet werden. Dieser Parameter kann **NULL** sein. Wenn *lpBuffer* **null** ist, gibt die DSDM die Größe des Puffers zurück, der zum Speichern der Liste der Freigaben im *lpcbtotalavailable* -Parameter erforderlich ist.

</dd> <dt>

*cbubsize* \[ in\]
</dt> <dd>

Die Größe des *lpBuffer* -Puffers in Bytes. Dieser Parameter muss NULL sein, wenn *lpBuffer* **null** ist.

</dd> <dt>

*lpnentriesread* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Gesamtzahl der aufgelisteten Freigaben empfängt. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*lpcbtotalavailable* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Gesamtzahl der Bytes empfängt, die im Puffer zum Speichern der Liste der DDE-Freigaben benötigt werden. Dieser Parameter darf nicht **null** sein.

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
| Unicode- und ANSI-Name<br/>   | **Ndde shareenumw** (Unicode) und **nddebug** (ANSI)<br/>                  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über das Netzwerk dynamischer Datenaustausch](network-dynamic-data-exchange.md)
</dt> <dt>

[Network DDE-Funktionen](network-dde-functions.md)
</dt> </dl>

 

 




