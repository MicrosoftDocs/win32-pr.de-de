---
description: Die AdvancedDocumentProperties-Funktion zeigt ein Dialogfeld für die Druckerkonfiguration für den angegebenen Drucker an, sodass der Benutzer diesen Drucker konfigurieren kann.
ms.assetid: 29e33f34-f6ec-4989-b076-e1fef8eb5bc4
title: AdvancedDocumentProperties-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdvancedDocumentProperties
- AdvancedDocumentPropertiesA
- AdvancedDocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 2451f8e0668e0064566511bbf5eeb05e65094967486142719629400cf8d97348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720270"
---
# <a name="advanceddocumentproperties-function"></a>AdvancedDocumentProperties-Funktion

Die **AdvancedDocumentProperties-Funktion** zeigt ein Dialogfeld für die Druckerkonfiguration für den angegebenen Drucker an, sodass der Benutzer diesen Drucker konfigurieren kann.

Diese Funktion ist ein Sonderfall der [**DocumentProperties-Funktion.**](documentproperties.md) Weitere Informationen finden Sie im Abschnitt "Hinweise".

## <a name="syntax"></a>Syntax


```C++
LONG AdvancedDocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hWnd* \[ In\]
</dt> <dd>

Ein Handle für das übergeordnete Fenster des Dialogfelds "Druckerkonfiguration".

</dd> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für ein Druckerobjekt. Verwenden Sie [**die OpenPrinter-**](openprinter.md) [**oder AddPrinter-Funktion,**](addprinter.md) um einen Druckerhandpunkt abzurufen.

</dd> <dt>

*pDeviceName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Namen des Geräts angibt, für das ein Dialogfeld für die Druckerkonfiguration angezeigt werden soll.

</dd> <dt>

*pDevModeOutput* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die die vom Benutzer angegebenen Konfigurationsdaten enthält.

</dd> <dt>

*pDevModeInput* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**DEVMODE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) die die Konfigurationsdaten enthält, die zum Initialisieren der Steuerelemente des Dialogfelds "Druckerkonfiguration" verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die [**DocumentProperties-Funktion**](documentproperties.md) mit diesen Parametern erfolgreich ist, ist der Rückgabewert von **AdvancedDocumentProperties** 1. Andernfalls ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückkehrt. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren des Druckertreibers ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion aus einem Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte dazu kommen, dass die Anwendung nicht reagiert.

 

Diese Funktion kann nur das Dialogfeld "Druckerkonfiguration" anzeigen, damit ein Benutzer es konfigurieren kann. Verwenden Sie [**documentProperties, um**](documentproperties.md)mehr Kontrolle zu haben. Die Eingabeparameter für diese Funktion werden direkt an **DocumentProperties** übergeben, und der *fMode-Wert* wird auf DM \_ IN BUFFER DM IN PROMPT DM OUT \_ BUFFER \| \_ \_ \| \_ \_ festgelegt. Im **Gegensatz zu DocumentProperties** gibt diese Funktion nur 1 oder 0 zurück. Daher können Sie die erforderliche Größe von [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) nicht ermitteln, indem *Sie pDevMode auf* 0 (null) festlegen.

Eine Anwendung kann den Namen abrufen, auf den der *pDeviceName-Parameter* verweist, indem sie die [**GetPrinter-Funktion**](getprinter.md) aufruft und dann den **pPrinterName-Member** der [**PRINTER INFO \_ \_ 2-Struktur**](printer-info-2.md) untersucht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **AdvancedDocumentPropertiesW** (Unicode) und **AdvancedDocumentPropertiesA** (ANSI)<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**Documentproperties**](documentproperties.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**DRUCKERINFORMATIONEN \_ \_ 2**](printer-info-2.md)
</dt> </dl>

 

 




