---
description: Legt verschiedene Akkuinformationen fest.
ms.assetid: b827983d-5fb8-43f2-b732-541d16b3eb7b
title: IOCTL_BATTERY_SET_INFORMATION Steuerelementcode (Poclass.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: be6fca1042c4ba381996ccca1740d1662f9795269aaaa8b3e429576d96011dbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143493"
---
# <a name="ioctl_battery_set_information-control-code"></a>IOCTL \_ BATTERY SET INFORMATION Control \_ \_ Code

Legt verschiedene Akkuinformationen fest. Die Eingabeparameterstruktur [**BATTERY \_ SET \_ INFORMATION**](battery-set-information-str.md)gibt an, welche Informationen zum Akkustatus festgelegt werden sollen.

Rufen Sie zum Ausführen dieses Vorgangs die [**DeviceIoControl-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern auf.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to battery
  IOCTL_BATTERY_SET_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,           // input buffer
  (DWORD) nInBufferSize,         // size of input buffer
  NULL,                          // lpOutBuffer
  0,                             // nOutBufferSize
  (LPDWORD) lpBytesReturned,     // number of bytes returned
  (LPOVERLAPPED) lpOverlapped    // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDevice* 
</dt> <dd>

Ein Handle für den Akku, für den die Informationen festgelegt werden sollen. Um ein Gerätehandle abzurufen, rufen Sie die [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) auf.

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Der Steuerelementcode für den Vorgang. Dieser Wert gibt den spezifischen auszuführenden Vorgang und den Typ des Geräts an, auf dem er ausgeführt werden soll. Verwenden Sie **IOCTL \_ BATTERY \_ SET \_ INFORMATION** für diesen Vorgang.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Ein Zeiger auf eine [**BATTERY \_ SET \_ INFORMATION-Struktur.**](battery-set-information-str.md)

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Die Größe des Eingabepuffers in Bytes.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Wird nicht mit diesem Vorgang verwendet. legen Sie auf **NULL** fest.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Wird nicht mit diesem Vorgang verwendet. auf 0 (null) festgelegt.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der im *lpOutBuffer-Puffer* zurückgegebenen Daten in Bytes empfängt.

Wenn der Ausgabepuffer zu klein ist, um Daten zurückzugeben, schlägt der Aufruf fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehlercode ERROR \_ INSUFFICIENT BUFFER \_ zurück, und die zurückgegebene Byteanzahl ist 0 (null).

Wenn *lpOverlapped* **NULL** ist (nicht überlagerte E/A), kann *lpBytesReturned* nicht **NULL** sein, auch wenn *lpOutBuffer* **NULL** ist.

Wenn *lpOverlapped* nicht **NULL** ist (überlappende E/A), kann *lpBytesReturned* **NULL** sein. Wenn es sich um einen überlappenden Vorgang handelt, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie die [**GetOverlappedResult-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) aufrufen. Wenn *hDevice* einem E/A-Abschlussport zugeordnet ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie die [**GetQueuedCompletionStatus-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) aufrufen.

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Ein Zeiger auf eine [**OVERLAPPED-Struktur.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

Wenn *hDevice* mit dem FLAG FILE FLAG OVERLAPPED geöffnet \_ \_ wurde, muss *lpOverlapped* auf eine gültige [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) verweisen. In diesem Fall wird [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) als überlappender (asynchroner) Vorgang ausgeführt. Wenn das Gerät mit dem FLAG FILE FLAG OVERLAPPED geöffnet wurde \_ \_ und *lpOverlapped* **NULL** ist, schlägt die Funktion auf unvorhersehbare Weise fehl.

Wenn *hDevice* geöffnet wurde, ohne das FLAG FILE \_ FLAG \_ OVERLAPPED anzugeben, wird *lpOverlapped* ignoriert, und die [**DeviceIoControl-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) wird erst zurückgegeben, nachdem der Vorgang abgeschlossen wurde oder bis ein Fehler auftritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wurde, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.

Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 0 (null) zurück. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Alle Anforderungen zum Festlegen von Akkuinformationen werden mit dem Status \_ FEHLERDATEI \_ NICHT GEFUNDEN \_ abgeschlossen, wenn das Akkutag der Anforderung nicht mit dem des aktuellen Akkutags übereinstimmt.

Informationen zu den Auswirkungen überlappender E/A-Vorgänge auf diesen Vorgang finden Sie im Abschnitt "Hinweise" des Themas [**DeviceIoControl.**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                                                                                                                                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h auf Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Akkuinformationen](battery-information.md)
</dt> <dt>

[Steuerungscodes für die Energieverwaltung](power-management-control-codes.md)
</dt> <dt>

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**\_INFORMATIONEN ZUM AKKUSATZ \_**](battery-set-information-str.md)
</dt> <dt>

[**IOCTL \_ BATTERY \_ QUERY \_ INFORMATION**](ioctl-battery-query-information.md)
</dt> <dt>

[**IOCTL \_ BATTERY \_ QUERY \_ STATUS**](ioctl-battery-query-status.md)
</dt> <dt>

[**IOCTL \_ BATTERY \_ QUERY \_ TAG**](ioctl-battery-query-tag.md)
</dt> </dl>

 

