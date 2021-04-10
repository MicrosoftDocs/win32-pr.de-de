---
description: Die enumprinterdata-Funktion Listet Konfigurationsdaten für einen angegebenen Drucker auf.
ms.assetid: 0a4c8436-46fe-4e21-8d55-c5031a3d1b38
title: Enumprinterdata-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterData
- EnumPrinterDataA
- EnumPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d7c175b0c90853a592e0ff979095d41432c16b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215855"
---
# <a name="enumprinterdata-function"></a>Enumprinterdata-Funktion

Die **enumprinterdata** -Funktion Listet Konfigurationsdaten für einen angegebenen Drucker auf.

Um die Konfigurationsdaten in einem einzelnen-Befehl abzurufen, verwenden Sie die [**enumprinterdataex**](enumprinterdataex.md) -Funktion.

## <a name="syntax"></a>Syntax


```C++
DWORD EnumPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   dwIndex,
  _Out_ LPTSTR  pValueName,
  _In_  DWORD   cbValueName,
  _Out_ LPDWORD pcbValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbData,
  _Out_ LPDWORD pcbData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker, dessen Konfigurationsdaten abgerufen werden sollen. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

*dwIndex* \[ in\]
</dt> <dd>

Ein Indexwert, der den abzurufenden Konfigurationsdaten Wert angibt.

Legen Sie diesen Parameter auf 0 (null) für den ersten **enumprinterdata** -Aufrufwert für ein bestimmtes Drucker Handle fest. Erhöhen Sie den Parameter dann um einen für nachfolgende Aufrufe, die denselben Drucker betreffen, bis die Funktion Fehler \_ ohne \_ Weitere Elemente zurückgibt \_ . Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".

Wenn Sie das in den Beschreibungen der Parameter *cbvaluename* und *cbData* erwähnte Verfahren verwenden, um geeignete Puffergrößen Werte zu erhalten, wobei beide Parameter beim ersten **Aufzählen von enumprinterdata** für ein angegebenes Drucker Handle auf 0 (null) festgelegt werden, ist der Wert von *dwIndex* für diesen Befehl nicht von Bedeutung. Legen Sie *dwIndex* beim nächsten Aufzählung von **enumprinterdata** auf NULL fest, um den eigentlichen enumerationsprozess zu starten.

Konfigurationsdaten Werte sind nicht geordnet. Neue Werte haben einen beliebigen Index. Dies bedeutet, dass die **enumprinterdata** -Funktion Werte in beliebiger Reihenfolge zurückgeben kann.

</dd> <dt>

*pvaluename* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Namen des Konfigurationsdaten Werts einschließlich eines abschließenden NULL-Zeichens empfängt.

</dd> <dt>

*cbvaluename* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Puffers, auf den *pvaluename* zeigt.

Wenn Sie möchten, dass das Betriebssystem eine angemessene Puffergröße bereitstellt, legen Sie für den ersten **enumprinterdata** -aufzurufenden Parameter sowohl diesen Parameter als auch den *cbData* -Parameter auf 0 (null) fest. Wenn die Funktion zurückgegeben wird, enthält die Variable, auf die von *pcbvaluename* verwiesen wird, eine Puffergröße, die groß genug ist, um alle Namen von Konfigurationsdaten für den Drucker erfolgreich aufzulisten.

</dd> <dt>

*pcbvaluename* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der Bytes empfängt, die im Puffer gespeichert werden, auf die von *pvaluename* verwiesen wird.

</dd> <dt>

*pType* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Code empfängt, der den Typ der im angegebenen Wert gespeicherten Daten angibt. Eine Liste der möglichen Typcodes finden Sie unter [Registrierungs Werttypen](/windows/desktop/SysInfo/registry-value-types). Der *pType* -Parameter kann **null** sein, wenn der Typcode nicht erforderlich ist.

</dd> <dt>

*pData* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Konfigurationsdaten Wert empfängt.

Dieser Parameter kann **null** sein, wenn der Wert für die Konfigurationsdaten nicht erforderlich ist.

</dd> <dt>

*cbData* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Puffers, auf den *pData* zeigt.

Wenn Sie möchten, dass das Betriebssystem eine angemessene Puffergröße bereitstellt, legen Sie für den ersten **enumprinterdata** -aufzurufenden Parameter sowohl diesen Parameter als auch den *cbvaluename* -Parameter auf 0 (null) fest. Wenn die Funktion zurückgegeben wird, enthält die Variable, auf die von *pcbData* verwiesen wird, eine Puffergröße, die groß genug ist, um alle Namen von Konfigurationsdaten für den Drucker erfolgreich aufzulisten.

</dd> <dt>

*pcbData* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der Bytes empfängt, die im Puffer gespeichert werden, auf die *pData* verweist.

Dieser Parameter kann **null** sein, wenn *pData* **null** ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Systemfehler Code.

Die Funktion gibt \_ einen Fehler ohne \_ Weitere Elemente zurück \_ , wenn keine weiteren Konfigurationsdaten Werte für ein angegebenes Drucker handle vorhanden sind.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

**Enumprinterdata** Ruft das von der [**setprinterdata**](setprinterdata.md) -Funktion festgelegte Drucker Konfigurations DataSet ab. Die Konfigurationsdaten eines Druckers bestehen aus einem Satz von benannten und typisierten Werten. Die **enumprinterdata** -Funktion Ruft bei jedem Aufruf einen dieser Werte und ihren Namen sowie einen Typcode ab. Rufen Sie die **enumprinterdata** -Funktion mehrmals nacheinander auf, um alle Konfigurationsdaten Werte eines Druckers zu erhalten.

Die Drucker Konfigurationsdaten werden in der Registrierung gespeichert. Beim Auflisten von Drucker Konfigurationsdaten sollten Sie keine Registrierungsfunktionen aufrufen, die diese Daten möglicherweise ändern.

Wenn Sie möchten, dass das Betriebssystem eine angemessene Puffergröße bereitstellt, müssen Sie zuerst **enumprinterdata** mit den Parametern *cbvaluename* und *cbData* auf NULL festlegen, wie zuvor im Abschnitt Parameters angegeben. Der Wert von *dwIndex* ist für diesen-Befehl nicht von Bedeutung. Wenn die Funktion zurückgegeben \* wird, enthalten *pcbvaluename* und \* *pcbData* Puffergrößen, die groß genug sind, um alle Namen und Werte der Konfigurationsdaten des Drucker aufzulisten. Beim nächsten-Befehl werden Werte Name und Datenpuffer zugewiesen, *cbvaluename* und *cbData* auf die Größen in Bytes der zugeordneten Puffer festgelegt, und *dwIndex* wird auf 0 (null) festgelegt. Setzen Sie anschließend die **enumprinterdata** -Funktion fort, und erhöhen Sie *dwIndex* jedes Mal um 1, bis die Funktion Fehler \_ ohne \_ Weitere \_ Elemente zurückgibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Enumprinterdataw** (Unicode) und **enumprinterdataa** (ANSI)<br/>                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Deleteprinterdata**](deleteprinterdata.md)
</dt> <dt>

[**Enumprinterdataex**](enumprinterdataex.md)
</dt> <dt>

[**Getprinterdata**](getprinterdata.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**Setprinterdata**](setprinterdata.md)
</dt> </dl>

 

