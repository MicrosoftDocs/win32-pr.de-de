---
description: Ruft das Akku-Stromtag ab.
ms.assetid: 0bbe59ba-e037-47ce-a54a-6500ea7c9bc5
title: IOCTL_BATTERY_QUERY_TAG -Steuerelementcode (Poclass.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_TAG
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: c68c9dc2385803155a6c0f8fd2a5b7c84cedaa8e78c98ae2baca6909104e7315
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143513"
---
# <a name="ioctl_battery_query_tag-control-code"></a>IOCTL \_ BATTERY \_ QUERY \_ TAG-Steuerungscode

Ruft das aktuelle Tag des Akkus ab.

Um diesen Vorgang durchzuführen, rufen Sie die [**Funktion DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern auf.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to battery
  IOCTL_BATTERY_QUERY_TAG,     // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of input buffer
  (LPVOID) lpOutBuffer,        // output buffer
  (DWORD) nOutBufferSize,      // size of output buffer
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped);// OVERLAPPED structure
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDevice* 
</dt> <dd>

Ein Handle für den Akku, aus dem das Tag abgerufen werden soll. Um ein Gerätehand handle abzurufen, rufen Sie die [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) auf.

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Der Steuerungscode für den Vorgang. Dieser Wert gibt den spezifischen Vorgang an, der ausgeführt werden soll, und den Typ des Geräts, auf dem er ausgeführt werden soll. Verwenden **Sie IOCTL \_ BATTERY QUERY \_ \_ TAG** für diesen Vorgang.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Ein Zeiger auf einen **ULONG-Eingabepuffer.** Der Wert gibt die Anzahl der Millisekunden an, die gewartet werden soll, wenn kein Akku vor sich geht. Der Wert -1 gibt an, dass die Anforderung unbegrenzt wartet (oder bis sie von einem anderen Ereignis abgebrochen wird).

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Die Größe des Eingabepuffers in Bytes.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Ein Zeiger auf einen **ULONG-Ausgabepuffer.** Bei Erfolg enthält dieser Puffer das aktuelle Akkutag, das einen beliebigen Wert außer BATTERY \_ TAG INVALID haben \_ kann. Wenn [**getLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) bei einem Fehler den Fehlercode **ERROR FILE \_ NOT \_ \_ FOUND** zurückgibt, enthält dieser Puffer den Wert **BATTERY TAG \_ \_ INVALID**.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Die Größe des Ausgabepuffers in Bytes.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der im *lpOutBuffer-Puffer* gespeicherten Daten in Bytes empfängt.

Wenn der Ausgabepuffer zu klein ist, um Daten zurückgibt, schlägt der Aufruf fehl. [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehlercode **ERROR INSUFFICIENT \_ \_ BUFFER** zurück, und die zurückgegebene Byteanzahl ist 0 (null).

Wenn *lpOverlapped* **NULL** ist (nicht übersprungene E/A), *kann lpBytesReturned* nicht **NULL sein.**

Wenn *lpOverlapped* nicht **NULL** (überlappende E/A) ist, *kann lpBytesReturned* **NULL sein.** Wenn es sich um einen überlappenden Vorgang handelt, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie die [**GetOverlappedResult-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) aufrufen. Wenn *hDevice einem* E/A-Abschlussport zugeordnet ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie die [**GetQueuedCompletionStatus-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) aufrufen.

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Ein Zeiger auf eine [**OVERLAPPED-Struktur.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

Wenn *hDevice mit* dem **FLAG FILE FLAG \_ \_ OVERLAPPED** geöffnet wurde, *muss lpOverlapped* auf eine gültige [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) verweisen. In diesem Fall wird [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) als überlappende (asynchrone) Operation ausgeführt. Wenn das Gerät mit dem **FLAG FILE \_ FLAG \_ OVERLAPPED** geöffnet wurde und *lpOverlapped* **NULL** ist, schlägt die Funktion auf unvorhersehbare Weise fehl.

Wenn *hDevice* geöffnet wurde, ohne das **FLAG FILE FLAG \_ \_ OVERLAPPED** anzugeben, wird *lpOverlapped* ignoriert, und die [**DeviceIoControl-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) gibt erst dann zurück, wenn der Vorgang abgeschlossen ist oder ein Fehler auftritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wurde, [**gibt DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.

Wenn der Vorgang fehlschlägt oder aussteht, [**gibt DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 0 (null) zurück. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Diese Akku-IOCTL ruft das aktuelle Tag des Akkus ab. Das Akkutag ist ein eindeutiger Wert ungleich 0 (null), der sich ändert, wenn der physische Akku erneut ein- oder ausgetauscht wird oder sich merkliche Änderungen durchläuft. Im Abschnitt Akkutags [](battery-information.md) des Themas Übersicht über Akkuinformationen finden Sie weitere Informationen dazu, wann sich ein Akkutag ändert, wie die Änderung erkannt wird und wie eine Anwendung nach einer Änderung des Akkutags fortgesetzt werden sollte. Wenn kein Akku vorhanden ist, wartet diese Anforderung die angegebene Zeit, und wenn immer noch kein Akku vorhanden ist, wird DIE FEHLERDATEI **\_ NICHT \_ \_ GEFUNDEN** zurückgegeben, und das Akkutag wird auf **BATTERY TAG \_ \_ INVALID** festgelegt. (Weitere Informationen finden Sie unter Akkuinformationen.)

Alle Anforderungen für andere Akkuinformationen erfordern, dass der Aufrufer das entsprechende Akkutag anpasst. Dadurch wird sichergestellt, dass der Aufrufer für jede Anforderung Informationen für denselben Akku empfängt, und stellt sicher, dass der Aufrufer Akkuänderungen ohne konstante Abrufe kennt.

Informationen zu den Auswirkungen von überlappenden E/A-Daten auf diesen Vorgang finden Sie im Abschnitt "Hinweise" des [**Themas DeviceIoControl.**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)

## <a name="examples"></a>Beispiele

Ein Beispiel finden Sie unter [Aufzählen von Akkugeräten.](enumerating-battery-devices.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                                                                                                                                                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>BatClass.h auf Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003</dt> und Windows XP </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Akkuinformationen](battery-information.md)
</dt> <dt>

[Energieverwaltungs-Steuerungscodes](power-management-control-codes.md)
</dt> <dt>

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**IOCTL \_ BATTERY \_ QUERY \_ INFORMATION**](ioctl-battery-query-information.md)
</dt> <dt>

[**IOCTL \_ BATTERY \_ QUERY \_ STATUS**](ioctl-battery-query-status.md)
</dt> <dt>

[**\_IOCTL-AKKUSATZINFORMATIONEN \_ \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

