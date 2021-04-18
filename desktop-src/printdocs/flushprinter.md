---
description: Die flushprinter-Funktion sendet einen Puffer an den Drucker, um ihn aus einem vorübergehenden Zustand zu löschen.
ms.assetid: 08e54175-da68-4ebd-91ec-8f4525f49d30
title: Flushprinter-Funktion (winspool. h)
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
ms.openlocfilehash: d46a4a8d7143e10fc13722d278ca21a0602b7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528997"
---
# <a name="flushprinter-function"></a>Flushprinter-Funktion

Die **flushprinter** -Funktion sendet einen Puffer an den Drucker, um ihn aus einem vorübergehenden Zustand zu löschen.

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

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für das Drucker Objekt. Dabei sollte es sich um das gleiche Handle handeln, das in einem vorherigen [**Write-Printer**](writeprinter.md) -Befehl vom Druckertreiber verwendet wurde.

</dd> <dt>

*PBUF* \[ in\]
</dt> <dd>

Ein Zeiger auf ein Bytearray, das die Daten enthält, die in den Drucker geschrieben werden sollen.

</dd> <dt>

*cbbuf* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Arrays, auf das von *PBUF* verwiesen wird.

</dd> <dt>

*pcwritten* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Wert, der die Anzahl der Daten Bytes empfängt, die an den Drucker geschrieben wurden.

</dd> <dt>

*csleep* \[ in\]
</dt> <dd>

Die Zeit (in Millisekunden), für die die e/a-Linie zum Druckerport im Leerlauf bleiben soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null.

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

**Flushprinter** sollte nur aufgerufen werden, wenn bei " [**Write-Printer**](writeprinter.md) " ein Fehler aufgetreten ist, sodass der Drucker in einem vorübergehenden Zustand ist. Beispielsweise könnte der Drucker in einen vorübergehenden Zustand geraten, wenn der Auftrag abgebrochen wird, und der Druckertreiber hat einige Rohdaten teilweise an den Drucker gesendet.

**Flushprinter** kann auch einen Leerlauf Zeitraum angeben, in dem der Druck Spooler keine Aufträge für den entsprechenden Druckerport plant.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**"Write Printer"**](writeprinter.md)
</dt> </dl>

 

 




