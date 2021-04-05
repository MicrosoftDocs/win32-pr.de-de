---
description: Die enumprinterdrivers-Funktion Listet die Druckertreiber auf, die auf einem angegebenen Drucker Server installiert sind.
ms.assetid: fa3d8cf4-70bc-4362-833e-e4217ed5d43b
title: Enumprinterdrivers-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDrivers
- EnumPrinterDriversA
- EnumPrinterDriversW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: c5175daf0a59ac4231baa1a32772863a0017c45d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756396"
---
# <a name="enumprinterdrivers-function"></a>Enumprinterdrivers-Funktion

Die **enumprinterdrivers** -Funktion Listet die Druckertreiber auf, die auf einem angegebenen Drucker Server installiert sind.

## <a name="syntax"></a>Syntax


```C++
BOOL EnumPrinterDrivers(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Servers angibt, auf dem die Druckertreiber aufgelistet werden.

Wenn *PName* den Wert **null** hat, listet die Funktion die lokalen Druckertreiber auf.

</dd> <dt>

nach-oben  \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Umgebung angibt (z. b. Windows x86, Windows ia64, Windows x64 oder Windows NT R4000). Wenn dieser Parameter **null** ist, verwendet die Funktion die aktuelle Umgebung des Aufrufers/Clients (nicht des Ziels/Servers).

Wenn in *der Zeichen* Folge "" die Zeichenfolge "All" angegeben ist, listet **enumprinterdrivers** Druckertreiber für alle auf dem angegebenen Server installierten Plattformen auf.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Der Typ der Informationsstruktur, der im *pdriverinfo* -Puffer zurückgegeben wird. Dies kann einer der folgenden sein:



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

Ein Zeiger auf einen Puffer, der ein Array von Treiber \_ Informations \_ \* Strukturen empfängt, wie von *Level* angegeben. Jede Struktur enthält Daten, die einen verfügbaren Druckertreiber beschreiben. Der Puffer muss groß genug sein, um das Array von Strukturen und Zeichen folgen oder andere Daten zu erhalten, auf die die Strukturmember zeigen.

Um die erforderliche Puffergröße zu ermitteln, muss **enumprinterdrivers** aufgerufen werden, wobei *cbbuf* auf NULL festgelegt ist. **Enumprinterdrivers** schlägt fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen fehlerhaften \_ Puffer zurück \_ , und der *pcbrequired* -Parameter gibt die Größe (in Bytes) des Puffers zurück, der für das Array von Strukturen und deren Daten erforderlich ist.

</dd> <dt>

*cbbuf* \[ in\]
</dt> <dd>

Die Größe (in Bytes) des Puffers, auf den *pdriverinfo* zeigt.

</dd> <dt>

*pcbbenötigte* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl von Bytes empfängt, die in den *pdriverinfo* -Puffer kopiert werden, wenn die Funktion erfolgreich ausgeführt wird. Wenn der Puffer zu klein ist, schlägt die Funktion fehl, und die Variable erhält die erforderliche Anzahl von Bytes.

</dd> <dt>

*pkreturned* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der im *pdriverinfo* -Puffer zurückgegebenen Strukturen empfängt. Dies ist die Anzahl der Druckertreiber, die auf dem angegebenen Drucker Server installiert sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

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
| Unicode- und ANSI-Name<br/>   | **Enumprinterdriversw** (Unicode) und **enumprinterdriversa** (ANSI)<br/>                           |



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

[**Getprinterdriver**](getprinterdriver.md)
</dt> </dl>

 

