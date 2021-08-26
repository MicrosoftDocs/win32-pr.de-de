---
description: Die DeletePrinterConnection-Funktion löscht eine Verbindung mit einem Drucker, der durch einen Aufruf von AddPrinterConnection oder ConnectToPrinterDlg hergestellt wurde.
ms.assetid: 7b056eea-fbd9-4a08-a2dc-7326caeec387
title: DeletePrinterConnection-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterConnection
- DeletePrinterConnectionA
- DeletePrinterConnectionW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: e8a00b8b29ff5da4fb9b75af435c36f6313bd46d287408731eb3171d2e3b5001
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950060"
---
# <a name="deleteprinterconnection-function"></a>DeletePrinterConnection-Funktion

Die **DeletePrinterConnection-Funktion** löscht eine Verbindung mit einem Drucker, der durch einen Aufruf von [**AddPrinterConnection**](addprinterconnection.md) oder [**ConnectToPrinterDlg hergestellt wurde.**](connecttoprinterdlg.md)

## <a name="syntax"></a>Syntax


```C++
BOOL DeletePrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen der zu löschenden Druckerverbindung angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

Die **DeletePrinterConnection-Funktion** löscht keine Druckertreiberdateien, die auf den Server kopiert wurden, an den der Drucker angefügt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **DeletePrinterConnectionW** (Unicode) und **DeletePrinterConnectionA** (ANSI)<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterConnection**](addprinterconnection.md)
</dt> <dt>

[**AddPrinterConnection2**](addprinterconnection2.md)
</dt> <dt>

[**ConnectToPrinterDlg**](connecttoprinterdlg.md)
</dt> </dl>

 

 




