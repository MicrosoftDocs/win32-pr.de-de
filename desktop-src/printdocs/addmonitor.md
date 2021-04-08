---
description: Mit der addmonitor-Funktion wird ein lokaler Port Monitor installiert, und die Konfigurations-, Daten-und Überwachungs Dateien werden verknüpft.
ms.assetid: 6a556422-5360-42d2-b177-dba0498c06d8
title: Addmonitor-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMonitor
- AddMonitorA
- AddMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 40b45c4dc05580837a2cf4a001cf8d18e646e5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050494"
---
# <a name="addmonitor-function"></a>Addmonitor-Funktion

Mit der **addmonitor** -Funktion wird ein lokaler Port Monitor installiert, und die Konfigurations-, Daten-und Überwachungs Dateien werden verknüpft.

## <a name="syntax"></a>Syntax


```C++
BOOL AddMonitor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pMonitors
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PName* \[ in\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Servers angibt, auf dem der Monitor installiert werden soll. Für Systeme, die nur die lokale Installation von Monitoren unterstützen, sollte diese Zeichenfolge **null** sein.

</dd> <dt>

*Ebene* \[ in\]
</dt> <dd>

Die Version der-Struktur, auf die *pmonitors* zeigt. Dieser Wert muss 2 sein.

</dd> <dt>

*pmonitors* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**Monitor \_ Info \_ 2**](monitor-info-2.md) -Struktur. Wenn das Element " **pvironment** " der *pmonitors* -Struktur **null** ist, wird die aktuelle Umgebung des Aufrufers (Client) nicht des Ziels (Server) verwendet.

Beachten Sie, dass der-Befehl fehlschlägt, wenn die Umgebung nicht der Umgebung des Servers entspricht, d. h., Sie können nur einen Monitor hinzufügen, der für die Architektur des Servers geschrieben wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Der [Aufrufer muss über die SeLoadDriverPrivilege-Berechtigung](/windows/desktop/SecAuthZ/authorization-constants)verfügen.

Bevor eine Anwendung die **addmonitor** -Funktion aufruft, müssen alle Dateien, die für den Monitor erforderlich sind, in das Verzeichnis System32 kopiert werden.

Um die derzeit installierten Port Monitore zu ermitteln, müssen Sie die [**enummonitors**](enummonitors.md) -Funktion aufzurufen.

Um einen von **addmonitor** hinzugefügten Monitor zu entfernen, müssen Sie die [**deletemonitor**](deletemonitor.md) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Addmonitorw** (Unicode) und **addmonitora** (ANSI)<br/>                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Deletemonitor**](deletemonitor.md)
</dt> <dt>

[**Enumüberwachungen**](enummonitors.md)
</dt> <dt>

[**Überwachen von \_ Informationen \_ 2**](monitor-info-2.md)
</dt> </dl>

 

