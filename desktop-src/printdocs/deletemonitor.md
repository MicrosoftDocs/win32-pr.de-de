---
description: Die deletemonitor-Funktion entfernt einen von der addmonitor-Funktion hinzugefügten Port Monitor.
ms.assetid: 32548d4f-830a-471d-8a72-c0f62f43ffa2
title: Deletemonitor-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteMonitor
- DeleteMonitorA
- DeleteMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0f11504be516f79610200d4f7da9d571ae1cab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347558"
---
# <a name="deletemonitor-function"></a>Deletemonitor-Funktion

Die **deletemonitor** -Funktion entfernt einen von der [**addmonitor**](addmonitor.md) -Funktion hinzugefügten Port Monitor.

## <a name="syntax"></a>Syntax


```C++
BOOL DeleteMonitor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, von dem der Monitor entfernt werden soll. Wenn dieser Parameter **null** ist, wird der Port Monitor lokal entfernt.

</dd> <dt>

nach-oben  \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die die Umgebung angibt, aus der der Monitor entfernt werden soll (z. b. Windows x86, Windows ia64 oder Windows x64). Wenn dieser Parameter **null** ist, wird der Monitor aus der aktuellen Umgebung der aufrufenden Anwendung und des Client Computers (nicht der Zielanwendung und des Druck Servers) entfernt.

</dd> <dt>

*pmonitorname* \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des zu entfernenden Monitors angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Der [Aufrufer muss über SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants)verfügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Deletemonitorw** (Unicode) und **deletemonitora** (ANSI)<br/>                                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addmonitor**](addmonitor.md)
</dt> </dl>

 

