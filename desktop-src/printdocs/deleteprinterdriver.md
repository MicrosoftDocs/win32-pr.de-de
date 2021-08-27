---
description: Die DeletePrinterDriver-Funktion entfernt den angegebenen Druckertreibernamen aus der Liste der Namen der unterstützten Treiber auf einem Server.
ms.assetid: b159bd8b-3416-44a5-91bf-c0447ed6b465
title: DeletePrinterDriver-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriver
- DeletePrinterDriverA
- DeletePrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d878bb848eebed7eaccd904d4cdfd035d5056ee32eaa67eac5064dd5cf4e1e51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060030"
---
# <a name="deleteprinterdriver-function"></a>DeletePrinterDriver-Funktion

Die **DeletePrinterDriver-Funktion** entfernt den angegebenen Druckertreibernamen aus der Liste der Namen der unterstützten Treiber auf einem Server.

Verwenden Sie die [**DeletePrinterDriverEx-Funktion,**](deleteprinterdriverex.md) um die dateien, die dem Treiber zugeordnet sind, zusätzlich zum Entfernen des angegebenen Druckertreibernamens aus der Liste der Namen der unterstützten Treiber für einen Server zu löschen.

**DeletePrinterDriver** löscht einen Treiber nur, wenn keine Version des Treibers für die angegebene Umgebung verwendet wird. [**DeletePrinterDriverEx**](deleteprinterdriverex.md) kann bestimmte Versionen des Treibers löschen.

## <a name="syntax"></a>Syntax


```C++
BOOL DeletePrinterDriver(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, von dem der Treiber gelöscht werden soll. Wenn dieser Parameter **NULL** ist, wird der Name des Druckertreibers lokal entfernt.

</dd> <dt>

*pEnvironment* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Umgebung angibt, aus der der Treiber gelöscht werden soll (z. B. Windows x86, Windows IA64 oder Windows x64). Wenn dieser Parameter **NULL** ist, wird der Treibername aus der aktuellen Umgebung der aufrufenden Anwendung und des Clientcomputers (nicht der Zielanwendung und des Druckerservers) gelöscht.

</dd> <dt>

*pDriverName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des zu löschenden Treibers angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion und wird möglicherweise nicht sofort zurückgegeben. Wie schnell diese Funktion zurückgegeben wird, hängt von Laufzeitfaktoren wie Netzwerkstatus, Druckerserverkonfiguration und Implementierungsfaktoren für Druckertreiber ab, die beim Schreiben einer Anwendung schwer vorherzusagen sind. Das Aufrufen dieser Funktion über einen Thread, der die Interaktion mit der Benutzeroberfläche verwaltet, kann dazu bringen, dass die Anwendung scheinbar nicht reagiert.

 

Der Aufrufer muss über [seLoadDriverPrivilege verfügen.](/windows/desktop/SecAuthZ/authorization-constants)

Die **DeletePrinterDriver-Funktion** löscht die zugeordneten Dateien nicht, sondern entfernt lediglich den Treibernamen aus der Liste, die von der [**EnumPrinterDrivers-Funktion**](enumprinterdrivers.md) zurückgegeben wird.

Vor dem Aufrufen von **DeletePrinterDriver** müssen Sie alle Druckerobjekte löschen, die den Druckertreiber verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **DeletePrinterDriverW** (Unicode) und **DeletePrinterDriverA** (ANSI)<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDriverEx**](deleteprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> </dl>

 

