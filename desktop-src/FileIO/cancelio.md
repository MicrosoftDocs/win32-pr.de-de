---
description: Bricht alle ausstehenden Eingabe-und Ausgabe Vorgänge (e/a-Vorgänge) ab, die vom aufrufenden Thread für die angegebene Datei ausgegeben werden.
ms.assetid: b28162dc-0da8-41c6-9901-29381d2d72c4
title: CancelIo-Funktion (ioapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: adb1ab95b30b31670a6ff5a4cc0e0205943f7683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367878"
---
# <a name="cancelio-function"></a>CancelIo-Funktion

Bricht alle ausstehenden Eingabe-und Ausgabe Vorgänge (e/a-Vorgänge) ab, die vom aufrufenden Thread für die angegebene Datei ausgegeben werden. Mit der-Funktion werden keine e/a-Vorgänge abgebrochen, die von anderen Threads für ein Datei Handle ausgegeben werden.

Zum Abbrechen von e/a-Vorgängen von einem anderen Thread verwenden Sie die Funktion [**CancelIoEx**](cancelioex-func.md) .

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CancelIo(
  _In_ HANDLE hFile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFile* \[ in\]
</dt> <dd>

Ein Handle für die Datei.

Die-Funktion bricht alle ausstehenden e/a-Vorgänge für dieses Datei Handle ab.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null. Der Abbruch Vorgang für alle ausstehenden e/a-Vorgänge, die vom aufrufenden Thread für das angegebene Datei Handle ausgegeben wurden, wurde erfolgreich angefordert. Der Thread kann die [**gedeverlappedresult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) -Funktion verwenden, um zu bestimmen, wann die e/a-Vorgänge selbst abgeschlossen wurden.

Wenn die Funktion fehlschlägt, ist der Rückgabewert 0 (null). Um erweiterte Fehlerinformationen abzurufen, müssen Sie die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion aufrufen.

## <a name="remarks"></a>Bemerkungen

Wenn für das angegebene Datei Handle ausstehende e/a-Vorgänge ausgeführt werden und diese vom aufrufenden Thread ausgegeben werden, werden diese von der **CancelIo** -Funktion abgebrochen. **CancelIo** bricht nur ausstehende e/a-Vorgänge für das Handle ab, ändert den Zustand des Handles nicht. Dies bedeutet, dass Sie sich nicht auf den Zustand des Handles verlassen können, weil Sie nicht wissen, ob der Vorgang erfolgreich abgeschlossen wurde oder abgebrochen wurde.

Die e/a-Vorgänge müssen als überlappende e/a-Vorgänge ausgegeben werden. Wenn dies nicht der Fall ist, werden die e/a-Vorgänge nicht zurückgegeben, damit der Thread die **CancelIo** -Funktion aufruft. Das Aufrufen der **CancelIo** -Funktion mit einem Datei Handle, das nicht mit einem überlappenden **\_ Dateiflag \_** geöffnet wurde, bewirkt nichts.

Alle e/a-Vorgänge, die abgebrochen werden, werden mit dem Fehler **\_ Vorgang \_ abgebrochen**, und alle Abschluss Benachrichtigungen für die e/a-Vorgänge treten in der Regel auf.

In Windows 8 und Windows Server 2012 wird diese Funktion von den folgenden Technologien unterstützt.



| Technologie                                           | Unterstützt      |
|------------------------------------------------------|----------------|
| Server Message Block-Protokoll (SMB) 3,0<br/>   | Ja<br/> |
| SMB 3,0 transparent Failover (TFO)<br/>        | Ja<br/> |
| SMB 3,0 mit Dateifreigaben mit horizontaler Skalierung (also)<br/>   | Ja<br/> |
| Freigegebenes Clustervolume Datei System (csvfs)<br/> | Ja<br/> |
| Robustes Dateisystem (Resilient File System, ReFS)<br/>              | Ja<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[UWP-Apps für Windows XP-Desktop-Apps \|\]<br/>                                                                                                                                                                                                                                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 \[ -Desktop-Apps \| UWP-apps\]<br/>                                                                                                                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Ioapi. h (Include Windows. h); </dt> <dt>Winbase. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CancelIoEx**](cancelioex-func.md)
</dt> <dt>

[**CancelSynchronousIo**](cancelsynchronousio-func.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Dateiverwaltungsfunktionen](file-management-functions.md)
</dt> <dt>

[**Lockfileex**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[**"Read directoriychangesw"**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[Synchrone und asynchrone e/a](synchronous-and-asynchronous-i-o.md)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> <dt>

[**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

