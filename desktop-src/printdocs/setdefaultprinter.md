---
description: Mit der Funktion "SetDefaultPrinter" wird der Druckername des Standard Druckers für den aktuellen Benutzer auf dem lokalen Computer festgelegt.
ms.assetid: 55eec548-577f-422b-80e3-8b23aa4d2159
title: SetDefaultPrinter-Funktion (winspool. h)
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
ms.openlocfilehash: 346d356aea3d806284823541aa219699e51c2187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348141"
---
# <a name="setdefaultprinter-function"></a>SetDefaultPrinter-Funktion

Mit der Funktion " **SetDefaultPrinter** " wird der Druckername des Standard Druckers für den aktuellen Benutzer auf dem lokalen Computer festgelegt.

## <a name="syntax"></a>Syntax


```C++
BOOL SetDefaultPrinter(
  _In_ LPCTSTR pszPrinter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszprinter* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Standarddrucker Namen enthält. Bei einer Remote Druckerverbindung lautet das Namensformat **\\\\** _Server_- *_\\_* _Druckername_. Bei einem lokalen Drucker lautet das Namensformat " *Druckername*".

Wenn dieser Parameter **null** ist oder eine leere Zeichenfolge ist, d. h. "", wählt **SetDefaultPrinter** einen Standarddrucker von einem der installierten Drucker aus. Wenn bereits ein Standarddrucker vorhanden ist, kann der Standarddrucker durch Aufrufen von **SetDefaultPrinter** mit **null** oder einer leeren Zeichenfolge in diesem Parameter geändert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

Wenn Sie diese Methode verwenden, müssen Sie einen gültigen Drucker, Treiber und Port angeben. Wenn Sie ungültig sind, schlagen die APIs nicht fehl, aber das Ergebnis ist nicht definiert. Dies könnte dazu führen, dass andere Programme den Drucker auf den vorherigen gültigen Drucker zurücksetzen. Mit [**enumdruckern**](enumprinters.md) können Sie den Drucker Namen, den Treiber Namen und den Portnamen aller verfügbaren Drucker abrufen.

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
| Unicode- und ANSI-Name<br/>   | **Setdefaultprinterw** (Unicode) und **setdefaultprintera** (ANSI)<br/>                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Enumdrucker**](enumprinters.md)
</dt> <dt>

[**GetDefaultPrinter**](getdefaultprinter.md)
</dt> </dl>

 

 




