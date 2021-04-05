---
description: Die enumprinterdataex-Funktion Listet alle Wertnamen und-Daten für einen angegebenen Drucker und Schlüssel auf.
ms.assetid: bc5ecc46-24a4-4b54-9431-0eaf6446e2d6
title: Enumprinterdataex-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDataEx
- EnumPrinterDataExA
- EnumPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 517d480d1c831627cadb289c41f99d24b1025ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757854"
---
# <a name="enumprinterdataex-function"></a>Enumprinterdataex-Funktion

Die **enumprinterdataex** -Funktion Listet alle Wertnamen und-Daten für einen angegebenen Drucker und Schlüssel auf.

Druckerdaten werden in der Registrierung gespeichert. Wenn Sie Druckerdaten auflisten, dürfen Sie keine Registrierungsfunktionen aufzurufen, die die Daten möglicherweise ändern.

## <a name="syntax"></a>Syntax


```C++
DWORD EnumPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPBYTE  pEnumValues,
  _In_  DWORD   cbEnumValues,
  _Out_ LPDWORD pcbEnumValues,
  _Out_ LPDWORD pnEnumValues
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker, für den die Funktion Konfigurationsdaten abruft. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

*pkeyname* \[ in\]
</dt> <dd>

Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die den Schlüssel angibt, der die aufzuzählenden Werte enthält. Verwenden Sie den umgekehrten Schrägstrich ( \\ ) als Trennzeichen, um einen Pfad mit einem oder mehreren unter Schlüsseln anzugeben. **Enumprinterdataex** listet alle Werte des Schlüssels auf, listet jedoch keine Werte der untergeordneten Schlüssel des angegebenen Schlüssels auf. Verwenden Sie die [**enumprinterkey**](enumprinterkey.md) -Funktion, um Unterschlüssel aufzuzählen.

Wenn *pkeyname* **null** oder eine leere Zeichenfolge ist, gibt **enumprinterdataex** einen \_ ungültigen \_ Parameter zurück.

</dd> <dt>

" *Pum Values* \[ " vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der ein Array von [**druckerenumerationswert \_ \_**](printer-enum-values.md) -Strukturen empfängt. Jede Struktur enthält den Wertnamen, den Typ, die Daten und die Größe eines Werts unter dem Schlüssel.

</dd> <dt>

*cbenumschlag-Werte* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Puffers, auf den *pcbenumschlag Values* zeigt. Wenn Sie " *cbenenumvalues* " auf NULL festlegen, gibt der Parameter " *pcbenumschlag Values* " die erforderliche Puffergröße zurück.

</dd> <dt>

*pcbenumschlag Values* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der abgerufenen Konfigurationsdaten in Bytes empfängt. Wenn die von *cbenumschlag Values* angegebene Puffergröße zu klein ist, gibt die Funktion Fehler \_ Weitere \_ Daten zurück, und *pcbenumschlag Values* gibt die erforderliche Puffergröße an.

</dd> <dt>

*pnenumvalues* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der in " *pumvalues*" zurückgegebenen Strukturen der [**druckerenumerationswerte \_ \_**](printer-enum-values.md) empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Systemfehler Code.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

**Enumprinterdataex** Ruft die Drucker Konfigurationsdaten ab, die von den Funktionen [**setprinterdataex**](setprinterdataex.md) und [**setprinterdata**](setprinterdata.md) festgelegt wurden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Enumprinterdataexw** (Unicode) und **enumprinterdataexa** (ANSI)<br/>                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Deleteprinterdataex**](deleteprinterdataex.md)
</dt> <dt>

[**Enumprinterkey**](enumprinterkey.md)
</dt> <dt>

[**Getprinterdataex**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**druckerenumerationswerte \_ \_**](printer-enum-values.md)
</dt> <dt>

[**Setprinterdata**](setprinterdata.md)
</dt> <dt>

[**Setprinterdataex**](setprinterdataex.md)
</dt> </dl>

 

 




