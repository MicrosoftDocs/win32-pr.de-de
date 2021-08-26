---
description: Ruft DDE-Freigabeinformationen ab. Dies erfolgt in der Regel für die Bearbeitung.
ms.assetid: a2e48a4d-2b72-40a3-b827-474da1db0910
title: NDdeShareGetInfo-Funktion (Nddeapi.h)
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
ms.openlocfilehash: 2c622a611b3d917dcf67de2ec6b96070ec0e54e9e53b0cef04c3c9e35b859e40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014750"
---
# <a name="nddesharegetinfo-function"></a>NDdeShareGetInfo-Funktion

\[Netzwerk-DDE wird nicht mehr unterstützt. Nddeapi.dll ist auf Windows Vista vorhanden, aber alle Funktionsaufrufe geben NDDE \_ NICHT \_ IMPLEMENTIERT zurück.\]

Ruft DDE-Freigabeinformationen ab. Dies erfolgt in der Regel für die Bearbeitung.

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

*lpszServer* \[ In\]
</dt> <dd>

Der Name des Servers, auf dem sich das DSDM befindet.

</dd> <dt>

*lpszShareName* \[ In\]
</dt> <dd>

Der Freigabename, dessen Informationen aus dem DSDM abgerufen werden sollen. Dieser Parameter darf nicht NULL **sein.**

</dd> <dt>

*nLevel* \[ In\]
</dt> <dd>

Die Informationsebene. Dieser Parameter muss 2 sein.

</dd> <dt>

*lpBuffer* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die [**NDDESHAREINFO-Struktur**](nddeshareinfo-str.md) und die zugeordneten Daten empfängt, auf die die Member zeigen. Dieser Parameter kann **NULL** sein. Wenn *lpBuffer* **NULL ist,** berechnet das DSDM die Anzahl der Bytes, die zum Speichern der angeforderten Freigabeinformationen erforderlich sind, und gibt diesen Wert zusammen mit dem Fehler NDDE BUF TOO SMALL im Feld *lpnTotalAvailable* \_ \_ \_ zurück.

</dd> <dt>

*cBufSize* \[ In\]
</dt> <dd>

Die Größe des *lpBuffer-Puffers* in Bytes. Wenn *lpBuffer* NULL **ist,** sollte *cBufSize* 0 (null) sein.

</dd> <dt>

*lpnTotalAvailable* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Gesamtzahl der Bytes empfängt, die zum Speichern der angeforderten Freigabeinformationen erforderlich sind. Dieser Parameter darf nicht **NULL sein.**

</dd> <dt>

*lpnItems* \[ In\]
</dt> <dd>

Ein Zeiger auf eine Elementauswahlmaske zum Abrufen von Teilfreigabeinformationen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert NDDE \_ NO \_ ERROR.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode, der durch Aufrufen von [**NDdeGetErrorString**](nddegeterrorstring.md)in eine Textfehlermeldung übersetzt werden kann. Wenn der *lpBuffer-Parameter* **NULL ist,** wird NDDE \_ BUF \_ TOO SMALL \_ zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **NDdeShareGetInfoW** (Unicode) und **NDdeShareGetInfoA** (ANSI)<br/>            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht dynamische Daten Exchange Netzwerksicherheit](network-dynamic-data-exchange.md)
</dt> <dt>

[DDE-Netzwerkfunktionen](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeShareSetInfo**](nddesharesetinfo.md)
</dt> </dl>

 

 




