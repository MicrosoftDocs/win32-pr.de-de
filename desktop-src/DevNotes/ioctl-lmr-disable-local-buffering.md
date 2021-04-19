---
description: Der IOCTL \_ LMR \_ \_ \_ -Code zum Deaktivieren der lokalen Puffer Steuerung deaktiviert das lokale Zwischenspeichern von Daten beim Lesen von Daten aus oder Schreiben von Daten in eine Remote Datei. Dabei handelt es sich um einen intern definierten Steuerungs Code, der in einem öffentlichen Header nicht verfügbar ist.
ms.assetid: a464671b-253c-4f35-84a2-2619cb15b009
title: IOCTL_LMR_DISABLE_LOCAL_BUFFERING Steuerungs Codes
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
ms.openlocfilehash: 0d596402c489caee972e1305f2a32881312fd3e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342972"
---
# <a name="ioctl_lmr_disable_local_buffering-control-code"></a>IOCTL \_ LMR \_ deaktiviert \_ den Code für die lokale \_ Puffer Steuerung.

Der **IOCTL \_ LMR-Code zum \_ Deaktivieren der \_ lokalen \_ Puffer** Steuerung deaktiviert das lokale Zwischenspeichern von Daten beim Lesen von Daten aus oder Schreiben von Daten in eine Remote Datei. Dabei handelt es sich um einen intern definierten Steuerungs Code, der in einem öffentlichen Header nicht verfügbar ist.

Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.


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

*hdevice* \[ in\]
</dt> <dd>

Ein Handle für die Remote Datei. Um dieses Handle zu erhalten, rufen [**Sie die Funktion**](/windows/win32/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.

</dd> <dt>

*dwIoControlCode* \[ in\]
</dt> <dd>

Der Steuerelement Code für den Vorgang. Verwenden Sie für diesen Vorgang den Wert 0x140390.

</dd> <dt>

*lpinbuffer* 
</dt> <dd>

Nicht verwendet, muss **null** sein.

</dd> <dt>

*nInBufferSize* \[ in\]
</dt> <dd>

Die Größe des Eingabe Puffers in Bytes. Muss Null sein.

</dd> <dt>

*lpoutbuffer* \[ vorgenommen\]
</dt> <dd>

Nicht verwendet, muss **null** sein.

</dd> <dt>

*nOutBufferSize* \[ in\]
</dt> <dd>

Die Größe des Ausgabepuffers in Bytes. Muss Null sein.

</dd> <dt>

*lpbyteszurück gegeben* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.

Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, die [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion gibt einen **fehlerhaften \_ \_ Puffer** zurück, und *lpbytesreturns* ist 0 (null).

Wenn der *lpoverllapp* -Parameter **null** ist, kann *lpbytes-Rückgabe* Wert nicht **null** sein. Selbst wenn ein Vorgang keine Ausgabedaten zurückgibt und der *lpoutbuffer* -Parameter den Wert **null** hat, verwendet [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) *lpbytesreturn*. Nach einem solchen Vorgang ist der Wert von *lpbytesno* bedeutungslos.

Wenn *lpoverllapp* nicht **null** ist, kann *lpbytesgab* **null** sein. Wenn *lpoverlgetauscht* nicht **null** ist und der Vorgang Daten zurückgibt, ist *lpbytesreturns* bedeutungslos, bis der überlappende Vorgang abgeschlossen ist. Um die Anzahl der zurückgegebenen Bytes abzurufen, rufen Sie die Funktion [**ge-verlappedresult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) auf. Wenn der *hdevice* -Parameter einem e/a-Abschlussport zugeordnet ist, können Sie die Anzahl der zurückgegebenen Bytes abrufen, indem Sie die [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion aufrufen.

</dd> <dt>

*lpoverlgetauscht* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur.

Wenn der *hdevice* -Parameter ohne Angabe eines **überlappenden \_ Dateiflags \_** geöffnet wurde, wird *lpoverlgetauscht* ignoriert.

Wenn *hdevice* mit dem überlappenden Flag für das **\_ \_ Dateiflag** geöffnet wurde, wird der Vorgang als überlappende (asynchrone) Vorgang ausgeführt. In diesem Fall muss *lpoverlgetauscht* auf eine gültige [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur verweisen, die ein Handle für ein Ereignis Objekt enthält. Andernfalls schlägt die Funktion auf unvorhersehbare Weise fehl.

Bei überlappenden Vorgängen gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) sofort zurück, und das Ereignis Objekt wird signalisiert, wenn der Vorgang abgeschlossen wurde. Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) einen Wert ungleich 0 (null) zurück.

Wenn der Vorgang fehlschlägt oder aussteht, gibt [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) den Wert 0 (null) zurück. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Der **ioctl LMR-Code für die \_ \_ \_ lokale \_ Puffer Aktivierung** wird intern vom System als 0x140390 und nicht in einer öffentlichen Header Datei definiert. Sie wird von Anwendungen für zweckgebundene Anwendungen verwendet, um das Client seitige Zwischenspeichern von Daten beim Lesen von Daten aus oder das Schreiben von Daten in eine Remote Datei zu deaktivieren. Nach der Deaktivierung der lokalen Pufferung bleibt die Einstellung wirksam, bis alle geöffneten Handles für die Datei geschlossen sind und der Redirector die internen Datenstrukturen bereinigt.

Anwendungen für allgemeine Zwecke sollten nicht **IOCTL \_ LMR \_ Deaktivieren \_ lokale \_ Pufferung** verwenden, da dies zu einem übermäßigen Netzwerkverkehr und einem zugehörigen Leistungsverlust führen kann. Der **ioctl-LMR-Code für die \_ \_ \_ lokale \_ Puffer Aktivierung** sollte nur in spezialisierten Anwendungen verwendet werden, die große Datenmengen über das Netzwerk verschieben, während versucht wird, die Nutzung der Netzwerkbandbreite zu maximieren. Die Funktionen [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) und [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) verwenden z. b. **IOCTL \_ LMR \_ \_ \_** , um die Leistung großer Datei Kopien zu verbessern.

**IOCTL \_ LMR- \_ Deaktivierung der \_ lokalen \_ Pufferung** wird nicht von lokalen Dateisystemen implementiert, und die Fehlermeldung " **\_ ungültige \_ Funktion**" schlägt fehl. Bei der Ausgabe von **ioctl LMR wird der Code für die \_ \_ \_ lokale \_ Puffer** Steuerung nicht auf Remote Verzeichnis Handles festgelegt, und die Fehlermeldung wird **\_ nicht \_ unterstützt**.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
