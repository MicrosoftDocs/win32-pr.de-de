---
description: Die deleteprinter-Funktion löscht das angegebene Drucker Objekt.
ms.assetid: 04d9c073-b795-4307-ba89-d4984bc5b354
title: Deleteprinter-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 16d82a263b09c87f5c9b9725db48dd6634404ad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349834"
---
# <a name="deleteprinter-function"></a>Deleteprinter-Funktion

Die **deleteprinter** -Funktion löscht das angegebene Drucker Objekt.

## <a name="syntax"></a>Syntax


```C++
BOOL DeletePrinter(
  _Inout_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprinter* \[ in, out\]
</dt> <dd>

Handle für ein Drucker Objekt, das gelöscht wird. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Wenn noch Druckaufträge für den angegebenen Drucker verarbeitet werden, markiert **deleteprinter** den Drucker für das ausstehende löschen und löscht ihn dann, wenn alle Druckaufträge gedruckt wurden. Einem Drucker, der zum ausstehenden Löschen markiert ist, können keine Druckaufträge hinzugefügt werden.

Ein Drucker, der zum Löschen ausstehend markiert ist, kann nicht gespeichert werden, seine Druckaufträge können jedoch gehalten, fortgesetzt und neu gestartet werden. Wenn der Drucker angehalten wird und Aufträge für den Drucker vorhanden sind, schlägt **deleteprinter** mit Fehler \_ Zugriff \_ verweigert fehl.

Beachten Sie, dass **deleteprinter** das an ihn übertragende Handle nicht schließt. Daher muss die Anwendung [**closeprinter**](closeprinter.md)weiterhin aufzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**Enumdrucker**](enumprinters.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




