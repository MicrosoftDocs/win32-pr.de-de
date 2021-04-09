---
description: Legt verschiedene Akku Informationen fest.
ms.assetid: b827983d-5fb8-43f2-b732-541d16b3eb7b
title: IOCTL_BATTERY_SET_INFORMATION Steuerungs Code (poclass. h)
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
ms.openlocfilehash: f540037486f16e920b3346620ff934b279652e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865080"
---
# <a name="ioctl_battery_set_information-control-code"></a>Code der IOCTL- \_ Akku \_ Satz- \_ Informations Steuerung

Legt verschiedene Akku Informationen fest. Die Eingabeparameter Struktur, [**Batterie \_ Satz \_ Informationen**](battery-set-information-str.md), gibt an, welche Akku Statusinformationen festgelegt werden sollen.

Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.


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

*hdevice* 
</dt> <dd>

Ein Handle für den Akku, auf dem die Informationen festgelegt werden sollen. Rufen Sie zum Abrufen eines Geräte [**Handles die Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Der Steuerelement Code für den Vorgang. Dieser Wert identifiziert den spezifischen Vorgang, der ausgeführt werden soll, und den Typ des Geräts, auf dem es ausgeführt werden soll. Verwenden Sie die **IOCTL- \_ Akku \_ Satz \_ Informationen** für diesen Vorgang.

</dd> <dt>

*lpinbuffer* 
</dt> <dd>

Ein Zeiger auf eine [**Batterie \_ Satz \_ Informations**](battery-set-information-str.md) Struktur.

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Die Größe des Eingabe Puffers in Bytes.

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

Ein Zeiger auf eine Variable, die die Größe der im *lpoutbuffer* -Puffer zurückgegebenen Daten (in Bytes) empfängt.

Wenn der Ausgabepuffer zu klein ist, um Daten zurückzugeben, schlägt der-Befehl fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehlercode Fehler \_ unzureichend zurück \_ , und die zurückgegebene Byte Anzahl ist 0 (null).

Wenn *lpoverllapp* den Wert **null** hat (nicht überlappende e/a), kann *lpbytesgab* nicht **null** sein, auch wenn *lpoutbuffer* **null** ist.

Wenn *lpoverllapp* nicht **null** (überlappende e/a) ist, kann *lpbytesgab* **null** sein. Wenn dies ein überlappende Vorgang ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie die [**GetOverLappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) -Funktion aufrufen. Wenn *hdevice* einem e/a-Abschlussport zugeordnet ist, können Sie die Anzahl der Bytes abrufen, die durch Aufrufen der [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion zurückgegeben werden.

</dd> <dt>

*lpoverlgetauscht* 
</dt> <dd>

Ein Zeiger auf eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.

Wenn *hdevice* mit dem überlappenden \_ Flag für das Dateiflag geöffnet wurde \_ , muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur zeigen. In diesem Fall wird [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) als überlappende (asynchrone) Operation ausgeführt. Wenn das Gerät mit dem überlappenden \_ Flag für das Dateiflag geöffnet wurde \_ und *lpoverlgetauscht* den Wert **null** hat, schlägt die Funktion auf unvorhersehbare Weise fehl.

Wenn *hdevice* ohne Angabe des überlappenden \_ Flag für das Dateiflag geöffnet wurde \_ , wird *lpoverlgetauscht* ignoriert, und die [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) -Funktion gibt nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.

Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Alle Anforderungen zum Festlegen der Akku Informationen werden mit dem Status "Fehler \_ Datei \_ nicht \_ gefunden", wenn das Akku-Tag der Anforderung nicht mit der des aktuellen Akku-Tags identisch ist, vervollständigt.

Informationen zu den Auswirkungen von überlappenden e/a-Vorgängen für diesen Vorgang finden Sie im Abschnitt "Hinweise" des Themas " [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                                                                                                                                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Akku Informationen](battery-information.md)
</dt> <dt>

[Steuerungs Codes der Energie Verwaltung](power-management-control-codes.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**Informationen zum Akku \_ Satz \_**](battery-set-information-str.md)
</dt> <dt>

[**IOCTL- \_ Akku \_ Abfrage \_ Informationen**](ioctl-battery-query-information.md)
</dt> <dt>

[**IOCTL \_ Akku \_ Query- \_ Status**](ioctl-battery-query-status.md)
</dt> <dt>

[**IOCTL \_ Akku \_ - \_ abfragetag**](ioctl-battery-query-tag.md)
</dt> </dl>

 

