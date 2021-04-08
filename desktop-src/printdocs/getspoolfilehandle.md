---
description: Die getspoolfilehandle-Funktion Ruft ein Handle für die Spooldatei ab, die dem derzeit von der Anwendung übermittelten Auftrag zugeordnet ist.
ms.assetid: df6f28b3-66a6-4fb7-bdde-40cd7d934c5f
title: Getspoolfilehandle-Funktion (winspool. h)
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
ms.openlocfilehash: 9ac4dd4b0db9a59cc0140872ff04f89adaf8b6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050492"
---
# <a name="getspoolfilehandle-function"></a>Getspoolfilehandle-Funktion

Die **getspoolfilehandle** -Funktion Ruft ein Handle für die Spooldatei ab, die dem derzeit von der Anwendung übermittelten Auftrag zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HANDLE GetSpoolFileHandle(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker, an den der Auftrag übermittelt wurde. Dies sollte das gleiche Handle sein, das verwendet wurde, um den Auftrag zu übermitteln. (Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird ein Handle für die Spooldatei zurückgegeben.

Wenn die Funktion fehlschlägt, wird ein **ungültiger \_ handle- \_ Wert** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Mit dem Handle für die Spooldatei kann die Anwendung mit Aufrufen von "Write [**File**](/windows/desktop/api/fileapi/nf-fileapi-writefile) " in die Spooldatei schreiben, gefolgt von " [**commitspooldata**](commitspooldata.md)".

Die Anwendung darf " [**closeprinter**](closeprinter.md) " nicht auf dem *hprinter* aufrufen, bis Sie zum letzten Mal auf die Spooldatei zugegriffen hat. Dann sollte es [**closespoolfilehandle**](closespoolfilehandle.md) gefolgt von **closeprinter** aufgerufen werden. Wenn Sie versuchen, auf das spooldateihandle zuzugreifen, nachdem der ursprüngliche *hprinter* geschlossen wurde, tritt ein Fehler auf, auch wenn das Datei Handle selbst nicht geschlossen wurde. **Closespoolfilehandle** schlägt selbst fehl, wenn **closeprinter** zuerst aufgerufen wird.

Diese Funktion schlägt fehl, wenn Sie aufgerufen wird, bevor der Druckauftrag das Spoolvorgang abgeschlossen hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Getspoolfilelenker** (Unicode) und **getspoolfilehandlea** (ANSI)<br/>                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**Closeprinter**](closeprinter.md)
</dt> <dt>

[**Closespoolfilehandle**](closespoolfilehandle.md)
</dt> <dt>

[**Commitspooldata**](commitspooldata.md)
</dt> </dl>

 

