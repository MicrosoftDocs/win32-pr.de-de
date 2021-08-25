---
description: Legt die aktuellen Ac- und DC-Hintergrundbeleuchtungsebenen fest.
ms.assetid: baa77811-046d-4a07-b3df-2a31fba2d9a7
title: IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS -Steuerelementcode (Ntddvdeo.h)
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
ms.openlocfilehash: ec4bb5200378f9f530913f26d33bfbd485d81ae184c7b478a51c90bca18d95da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961850"
---
# <a name="ioctl_video_set_display_brightness-control-code"></a>IOCTL \_ VIDEO SET DISPLAY \_ \_ \_ BRIGHTNESS-Steuerungscode

Legt die aktuellen Ac- und DC-Hintergrundbeleuchtungsebenen fest.

Um diesen Vorgang durchzuführen, rufen Sie die [**Funktion DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern auf.


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

*hDevice* 
</dt> <dd>

Ein Handle für \\ \\ den . \\ DAS GERÄT. Um ein Gerätehand handle abzurufen, rufen Sie die [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) auf.

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Der Steuerungscode für den Vorgang. Dieser Wert gibt den spezifischen Vorgang an, der ausgeführt werden soll, und den Typ des Geräts, auf dem er ausgeführt werden soll. Verwenden **Sie IOCTL \_ VIDEO SET DISPLAY \_ \_ \_ BRIGHTNESS** für diesen Vorgang.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Ein Zeiger auf eine [**DISPLAY \_ BRIGHTNESS-Struktur.**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Die Größe des Puffers, auf den *lpOutBuffer* zeigt, in Bytes.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Wird mit diesem Vorgang nicht verwendet. auf **NULL festgelegt.**

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Wird mit diesem Vorgang nicht verwendet. auf 0 (null) festgelegt.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die tatsächliche Anzahl von Bytes empfängt, die von der Funktion im Ausgabepuffer zurückgegeben werden.

Wenn *lpOverlapped* **NULL** (nicht übersprungene E/A) ist, wird *lpBytesReturned* intern verwendet und darf nicht **NULL sein.**

Wenn *lpOverlapped* nicht **NULL** (überlappende E/A) ist, *kann lpBytesReturned* **NULL sein.**

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Ein Zeiger auf eine [**OVERLAPPED-Struktur.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

Wenn *hDevice mit* dem FLAG FILE FLAG OVERLAPPED geöffnet \_ \_ wurde, muss *lpOverlapped* auf eine gültige [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) verweisen. In diesem Fall wird der Vorgang als überlappende (asynchrone) Operation ausgeführt. Wenn das Gerät mit dem FLAG FILE FLAG OVERLAPPED geöffnet wurde und \_ \_ *lpOverlapped* **NULL** ist, schlägt die Funktion auf unvorhersehbare Weise fehl.

Wenn *hDevice* geöffnet wurde, ohne das FLAG FILE \_ FLAG OVERLAPPED anzugeben, wird \_ *lpOverlapped* ignoriert, und [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) gibt erst dann zurück, wenn der Vorgang abgeschlossen ist oder ein Fehler auftritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wurde, [**gibt DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.

Wenn der Vorgang fehlschlägt oder aussteht, [**gibt DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 0 (null) zurück. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Die in den **UcACBrightness-** und **ucDCBrightness-Membern** der [**DISPLAY \_ BRIGHTNESS-Struktur**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) angegebenen Werte müssen zuvor von [**IOCTL \_ VIDEO QUERY SUPPORTED BRIGHTNESS zurückgegeben worden \_ \_ \_ sein.**](ioctl-video-query-supported-brightness.md) Wenn die unterstützten Werte beispielsweise 10, 20, 30, 40, 50, 60, 70, 80, 90 und 100 sind, wäre die Verwendung des Werts 33 ein Fehler.

Die Headerdatei zum Erstellen von Anwendungen, die diese Funktionalität enthalten, Ntddvdeo.h, ist im Microsoft Windows Driver Development Kit (DDK) enthalten. Informationen zum Abrufen des DDK finden Sie unter [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .

Alternativ können Sie diesen Steuerelementcode wie folgt definieren:

``` syntax
#define IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x127, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP nur mit \[ SP1-Desktop-Apps\]<br/>                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ntddvdeo.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Backlight-Steuerelementschnittstelle](backlight-control-interface.md)
</dt> <dt>

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**HELLIGKEIT \_ ANZEIGEN**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))
</dt> <dt>

[**HELLIGKEIT DER ANZEIGE VON \_ IOCTL-VIDEOABFRAGEN \_ \_ \_**](ioctl-video-query-display-brightness.md)
</dt> <dt>

[**UNTERSTÜTZTE HELLIGKEIT DER \_ IOCTL-VIDEOABFRAGE \_ \_ \_**](ioctl-video-query-supported-brightness.md)
</dt> </dl>

 

