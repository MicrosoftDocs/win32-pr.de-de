---
description: Die getprinterdriverdirectory-Funktion Ruft den Pfad des druckertreiberverzeichnisses ab.
ms.assetid: 69c9cc87-d7e3-496a-b631-b3ae30cdb3fd
title: Getprinterdriverdirectory-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverDirectory
- GetPrinterDriverDirectoryA
- GetPrinterDriverDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 7acc68f99f9791ba4231bcfea2b1788cfb37011c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362712"
---
# <a name="getprinterdriverdirectory-function"></a>Getprinterdriverdirectory-Funktion

Die **getprinterdriverdirectory** -Funktion Ruft den Pfad des druckertreiberverzeichnisses ab.

## <a name="syntax"></a>Syntax


```C++
BOOL GetPrinterDriverDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverDirectory,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Servers angibt, auf dem sich der Druckertreiber befindet. Wenn dieser Parameter **null** ist, wird der Pfad des lokalen Treiber Verzeichnisses abgerufen.

</dd> <dt>

nach-oben  \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die die Umgebung angibt (z. b. Windows x86, Windows ia64 oder Windows x64). Wenn dieser Parameter **null** ist, wird die aktuelle Umgebung der aufrufenden Anwendung und des Client Computers (nicht der Zielanwendung und des Druck Servers) verwendet.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Die Struktur Ebene. Dieser Wert muss 1 sein.

</dd> <dt>

*pdriverdirectory* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Pfad empfängt.

</dd> <dt>

*cbbuf* \[ in\]
</dt> <dd>

Die Größe des Puffers, auf den *pdriverdirectory* verweist.

</dd> <dt>

*pcbbenötigte* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen-Wert, der die Anzahl der Bytes angibt, die beim Erfolg der Funktion kopiert werden, oder die Anzahl der Bytes, die erforderlich sind, wenn *cbbuf* zu klein ist.

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
| Unicode- und ANSI-Name<br/>   | **Getprinterdriverdirectoren** (Unicode) und **getprinterdriverdirector ya** (ANSI)<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addprinterdriver**](addprinterdriver.md)
</dt> </dl>

 

 




