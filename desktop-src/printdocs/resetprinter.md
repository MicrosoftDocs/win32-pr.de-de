---
description: Die ResetPrinter-Funktion gibt die Datentyp- und Gerätemoduswerte an, die zum Drucken von Dokumenten verwendet werden sollen, die von der StartDocPrinter-Funktion übermittelt werden. Diese Werte können mithilfe der SetJob-Funktion überschrieben werden, nachdem der Dokumentdruck gestartet wurde.
ms.assetid: 9efc6629-dbb7-4320-90b9-07c66f0add47
title: ResetPrinter-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResetPrinter
- ResetPrinterA
- ResetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: f68601acde884d15572871848eed2d2388c927cf04758ad1183343486d4cc0f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470279"
---
# <a name="resetprinter-function"></a>ResetPrinter-Funktion

Die **ResetPrinter-Funktion** gibt die Datentyp- und Gerätemoduswerte an, die zum Drucken von Dokumenten verwendet werden sollen, die von der [**StartDocPrinter-Funktion übermittelt**](startdocprinter.md) werden. Diese Werte können mithilfe der [**SetJob-Funktion überschrieben**](setjob.md) werden, nachdem der Dokumentdruck gestartet wurde.

## <a name="syntax"></a>Syntax


```C++
BOOL ResetPrinter(
  _In_ HANDLE             hPrinter,
  _In_ LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Handle für den Drucker. Verwenden Sie [**die OpenPrinter-**](openprinter.md) [**oder AddPrinter-Funktion,**](addprinter.md) um einen Druckerhandpunkt abzurufen.

</dd> <dt>

*pDefault* \[ In\]
</dt> <dd>

Zeiger auf eine [**PRINTER \_ DEFAULTS-Struktur.**](printer-defaults.md)

Die **ResetPrinter-Funktion** ignoriert das **DesiredAccess-Member** der [**PRINTER \_ DEFAULTS-Struktur.**](printer-defaults.md) Legen Sie diesen Member auf 0 (null) fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **ResetPrinterW** (Unicode) und **ResetPrinterA** (ANSI)<br/>                                       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**\_DRUCKEREINSTELLUNGEN**](printer-defaults.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

 




