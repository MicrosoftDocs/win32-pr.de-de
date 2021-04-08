---
description: Legt die aktuellen AC-und DC-Timeout-Ebenen fest.
ms.assetid: baa77811-046d-4a07-b3df-2a31fba2d9a7
title: IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS Steuerungs Code (ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a0c679f352012eea66b80335bc3ad1547501dd92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959742"
---
# <a name="ioctl_video_set_display_brightness-control-code"></a>IOCTL- \_ Video \_ Satz Anzeige des \_ \_ Helligkeits Steuerungs Codes

Legt die aktuellen AC-und DC-Timeout-Ebenen fest.

Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS, // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of the input buffer
  NULL,                        // lpOutBuffer
  0,                           // nOutBufferSize 
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* 
</dt> <dd>

Ein Handle für den \\ \\ . \\ LCD-Gerät. Rufen Sie zum Abrufen eines Geräte [**Handles die Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Der Steuerelement Code für den Vorgang. Dieser Wert identifiziert den spezifischen Vorgang, der ausgeführt werden soll, und den Typ des Geräts, auf dem es ausgeführt werden soll. Verwenden Sie die **IOCTL- \_ Video \_ Satz \_ Anzeige \_ Helligkeit** für diesen Vorgang.

</dd> <dt>

*lpinbuffer* 
</dt> <dd>

Ein Zeiger auf eine [**Anzeige \_ Helligkeits**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) Struktur.

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Die Größe des Puffers, auf den *lpoutbuffer* zeigt (in Bytes).

</dd> <dt>

*lpoutbuffer* 
</dt> <dd>

Wird bei diesem Vorgang nicht verwendet. auf **null** festgelegt.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Wird bei diesem Vorgang nicht verwendet. auf NULL festgelegt.

</dd> <dt>

*lpbyteszurück gegeben* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die tatsächliche Anzahl von Bytes empfängt, die von der Funktion im Ausgabepuffer zurückgegeben werden.

Wenn " *lpoverlused* " **null** (nicht überlappende e/a) ist, wird " *lpbytesused* " intern verwendet und kann nicht **null** sein.

Wenn *lpoverllapp* nicht **null** (überlappende e/a) ist, kann *lpbytesgab* **null** sein.

</dd> <dt>

*lpoverlgetauscht* 
</dt> <dd>

Ein Zeiger auf eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.

Wenn *hdevice* mit dem überlappenden \_ Flag für das Dateiflag geöffnet wurde \_ , muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur zeigen. In diesem Fall wird der Vorgang als überlappende (asynchrone) Vorgang ausgeführt. Wenn das Gerät mit dem überlappenden \_ Flag für das Dateiflag geöffnet wurde \_ und *lpoverlgetauscht* den Wert **null** hat, schlägt die Funktion auf unvorhersehbare Weise fehl.

Wenn *hdevice* ohne Angabe des überlappenden \_ Flags für das Dateiflag geöffnet wurde \_ , wird *lpoverllapp* ignoriert, und [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) wird nicht zurückgegeben, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.

Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Die Werte, die in den Elementen **ucachelligkeit** und **ucdchelligkeit** der [**Anzeige \_ Helligkeits**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) Struktur angegeben sind, müssen zuvor von der [**\_ \_ \_ unterstützten \_ Helligkeit von IOCTL-Video Abfragen**](ioctl-video-query-supported-brightness.md)zurückgegeben worden sein. Wenn die unterstützten Werte beispielsweise 10, 20, 30, 40, 50, 60, 70, 80, 90 und 100 sind, ist die Verwendung des Werts 33 ein Fehler.

Die Header Datei, die zum Erstellen von Anwendungen verwendet wird, die diese Funktion (ntddvdeo. h) enthalten, ist im Microsoft Windows Driver Development Kit (DDK) enthalten. Weitere Informationen zum Abrufen des DDK finden Sie unter [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .

Alternativ können Sie diesen Steuerelement Code wie folgt definieren:

``` syntax
#define IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x127, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP mit SP1 \[ Desktop-Apps\]<br/>                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ntddvdeo. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Backlight-Steuerungs Schnittstelle](backlight-control-interface.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**\_Helligkeit anzeigen**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))
</dt> <dt>

[**Bildschirmhelligkeit der IOCTL- \_ Video \_ Abfrage \_ \_**](ioctl-video-query-display-brightness.md)
</dt> <dt>

[**\_ \_ \_ unterstützte \_ Helligkeit der IOCTL-Video Abfrage**](ioctl-video-query-supported-brightness.md)
</dt> </dl>

 

