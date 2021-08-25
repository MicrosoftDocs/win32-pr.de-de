---
description: Die EnumPrinterData-Funktion listet Konfigurationsdaten für einen angegebenen Drucker auf.
ms.assetid: 0a4c8436-46fe-4e21-8d55-c5031a3d1b38
title: EnumPrinterData-Funktion (Winspool.h)
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
ms.openlocfilehash: a542b6a0432ccf7065d94eeb8ebb3acbd8e2ace22044f2cc8984a1f4b2404299
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846080"
---
# <a name="enumprinterdata-function"></a>EnumPrinterData-Funktion

Die **EnumPrinterData-Funktion** listet Konfigurationsdaten für einen angegebenen Drucker auf.

Um die Konfigurationsdaten in einem einzelnen Aufruf abzurufen, verwenden Sie die [**EnumPrinterDataEx-Funktion.**](enumprinterdataex.md)

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

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für den Drucker, dessen Konfigurationsdaten abgerufen werden sollen. Verwenden Sie die [**OpenPrinter-**](openprinter.md) oder [**AddPrinter-Funktion,**](addprinter.md) um ein Druckerhandle abzurufen.

</dd> <dt>

*dwIndex* \[ In\]
</dt> <dd>

Ein Indexwert, der den abzurufenden Konfigurationsdatenwert angibt.

Legen Sie diesen Parameter für den ersten Aufruf von **EnumPrinterData** für ein angegebenes Druckerhandle auf 0 fest. Erhöhen Sie dann den Parameter für nachfolgende Aufrufe, die den gleichen Drucker betreffen, um einen Parameter, bis die Funktion ERROR \_ NO MORE ITEMS zurückgibt. \_ \_ Weitere Informationen finden Sie im abschnitt "Hinweise".

Wenn Sie die in den Beschreibungen der *CbValueName-* und *cbData-Parameter* beschriebene Technik verwenden, um geeignete Puffergrößenwerte zu erhalten und beide Parameter bei einem ersten Aufruf von **EnumPrinterData** für ein angegebenes Druckerhandle auf null festzulegen, spielt der Wert von *dwIndex* für diesen Aufruf keine Rolle. Legen Sie *dwIndex* im nächsten Aufruf von **EnumPrinterData** auf null fest, um den tatsächlichen Enumerationsprozess zu starten.

Konfigurationsdatenwerte sind nicht sortiert. Neue Werte verfügen über einen beliebigen Index. Dies bedeutet, dass die **EnumPrinterData-Funktion** Werte in beliebiger Reihenfolge zurückgeben kann.

</dd> <dt>

*pValueName* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Namen des Konfigurationsdatenwerts empfängt, einschließlich eines abschließenden NULL-Zeichens.

</dd> <dt>

*cbValueName* \[ In\]
</dt> <dd>

Die Größe des Puffers in Bytes, auf den *pValueName* zeigt.

Wenn das Betriebssystem eine angemessene Puffergröße bereitstellen soll, legen Sie sowohl diesen Parameter als auch den *cbData-Parameter* für den ersten Aufruf von **EnumPrinterData** für ein angegebenes Druckerhandle auf null fest. Wenn die Funktion zurückgegeben wird, enthält die Variable, auf die von *"pwValueName"* verwiesen wird, eine Puffergröße, die groß genug ist, um alle Namen der Konfigurationsdatenwerte des Druckers erfolgreich aufzulisten.

</dd> <dt>

*pwValueName* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl von Bytes empfängt, die in dem Puffer gespeichert sind, auf den *pValueName* zeigt.

</dd> <dt>

*pType* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Code empfängt, der den Typ der im angegebenen Wert gespeicherten Daten angibt. Eine Liste der möglichen Typcodes finden Sie unter [Registrierungswerttypen.](/windows/desktop/SysInfo/registry-value-types) Der *pType-Parameter* kann **NULL** sein, wenn der Typcode nicht erforderlich ist.

</dd> <dt>

*pData* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Konfigurationsdatenwert empfängt.

Dieser Parameter kann **NULL** sein, wenn der Konfigurationsdatenwert nicht erforderlich ist.

</dd> <dt>

*cbData* \[ In\]
</dt> <dd>

Die Größe des Puffers in Bytes, auf den *pData* zeigt.

Wenn das Betriebssystem eine angemessene Puffergröße bereitstellen soll, legen Sie sowohl diesen Parameter als auch den *cbValueName-Parameter* für den ersten Aufruf von **EnumPrinterData** für ein angegebenes Druckerhandle auf 0 (null) fest. Wenn die Funktion zurückgegeben wird, enthält die Variable, auf die *von "data"* verwiesen wird, eine Puffergröße, die groß genug ist, um alle Namen der Konfigurationsdatenwerte des Druckers erfolgreich aufzulisten.

</dd> <dt>

*data* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl von Bytes empfängt, die in dem Puffer gespeichert sind, auf den *pData* zeigt.

Dieser Parameter kann **NULL** sein, wenn *pData* **NULL** ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Systemfehlercode.

Die Funktion gibt ERROR \_ NO \_ MORE ITEMS \_ zurück, wenn für ein angegebenes Druckerhandle keine Konfigurationsdatenwerte mehr abgerufen werden müssen.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

**EnumPrinterData** ruft das Druckerkonfigurationsdataset von der [**SetPrinterData-Funktion**](setprinterdata.md) ab. Die Konfigurationsdaten eines Druckers bestehen aus einem Satz benannter und typisierter Werte. Die **EnumPrinterData-Funktion** ruft bei jedem Aufruf einen dieser Werte sowie ihren Namen und einen Typcode ab. Rufen Sie die **EnumPrinterData-Funktion** mehrmals nacheinander auf, um alle Konfigurationsdatenwerte eines Druckers abzurufen.

Druckerkonfigurationsdaten werden in der Registrierung gespeichert. Beim Aufzählen von Druckerkonfigurationsdaten sollten Sie das Aufrufen von Registrierungsfunktionen vermeiden, die diese Daten möglicherweise ändern.

Wenn das Betriebssystem eine angemessene Puffergröße bereitstellen soll, rufen Sie zunächst **EnumPrinterData** auf, wobei die Parameter *cbValueName* und *cbData* auf 0 (null) festgelegt sind, wie weiter oben im Abschnitt Parameter beschrieben. Der Wert von *dwIndex* spielt für diesen Aufruf keine Rolle. Wenn die Funktion zurückgegeben \* wird, enthalten *"valueName"* und \* *"data"* Puffergrößen, die groß genug sind, um alle Namen und Werte der Konfigurationsdatenwerte des Druckers aufzulisten. Weisen Sie beim nächsten Aufruf Wertname und Datenpuffer zu, legen Sie *cbValueName* und *cbData* auf die Größen in Bytes der zugeordneten Puffer fest, und legen Sie *dwIndex* auf 0 (null) fest. Danach rufen Sie weiterhin die **EnumPrinterData-Funktion** auf und erhöhen *dwIndex* jedes Mal um eins, bis die Funktion ERROR NO MORE ITEMS zurückgibt. \_ \_ \_

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **EnumPrinterDataW** (Unicode) und **EnumPrinterDataA** (ANSI)<br/>                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterData**](deleteprinterdata.md)
</dt> <dt>

[**EnumPrinterDataEx**](enumprinterdataex.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> </dl>

 

