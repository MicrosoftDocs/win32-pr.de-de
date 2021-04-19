---
description: Der IOCTL \_ copychunk-Steuerungs Code initiiert eine serverseitige Kopie eines Datenbereichs, auch als Block bezeichnet.
ms.assetid: 36f68840-bd5c-4cfc-a8ad-0cfbbdc5a2a9
title: IOCTL_COPYCHUNK Steuerungs Codes
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
ms.openlocfilehash: c425fc53563e6dfc16d2040fb575f47f0f8fdf35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344804"
---
# <a name="ioctl_copychunk-control-code"></a>IOCTL \_ copychunk-Steuerungs Code

Der **IOCTL \_ copychunk** -Steuerungs Code initiiert eine serverseitige Kopie eines Datenbereichs, auch als Block bezeichnet.

Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.


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

*hdevice* \[ in\]
</dt> <dd>

Ein Handle für die Datei, die das Ziel des serverseitigen Kopiervorgangs ist. Um dieses Handle zu erhalten, rufen [**Sie die Funktion**](/windows/win32/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.

</dd> <dt>

*dwIoControlCode* \[ in\]
</dt> <dd>

Der Steuerelement Code für den Vorgang. Verwenden Sie **IOCTL \_ copychunk** für diesen Vorgang.

</dd> <dt>

*lpinbuffer* 
</dt> <dd>

Ein Zeiger auf den Eingabepuffer, eine **SRV \_ copychunk- \_ Kopier** Struktur. Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> <dt>

*nInBufferSize* \[ in\]
</dt> <dd>

Die Größe des Eingabe Puffers in Bytes.

</dd> <dt>

*lpoutbuffer* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den Ausgabepuffer, eine **SRV- \_ copychunk- \_ Antwort** Struktur. Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> <dt>

*nOutBufferSize* \[ in\]
</dt> <dd>

Die Größe des Ausgabepuffers in Bytes.

</dd> <dt>

*lpbyteszurück gegeben* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.

Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, die [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion gibt einen **fehlerhaften \_ \_ Puffer** zurück, und *lpbytesreturns* ist 0 (null).

Wenn der *lpoverllapp* -Parameter **null** ist, kann *lpbytes-Rückgabe* Wert nicht **null** sein. Selbst wenn ein Vorgang keine Ausgabedaten zurückgibt und der *lpoutbuffer* -Parameter den Wert **null** hat, verwendet [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) *lpbytesreturn*. Nach einem solchen Vorgang ist der Wert von *lpbytesno* bedeutungslos.

Wenn *lpoverllapp* nicht **null** ist, kann *lpbytesgab* **null** sein. Wenn *lpoverlgetauscht* nicht **null** ist und der Vorgang Daten zurückgibt, ist *lpbytesreturns* bedeutungslos, bis der überlappende Vorgang abgeschlossen ist. Um die Anzahl der zurückgegebenen Bytes abzurufen, rufen Sie die Funktion [**ge-verlappedresult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) auf. Wenn der *hdevice* -Parameter einem e/a-Abschlussport zugeordnet ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie die [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion aufrufen.

</dd> <dt>

*lpoverlgetauscht* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.

Wenn der *hdevice* -Parameter ohne Angabe eines **überlappenden \_ Dateiflags \_** geöffnet wurde, wird *lpoverlgetauscht* ignoriert.

Wenn *hdevice* mit dem überlappenden Flag für das **\_ \_ Dateiflag** geöffnet wurde, wird der Vorgang als überlappende (asynchrone) Vorgang ausgeführt. In diesem Fall muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur verweisen, die ein Handle für ein Ereignis Objekt enthält. Andernfalls schlägt die Funktion auf unvorhersehbare Weise fehl.

Bei überlappenden Vorgängen gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) sofort zurück, und das Ereignis Objekt wird signalisiert, wenn der Vorgang abgeschlossen wurde. Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.

Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Diesem Steuerungs Code ist keine Header Datei zugeordnet. Sie müssen den Steuerungs Code und die Datenstrukturen wie folgt definieren.

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
| <span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Füll**<br/>                                             | Die Anzahl der Daten Bytes im Block, die kopiert werden sollen. Muss größer als 0 (null) und kleiner oder gleich 1 MB sein. **Länge** \* " **Chunkcount** " muss kleiner oder gleich 16 MB sein.<br/>                                                                                                                                                                         |
| <span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**<br/>                             | Ein Schlüssel, der die Quelldatei mit den zu kopierenden Daten darstellt. Dieser Schlüssel wird über den Schlüssel zum Fortsetzen der [**fisctl- \_ SRV- \_ Anforderung \_ \_**](fsctl-srv-request-resume-key.md)abgerufen.<br/>                                                                                                                                                                                   |
| <span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**Anzahl von Blöcken**<br/>                             | Die Anzahl der Blöcke, die kopiert werden sollen. Muss größer als 0 (null) und kleiner oder gleich 256 sein.<br/>                                                                                                                                                                                                                                                                |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Bleiben**<br/>                                     | Dieses Mitglied ist für die Verwendung durch das System reserviert. Verwenden Sie nicht.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Block**<br/>                                                 | Ein Array von Block **count** - **SRV- \_ copychunk** -Strukturen, eines für jeden zu kopierenden Block. Die Länge dieses Arrays in Bytes muss " **chunkcount** \* sizeof (**SRV \_ copyblock**)" lauten.<br/>                                                                                                                                                                       |
| <span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**Chunksgeschrieben**<br/>                 | Wenn bei dem Vorgang ein **Fehler aufgrund eines \_ ungültigen \_ Parameters aufgetreten** ist, gibt dieser Wert die maximale Anzahl von Blöcken an, die der Server in einer einzelnen Anforderung akzeptiert, d. h. 256. Andernfalls gibt dieser Wert die Anzahl von Blöcken an, die erfolgreich geschrieben wurden.<br/>                                                                                               |
| <span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**Chunkbyteswritten**<br/> | Wenn bei dem Vorgang ein **Fehler aufgrund eines \_ ungültigen \_ Parameters aufgetreten** ist, gibt dieser Wert die maximale Anzahl von Bytes an, die der Server in einem einzelnen Block schreiben darf (1 MB). Andernfalls gibt dieser Wert die Anzahl von Bytes an, die erfolgreich in das letzte Segment geschrieben wurden, das nicht erfolgreich verarbeitet wurde (bei einem partiellen Schreibvorgang).<br/> |
| <span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**Total byteswritten**<br/> | Wenn bei dem Vorgang ein **Fehler aufgrund eines \_ ungültigen \_ Parameters aufgetreten** ist, gibt dieser Wert die maximale Anzahl von Bytes an, die der Server in einer einzelnen Anforderung kopiert, d. h. 16 MB. Andernfalls gibt dieser Wert die Anzahl der Bytes an, die erfolgreich geschrieben wurden.<br/>                                                                                                 |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**Fortsetzen des Schlüssels der ssctl \_ SRV- \_ Anforderung \_ \_**](fsctl-srv-request-resume-key.md)
</dt> </dl>

 

 
