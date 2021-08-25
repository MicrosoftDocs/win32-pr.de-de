---
description: Die GetPrinterDriver2-Funktion ruft Treiberdaten für den angegebenen Drucker ab. Wenn der Treiber nicht auf dem lokalen Computer installiert ist, installiert GetPrinterDriver2 ihn und zeigt eine beliebige Benutzeroberfläche im angegebenen Fenster an.
ms.assetid: 0d482d28-7668-4734-ba71-5b355c18ddec
title: GetPrinterDriver2-Funktion (Winspool.h)
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
ms.openlocfilehash: e5217ee8445ce8ccae5f22d7c85a4a88dd33f31a1a714aad4899b539ce4edced
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846010"
---
# <a name="getprinterdriver2-function"></a>GetPrinterDriver2-Funktion

Die **GetPrinterDriver2-Funktion** ruft Treiberdaten für den angegebenen Drucker ab. Wenn der Treiber nicht auf dem lokalen Computer installiert ist, installiert **GetPrinterDriver2** ihn und zeigt eine beliebige Benutzeroberfläche im angegebenen Fenster an.

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

*hWnd* \[ in, optional\]
</dt> <dd>

Ein Handle des Fensters, das als übergeordnetes Fenster einer beliebigen Benutzeroberfläche verwendet wird, z. B. eines Dialogfelds, das der Treiber während der Installation anzeigt. Wenn der Wert dieses Parameters **NULL ist,** wird dem Benutzer während der Installation weiterhin die Benutzeroberfläche des Treibers angezeigt, es wird jedoch kein übergeordnetes Fenster angezeigt.

</dd> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für den Drucker, für den die Treiberdaten abgerufen werden sollen. Verwenden Sie [**die OpenPrinter-**](openprinter.md) [**oder AddPrinter-Funktion,**](addprinter.md) um einen Druckerhandpunkt abzurufen.

</dd> <dt>

*pUmgebung* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Zeichenfolge, die die Umgebung angibt (z. B. Windows x86, Windows IA64 oder Windows x64). Wenn dieser Parameter **NULL ist,** wird die aktuelle Umgebung der aufrufenden Anwendung und des Clientcomputers (nicht der Zielanwendung und des Druckerservers) verwendet.

</dd> <dt>

*Ebene* \[ In\]
</dt> <dd>

Die im *pDriverInfo-Puffer zurückgegebene Druckertreiberstruktur.* Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                | Bedeutung                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | [**TREIBERINFORMATIONEN \_ \_ 1**](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**TREIBERINFORMATIONEN \_ \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**TREIBERINFORMATIONEN \_ \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**TREIBERINFORMATIONEN \_ \_ 4**](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | [**TREIBERINFORMATIONEN \_ \_ 5**](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**TREIBERINFORMATIONEN \_ \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**TREIBERINFORMATIONEN \_ \_ 8**](driver-info-8.md)<br/> |



 

</dd> <dt>

*pDriverInfo* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine -Struktur empfängt, die Informationen über den Treiber enthält, wie von *Level angegeben.* Der Puffer muss groß genug sein, um die Zeichenfolgen zu speichern, auf die die Strukturmitglieder zeigt.

Um die erforderliche Puffergröße zu bestimmen, rufen **Sie GetPrinterDriver2 mit** *cbBuf* auf 0 (null) auf. **GetPrinterDriver2** schlägt fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt **ERROR INSUFFICIENT \_ \_ BUFFER** zurück, und der *Parameter "arraysNeeded"* gibt die Größe des Puffers in Bytes zurück, der zum Speichern des Arrays von Strukturen und deren Daten erforderlich ist.

</dd> <dt>

*cbBuf* \[ In\]
</dt> <dd>

Die Größe des Arrays in Bytes, auf das *pDriverInfo* zeigt.

</dd> <dt>

*-Needed* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Wert, der die Anzahl der kopierten Bytes empfängt, wenn die Funktion erfolgreich ist, oder die Erforderliche Anzahl von Bytes, wenn *cbBuf* zu klein ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null. Rufen Sie GetLastError auf, um den [**Rückgabestatus zu erhalten.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Hinweise

Die [**Driver \_ INFO \_ 2-,**](driver-info-2.md) [**DRIVER INFO \_ \_ 3-,**](driver-info-3.md) [**DRIVER INFO \_ \_ 4-,**](driver-info-4.md) [**DRIVER INFO \_ \_ 5-,**](driver-info-5.md) [**DRIVER INFO \_ \_ 6-**](driver-info-6.md)und [**DRIVER INFO \_ \_ 8-Strukturen**](driver-info-8.md) enthalten den Dateinamen oder den vollständigen Pfad und Dateinamen des Druckertreibers im **pDriverPath-Mitglied.** Eine Anwendung kann den Pfad und den Dateinamen verwenden, um einen Druckertreiber zu laden, indem sie die [**LoadLibrary-Funktion**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) aufruft und den Pfad und den Dateinamen als einzelnes Argument anordnt.

Die ANSI-Version dieser Funktion **GetPrinterDriver2A** wird nicht unterstützt und gibt **ERROR NOT SUPPORTED \_ \_ zurück.**

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **GetPrinterDriver2W** (Unicode)<br/>                                                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**TREIBERINFORMATIONEN \_ \_ 1**](driver-info-1.md)
</dt> <dt>

[**TREIBERINFORMATIONEN \_ \_ 2**](driver-info-2.md)
</dt> <dt>

[**TREIBERINFORMATIONEN \_ \_ 3**](driver-info-3.md)
</dt> <dt>

[**TREIBERINFORMATIONEN \_ \_ 4**](driver-info-4.md)
</dt> <dt>

[**TREIBERINFORMATIONEN \_ \_ 5**](driver-info-5.md)
</dt> <dt>

[**TREIBERINFORMATIONEN \_ \_ 6**](driver-info-6.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

