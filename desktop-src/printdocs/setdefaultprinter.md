---
description: Die SetDefaultPrinter-Funktion legt den Druckernamen des Standarddruckers für den aktuellen Benutzer auf dem lokalen Computer fest.
ms.assetid: 55eec548-577f-422b-80e3-8b23aa4d2159
title: SetDefaultPrinter-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDefaultPrinter
- SetDefaultPrinterA
- SetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 570e0d57c4a04cd4845883e825acfbbef0282186cc7289751737798ed52b9592
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112120"
---
# <a name="setdefaultprinter-function"></a>SetDefaultPrinter-Funktion

Die **SetDefaultPrinter-Funktion** legt den Druckernamen des Standarddruckers für den aktuellen Benutzer auf dem lokalen Computer fest.

## <a name="syntax"></a>Syntax


```C++
BOOL SetDefaultPrinter(
  _In_ LPCTSTR pszPrinter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszPrinter* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Standarddruckernamen enthält. Für eine Remotedruckerverbindung lautet das Namensformat **\\\\**  *_\\_* _Serverdruckername_. Bei einem lokalen Drucker lautet das Namensformat *druckername*.

Wenn dieser Parameter **NULL** oder eine leere Zeichenfolge ist, d. h. "", wählt **SetDefaultPrinter** einen Standarddrucker aus einem der installierten Drucker aus. Wenn bereits ein Standarddrucker vorhanden ist, kann das Aufrufen von **SetDefaultPrinter** mit einem **NULL-Wert** oder einer leeren Zeichenfolge in diesem Parameter den Standarddrucker ändern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

Wenn Sie diese Methode verwenden, müssen Sie einen gültigen Drucker, Treiber und Port angeben. Wenn sie ungültig sind, schlagen die APIs nicht fehl, aber das Ergebnis ist nicht definiert. Dies kann dazu führen, dass andere Programme den Drucker wieder auf den vorherigen gültigen Drucker festlegen. Sie können [**EnumPrinters**](enumprinters.md) verwenden, um den Druckernamen, Treibernamen und Portnamen aller verfügbaren Drucker abzurufen.

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
| Unicode- und ANSI-Name<br/>   | **SetDefaultPrinterW** (Unicode) und **SetDefaultPrinterA** (ANSI)<br/>                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**GetDefaultPrinter**](getdefaultprinter.md)
</dt> </dl>

 

 




