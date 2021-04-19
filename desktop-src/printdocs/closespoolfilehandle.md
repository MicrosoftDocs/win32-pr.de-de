---
description: Die closespoolfilehandle-Funktion schließt ein Handle für eine Spooldatei, die dem gerade von der Anwendung übermittelten Druckauftrag zugeordnet ist.
ms.assetid: e2c0e68f-b72e-4a97-ba18-8943bc5789c1
title: Closespoolfilehandle-Funktion (winspool. h)
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
ms.openlocfilehash: c808bddde5b9b4e4a87a8608c1efb3999ce1f391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349387"
---
# <a name="closespoolfilehandle-function"></a>Closespoolfilehandle-Funktion

Die **closespoolfilehandle** -Funktion schließt ein Handle für eine Spooldatei, die dem gerade von der Anwendung übermittelten Druckauftrag zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
BOOL CloseSpoolFileHandle(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker, an den der Auftrag übermittelt wurde. Dabei sollte es sich um das gleiche Handle handeln, das zum Abrufen von *hspoolfile* mit [**getspoolfilehandle**](getspoolfilehandle.md)verwendet wurde.

</dd> <dt>

*hspoolfile* \[ in\]
</dt> <dd>

Ein Handle für die Spooldatei, die geschlossen wird. Wenn [**commitspooldata**](commitspooldata.md) seit dem Aufruf von [**getspoolfilehandle**](getspoolfilehandle.md) nicht aufgerufen wurde, sollte dies das gleiche Handle sein, das von **getspoolfilehandle** zurückgegeben wurde. Andernfalls sollte es sich um das Handle handeln, das durch den letzten **Commit von commitspooldata** zurückgegeben wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**True**, wenn der Vorgang erfolgreich ist, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Die Anwendung darf " [**closeprinter**](closeprinter.md) " nicht auf dem *hprinter* aufrufen, bis Sie zum letzten Mal auf die Spooldatei zugegriffen hat. Dann sollte es **closespoolfilehandle** gefolgt von **closeprinter** aufgerufen werden. Wenn Sie versuchen, auf das spooldateihandle zuzugreifen, nachdem der ursprüngliche *hprinter* geschlossen wurde, tritt ein Fehler auf, auch wenn das Datei Handle selbst nicht geschlossen wurde. **Closespoolfilehandle** schlägt fehl, wenn **closeprinter** zuerst aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Closeprinter**](closeprinter.md)
</dt> <dt>

[**Getspoolfilehandle**](getspoolfilehandle.md)
</dt> </dl>

 

 




