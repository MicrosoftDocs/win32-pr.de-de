---
description: Ruft die aktuellen Ac- und DC-Hintergrundlichtstufen und den aktuellen Energiezustand ab.
ms.assetid: c7b7c302-6e92-46a7-b9a6-e3f2a3e44d1b
title: IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS Steuerelementcode (Ntddvdeo.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: 673930fbde301c031049316255c9bcee40fd4e6a4f3c362977caf6e0569c5f5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143413"
---
# <a name="ioctl_video_query_display_brightness-control-code"></a>\_IOCTL VIDEO QUERY DISPLAY BRIGHTNESS Control \_ \_ \_ Code

\[Dieser Steuerungscode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Die Unterstützung für diesen Steuerelementcode wurde in Windows Server 2008 und Windows Vista entfernt. Verwenden Sie stattdessen die [**WmiMonitorBrightness-Klasse.**](/windows/desktop/WmiCoreProv/wmimonitorbrightness)\]

Ruft die aktuellen Ac- und DC-Hintergrundlichtstufen und den aktuellen Energiezustand ab.

Rufen Sie zum Ausführen dieses Vorgangs die [**DeviceIoControl-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern auf.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDevice* 
</dt> <dd>

Ein Handle für die \\ \\ . \\ INSTRUMENT-Gerät. Um ein Gerätehandle abzurufen, rufen Sie die [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) auf.

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Der Steuerelementcode für den Vorgang. Dieser Wert gibt den spezifischen auszuführenden Vorgang und den Typ des Geräts an, auf dem er ausgeführt werden soll. Verwenden Sie **IOCTL \_ VIDEO QUERY DISPLAY \_ \_ \_ BRIGHTNESS** für diesen Vorgang.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Wird nicht mit diesem Vorgang verwendet. legen Sie auf **NULL** fest.

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Wird nicht mit diesem Vorgang verwendet. auf 0 (null) festgelegt.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine [**DISPLAY \_ BRIGHTNESS-Struktur**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) empfängt.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Die Größe des Ausgabepuffers in Bytes.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der zurückgegebenen Ausgabedaten in Bytes empfängt.

Wenn der Ausgabepuffer zu klein ist, um Daten zurückzugeben, schlägt der Aufruf fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehlercode ERROR \_ INSUFFICIENT BUFFER \_ zurück, und die zurückgegebene Byteanzahl ist 0 (null).

Wenn der Ausgabepuffer zu klein ist, um alle Daten aufzunehmen, aber einige Einträge enthalten kann, gibt das Betriebssystem so viel zurück, wie es passt, der Aufruf schlägt fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehlercode ERROR \_ MORE DATA \_ zurück, und *lpBytesReturned* gibt die Menge der zurückgegebenen Daten an. Ihre Anwendung sollte [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit demselben Vorgang erneut aufrufen und einen neuen Startpunkt angeben.

Wenn *lpOverlapped* **NULL** ist (nicht überlagerte E/A), darf *lpBytesReturned* nicht **NULL** sein.

Wenn *lpOverlapped* nicht **NULL** ist (überlappende E/A), kann *lpBytesReturned* **NULL** sein. Wenn es sich um einen überlappenden Vorgang handelt, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie die [**GetOverlappedResult-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) aufrufen. Wenn *hDevice* einem E/A-Abschlussport zugeordnet ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie die [**GetQueuedCompletionStatus-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) aufrufen.

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Ein Zeiger auf eine [**OVERLAPPED-Struktur.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

Wenn *hDevice* mit dem FLAG FILE FLAG OVERLAPPED geöffnet \_ \_ wurde, muss *lpOverlapped* auf eine gültige [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) verweisen. In diesem Fall wird der Vorgang als überlappender (asynchroner) Vorgang ausgeführt. Wenn das Gerät mit dem FLAG FILE FLAG OVERLAPPED geöffnet wurde \_ \_ und *lpOverlapped* **NULL** ist, schlägt die Funktion auf unvorhersehbare Weise fehl.

Wenn *hDevice* geöffnet wurde, ohne das FLAG FILE \_ FLAG \_ OVERLAPPED anzugeben, wird *lpOverlapped* ignoriert, und [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) wird erst zurückgegeben, nachdem der Vorgang abgeschlossen wurde oder bis ein Fehler auftritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wurde, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.

Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 0 (null) zurück. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Die Headerdatei zum Erstellen von Anwendungen, die diese Funktionalität enthalten, Ntddvdeo.h, ist im Microsoft Windows Driver Development Kit (DDK) enthalten. Informationen zum Abrufen des DDK finden Sie unter [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .

Alternativ können Sie diesen Steuerelementcode wie folgt definieren:

``` syntax
#define IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x126, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP1-Desktop-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Ende des Supports (Client)<br/>    | Windows XP mit SP2<br/>                                                        |
| Ende des Supports (Server)<br/>    | Windows Server 2003 R2<br/>                                                     |
| Header<br/>                   | <dl> <dt>Ntddvdeo.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Backlight-Steuerelementschnittstelle](backlight-control-interface.md)
</dt> <dt>

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**\_DISPLAY-HELLIGKEIT**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))
</dt> <dt>

[**IOCTL \_ VIDEO \_ SET \_ DISPLAY \_ BRIGHTNESS**](ioctl-video-set-display-brightness.md)
</dt> </dl>

 

