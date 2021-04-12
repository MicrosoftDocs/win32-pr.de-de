---
description: Die enumprinterkey-Funktion Listet die Unterschlüssel eines angegebenen Schlüssels für einen angegebenen Drucker auf.
ms.assetid: 721b1d23-a594-4439-b8f9-9b11be5fe874
title: Enumprinterkey-Funktion (winspool. h)
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
ms.openlocfilehash: d9af6a9ef26612385cee68eba9733c148cd36b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347498"
---
# <a name="enumprinterkey-function"></a>Enumprinterkey-Funktion

Die **enumprinterkey** -Funktion Listet die Unterschlüssel eines angegebenen Schlüssels für einen angegebenen Drucker auf.

Druckerdaten werden in der Registrierung gespeichert. Wenn Sie Druckerdaten auflisten, dürfen Sie keine Registrierungsfunktionen aufzurufen, die die Daten möglicherweise ändern.

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

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker, für den die-Funktion Unterschlüssel auflistet. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

*pkeyname* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Schlüssel mit den unter Schlüsseln angibt, die aufgelistet werden sollen. Verwenden Sie den umgekehrten Schrägstrich ' \\ ' als Trennzeichen, um einen Pfad mit einem oder mehreren unter Schlüsseln anzugeben. **Enumprinterkey** listet alle Unterschlüssel des Schlüssels auf, listet aber nicht die untergeordneten Schlüssel dieser Unterschlüssel auf.

Wenn " *pkeyname* " eine leere Zeichenfolge ("") ist, listet " **enumprinterkey** " den Schlüssel der obersten Ebene für den Drucker auf. Wenn *pkeyname* **null** ist, gibt **enumprinterkey** einen \_ ungültigen \_ Parameter zurück.

</dd> <dt>

*psubkey* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der ein Array von auf NULL endenden Unterschlüssel Namen empfängt. Das Array wird mit zwei NULL-Zeichen beendet.

</dd> <dt>

*cbsubkey* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Puffers, auf den *psubkey* zeigt. Wenn Sie *cbsubkey* auf NULL festlegen, gibt der *pcbsubkey* -Parameter die erforderliche Puffergröße zurück.

</dd> <dt>

*pcbsubkey* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl von Bytes empfängt, die im *psubkey* -Puffer abgerufen wurden. Wenn die von *cbsubkey* angegebene Puffergröße zu klein ist, gibt die Funktion Fehler \_ Weitere \_ Daten zurück, und *pcbsubkey* gibt die erforderliche Puffergröße an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Systemfehler Code. Wenn " *pkeyname* " nicht vorhanden ist, lautet der Rückgabewert "Fehler \_ Datei \_ nicht \_ gefunden".

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
| Unicode- und ANSI-Name<br/>   | **Enumprinterkeyw** (Unicode) und **enumprinterkeya** (ANSI)<br/>                                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Deleteprinterdataex**](deleteprinterdataex.md)
</dt> <dt>

[**Getprinterdataex**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Setprinterdataex**](setprinterdataex.md)
</dt> </dl>

 

 




