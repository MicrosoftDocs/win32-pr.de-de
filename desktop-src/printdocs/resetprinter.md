---
description: Die resetprinter-Funktion gibt die Werte für Datentyp und Geräte Modus an, die zum Drucken von Dokumenten verwendet werden, die von der StartDocPrinter-Funktion gesendet werden. Diese Werte können überschrieben werden, indem die Funktion setjob verwendet wird, nachdem der Druck von Dokumenten begonnen wurde.
ms.assetid: 9efc6629-dbb7-4320-90b9-07c66f0add47
title: Resetprinter-Funktion (winspool. h)
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
ms.openlocfilehash: 8bdfef0229a646e802878a96370d27d49a6bfc2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362497"
---
# <a name="resetprinter-function"></a>Resetprinter-Funktion

Die **resetprinter** -Funktion gibt die Werte für Datentyp und Geräte Modus an, die zum Drucken von Dokumenten verwendet werden, die von der [**StartDocPrinter**](startdocprinter.md) -Funktion gesendet werden. Diese Werte können überschrieben werden, indem die Funktion [**setjob**](setjob.md) verwendet wird, nachdem der Druck von Dokumenten begonnen wurde.

## <a name="syntax"></a>Syntax


```C++
BOOL ResetPrinter(
  _In_ HANDLE             hPrinter,
  _In_ LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprinter* \[ in\]
</dt> <dd>

Handle für den Drucker. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

*pdefault* \[ in\]
</dt> <dd>

Zeiger auf eine [**Drucker \_ Standard**](printer-defaults.md) Struktur.

Die **resetprinter** -Funktion ignoriert den **desiredAccess** -Member der [**Drucker \_ Standard**](printer-defaults.md) Struktur. Legen Sie diesen Member auf NULL fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Resetprinterw** (Unicode) und **resetprintera** (ANSI)<br/>                                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Drucker \_ Standardwerte**](printer-defaults.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**Setjob**](setjob.md)
</dt> </dl>

 

 




