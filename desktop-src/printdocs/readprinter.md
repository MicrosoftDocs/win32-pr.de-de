---
description: Die ReadPrinter-Funktion ruft Daten aus dem angegebenen Drucker ab.
ms.assetid: d7c3f186-c53e-424b-89bf-6742babb998f
title: ReadPrinter-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 63683e421441fb15ec299f3077088bd8f9cffb65644550be912ee39b5c530371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824020"
---
# <a name="readprinter-function"></a>ReadPrinter-Funktion

Die **ReadPrinter-Funktion** ruft Daten aus dem angegebenen Drucker ab.

## <a name="syntax"></a>Syntax


```C++
BOOL ReadPrinter(
  _In_  HANDLE  hPrinter,
  _Out_ LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pNoBytesRead
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für das Druckerobjekt, für das Daten abgerufen werden. Verwenden Sie die [**OpenPrinter-Funktion,**](openprinter.md) um ein Druckerobjekthand handle abzurufen. Verwenden Sie das Format Druckername, Auftrag xxxx.

</dd> <dt>

*pBuf* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die Druckerdaten empfängt.

</dd> <dt>

*cbBuf* \[ In\]
</dt> <dd>

Die Größe des Puffers in Bytes, auf den *pBuf* zeigt.

</dd> <dt>

*pNoBytesRead* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der Bytes von Daten empfängt, die in das Array kopiert werden, auf das *pBuf* zeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

**ReadPrinter gibt** einen Fehler zurück, wenn das Gerät oder der Drucker nicht bidirektional ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




