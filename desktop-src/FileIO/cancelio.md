---
description: Bricht alle ausstehenden Eingabe- und Ausgabevorgänge (E/A) ab, die vom aufrufenden Thread für die angegebene Datei ausgegeben werden.
ms.assetid: b28162dc-0da8-41c6-9901-29381d2d72c4
title: CancelIo-Funktion (IoAPI.h)
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
ms.openlocfilehash: 900a47d51df882ce1f2931489ea93b5e3b4c498b8d5cc0f35e521e015e12c1d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075340"
---
# <a name="cancelio-function"></a>CancelIo-Funktion

Bricht alle ausstehenden Eingabe- und Ausgabevorgänge (E/A) ab, die vom aufrufenden Thread für die angegebene Datei ausgegeben werden. Die Funktion bricht keine E/A-Vorgänge ab, die andere Threads für ein Dateihand handle ausführen.

Verwenden Sie zum Abbrechen von E/A-Vorgängen aus einem anderen Thread [**die CancelIoEx-Funktion.**](cancelioex-func.md)

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CancelIo(
  _In_ HANDLE hFile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFile* \[ In\]
</dt> <dd>

Ein Handle für die Datei.

Die Funktion bricht alle ausstehenden E/A-Vorgänge für dieses Dateihand handle ab.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null. Der Abbrichtvorgang für alle ausstehenden E/A-Vorgänge, die vom aufrufenden Thread für das angegebene Dateihand handle ausgegeben wurden, wurde erfolgreich angefordert. Der Thread kann die [**GetOverlappedResult-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) verwenden, um zu bestimmen, wann die E/A-Vorgänge selbst abgeschlossen wurden.

Wenn die Funktion fehlschlägt, ist der Rückgabewert 0 (null). Um erweiterte Fehlerinformationen zu erhalten, rufen Sie die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Hinweise

Wenn für das angegebene Dateihand handle ausstehende E/A-Vorgänge ausgeführt werden und diese vom aufrufenden Thread ausgegeben werden, bricht die **CancelIo-Funktion** sie ab. **CancelIo** bricht nur ausstehende E/A für das Handle ab. Der Zustand des Handles wird nicht geändert. Dies bedeutet, dass Sie sich nicht auf den Status des Handle verlassen können, da Sie nicht wissen, ob der Vorgang erfolgreich abgeschlossen oder abgebrochen wurde.

Die E/A-Vorgänge müssen als überlappende E/A-Vorgänge ausgegeben werden. Falls nicht, werden die E/A-Vorgänge nicht zurückgerufen, damit der Thread die **CancelIo-Funktion aufrufen** kann. Das Aufrufen **der CancelIo-Funktion** mit einem Dateihandl, das nicht mit **FILE FLAG \_ \_ OVERLAPPED geöffnet** wird, führt nichts aus.

Alle E/A-Vorgänge, die abgebrochen werden, werden mit dem Fehler **ERROR \_ OPERATION \_ ABORTED** abgeschlossen, und alle Abschlussbenachrichtigungen für die E/A-Vorgänge treten normal auf.

In Windows 8 und Windows Server 2012 wird diese Funktion von den folgenden Technologien unterstützt.



| Technologie                                           | Unterstützt      |
|------------------------------------------------------|----------------|
| Server Message Block (SMB) 3.0-Protokoll<br/>   | Ja<br/> |
| SMB 3.0 Transparent Failover (TFO)<br/>        | Ja<br/> |
| SMB 3.0 mit Dateifreigaben mit aufskalieren (SO)<br/>   | Ja<br/> |
| Freigegebenes Clustervolume Dateisystem (CsvFS)<br/> | Ja<br/> |
| Robustes Dateisystem (Resilient File System, ReFS)<br/>              | Ja<br/> |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[XP-Desktop-Apps \| UWP-Apps\]<br/>                                                                                                                                                                                                                                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2003-Desktop-Apps \|\]<br/>                                                                                                                                                                                                                                              |
| Header<br/>                   | <dl> <dt>IoAPI.h (include Windows.h);</dt> <dt>WinBase.h auf Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP (einschließlich Windows.h)</dt> </dl> |
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

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Dateiverwaltungsfunktionen](file-management-functions.md)
</dt> <dt>

[**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[Synchrone und asynchrone E/A](synchronous-and-asynchronous-i-o.md)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> <dt>

[**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

