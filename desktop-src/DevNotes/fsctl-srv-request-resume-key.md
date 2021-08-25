---
description: Der FSCTL \_ SRV \_ REQUEST RESUME \_ \_ KEY-Steuerungscode wird verwendet, um einen nicht transparenten Dateiverweis für die Verwendung mit dem IOCTL \_ COPYCHUNK-Steuerungscode abzurufen.
ms.assetid: a6e0d253-5beb-4de8-8c40-d004f5794d47
title: FSCTL_SRV_REQUEST_RESUME_KEY Steuerelementcode
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
ms.openlocfilehash: a3654cd78b3e337e07c8267a98a09e0dcabbbb5cb193238e3ca3ebe31c59b12b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161814"
---
# <a name="fsctl_srv_request_resume_key-control-code"></a>FSCTL \_ SRV \_ REQUEST RESUME \_ \_ KEY-Steuerungscode

Der **FSCTL \_ SRV \_ REQUEST RESUME \_ KEY-Steuerungscode \_** wird verwendet, um einen nicht transparenten Dateiverweis für die Verwendung mit dem [**IOCTL \_ COPYCHUNK-Steuerungscode**](ioctl-copychunk.md) abzurufen.

Rufen Sie zum Ausführen dieses Vorgangs die [**DeviceIoControl-Funktion**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern auf.


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

*hDevice* \[ In\]
</dt> <dd>

Ein Handle für die Datei, für die der Quelldateischlüssel angefordert werden soll. Rufen Sie die [**CreateFile-Funktion**](/windows/win32/api/fileapi/nf-fileapi-createfilea) auf, um dieses Handle abzurufen.

</dd> <dt>

*dwIoControlCode* \[ In\]
</dt> <dd>

Der Steuerelementcode für den Vorgang. Verwenden Sie **FSCTL \_ SRV \_ REQUEST RESUME \_ \_ KEY** für diesen Vorgang.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Wird nicht mit diesem Vorgang verwendet. legen Sie auf **NULL** fest.

</dd> <dt>

*nInBufferSize* \[ In\]
</dt> <dd>

Wird nicht mit diesem Vorgang verwendet. auf 0 (null) festgelegt.

</dd> <dt>

*lpOutBuffer* \[ out\]
</dt> <dd>

Ein Zeiger auf den Ausgabepuffer, eine **SRV \_ REQUEST RESUME \_ \_ KEY-Struktur.** Weitere Informationen finden Sie im Abschnitt "Hinweise".

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



| Member                                                                                                                       | Beschreibung                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ResumeKey**<br/>                 | Ein nicht transparenter Wert, der die Quelldatei für den Server identifiziert.<br/>                                                                                                   |
| <span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Timestamp**<br/>                 | Ein nicht transparenter Wert, der den Zeitpunkt angibt, zu dem die Datei geöffnet wurde.<br/>                                                                                               |
| <span id="Pid"></span><span id="pid"></span><span id="PID"></span>**Pid**<br/>                                         | Ein nicht transparenter Wert, der den Prozess identifiziert, der die Datei geöffnet hat.<br/>                                                                                                |
| <span id="Key"></span><span id="key"></span><span id="KEY"></span>**Schlüssel**<br/>                                         | Eine **SRV \_ RESUME \_ KEY-Struktur.** Um einen serverseitigen Kopiervorgang auszuführen, verwenden Sie diese Struktur mit dem [**IOCTL \_ COPYCHUNK-Steuerelementcode.**](ioctl-copychunk.md)<br/> |
| <span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**ContextLength**<br/> | Dieser Member ist für die Systemverwendung reserviert. nicht verwenden.<br/>                                                                                                              |
| <span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Kontext**<br/>                         | Dieser Member ist für die Systemverwendung reserviert. nicht verwenden.<br/>                                                                                                              |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Deviceiocontrol**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**IOCTL \_ COPYCHUNK**](ioctl-copychunk.md)
</dt> </dl>

 

 
