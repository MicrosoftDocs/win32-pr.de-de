---
description: Die GetSpoolFileHandle-Funktion ruft ein Handle für die Spooldatei ab, die dem aktuell von der Anwendung übermittelten Auftrag zugeordnet ist.
ms.assetid: df6f28b3-66a6-4fb7-bdde-40cd7d934c5f
title: GetSpoolFileHandle-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSpoolFileHandle
- GetSpoolFileHandleA
- GetSpoolFileHandleW
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 10b0b36333e51dfb5c831f6c74e00c6930ccbb9d1ce31646fed0d689abc7f639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117686693"
---
# <a name="getspoolfilehandle-function"></a>GetSpoolFileHandle-Funktion

Die **GetSpoolFileHandle-Funktion** ruft ein Handle für die Spooldatei ab, die dem aktuell von der Anwendung übermittelten Auftrag zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HANDLE GetSpoolFileHandle(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für den Drucker, an den der Auftrag übermittelt wurde. Dies sollte dasselbe Handle sein, das zum Übermitteln des Auftrags verwendet wurde. (Verwenden Sie die [**OpenPrinter-**](openprinter.md) oder [**AddPrinter-Funktion,**](addprinter.md) um ein Druckerhand handle abzurufen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, wird ein Handle an die Spooldatei zurückgegeben.

Wenn die Funktion fehlschlägt, gibt sie **INVALID \_ HANDLE VALUE \_ zurück.**

## <a name="remarks"></a>Hinweise

Mit dem Handle für die Spooldatei kann Ihre Anwendung mit Aufrufen von [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) gefolgt von CommitSpoolData in die [**Spooldatei schreiben.**](commitspooldata.md)

Ihre Anwendung darf [**ClosePrinter in**](closeprinter.md) *hPrinter* erst aufrufen, nachdem sie zum letzten Mal auf die Spooldatei zugegriffen hat. Anschließend sollte [**CloseSpoolFileHandle**](closespoolfilehandle.md) gefolgt von **ClosePrinter genannt werden.** Versuche, auf das Spooldateihand handle zu zugreifen, nachdem der ursprüngliche *hPrinter* geschlossen wurde, führen auch dann zu einem Fehler, wenn das Dateihand handle selbst nicht geschlossen wurde. **CloseSpoolFileHandle selbst kann** nicht verwendet werden, **wenn ClosePrinter** zuerst aufgerufen wird.

Diese Funktion kann nicht verwendet werden, wenn sie aufgerufen wird, bevor das Spoolen des Druckauftrags abgeschlossen ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **GetSpoolFileHandleW** (Unicode) und **GetSpoolFileHandleA** (ANSI)<br/>                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**CloseSpoolFileHandle**](closespoolfilehandle.md)
</dt> <dt>

[**CommitSpoolData**](commitspooldata.md)
</dt> </dl>

 

