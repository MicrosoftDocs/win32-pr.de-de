---
description: Der IOCTL \_ COPYCHUNK-Steuerungscode initiiert eine serverseitige Kopie eines Datenbereichs, der auch als Block bezeichnet wird.
ms.assetid: 36f68840-bd5c-4cfc-a8ad-0cfbbdc5a2a9
title: IOCTL_COPYCHUNK-Steuerelementcode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPY_CHUNK
api_type:
- NA
api_location: ''
ms.openlocfilehash: 415e94d8ed19d3248beb31d8a5e6327e1adc11078483d4f60fcd42699e4dab89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001730"
---
# <a name="ioctl_copychunk-control-code"></a>IOCTL \_ COPYCHUNK-Steuerungscode

Der **IOCTL \_ COPYCHUNK-Steuerungscode** initiiert eine serverseitige Kopie eines Datenbereichs, der auch als Block bezeichnet wird.

Rufen Sie zum Ausführen dieses Vorgangs die [**DeviceIoControl-Funktion**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern auf.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_COPYCHUNK,              // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDevice* \[ In\]
</dt> <dd>

Ein Handle für die Datei, die das Ziel des serverseitigen Kopiervorgangs ist. Rufen Sie die [**CreateFile-Funktion**](/windows/win32/api/fileapi/nf-fileapi-createfilea) auf, um dieses Handle abzurufen.

</dd> <dt>

*dwIoControlCode* \[ In\]
</dt> <dd>

Der Steuerelementcode für den Vorgang. Verwenden Sie **IOCTL \_ COPYCHUNK** für diesen Vorgang.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Ein Zeiger auf den Eingabepuffer, eine **SRV \_ COPYCHUNK \_ COPY-Struktur.** Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> <dt>

*nInBufferSize* \[ In\]
</dt> <dd>

Die Größe des Eingabepuffers in Bytes.

</dd> <dt>

*lpOutBuffer* \[ out\]
</dt> <dd>

Ein Zeiger auf den Ausgabepuffer, eine **SRV \_ COPYCHUNK \_ RESPONSE-Struktur.** Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> <dt>

*nOutBufferSize* \[ In\]
</dt> <dd>

Die Größe des Ausgabepuffers in Bytes.

</dd> <dt>

*lpBytesReturned* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten in Bytes empfängt.

Wenn der Ausgabepuffer zu klein ist, schlägt der Aufruf fehl, die [**GetLastError-Funktion**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt **ERROR INSUFFICIENT \_ \_ BUFFER** zurück, und *lpBytesReturned* ist 0 (null).

Wenn der *lpOverlapped-Parameter* **NULL** ist, kann *lpBytesReturned* nicht **NULL** sein. Selbst wenn ein Vorgang keine Ausgabedaten zurückgibt und der *lpOutBuffer-Parameter* **NULL** ist, verwendet [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) *lpBytesReturned.* Nach einem solchen Vorgang ist der Wert von *lpBytesReturned bedeutungslos.*

Wenn *lpOverlapped* nicht **NULL** ist, kann *lpBytesReturned* **NULL** sein. Wenn *lpOverlapped* nicht **NULL** ist und der Vorgang Daten zurückgibt, ist *lpBytesReturned bedeutungslos,* bis der überlappende Vorgang abgeschlossen ist. Rufen Sie die [**GetOverlappedResult-Funktion**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) auf, um die Anzahl der zurückgegebenen Bytes abzurufen. Wenn der *hDevice-Parameter* einem E/A-Abschlussport zugeordnet ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie die [**GetQueuedCompletionStatus-Funktion**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) aufrufen.

</dd> <dt>

*lpOverlapped* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**OVERLAPPED-Struktur.**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)

Wenn der *hDevice-Parameter* ohne Angabe von **FILE FLAG \_ \_ OVERLAPPED** geöffnet wurde, wird *lpOverlapped* ignoriert.

Wenn *hDevice* mit dem **FLAG FILE FLAG \_ \_ OVERLAPPED** geöffnet wurde, wird der Vorgang als überlappender (asynchroner) Vorgang ausgeführt. In diesem Fall muss *lpOverlapped* auf eine gültige [**OVERLAPPED-Struktur**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) zeigen, die ein Handle für ein Ereignisobjekt enthält. Andernfalls schlägt die Funktion auf unvorhersehbare Weise fehl.

Für überlappende Vorgänge gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) sofort zurück, und das Ereignisobjekt wird signalisiert, wenn der Vorgang abgeschlossen wurde. Andernfalls wird die Funktion erst zurückgegeben, nachdem der Vorgang abgeschlossen wurde oder bis ein Fehler auftritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wurde, gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.

Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 0 (null) zurück. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Diesem Steuerelementcode ist keine Headerdatei zugeordnet. Sie müssen den Steuerelementcode und die Datenstrukturen wie folgt definieren.

