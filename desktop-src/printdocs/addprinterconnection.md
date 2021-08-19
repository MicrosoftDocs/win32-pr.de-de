---
description: Die AddPrinterConnection-Funktion fügt dem angegebenen Drucker für den aktuellen Benutzer eine Verbindung hinzu.
ms.assetid: 6decf89a-1411-4e7e-aa20-60e7068658c2
title: AddPrinterConnection-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection
- AddPrinterConnectionA
- AddPrinterConnectionW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 83c4d348266e0d596deccb03b39e98ec41f8f23837727520d55b9baff82fec4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869032"
---
# <a name="addprinterconnection-function"></a>AddPrinterConnection-Funktion

Die **AddPrinterConnection-Funktion** fügt dem angegebenen Drucker für den aktuellen Benutzer eine Verbindung hinzu.

## <a name="syntax"></a>Syntax


```C++
BOOL AddPrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen eines Druckers angibt, mit dem der aktuelle Benutzer eine Verbindung herstellen möchte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

Wenn Windows eine Verbindung mit einem Drucker herstellen, müssen möglicherweise Druckertreiberdateien auf den Server kopiert werden, an den der Drucker angefügt ist. Wenn der Benutzer nicht über die Berechtigung zum Kopieren von Dateien an den entsprechenden Speicherort verfügt, schlägt die **Funktion AddPrinterConnection** fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt ERROR \_ ACCESS \_ DENIED zurück.

Eine Druckerverbindung, die durch Aufrufen von **AddPrinterConnection** hergestellt wird, wird aufzählt, wenn [**EnumPrinters**](enumprinters.md) aufgerufen wird, wobei *dwType* auf PRINTER \_ ENUM CONNECTION festgelegt \_ ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **AddPrinterConnectionW** (Unicode) und **AddPrinterConnectionA** (ANSI)<br/>                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ConnectToPrinterDlg**](connecttoprinterdlg.md)
</dt> <dt>

[**DeletePrinterConnection**](deleteprinterconnection.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> </dl>

 

