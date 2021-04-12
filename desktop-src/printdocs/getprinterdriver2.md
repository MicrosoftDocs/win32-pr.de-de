---
description: Die GetPrinterDriver2-Funktion ruft Treiber Daten für den angegebenen Drucker ab. Wenn der Treiber nicht auf dem lokalen Computer installiert ist, installiert GetPrinterDriver2 ihn und zeigt eine beliebige Benutzeroberfläche für das angegebene Fenster an.
ms.assetid: 0d482d28-7668-4734-ba71-5b355c18ddec
title: GetPrinterDriver2-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver2
- GetPrinterDriver2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b0a9d2bfe7827a2c0e3db9fff9e8249b73bf5102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218226"
---
# <a name="getprinterdriver2-function"></a>GetPrinterDriver2-Funktion

Die **GetPrinterDriver2** -Funktion ruft Treiber Daten für den angegebenen Drucker ab. Wenn der Treiber nicht auf dem lokalen Computer installiert ist, installiert **GetPrinterDriver2** ihn und zeigt eine beliebige Benutzeroberfläche für das angegebene Fenster an.

## <a name="syntax"></a>Syntax


```C++
BOOL GetPrinterDriver2(
  _In_opt_ HWND    hWnd,
  _In_     HANDLE  hPrinter,
  _In_opt_ LPTSTR  pEnvironment,
  _In_     DWORD   Level,
  _Out_    LPBYTE  pDriverInfo,
  _In_     DWORD   cbBuf,
  _Out_    LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* \[ in, optional\]
</dt> <dd>

Ein Handle des Fensters, das als übergeordnetes Fenster einer beliebigen Benutzeroberfläche verwendet wird, z. b. ein Dialogfeld, das der Treiber während der Installation anzeigt. Wenn der Wert dieses Parameters **null** ist, wird die Benutzeroberfläche des Treibers während der Installation weiterhin für den Benutzer angezeigt, aber es ist kein übergeordnetes Fenster vorhanden.

</dd> <dt>

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker, für den die Treiber Daten abgerufen werden sollen. Verwenden Sie die Funktion [**OpenPrinter**](openprinter.md) oder [**addprinter**](addprinter.md) zum Abrufen eines Drucker Handles.

</dd> <dt>

nach-oben  \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Umgebung angibt (z. b. Windows x86, Windows ia64 oder Windows x64). Wenn dieser Parameter **null** ist, wird die aktuelle Umgebung der aufrufenden Anwendung und des Client Computers (nicht der Zielanwendung und des Druck Servers) verwendet.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Die Druckertreiber Struktur, die im *pdriverinfo* -Puffer zurückgegeben wurde. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                | Bedeutung                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | [**Treiber \_ Informationen \_ 1**](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**Treiber \_ Informationen \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**Treiber \_ Info \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**Treiber \_ Info \_ 4**](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | [**Treiber \_ Informationen \_ 5**](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**Treiber \_ Info \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**Treiber \_ Informationen \_ 8**](driver-info-8.md)<br/> |



 

</dd> <dt>

*pdriverinfo* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine-Struktur mit Informationen über den Treiber empfängt, wie von *Level* angegeben. Der Puffer muss groß genug sein, um die Zeichen folgen zu speichern, auf die von den Strukturmembern verwiesen wird.

Um die erforderliche Puffergröße zu ermitteln, müssen Sie **GetPrinterDriver2** mit *cbbuf* auf 0 (null) festlegen. **GetPrinterDriver2** schlägt fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen **fehlerhaften \_ \_ Puffer** zurück, und der *pcbrequired* -Parameter gibt die Größe (in Bytes) des Puffers zurück, der für das Array von Strukturen und deren Daten erforderlich ist.

</dd> <dt>

*cbbuf* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Arrays, bei dem *pdriverinfo* zeigt.

</dd> <dt>

*pcbbenötigte* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Wert, der die Anzahl der kopierten Bytes empfängt, wenn die Funktion erfolgreich ausgeführt wird, oder die Anzahl der Bytes, die erforderlich sind, wenn *cbbuf* zu klein ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null. Um den Rückgabestatus abzurufen, nennen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Bemerkungen

Die [**Strukturen \_ Treiber \_ Info 2**](driver-info-2.md), [**Driver \_ Info \_ 3**](driver-info-3.md), [**Driver \_ Info \_ 4**](driver-info-4.md), [**Driver \_ Info \_ 5**](driver-info-5.md), [**Driver \_ Info \_ 6**](driver-info-6.md)und [**Driver \_ Info \_ 8**](driver-info-8.md) enthalten den Dateinamen oder den vollständigen Pfad und den Dateinamen des Druckertreibers im **pdriverpath** -Member. Eine Anwendung kann den Pfad und den Dateinamen verwenden, um einen Druckertreiber zu laden, indem die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion aufgerufen und der Pfad und der Dateiname als einzelnes Argument bereitgestellt werden.

Die ANSI-Version dieser Funktion, **GetPrinterDriver2A** wird nicht unterstützt und gibt einen Fehler zurück, der **\_ nicht \_ unterstützt** wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **GetPrinterDriver2W** (Unicode)<br/>                                                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addprinterdriver**](addprinterdriver.md)
</dt> <dt>

[**Treiber \_ Informationen \_ 1**](driver-info-1.md)
</dt> <dt>

[**Treiber \_ Informationen \_ 2**](driver-info-2.md)
</dt> <dt>

[**Treiber \_ Info \_ 3**](driver-info-3.md)
</dt> <dt>

[**Treiber \_ Info \_ 4**](driver-info-4.md)
</dt> <dt>

[**Treiber \_ Informationen \_ 5**](driver-info-5.md)
</dt> <dt>

[**Treiber \_ Info \_ 6**](driver-info-6.md)
</dt> <dt>

[**Enumprinterdrivers**](enumprinterdrivers.md)
</dt> <dt>

[**Getprinterdriver**](getprinterdriver.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

