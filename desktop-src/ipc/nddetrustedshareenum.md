---
description: Ruft die Namen aller Netzwerk-DDE-Freigaben ab, die im Kontext des aufrufenden Prozesses als vertrauenswürdig eingestuft werden.
ms.assetid: 8e2323a4-0c27-44e6-9598-08a3c1a88bd3
title: NDdeTrustedShareEnum-Funktion (Nddeapi.h)
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
ms.openlocfilehash: fc8eefd335ad9c54e7dc4aefa5a1027785de1b9c33cd3346c8bb1c8a4872b939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117695042"
---
# <a name="nddetrustedshareenum-function"></a>NDdeTrustedShareEnum-Funktion

\[Netzwerk-DDE wird nicht mehr unterstützt. Nddeapi.dll ist auf Windows Vista vorhanden, aber alle Funktionsaufrufe geben NDDE \_ NOT \_ IMPLEMENTED zurück.\]

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

*lpszServer* \[ In\]
</dt> <dd>

Der Name des Servers, auf dem sich das DSDM befindet.

</dd> <dt>

*nLevel* \[ In\]
</dt> <dd>

Reserviert. Dieser Parameter muss 0 (null) sein.

</dd> <dt>

*lpBuffer* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Liste der vertrauenswürdigen DDE-Freigaben empfängt. Die Liste der vertrauenswürdigen DDE-Freigaben wird als Sequenz von durch NULL getrennten Zeichenfolgen zurückgegeben, die am Ende mit einem doppelten NULL-Zeichen beendet werden. Dieser Parameter kann **NULL** sein. Wenn *lpBuffer* **NULL** ist, gibt das DSDM die Größe des Puffers zurück, der für die Liste der Freigaben im Feld *lpcbTotalAvailable* erforderlich ist.

</dd> <dt>

*cBufSize* \[ In\]
</dt> <dd>

Die Größe des *lpBuffer-Puffers* in Bytes. Dieser Parameter muss 0 (null) sein, wenn *lpBuffer* **NULL** ist.

</dd> <dt>

*lpnEntriesRead* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Gesamtzahl der vertrauenswürdigen Freigaben empfängt, die aufgezählt werden. Dieser Parameter darf nicht **NULL** sein.

</dd> <dt>

*lpcbTotalAvailable* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Gesamtzahl der Bytes empfängt, die zum Speichern der Liste der vertrauenswürdigen DDE-Freigaben erforderlich sind. Dieser Parameter darf nicht **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert NDDE \_ NO \_ ERROR.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch Aufrufen von [**NDdeGetErrorString**](nddegeterrorstring.md)in eine Textfehlermeldung übersetzt werden kann. Wenn der *lpBuffer-Parameter* **NULL** ist, wird NDDE \_ BUF \_ TOO SMALL \_ zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **NDdeTrustedShareEnumW** (Unicode) und **NDdeTrustedShareEnumA** (ANSI)<br/>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Network dynamische Daten Exchange Overview (Übersicht über Netzwerk-dynamische Daten Exchange)](network-dynamic-data-exchange.md)
</dt> <dt>

[Netzwerk-DDE-Funktionen](network-dde-functions.md)
</dt> </dl>

 

 