``` syntax
#define IOCTL_COPYCHUNK CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 262, METHOD_BUFFERED,  FILE_READ_ACCESS)

typedef struct _SRV_COPYCHUNK {
    LARGE_INTEGER SourceOffset;
    LARGE_INTEGER DestinationOffset;
    ULONG  Length;
} SRV_COPYCHUNK, *PSRV_COPYCHUNK;

typedef struct _SRV_COPYCHUNK_COPY {
    SRV_RESUME_KEY SourceFile;
    ULONG          ChunkCount;
    ULONG          Reserved;
    SRV_COPYCHUNK  Chunk[1];    // Array
} SRV_COPYCHUNK_COPY, *PSRV_COPYCHUNK_COPY;

typedef struct _SRV_COPYCHUNK_RESPONSE {
    ULONG          ChunksWritten;
    ULONG          ChunkBytesWritten;
    ULONG          TotalBytesWritten;
} SRV_COPYCHUNK_RESPONSE, *PSRV_COPYCHUNK_RESPONSE;
```

Diese Member können wie folgt beschrieben werden.



| Member                                                                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**SourceOffset**<br/>                     | Der Offset in Bytes vom Anfang der Quelldatei bis zum zu kopierenden Block.<br/>                                                                                                                                                                                                                                                                     |
| <span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**DestinationOffset**<br/> | Der Offset in Bytes vom Anfang der Zieldatei bis zum Speicherort, an den der Block kopiert werden soll.<br/>                                                                                                                                                                                                                                               |
| <span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Länge**<br/>                                             | Die Anzahl der Datenbytes im zu kopierenden Block. Muss größer als 0 (null) und kleiner oder gleich 1 MB sein. **Länge** \* **ChunkCount** muss kleiner oder gleich 16 MB sein.<br/>                                                                                                                                                                         |
| <span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**Sourcefile**<br/>                             | Ein Schlüssel, der die Quelldatei mit den zu kopierenden Daten darstellt. Dieser Schlüssel wird über [**FSCTL \_ SRV \_ REQUEST RESUME \_ \_ KEY**](fsctl-srv-request-resume-key.md)abgerufen.<br/>                                                                                                                                                                                   |
| <span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**ChunkCount**<br/>                             | Die Anzahl der zu kopierenden Blöcke. Muss größer als 0 (null) und kleiner oder gleich 256 sein.<br/>                                                                                                                                                                                                                                                                |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserviert**<br/>                                     | Dieser Member ist für die Systemverwendung reserviert. nicht verwenden.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Stück**<br/>                                                 | Ein Array von **ChunkCount-SRV \_ COPYCHUNK-Strukturen,** eine für jeden zu kopierenden Block.  Die Länge dieses Arrays in Bytes muss **ChunkCount** \* sizeof(**SRV \_ COPYCHUNK**) sein.<br/>                                                                                                                                                                       |
| <span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**SegmenteGeschrieben**<br/>                 | Wenn der Vorgang mit **ERROR \_ INVALID \_ PARAMETER** fehlgeschlagen ist, gibt dieser Wert die maximale Anzahl von Blöcken an, die der Server in einer einzelnen Anforderung akzeptiert ( 256). Andernfalls gibt dieser Wert die Anzahl der Blöcke an, die erfolgreich geschrieben wurden.<br/>                                                                                               |
| <span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**ChunkBytesWritten**<br/> | Wenn der Vorgang mit **ERROR \_ INVALID \_ PARAMETER** fehlgeschlagen ist, gibt dieser Wert die maximale Anzahl von Bytes an, die der Server in einem einzelnen Block schreiben darf (1 MB). Andernfalls gibt dieser Wert die Anzahl der Bytes an, die erfolgreich im letzten Block geschrieben wurden, der nicht erfolgreich verarbeitet wurde (wenn ein teilgeschrieben wurde).<br/> |
| <span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**TotalBytesWritten**<br/> | Wenn der Vorgang mit **ERROR \_ INVALID \_ PARAMETER** fehlgeschlagen ist, gibt dieser Wert die maximale Anzahl von Bytes an, die der Server in einer einzelnen Anforderung kopiert, die 16 MB beträgt. Andernfalls gibt dieser Wert die Anzahl der Bytes an, die erfolgreich geschrieben wurden.<br/>                                                                                                 |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Deviceiocontrol**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**FSCTL \_ SRV \_ REQUEST \_ RESUME \_ KEY**](fsctl-srv-request-resume-key.md)
</dt> </dl>

 

 
