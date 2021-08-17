---
description: Die EnumPrinterKey-Funktion aufzählt die Unterschlüssel eines angegebenen Schlüssels für einen angegebenen Drucker.
ms.assetid: 721b1d23-a594-4439-b8f9-9b11be5fe874
title: EnumPrinterKey-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterKey
- EnumPrinterKeyA
- EnumPrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c3666cce36884a331085d074df44e05b5bcfd0422433ce24bdbf3dbc385d7f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471784"
---
# <a name="enumprinterkey-function"></a>EnumPrinterKey-Funktion

Die **EnumPrinterKey-Funktion** aufzählt die Unterschlüssel eines angegebenen Schlüssels für einen angegebenen Drucker.

Druckerdaten werden in der Registrierung gespeichert. Rufen Sie beim Aufzählen von Druckerdaten keine Registrierungsfunktionen auf, die die Daten ändern könnten.

## <a name="syntax"></a>Syntax


```C++
DWORD EnumPrinterKey(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPTSTR  pSubkey,
  _In_  DWORD   cbSubkey,
  _Out_ LPDWORD pcbSubkey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für den Drucker, für den die Funktion Unterschlüssel aufzählt. Verwenden Sie [**die OpenPrinter-**](openprinter.md) [**oder AddPrinter-Funktion,**](addprinter.md) um einen Druckerhandpunkt abzurufen.

</dd> <dt>

*pKeyName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die den Schlüssel angibt, der die aufzählenden Unterschlüssel enthält. Verwenden Sie den schrägen Schrägstrich '' als Trennzeichen, um einen Pfad \\ mit mindestens einem Unterschlüssel anzugeben. **EnumPrinterKey** aufzählt alle Unterschlüssel des Schlüssels, aber nicht die Unterschlüssel dieser Unterschlüssel.

Wenn *pKeyName eine* leere Zeichenfolge ("") ist, **enumPrinterKey** den Schlüssel der obersten Ebene für den Drucker aufzählt. Wenn *pKeyName* NULL **ist,** gibt **EnumPrinterKey** ERROR \_ INVALID PARAMETER \_ zurück.

</dd> <dt>

*pSubkey* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der ein Array von Null-Terminierungsunterschlüsselnamen empfängt. Das Array wird mit zwei NULL-Zeichen beendet.

</dd> <dt>

*cbSubkey* \[ In\]
</dt> <dd>

Die Größe des Puffers in Bytes, auf den *pSubkey zeigt.* Wenn Sie *cbSubkey auf* 0 (null) festlegen, gibt der *parameter "ierungSubkey"* die erforderliche Puffergröße zurück.

</dd> <dt>

*dateiSubkey* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der im *pSubkey-Puffer abgerufenen Bytes* empfängt. Wenn die von *cbSubkey* angegebene Puffergröße zu klein ist, gibt die Funktion ERROR MORE DATA zurück, und \_ \_ *"malwareSubkey"* gibt die erforderliche Puffergröße an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Systemfehlercode. Wenn *pKeyName nicht* vorhanden ist, ist der Rückgabewert ERROR \_ FILE NOT \_ \_ FOUND.

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
| Unicode- und ANSI-Name<br/>   | **EnumPrinterKeyW** (Unicode) und **EnumPrinterKeyA** (ANSI)<br/>                                   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDataEx**](deleteprinterdataex.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




