---
description: Sendet ein E/A-Abschlusspaket an einen E/A-Abschlussport.
ms.assetid: 69a9b1e5-2d40-42de-a14a-f7b6f29bf571
title: PostQueuedCompletionStatus-Funktion (IoAPI.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostQueuedCompletionStatus
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: e56bad8b9de85f22836f9446b67340d22e71fe83552da6796e7864d3baddae4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683360"
---
# <a name="postqueuedcompletionstatus-function"></a>PostQueuedCompletionStatus-Funktion

Sendet ein E/A-Abschlusspaket an einen E/A-Abschlussport.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI PostQueuedCompletionStatus(
  _In_     HANDLE       CompletionPort,
  _In_     DWORD        dwNumberOfBytesTransferred,
  _In_     ULONG_PTR    dwCompletionKey,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*CompletionPort* \[ In\]
</dt> <dd>

Ein Handle für einen E/A-Abschlussport, an den das E/A-Abschlusspaket gesendet werden soll.

</dd> <dt>

*dwNumberOfBytesTransferred* \[ In\]
</dt> <dd>

Der Wert, der über den *lpNumberOfBytesTransferred-Parameter* der [**GetQueuedCompletionStatus-Funktion**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) zurückgegeben werden soll.

</dd> <dt>

*dwCompletionKey* \[ In\]
</dt> <dd>

Der Wert, der über den *lpCompletionKey-Parameter* der [**GetQueuedCompletionStatus-Funktion**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) zurückgegeben werden soll.

</dd> <dt>

*lpOverlapped* \[ in, optional\]
</dt> <dd>

Der Wert, der über den *lpOverlapped-Parameter* der [**GetQueuedCompletionStatus-Funktion**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) zurückgegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null.

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null. Rufen [**Sie GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf, um erweiterte Fehlerinformationen abzurufen.

## <a name="remarks"></a>Hinweise

Das E/A-Abschlusspaket erfüllt einen ausstehenden Aufruf der [**GetQueuedCompletionStatus-Funktion.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) Diese Funktion gibt mit den drei Werten zurück, die als zweiter, dritter und vierter Parameter des Aufrufs von **PostQueuedCompletionStatus** übergeben werden. Das System verwendet oder überprüft diese Werte nicht. Insbesondere muss der *lpOverlapped-Parameter* nicht auf eine [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) verweisen.

In Windows 8 und Windows Server 2012 wird diese Funktion von den folgenden Technologien unterstützt.



| Technologie                                           | Unterstützt      |
|------------------------------------------------------|----------------|
| Server Message Block (SMB) 3.0-Protokoll<br/>   | Ja<br/> |
| Transparentes SMB 3.0-Failover (TFO)<br/>        | Ja<br/> |
| SMB 3.0 mit Dateifreigaben mit aufskalieren (SO)<br/>   | Ja<br/> |
| Freigegebenes Clustervolume File System (CsvFS)<br/> | Ja<br/> |
| Robustes Dateisystem (Resilient File System, ReFS)<br/>              | Ja<br/> |



 

CsvFs verwenden umgeleitete E/A-Leitungen für komprimierte Dateien.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[XP-Desktop-Apps \| UWP-Apps\]<br/>                                                                                                                                                                                                                                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für \[ Server 2003-Desktop-Apps \|\]<br/>                                                                                                                                                                                                                                              |
| Header<br/>                   | <dl> <dt>IoAPI.h (include Windows.h);</dt> <dt>WinBase.h auf Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP (einschließlich Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[Dateiverwaltungsfunktionen](file-management-functions.md)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**Überlappende**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)
</dt> </dl>

 

