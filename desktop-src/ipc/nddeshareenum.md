---
description: Ruft die Liste der verfügbaren DDE-Freigaben ab.
ms.assetid: ce5aeddd-d9d1-40a2-a807-1a9c9f98f171
title: NDdeShareEnum-Funktion (Nddeapi.h)
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
ms.openlocfilehash: e6b101a7ba45e28175a8d6ee0730e704a6f519142f94e4fc2273d1d76dcfe1cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014740"
---
# <a name="nddeshareenum-function"></a>NDdeShareEnum-Funktion

\[Netzwerk-DDE wird nicht mehr unterstützt. Nddeapi.dll ist auf Windows Vista vorhanden, aber alle Funktionsaufrufe geben NDDE \_ NOT \_ IMPLEMENTED zurück.\]

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

Ein Zeiger auf einen Puffer, der die Liste der DDE-Freigaben empfängt. Die Liste der DDE-Freigaben wird als Sequenz von Durch NULL getrennten Zeichenfolgen gespeichert, die am Ende mit einem doppelten NULL-Zeichen enden. Dieser Parameter kann **NULL** sein. Wenn *lpBuffer* **NULL** ist, gibt das DSDM die Größe des Puffers zurück, der für die Liste der Freigaben im *lpcbTotalAvailable-Parameter* erforderlich ist.

</dd> <dt>

*cBufSize* \[ In\]
</dt> <dd>

Die Größe des *lpBuffer-Puffers* in Bytes. Dieser Parameter muss 0 (null) sein, wenn *lpBuffer* **NULL** ist.

</dd> <dt>

*lpnEntriesRead* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Gesamtzahl der aufgezählten Freigaben empfängt. Dieser Parameter darf nicht **NULL** sein.

</dd> <dt>

*lpcbTotalAvailable* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Gesamtzahl der Bytes empfängt, die im Puffer zum Speichern der Liste der DDE-Freigaben benötigt werden. Dieser Parameter darf nicht **NULL** sein.

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
| Unicode- und ANSI-Name<br/>   | **NDdeShareEnumW** (Unicode) und **NDdeShareEnumA** (ANSI)<br/>                  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Network dynamische Daten Exchange Overview (Übersicht über Netzwerk-dynamische Daten Exchange)](network-dynamic-data-exchange.md)
</dt> <dt>

[Netzwerk-DDE-Funktionen](network-dde-functions.md)
</dt> </dl>

 

 




