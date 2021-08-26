---
description: Die CloseSpoolFileHandle-Funktion schließt ein Handle für eine Spooldatei, die dem aktuell von der Anwendung übermittelten Druckauftrag zugeordnet ist.
ms.assetid: e2c0e68f-b72e-4a97-ba18-8943bc5789c1
title: CloseSpoolFileHandle-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CloseSpoolFileHandle
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: f62173747472820f1642578778b67f3cdc3403523d6ae28453888dae3d6d1a23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950530"
---
# <a name="closespoolfilehandle-function"></a>CloseSpoolFileHandle-Funktion

Die **CloseSpoolFileHandle-Funktion** schließt ein Handle für eine Spooldatei, die dem aktuell von der Anwendung übermittelten Druckauftrag zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
BOOL CloseSpoolFileHandle(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für den Drucker, an den der Auftrag übermittelt wurde. Dies sollte dasselbe Handle sein, das zum Abrufen von *hSpoolFile* mit [**GetSpoolFileHandle verwendet wurde.**](getspoolfilehandle.md)

</dd> <dt>

*hSpoolFile* \[ In\]
</dt> <dd>

Ein Handle für die zu schließende Spooldatei. Wenn [**CommitSpoolData**](commitspooldata.md) seit dem Aufgerufenen [**von GetSpoolFileHandle**](getspoolfilehandle.md) nicht aufgerufen wurde, sollte dies dasselbe Handle sein, das von **GetSpoolFileHandle zurückgegeben wurde.** Andernfalls sollte es das Handle sein, das durch den letzten Aufruf von **CommitSpoolData zurückgegeben wurde.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**TRUE,** wenn dies erfolgreich ist, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Ihre Anwendung darf [**ClosePrinter in**](closeprinter.md) *hPrinter* erst aufrufen, nachdem sie zum letzten Mal auf die Spooldatei zugegriffen hat. Anschließend sollte **CloseSpoolFileHandle** gefolgt von **ClosePrinter genannt werden.** Versuche, auf das Spooldateihand handle zu zugreifen, nachdem der ursprüngliche *hPrinter* geschlossen wurde, führen auch dann zu einem Fehler, wenn das Dateihand handle selbst nicht geschlossen wurde. **CloseSpoolFileHandle kann** nicht verwendet werden, **wenn ClosePrinter** zuerst aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool.drv</dt> </dl>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**GetSpoolFileHandle**](getspoolfilehandle.md)
</dt> </dl>

 

 




