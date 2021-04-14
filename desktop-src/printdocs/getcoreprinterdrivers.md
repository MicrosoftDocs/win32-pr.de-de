---
description: Ruft die GUID, die Version und das Datum der angegebenen Haupt Druckertreiber und den Pfad zu ihren Paketen ab.
ms.assetid: 98acad48-cd42-4d2b-be58-81c1366f6912
title: Getcoreprinterdrivers-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCorePrinterDrivers
- GetCorePrinterDriversA
- GetCorePrinterDriversW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 5bdebc3f4b716a21c56c9ec756ff56c02765d1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345288"
---
# <a name="getcoreprinterdrivers-function"></a>Getcoreprinterdrivers-Funktion

Ruft die GUID, die Version und das Datum der angegebenen Haupt Druckertreiber und den Pfad zu ihren Paketen ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCorePrinterDrivers(
  _In_  LPCTSTR              pszServer,
  _In_  LPCTSTR              pszEnvironment,
  _In_  LPCTSTR              pszzCoreDriverDependencies,
  _In_  DWORD                cCorePrinterDrivers,
  _Out_ PCORE_PRINTER_DRIVER pCorePrinterDrivers
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszserver* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die den Namen des Drucker Servers angibt. Verwenden Sie für den lokalen Computer **null** .

</dd> <dt>

*pszenvironment* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Konstante, auf NULL abschließende Zeichenfolge, die die Prozessorarchitektur angibt (z. b. Windows NT x86). Dieser Wert kann **null** sein.

</dd> <dt>

*pszzcoredriverdependen* \[ in\]
</dt> <dd>

Ein Zeiger auf eine mit NULL endenden Multizeichenfolge, die die GUIDs der Haupt Druckertreiber angibt.

</dd> <dt>

*ccoreprinterdrivers* \[ in\]
</dt> <dd>

Die Anzahl der Zeichen folgen in *pszzcoredriverdependen.*

</dd> <dt>

*pcoreprinterdrivers* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Array aus mindestens einer [**Kern \_ Drucker \_ Treiber**](core-printer-driver.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert S \_ OK; andernfalls enthält das **HRESULT** einen Fehlercode.

Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).

## <a name="remarks"></a>Bemerkungen

Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode- und ANSI-Name<br/>   | **Getcoreprinterdriversw** (Unicode) und **getcoreprinterdriversa** (ANSI)<br/>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> </dl>

 

