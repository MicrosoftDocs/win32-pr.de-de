---
description: Der FSCTL \_ SRV- \_ Anforderungs Code zum fort \_ setzen des \_ Schlüsselcodes wird verwendet, um einen nicht transparenten Datei Verweis für die Verwendung mit dem IOCTL \_ copychunk-Steuerungs Code abzurufen.
ms.assetid: a6e0d253-5beb-4de8-8c40-d004f5794d47
title: FSCTL_SRV_REQUEST_RESUME_KEY Steuerungs Codes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSCTL_SRV_REQUEST_RESUME_KEY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8f11b70f7b4bfd05cbd5f7c29323f1dca00083a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860660"
---
# <a name="fsctl_srv_request_resume_key-control-code"></a>F/a-Anforderung zum Fortsetzen des \_ \_ \_ \_ Schlüsselcodes

Der **FSCTL \_ SRV \_ - \_ Anforderungs \_** Code zum Fortsetzen des Schlüsselcodes wird verwendet, um einen nicht transparenten Datei Verweis für die Verwendung mit dem [**IOCTL \_ copychunk**](ioctl-copychunk.md) -Steuerungs Code abzurufen.

Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_SRV_REQUEST_RESUME_KEY, // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
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

Ein Handle für die Datei, für die der Quelldatei Schlüssel angefordert werden soll. Um dieses Handle zu erhalten, rufen [**Sie die Funktion**](/windows/win32/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.

</dd> <dt>

*dwIoControlCode* \[ in\]
</dt> <dd>

Der Steuerelement Code für den Vorgang. Verwenden Sie für diesen Vorgang den **\_ \_ \_ \_ Schlüssel** für die Fortsetzung des Befehls "f".

</dd> <dt>

*lpinbuffer* 
</dt> <dd>

Wird bei diesem Vorgang nicht verwendet. auf **null** festgelegt.

</dd> <dt>

*nInBufferSize* \[ in\]
</dt> <dd>

Wird bei diesem Vorgang nicht verwendet. auf NULL festgelegt.

</dd> <dt>

*lpoutbuffer* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den Ausgabepuffer, eine SRV-Anforderung zum Fortsetzen der **\_ \_ \_ Schlüssel** Struktur. Weitere Informationen finden Sie im Abschnitt "Hinweise".

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
#define FSCTL_SRV_REQUEST_RESUME_KEY CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 30, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _SRV_RESUME_KEY {
    UINT64 ResumeKey;
    UINT64 Timestamp;
    UINT64 Pid;
} SRV_RESUME_KEY, *PSRV_RESUME_KEY;

typedef struct _SRV_REQUEST_RESUME_KEY {
    SRV_RESUME_KEY Key;
    ULONG  ContextLength;
    BYTE   Context[1];
} SRV_REQUEST_RESUME_KEY, *PSRV_REQUEST_RESUME_KEY;
```

Diese Member können wie folgt beschrieben werden.



| Member                                                                                                                       | BESCHREIBUNG                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**Resumekey**<br/>                 | Ein nicht transparenter Wert, der die Quelldatei für den Server identifiziert.<br/>                                                                                                   |
| <span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Zeitstempel**<br/>                 | Ein nicht transparenter Wert, der die Uhrzeit angibt, zu der die Datei geöffnet wurde.<br/>                                                                                               |
| <span id="Pid"></span><span id="pid"></span><span id="PID"></span>**Lauer**<br/>                                         | Ein nicht transparenter Wert, der den Prozess identifiziert, der die Datei geöffnet hat.<br/>                                                                                                |
| <span id="Key"></span><span id="key"></span><span id="KEY"></span>**Wichtigen**<br/>                                         | Eine **SRV \_ Resume- \_ Schlüssel** Struktur. Um einen serverseitigen Kopiervorgang auszuführen, verwenden Sie diese Struktur mit dem [**IOCTL \_ copychunk**](ioctl-copychunk.md) -Steuerungs Code.<br/> |
| <span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**Contextlength**<br/> | Dieses Mitglied ist für die Verwendung durch das System reserviert. Verwenden Sie nicht.<br/>                                                                                                              |
| <span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Kontext**<br/>                         | Dieses Mitglied ist für die Verwendung durch das System reserviert. Verwenden Sie nicht.<br/>                                                                                                              |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**IOCTL- \_ copychunk**](ioctl-copychunk.md)
</dt> </dl>

 

 
