---
description: Die advanceddocumentproperties-Funktion zeigt ein druckerkonfigurationsdialogfeld für den angegebenen Drucker an, sodass der Benutzer diesen Drucker konfigurieren kann.
ms.assetid: 29e33f34-f6ec-4989-b076-e1fef8eb5bc4
title: Advanceddocumentproperties-Funktion (winspool. h)
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
ms.openlocfilehash: da8754add6e3f5997354c940c303c41d4588c7b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759559"
---
# <a name="advanceddocumentproperties-function"></a>Advanceddocumentproperties-Funktion

Die **advanceddocumentproperties** -Funktion zeigt ein druckerkonfigurationsdialogfeld für den angegebenen Drucker an, sodass der Benutzer diesen Drucker konfigurieren kann.

Diese Funktion ist ein Sonderfall der [**DocumentProperties**](documentproperties.md) -Funktion. Weitere Informationen finden Sie im Abschnitt "Hinweise".

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

*HWND* \[ in\]
</dt> <dd>

Ein Handle für das übergeordnete Fenster des druckerkonfigurationsdialogfelds.

</dd> <dt>

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für ein Drucker Objekt. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

*pdevicename* \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Geräts angibt, für das ein Dialogfeld für die Druckerkonfiguration angezeigt werden soll.

</dd> <dt>

*pdevmodeoutput* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die die vom Benutzer angegebenen Konfigurationsdaten enthält.

</dd> <dt>

*pdevmodeinput* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur, die die Konfigurationsdaten enthält, die zum Initialisieren der Steuerelemente im Dialogfeld Druckerkonfiguration verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die [**DocumentProperties**](documentproperties.md) -Funktion mit diesen Parametern erfolgreich ist, ist der Rückgabewert von **advanceddocumentproperties** 1. Andernfalls ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Diese Funktion kann nur das Dialogfeld Druckerkonfiguration anzeigen, sodass Sie von einem Benutzer konfiguriert werden kann. Wenn Sie mehr Kontrolle haben, verwenden Sie [**DocumentProperties**](documentproperties.md). Die Eingabeparameter für diese Funktion werden direkt an **DocumentProperties** übermittelt, und der *fmode* -Wert wird in der \_ Puffer- \_ \| DM \_ in der \_ Eingabeaufforderung-DM- \| \_ \_ Puffer auf DM festgelegt. Im Gegensatz zu **DocumentProperties** gibt diese Funktion nur 1 oder 0 zurück. Daher können Sie die erforderliche Größe von [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) nicht ermitteln, indem Sie *pdevmode* auf NULL festlegen.

Eine Anwendung kann den Namen, auf den der *pdevicename* -Parameter verweist, abrufen, indem Sie die [**GetPrinter**](getprinter.md) -Funktion aufruft und dann den **pprintername** -Member der " [**Printer \_ Info \_ 2**](printer-info-2.md) "-Struktur untersucht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Advanceddocumentpropertiesw** (Unicode) und **advanceddocumentpropertiesa** (ANSI)<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**DocumentProperties**](documentproperties.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 2**](printer-info-2.md)
</dt> </dl>

 

 




