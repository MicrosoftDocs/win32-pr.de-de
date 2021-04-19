---
description: Die GetPrinter-Funktion Ruft Informationen zu einem angegebenen Drucker ab.
ms.assetid: f162edbb-83ee-40c3-8710-9c867301d652
title: GetPrinter-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinter
- GetPrinterA
- GetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: e99b3574762b84b830845da8149b0406664b6da7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350117"
---
# <a name="getprinter-function"></a>GetPrinter-Funktion

Die **GetPrinter** -Funktion Ruft Informationen zu einem angegebenen Drucker ab.

## <a name="syntax"></a>Syntax


```C++
BOOL GetPrinter(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinter,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker, für den die Funktion Informationen abruft. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Die Ebene oder der Typ der Struktur, die die Funktion in dem Puffer speichert, auf den *pprinter* zeigt.

Dieser Wert kann 1, 2, 3, 4, 5, 6, 7, 8 oder 9 sein.

</dd> <dt>

*pprinter* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine-Struktur mit Informationen über den angegebenen Drucker empfängt. Der Puffer muss groß genug sein, um die Struktur und alle Zeichen folgen oder andere Daten zu empfangen, auf die die Strukturmember zeigen. Wenn der Puffer zu klein ist, gibt der Parameter *pcbrequired* die erforderliche Puffergröße zurück.

Der Typ der Struktur wird durch den Wert der *Ebene* bestimmt.



| Ebene                                                                                                | Struktur                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Eine Struktur von [**Drucker Informationen \_ \_ 1**](printer-info-1.md) , die allgemeine Drucker Informationen enthält.<br/>                                                                                                        |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Eine " [**Printer \_ Info \_ 2**](printer-info-2.md) "-Struktur, die ausführliche Informationen über den Drucker enthält.<br/>                                                                                             |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Eine [**Drucker \_ Info \_ 3**](printer-info-3.md) -Struktur, die die Sicherheitsinformationen des Druckers enthält.<br/>                                                                                                 |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Eine [**Drucker \_ Info \_ 4**](printer-info-4.md) -Struktur, die die minimalen Drucker Informationen enthält, einschließlich des Drucker namens, des Server namens und der Angabe, ob der Drucker Remote oder lokal ist.<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | Eine [**Drucker \_ Info \_ 5**](printer-info-5.md) -Struktur, die Drucker Informationen enthält, wie z. b. Drucker Attribute und Timeout Einstellungen.<br/>                                                               |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Eine [**Drucker \_ Info \_ 6**](printer-info-6.md) -Struktur, die den Statuswert eines Druckers angibt.<br/>                                                                                                      |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Eine [**Drucker \_ Info \_ 7**](printer-info-7.md) -Struktur, die angibt, ob der Drucker im Verzeichnisdienst veröffentlicht wird.<br/>                                                                      |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | Eine [**Drucker \_ Info \_ 8**](printer-info-8.md) -Struktur, die die globalen Standarddrucker Einstellungen angibt.<br/>                                                                                                |
| <span id="9"></span><dl> <dt>**9**</dt> </dl> | Eine [**Drucker \_ Info \_ 9**](printer-info-9.md) -Struktur, die die Standarddrucker Einstellungen pro Benutzer angibt.<br/>                                                                                              |



 

</dd> <dt>

*cbbuf* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Puffers, auf den *pprinter* zeigt.

</dd> <dt>

*pcbbenötigte* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die von der Funktion auf die Größe (in Bytes) der Drucker Informationen festgelegt wird. Wenn *cbbuf* kleiner ist als dieser Wert, schlägt **GetPrinter** fehl, und der Wert stellt die erforderliche Puffergröße dar. Wenn *cbbuf* größer oder gleich diesem Wert ist, ist **GetPrinter** erfolgreich, und der Wert stellt die Anzahl von Bytes dar, die im Puffer gespeichert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Der **pdevmode** -Member in den Strukturen [**Printer \_ Info \_ 2**](printer-info-2.md), [**Printer \_ Info \_ 8**](printer-info-8.md)und [**Printer \_ Info \_ 9**](printer-info-9.md) kann **null** sein. Wenn dies der Fall ist, kann der Drucker erst wieder verwendet werden, wenn der Treiber erfolgreich erneut installiert wurde.

Für die [**Drucker \_ Info \_ 2**](printer-info-2.md) -und [**Printer \_ Info \_ 3**](printer-info-3.md) -Strukturen, die einen Zeiger auf eine Sicherheits Beschreibung enthalten, ruft die Funktion nur die Komponenten der Sicherheits Beschreibung ab, für die der Aufrufer über Leseberechtigung verfügt. Zum Abrufen bestimmter sicherheitsbeschreibungkomponenten müssen Sie die erforderlichen Zugriffsrechte angeben, wenn Sie die [**OpenPrinter**](openprinter.md) -Funktion aufrufen, um ein Handle für den Drucker abzurufen. In der folgenden Tabelle sind die zum Lesen der verschiedenen sicherheitsbeschreibungkomponenten erforderlichen Zugriffsrechte aufgeführt.



| Zugriffsrecht                        | Sicherheitsbeschreibungerkomponente                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Lese \_ Steuerelement<br/>            | Besitzer<br/> Primäre Gruppe<br/> Freigegebene Zugriffs Steuerungs Liste (DACL)<br/> |
| Zugreifen auf die \_ System \_ Sicherheit<br/> | System Zugriffs Steuerungs Liste (SACL)<br/>                                                  |



 

Wenn Sie Ebene 7 angeben, gibt das **dwAction** -Mitglied von [**Printer \_ Info \_ 7**](printer-info-7.md) einen der folgenden Werte zurück, um anzugeben, ob der Drucker im Verzeichnisdienst veröffentlicht wird.



| dwAction-Wert     | Bedeutung                                                                                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dsprint- \_ Veröffentlichung   | Der Drucker wird veröffentlicht. Das **pszobjectguid** -Element enthält die GUID des Verzeichnisdienste-druckwarteschlangenobjekts, das dem Drucker zugeordnet ist.                                                                                                       |
| dsprint- \_ Veröffentlichung aufheben | Der Drucker ist nicht veröffentlicht.                                                                                                                                                                                                                            |
| dsprint \_ Ausstehend   | Gibt an, dass das System versucht, einen Veröffentlichungs-oder unveröffentlichungsvorgang abzuschließen. Wenn ein [**SetPrinter**](setprinter.md) -Rückruf einen Drucker nicht veröffentlichen oder nicht veröffentlichen kann, werden im Hintergrund weitere Versuche unternommen, den Vorgang abzuschließen. |



 

Ab Windows Vista werden die von **GetPrinter** zurückgegebenen Druckerdaten aus einem lokalen Cache abgerufen, wenn sich *hprinter* auf einen Drucker bezieht, der von einem Druckserver gehostet wird, und mindestens eine offene Verbindung zum Druckserver vorhanden ist. In allen anderen Konfigurationen werden die Druckerdaten vom Druckserver abgefragt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Getprinterw** (Unicode) und **getprintera** (ANSI)<br/>                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Abbruch Drucker**](abortprinter.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**Closeprinter**](closeprinter.md)
</dt> <dt>

[**Deleteprinter**](deleteprinter.md)
</dt> <dt>

[**Enumdrucker**](enumprinters.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 1**](printer-info-1.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 2**](printer-info-2.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 3**](printer-info-3.md)
</dt> <dt>

[**Drucker \_ Info \_ 4**](printer-info-4.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 5**](printer-info-5.md)
</dt> <dt>

[**Drucker \_ Info \_ 7**](printer-info-7.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 8**](printer-info-8.md)
</dt> <dt>

[**Drucker \_ Informationen \_ 9**](printer-info-9.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

 




