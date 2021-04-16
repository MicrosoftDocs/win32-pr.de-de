---
title: FSCTL_DFS_GET_PKT_ENTRY_STATE-Steuerungscode (LmDfs.h)
description: Der FSCTL_DFS_GET_PKT_ENTRY_STATE Steuerungs Code kann die gleichen Informationen wie die netdfsgetclientinfo-Funktion erhalten, kann jedoch bei manchen Konfigurationen mit hohen Wartezeiten für die DFS-Server eine bessere Leistung erzielen.
ms.assetid: d4eec104-128b-43b5-9fae-08ab0b977dec
topic_type:
- apiref
api_name:
- FSCTL_DFS_GET_PKT_ENTRY_STATE
api_location:
- LmDfs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a57fb448934908ebc1530e95a298715324aaee6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524032"
---
# <a name="fsctl_dfs_get_pkt_entry_state-control-code"></a>FSCTL_DFS_GET_PKT_ENTRY_STATE Steuerungs Codes

Der **FSCTL_DFS_GET_PKT_ENTRY_STATE** Steuerungs Code kann die gleichen Informationen wie die [**netdfsgetclientinfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) -Funktion erhalten, kann jedoch bei manchen Konfigurationen mit hohen Wartezeiten für die DFS-Server eine bessere Leistung erzielen. Es wird nicht empfohlen, den **FSCTL_DFS_GET_PKT_ENTRY_STATE** Control-Code zu verwenden, es sei denn, es treten Leistungsprobleme auf.

Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.

```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,            // handle to device
                    (DWORD)        FSCTL_DFS_GET_PKT_ENTRY_STATE, // dwIoControlCode(LPDWORD)      lpInBuffer,         // input buffer
                    (DWORD)        nInBufferSize,      // size of input buffer
                    (LPDWORD)      lpOutBuffer,        // output buffer
                    (DWORD)        nOutBufferSize,     // size of output buffer
                    (LPDWORD)      lpBytesReturned,    // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );     // OVERLAPPED structure
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* [in]
</dt> <dd>

Ein Handle für das Gerät. Rufen Sie zum Abrufen eines Geräte [**Handles die Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.

</dd> <dt>

*dwIoControlCode* [in]
</dt> <dd>

Der Steuerelement Code für den Vorgang. Verwenden Sie **FSCTL_DFS_GET_PKT_ENTRY_STATE** für diesen Vorgang.

</dd> <dt>

*lpinbuffer* 
</dt> <dd>

Adresse einer [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) Struktur und der folgenden 1-3-Unicode-Zeichen folgen.

</dd> <dt>

*nInBufferSize* [in]
</dt> <dd>

Größe (in Bytes) des Puffers, auf den der *lpinbuffer* -Parameter zeigt.

</dd> <dt>

*lpoutbuffer* [out]
</dt> <dd>

Die Adresse einer **DFS_INFO_ \#** Struktur und alle Zeichen folgen und Strukturen, auf die von der **DFS_INFO_ \#** Struktur verwiesen wird. Die angegebene Struktur ist abhängig vom **ebenenmember** in der [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) Struktur, die im Eingabepuffer weitergegeben wurde.

</dd> <dt>

*nOutBufferSize* [in]
</dt> <dd>

Größe (in Bytes) des Puffers, auf den der *lpoutbuffer* -Parameter verweist. Aufgrund der Zeichen folgen und Strukturen, auf die die zurückgegebene **DFS_INFO_ \#** -Struktur verweist, die sich ebenfalls im Ausgabepuffer befinden, sollte dieser Puffer größer als die angegebene **DFS_INFO_ \#** Struktur sein.

</dd> <dt>

*lpbyteszurück gegeben* [out]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.

Wenn der Ausgabepuffer zu klein ist, aber mindestens groß genug ist, um ein **DWORD** zu speichern, schlägt der-Befehl fehl, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt **ERROR_MORE_DATA** zurück, und das erste **DWORD** des Ausgabepuffers enthält die benötigte Größe. Wenn der Ausgabepuffer kein **DWORD** enthalten kann, schlägt der-Vorgang mit **ERROR_INSUFFICIENT_BUFFER** fehl, und *lpbyteshat* den Wert 0 (null) zurückgegeben.

Wenn *lpoverllapp* den **Wert NULL** hat, kann *lpbytes-Rückgabe* Wert nicht **null** sein. Selbst wenn ein Vorgang keine Ausgabedaten zurückgibt und *lpoutbuffer* den Wert **null** hat, verwendet [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) *lpbytesreturn*. Nach einem solchen Vorgang ist der Wert von *lpbytesno* bedeutungslos.

Wenn *lpoverllapp* nicht **null** ist, kann *lpbytesgab* **null** sein. Wenn dieser Parameter nicht **null** ist und der Vorgang Daten zurückgibt, ist *lpbytesreturns* bedeutungslos, bis der überlappende Vorgang abgeschlossen ist. Um die Anzahl der zurückgegebenen Bytes abzurufen, rufen Sie [**gezu verlappedresult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult)auf. Wenn der *hdevice* -Parameter einem e/a-Abschlussport zugeordnet ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)aufrufen.

</dd> <dt>

*lpoverlgetauscht* [in]
</dt> <dd>

Ein Zeiger auf eine [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.

Wenn *hdevice* geöffnet wurde, ohne **FILE_FLAG_OVERLAPPED** anzugeben, wird *lpoverlgetauscht* ignoriert.

Wenn *hdevice* mit dem **FILE_FLAG_OVERLAPPED** -Flag geöffnet wurde, wird der Vorgang als überlappende (asynchrone) Vorgang ausgeführt. In diesem Fall muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur verweisen, die ein Handle für ein Ereignis Objekt enthält. Andernfalls schlägt die Funktion auf unvorhersehbare Weise fehl.

Bei überlappenden Vorgängen gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) sofort zurück, und das Ereignis Objekt wird signalisiert, wenn der Vorgang abgeschlossen wurde. Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.

Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                       |
| Header<br/>                   | <dl> <dt>Lmdfs. h (Include lmdfs. h)</dt> </dl> |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**Netdfsgetclientinfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> </dl>
