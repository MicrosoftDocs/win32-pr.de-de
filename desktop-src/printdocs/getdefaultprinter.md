---
description: Die GetDefaultPrinter-Funktion Ruft den Drucker Namen des Standard Druckers für den aktuellen Benutzer auf dem lokalen Computer ab.
ms.assetid: 8ec06743-43ce-4fac-83c4-f09eac7ee333
title: GetDefaultPrinter-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDefaultPrinter
- GetDefaultPrinterA
- GetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 8db5b2aef859ea5d8247fc203611af74c8daddd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348599"
---
# <a name="getdefaultprinter-function"></a>GetDefaultPrinter-Funktion

Die **GetDefaultPrinter** -Funktion Ruft den Drucker Namen des Standard Druckers für den aktuellen Benutzer auf dem lokalen Computer ab.

## <a name="syntax"></a>Syntax


```C++
BOOL GetDefaultPrinter(
  _In_    LPTSTR  pszBuffer,
  _Inout_ LPDWORD pcchBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszbuffer* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine NULL-terminierte Zeichenfolge mit dem Standarddrucker Namen empfängt. Wenn dieser Parameter **null** ist, schlägt die Funktion fehl, und die Variable, auf die von *pcchBuffer* verwiesen wird, gibt die erforderliche Puffergröße in Zeichen zurück.

</dd> <dt>

*pcchBuffer* \[ in, out\]
</dt> <dd>

Gibt bei der Eingabe die Größe des *pszbuffer* -Puffers in Zeichen an. Bei der Ausgabe empfängt die Größe der Drucker Namen Zeichenfolge in Zeichen, einschließlich des abschließenden NULL-Zeichens.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich NULL, und die Variable, auf die von *pcchBuffer* verwiesen wird, enthält die Anzahl der Zeichen, die in den *pszbuffer* -Puffer kopiert werden, einschließlich des abschließenden NULL-Zeichens.

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.



| Wert                       | Bedeutung                                                                                                                        |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Fehler \_ beim \_ Puffer. | Der *pszbuffer* -Puffer ist zu klein. Die Variable, auf die von *pcchBuffer* verwiesen wird, enthält die erforderliche Puffergröße in Zeichen. |
| Fehler \_ Datei \_ nicht \_ gefunden.     | Es ist kein Standarddrucker vorhanden.                                                                                                   |



 

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
| Unicode- und ANSI-Name<br/>   | **Getdefaultprinterw** (Unicode) und **getdefaultprintera** (ANSI)<br/>                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Methode SetDefaultPrinter auf**](setdefaultprinter.md)
</dt> </dl>

 

 




