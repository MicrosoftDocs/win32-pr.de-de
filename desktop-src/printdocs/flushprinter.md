---
description: Die FlushPrinter-Funktion sendet einen Puffer an den Drucker, um ihn aus einem vorübergehenden Zustand zu löschen.
ms.assetid: 08e54175-da68-4ebd-91ec-8f4525f49d30
title: FlushPrinter-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FlushPrinter
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 78bd5b6ccc86651a717c29db8b938508c857f83dbd3bdf5364fb1596b8a2c956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949300"
---
# <a name="flushprinter-function"></a>FlushPrinter-Funktion

Die **FlushPrinter-Funktion** sendet einen Puffer an den Drucker, um ihn aus einem vorübergehenden Zustand zu löschen.

## <a name="syntax"></a>Syntax


```C++
BOOL FlushPrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten,
  _In_  DWORD   cSleep
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für das Druckerobjekt. Dies sollte dasselbe Handle sein, das in einem vorherigen [**WritePrinter-Aufruf**](writeprinter.md) vom Druckertreiber verwendet wurde.

</dd> <dt>

*pBuf* \[ In\]
</dt> <dd>

Ein Zeiger auf ein Bytearray, das die auf den Drucker zu schreibenden Daten enthält.

</dd> <dt>

*cbBuf* \[ In\]
</dt> <dd>

Die Größe des Arrays in Bytes, auf das *pBuf zeigt.*

</dd> <dt>

*pcWritten* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Wert, der die Anzahl der Bytes von Daten empfängt, die auf den Drucker geschrieben wurden.

</dd> <dt>

*cSleep* \[ In\]
</dt> <dd>

Die Zeit in Millisekunden, für die die E/A-Leitung zum Druckerport im Leerlauf bleiben soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null.

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

**FlushPrinter sollte nur** aufgerufen werden, [**wenn WritePrinter**](writeprinter.md) fehlgeschlagen ist und der Drucker in einem vorübergehenden Zustand ist. Beispielsweise kann der Drucker in einen vorübergehenden Zustand kommen, wenn der Auftrag abgebrochen wird und der Druckertreiber einige Rohdaten teilweise an den Drucker gesendet hat.

**FlushPrinter kann** auch einen Leerlaufzeitraum angeben, in dem der Druckspooler keine Aufträge am entsprechenden Druckerport geplant.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




