---
description: Ruft das aktuelle Akku-Tag ab.
ms.assetid: 0bbe59ba-e037-47ce-a54a-6500ea7c9bc5
title: IOCTL_BATTERY_QUERY_TAG Steuerungs Code (poclass. h)
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
ms.openlocfilehash: 1d8435e62c4f061ac13b3e18e5bcd64afcb399c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349411"
---
# <a name="ioctl_battery_query_tag-control-code"></a>IOCTL \_ Akku \_ Query \_ Tag Control Code

Ruft das aktuelle Tag des Akkus ab.

Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.


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

*hdevice* 
</dt> <dd>

Ein Handle für den Akku, von dem das Tag abgerufen werden soll. Rufen Sie zum Abrufen eines Geräte [**Handles die Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Der Steuerelement Code für den Vorgang. Dieser Wert identifiziert den spezifischen Vorgang, der ausgeführt werden soll, und den Typ des Geräts, auf dem es ausgeführt werden soll. Verwenden Sie für diesen Vorgang das **IOCTL \_ Akku- \_ abfragetag \_** .

</dd> <dt>

*lpinbuffer* 
</dt> <dd>

Ein Zeiger auf einen **ulong** -Eingabepuffer. Der Wert gibt an, wie viele Millisekunden gewartet werden soll, wenn kein Akku vorhanden ist. Der Wert-1 gibt an, dass die Anforderung unbegrenzt wartet (oder von einem anderen Ereignis abgebrochen wird).

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Die Größe des Eingabe Puffers in Bytes.

</dd> <dt>

*lpoutbuffer* 
</dt> <dd>

Ein Zeiger auf einen **ulong** -Ausgabepuffer. Bei Erfolg enthält dieser Puffer das aktuelle Akku Kennzeichen, bei dem es sich um einen beliebigen Wert mit Ausnahme eines \_ ungültigen Akku Tags handelt \_ . Wenn [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) bei einem Fehler die Fehlercode- **Fehler \_ Datei \_ nicht \_ gefunden** zurückgibt, enthält dieser Puffer den Wert des **Akku \_ Tags \_ ungültig**.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Die Größe des Ausgabepuffers in Bytes.

</dd> <dt>

*lpbyteszurück gegeben* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der im *lpoutbuffer* -Puffer gespeicherten Daten in Bytes empfängt.

Wenn der Ausgabepuffer zu klein ist, um Daten zurückzugeben, dann schlägt der-Befehl fehl, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den Fehlercode **Fehler \_ unzureichend \_** zurück, und die zurückgegebene Byte Anzahl ist 0 (null).

Wenn *lpoverllapp* den Wert **null** hat (nicht überlappende e/a), kann *lpbytesgab* nicht **null** sein.

Wenn *lpoverllapp* nicht **null** (überlappende e/a) ist, kann *lpbytesgab* **null** sein. Wenn dies ein überlappende Vorgang ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie die [**GetOverLappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) -Funktion aufrufen. Wenn *hdevice* einem e/a-Abschlussport zugeordnet ist, können Sie die Anzahl der Bytes abrufen, die durch Aufrufen der [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion zurückgegeben werden.

</dd> <dt>

*lpoverlgetauscht* 
</dt> <dd>

Ein Zeiger auf eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.

Wenn *hdevice* mit dem überlappenden Flag für das **\_ \_ Dateiflag** geöffnet wurde, muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur zeigen. In diesem Fall wird [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) als überlappende (asynchrone) Operation ausgeführt. Wenn das Gerät mit dem überlappenden Flag für das **\_ Dateiflag \_** geöffnet wurde und *lpoverlgetauscht* den Wert **null** hat, schlägt die Funktion auf unvorhersehbare Weise fehl.

Wenn *hdevice* ohne Angabe des überlappenden Flag für das **\_ \_ Dateiflag** geöffnet wurde, wird *lpoverlgetauscht* ignoriert, und die [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) -Funktion gibt nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.

Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Mit diesem Akku-IOCTL wird das aktuelle Tag des Akkus abgerufen. Das Akku-Tag ist ein eindeutiger Wert ungleich 0 (null), der sich ändert, wenn die physische Batterie wieder hergestellt, ersetzt oder geändert wird. Weitere Informationen zum Zeitpunkt der Änderung eines Akku Tags, zum Erkennen der Änderung und zum Fortsetzen einer Anwendung nach der Änderung eines Akku Tags finden Sie im Abschnitt "Akku-Tags" im Thema "Übersicht über [Akku Informationen](battery-information.md) ". Wenn kein Akku vorhanden ist, wartet diese Anforderung die festgelegte Zeit, und wenn noch kein Akku vorhanden ist, wird die **Fehler \_ Datei \_ nicht \_ gefunden** , und das Akku-Tag wird auf **\_ \_ ungültig** festgelegt. (Weitere Informationen finden Sie in den Akku Informationen.)

Alle Anforderungen für andere Akku Informationen erfordern, dass der Aufrufer das passende Akku Kennzeichen bereitstellt. Dadurch wird sichergestellt, dass der Aufrufer für jede Anforderung Informationen für den gleichen Akku empfängt und sicherstellt, dass der Aufrufer die Akku Änderungen ohne konstantenabruf kennt.

Informationen zu den Auswirkungen von überlappenden e/a-Vorgängen für diesen Vorgang finden Sie im Abschnitt "Hinweise" des Themas " [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ".

## <a name="examples"></a>Beispiele

Ein Beispiel finden Sie unter Auflisten von [Akku Geräten](enumerating-battery-devices.md).

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

[**IOCTL- \_ Akku \_ Abfrage \_ Informationen**](ioctl-battery-query-information.md)
</dt> <dt>

[**IOCTL \_ Akku \_ Query- \_ Status**](ioctl-battery-query-status.md)
</dt> <dt>

[**IOCTL- \_ Akku \_ Satz \_ Informationen**](ioctl-battery-set-information.md)
</dt> </dl>

 

