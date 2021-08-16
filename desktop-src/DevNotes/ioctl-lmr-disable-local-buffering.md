---
description: Der IOCTL \_ LMR \_ DISABLE LOCAL \_ \_ BUFFERING-Steuerungscode deaktiviert das lokale clientseitige In-Memory-Zwischenspeichern von Daten beim Lesen oder Schreiben von Daten in eine Remotedatei. Dies ist ein intern definierter Steuerelementcode, der in einem öffentlichen Header nicht verfügbar ist.
ms.assetid: a464671b-253c-4f35-84a2-2619cb15b009
title: IOCTL_LMR_DISABLE_LOCAL_BUFFERING Von Steuerelementcode
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
ms.openlocfilehash: 88a6fff0955fb9e0c57c7ea5fae99f532c7c6d4dcc3578a75e07da3f35867f9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827190"
---
# <a name="ioctl_lmr_disable_local_buffering-control-code"></a>IOCTL \_ LMR \_ DISABLE LOCAL \_ \_ BUFFERING control code

Der **IOCTL \_ LMR \_ DISABLE LOCAL \_ \_ BUFFERING-Steuerungscode** deaktiviert das lokale clientseitige In-Memory-Zwischenspeichern von Daten beim Lesen oder Schreiben von Daten in eine Remotedatei. Dies ist ein intern definierter Steuerelementcode, der in einem öffentlichen Header nicht verfügbar ist.

Rufen Sie zum Ausführen dieses Vorgangs die [**DeviceIoControl-Funktion**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern auf.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_LMR_DISABLE_LOCAL_BUFFERING, // dwIoControlCode
  (LPVOID) NULL,                // lpInBuffer
  (DWORD) 0,                    // nInBufferSize
  (LPVOID) NULL,                // lpOutBuffer
  (DWORD) 0,                    // nOutBufferSize
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDevice* \[ In\]
</dt> <dd>

Ein Handle für die Remotedatei. Rufen Sie die [**CreateFile-Funktion**](/windows/win32/api/fileapi/nf-fileapi-createfilea) auf, um dieses Handle abzurufen.

</dd> <dt>

*dwIoControlCode* \[ In\]
</dt> <dd>

Der Steuerelementcode für den Vorgang. Verwenden Sie den Wert 0x140390 für diesen Vorgang.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Nicht verwendet, muss **NULL** sein.

</dd> <dt>

*nInBufferSize* \[ In\]
</dt> <dd>

Die Größe des Eingabepuffers in Bytes. Muss Null sein.

</dd> <dt>

*lpOutBuffer* \[ out\]
</dt> <dd>

Nicht verwendet, muss **NULL** sein.

</dd> <dt>

*nOutBufferSize* \[ In\]
</dt> <dd>

Die Größe des Ausgabepuffers in Bytes. Muss Null sein.

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

Der **IOCTL \_ LMR \_ DISABLE LOCAL \_ \_ BUFFERING-Steuerungscode** wird intern vom System als 0x140390 und nicht in einer öffentlichen Headerdatei definiert. Sie wird von speziellen Anwendungen verwendet, um die lokale clientseitige Zwischenspeicherung von Daten im Arbeitsspeicher zu deaktivieren, wenn Daten aus einer Remotedatei gelesen oder in eine Remotedatei geschrieben werden. Nachdem die lokale Pufferung deaktiviert wurde, bleibt die Einstellung wirksam, bis alle geöffneten Handles für die Datei geschlossen sind und der Redirector die internen Datenstrukturen bereinigt.

Allgemeine Anwendungen sollten **IOCTL \_ LMR \_ DISABLE LOCAL \_ \_ BUFFERING** nicht verwenden, da dies zu übermäßigem Netzwerkdatenverkehr und damit verbundenen Leistungseinbußen führen kann. Der **IOCTL \_ LMR \_ DISABLE LOCAL \_ \_ BUFFERING-Steuerungscode** sollte nur in speziellen Anwendungen verwendet werden, die große Datenmengen über das Netzwerk verschieben und gleichzeitig versuchen, die Netzwerkbandbreite zu maximieren. Beispielsweise verwenden die Funktionen [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) und [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) **IOCTL \_ LMR \_ DISABLE LOCAL \_ \_ BUFFERING,** um die Leistung beim Kopieren großer Dateien zu verbessern.

**IOCTL \_ LMR \_ DISABLE \_ LOCAL \_ BUFFERING** wird von lokalen Dateisystemen nicht implementiert und schlägt mit dem Fehler **ERROR INVALID \_ \_ FUNCTION** fehl. Die Ausgabe des **IOCTL \_ LMR \_ DISABLE LOCAL \_ \_ BUFFERING-Steuerungscodes** auf Remoteverzeichnishandles schlägt mit dem Fehler **ERROR NOT SUPPORTED \_ \_ fehl.**

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Deviceiocontrol**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
