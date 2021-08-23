---
description: Die GetDefaultPrinter-Funktion ruft den Druckernamen des Standarddruckers für den aktuellen Benutzer auf dem lokalen Computer ab.
ms.assetid: 8ec06743-43ce-4fac-83c4-f09eac7ee333
title: GetDefaultPrinter-Funktion (Winspool.h)
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
ms.openlocfilehash: 59d6ba435b592076455690916f5c627c73f65370df381861c25a6fafa21bf0f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949100"
---
# <a name="getdefaultprinter-function"></a>GetDefaultPrinter-Funktion

Die **GetDefaultPrinter-Funktion** ruft den Druckernamen des Standarddruckers für den aktuellen Benutzer auf dem lokalen Computer ab.

## <a name="syntax"></a>Syntax


```C++
BOOL GetDefaultPrinter(
  _In_    LPTSTR  pszBuffer,
  _Inout_ LPDWORD pcchBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszBuffer* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine auf NULL endende Zeichenfolge empfängt, die den Standarddruckernamen enthält. Wenn dieser Parameter **NULL** ist, schlägt die Funktion fehl, und die Variable, auf die *pcchBuffer* zeigt, gibt die erforderliche Puffergröße in Zeichen zurück.

</dd> <dt>

*pcchBuffer* \[ in, out\]
</dt> <dd>

Gibt bei der Eingabe die Größe des *pszBuffer-Puffers* in Zeichen an. Empfängt bei der Ausgabe die Größe der Druckernamenzeichenfolge in Zeichen, einschließlich des abschließenden NULL-Zeichens.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null), und die Variable, auf die *pcchBuffer* zeigt, enthält die Anzahl der Zeichen, die in den *pszBuffer-Puffer* kopiert werden, einschließlich des abschließenden NULL-Zeichens.

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.



| Wert                       | Bedeutung                                                                                                                        |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| FEHLER: \_ \_ UNZUREICHENDER PUFFER | Der *pszBuffer-Puffer* ist zu klein. Die Variable, auf die *pcchBuffer* zeigt, enthält die erforderliche Puffergröße in Zeichen. |
| FEHLERDATEI \_ \_ NICHT \_ GEFUNDEN     | Es gibt keinen Standarddrucker.                                                                                                   |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **GetDefaultPrinterW** (Unicode) und **GetDefaultPrinterA** (ANSI)<br/>                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**SetDefaultPrinter**](setdefaultprinter.md)
</dt> </dl>

 

 




