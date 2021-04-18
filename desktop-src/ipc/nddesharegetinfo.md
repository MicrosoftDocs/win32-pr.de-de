---
description: Ruft DDE-Freigabe Informationen ab. Dies erfolgt in der Regel zur Bearbeitung.
ms.assetid: a2e48a4d-2b72-40a3-b827-474da1db0910
title: Ndde sharegetinfo-Funktion (nddecoapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareGetInfo
- NDdeShareGetInfoA
- NDdeShareGetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 72dc9ae12b174555debfa21afac15e5bfbed993e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344649"
---
# <a name="nddesharegetinfo-function"></a>Nddebug-Funktion

\[Network DDE wird nicht mehr unterstützt. Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]

Ruft DDE-Freigabe Informationen ab. Dies erfolgt in der Regel zur Bearbeitung.

## <a name="syntax"></a>Syntax


```C++
UINT NDdeShareGetInfo(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnTotalAvailable,
  _In_  LPWORD  lpnItems
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszserver* \[ in\]
</dt> <dd>

Der Name des Servers, auf dem sich die DSDM befindet.

</dd> <dt>

*lpszsharename* \[ in\]
</dt> <dd>

Der Freigabe Name, dessen Informationen aus dem DSDM abgerufen werden sollen. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*Nlevel* \[ in\]
</dt> <dd>

Die Informationsebene. Dieser Parameter muss 2 sein.

</dd> <dt>

*lpBuffer* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die [**ndbeshareingefo**](nddeshareinfo-str.md) -Struktur und die zugehörigen Daten empfängt, auf die von den Membern verwiesen wird. Dieser Parameter kann **NULL** sein. Wenn *lpBuffer* **null** ist, berechnet die DSDM die Anzahl der Bytes, die zum Speichern der angeforderten Freigabe Informationen erforderlich sind, und gibt diesen Wert im Feld *lpntotalavailable* zusammen mit dem \_ zu kleinen ndde buf- \_ Fehler zurück \_ .

</dd> <dt>

*cbubsize* \[ in\]
</dt> <dd>

Die Größe des *lpBuffer* -Puffers in Bytes. Wenn *lpBuffer* den Wert **null** hat, sollte *cbubsize* gleich NULL sein.

</dd> <dt>

*lpntotalavailable* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Gesamtzahl der Bytes empfängt, die zum Speichern der angeforderten Freigabe Informationen benötigt werden. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*lpnitems* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Elementauswahl Maske für das Abrufen partieller Freigabe Informationen.

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
| Unicode- und ANSI-Name<br/>   | **Nddebug** (Unicode) und **ndabsharegetinfoa** (ANSI)<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über das Netzwerk dynamischer Datenaustausch](network-dynamic-data-exchange.md)
</dt> <dt>

[Network DDE-Funktionen](network-dde-functions.md)
</dt> <dt>

[**Nddebug-Info**](nddeshareinfo-str.md)
</dt> <dt>

[**Nddesharesetinfo**](nddesharesetinfo.md)
</dt> </dl>

 

 




