---
description: Ruft den aktuellen Status des Akkus ab.
ms.assetid: 7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df
title: IOCTL_BATTERY_QUERY_STATUS Steuerungs Code (poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: e2de9d3ab48aec13a9a5c1957a5f98aefbe6a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348609"
---
# <a name="ioctl_battery_query_status-control-code"></a>IOCTL \_ Akku \_ Query- \_ Status Steuerungs Code

Ruft den aktuellen Status des Akkus ab.

Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,           // handle to battery
  IOCTL_BATTERY_QUERY_STATUS, // dwIoControlCode
  (LPVOID) lpInBuffer,        // input buffer
  (DWORD) nInBufferSize,      // size of input buffer
  (LPVOID) lpOutBuffer,       // output buffer
  (DWORD) nOutBufferSize,     // size of output buffer
  (LPDWORD) lpBytesReturned,  // number of bytes returned
  (LPOVERLAPPED) lpOverlapped // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* 
</dt> <dd>

Ein Handle für den Akku, von dem Informationen zurückgegeben werden sollen. Rufen Sie zum Abrufen eines Geräte [**Handles die Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Der Steuerelement Code für den Vorgang. Dieser Wert identifiziert den spezifischen Vorgang, der ausgeführt werden soll, und den Typ des Geräts, auf dem es ausgeführt werden soll. Verwenden Sie den **IOCTL- \_ Akku \_ Abfrage \_ Status** für diesen Vorgang.

</dd> <dt>

*lpinbuffer* 
</dt> <dd>

Ein Zeiger auf die [**\_ \_ Status Struktur der Akku Wartezeit**](battery-wait-status-str.md) .

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Die Größe des Eingabe Puffers in Bytes.

</dd> <dt>

*lpoutbuffer* 
</dt> <dd>

Ein Zeiger auf eine [**Akku \_ Status**](battery-status-str.md) Struktur.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Die Größe des Ausgabepuffers in Bytes.

</dd> <dt>

*lpbyteszurück gegeben* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der im *lpoutbuffer* -Puffer zurückgegebenen Daten (in Bytes) empfängt.

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

Diese Akku-ioctl Ruft den Status des Akkus zu dem Zeitpunkt ab, an dem der Vorgang zurückgegeben wird. Die Eingabeparameter Struktur, [**der \_ \_ Status der Akku Wartezeit**](battery-wait-status-str.md), gibt an, wann der Akku Status verarbeitet und zurückgegeben werden soll.

Anforderungen für den Akku Status können für die sofortige Rückgabe oder für das warten auf eine bestimmte Bedingung vor dem Abschlussfest gelegt werden. Beispielsweise kann eine Anforderung für Akku Informationen erfolgen, die warten, bis die Akkukapazität einen bestimmten Punkt erreicht oder sich der Akku Zustand ändert.

Alle Anforderungen für Akku Informationen werden mit dem Status der **Fehler \_ Datei \_ nicht \_ gefunden** , wenn das Element " **batterytag** " der Anforderung nicht mit der des aktuellen Akku Tags identisch ist. (Weitere Informationen finden Sie unter [Akku-Tags](battery-information.md) .) Hiermit wird sichergestellt, dass die zurückgegebenen Akku Informationen mit denen des angeforderten Akkus übereinstimmen.

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

[**Akku \_ Status**](battery-status-str.md)
</dt> <dt>

[**Status der Akku \_ Wartezeit \_**](battery-wait-status-str.md)
</dt> <dt>

[**IOCTL- \_ Akku \_ Abfrage \_ Informationen**](ioctl-battery-query-information.md)
</dt> <dt>

[**IOCTL \_ Akku \_ - \_ abfragetag**](ioctl-battery-query-tag.md)
</dt> <dt>

[**IOCTL- \_ Akku \_ Satz \_ Informationen**](ioctl-battery-set-information.md)
</dt> </dl>

 

