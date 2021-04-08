---
description: Ruft eine Vielzahl von Informationen für den Akku ab.
ms.assetid: 4cc89b89-ab33-47c2-8327-9627cbd1595e
title: IOCTL_BATTERY_QUERY_INFORMATION Steuerungs Code (poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: ee4010e055686c0df2987c34b48b133975b434ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959743"
---
# <a name="ioctl_battery_query_information-control-code"></a>Steuerungs Code der IOCTL- \_ Akku \_ Abfrage \_ Informationen

Ruft eine Vielzahl von Informationen für den Akku ab.

Um diesen Vorgang auszuführen, müssen Sie die Funktion [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern abrufen.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to battery
  IOCTL_BATTERY_QUERY_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,             // input buffer
  (DWORD) nInBufferSize,           // size of input buffer
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* 
</dt> <dd>

Ein Handle für den Akku, auf dem Informationen zurückgegeben werden sollen. Rufen Sie zum Abrufen eines Geräte [**Handles die Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "-Funktion" auf.

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Der Steuerelement Code für den Vorgang. Dieser Wert identifiziert den spezifischen Vorgang, der ausgeführt werden soll, und den Typ des Geräts, auf dem es ausgeführt werden soll. Verwenden Sie für diesen Vorgang **IOCTL- \_ Akku \_ Abfrage \_ Informationen** .

</dd> <dt>

*lpinbuffer* 
</dt> <dd>

Ein Zeiger auf eine [**Akku \_ Abfrage \_ Informations**](battery-query-information-str.md) Struktur.

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Die Größe des Eingabe Puffers in Bytes.

</dd> <dt>

*lpoutbuffer* 
</dt> <dd>

Ein Zeiger auf den Rückgabe Puffer. Der Datentyp (und somit die Größe) des Rückgabe Puffers hängt von den Informationen ab, die in der **Akku \_ Abfrage Informations \_ \_ Ebene** der Eingabe- [**Akku- \_ Abfrage \_ Informations**](battery-query-information-str.md) Struktur angefordert werden.

In der folgenden Tabelle werden die von einer bestimmten Informationsebene zurückgegebenen Daten angezeigt.



| Informationsebene                 | Zurückgegebene Daten                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Batterydevicename**             | Eine mit **null** beendete Unicode-Zeichenfolge, die den Namen des Akkus angibt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Batteryestimatedtime**          | Ein **ulong** -Wert, der die geschätzte Akkulaufzeit in Sekunden angibt. Wenn die für das **atrate** -Element der Struktur der [**Akku \_ Abfrage \_ Informationen**](battery-query-information-str.md) angegebene Ausgleichs Rate 0 (null) ist, basiert diese Berechnung auf der aktuellen Rate des Ausgleichs. Wenn **atate** ungleich NULL ist, ist die zurückgegebene Zeit die erwartete Laufzeit für die angegebene Rate. Wenn die geschätzte Zeit unbekannt ist (z. b. wenn der Akku nicht entladen wird und **atate** NULL ist), wird die **\_ unbekannte Akku \_ Zeit** zurückgegeben. Beachten Sie, dass dieser Wert für einige Akku Systeme nicht sehr genau ist. Der Wert kann abhängig von der aktuellen Stromversorgung, die von der Datenträger Aktivität und anderen Faktoren betroffen sein könnte, stark variieren. Es gibt keinen Benachrichtigungs Mechanismus für Änderungen dieses Werts. |
| **Batterygranularityinformation** | Ein Array variabler Länge mit [**Akku \_ Berichterstattungs- \_ Skalierungs**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) Strukturen, das die Granularität der Berichterstellung für die Akkukapazität enthält, die vom [**IOCTL- \_ Akku \_ Abfrage \_ Status**](ioctl-battery-query-status.md)zurückgegeben wird. Wenn die Granularität von der aktuellen Kapazität des Akkus abhängt, werden mehrere Einträge zurückgegeben. Die Interpretation des Arrays von Einträgen finden Sie unter **Akku \_ Bericht \_** Erstellung. Die Anzahl der Einträge wird durch die Größe des zurückgegebenen Puffers angegeben und kann als (*lpbytesgab* /sizeof (**Akku \_ Berichterstattungs \_ Skala**)) berechnet werden. Die maximale Anzahl von Einträgen, die zurückgegeben werden, ist vier.                                                                                                |
| **Akku Informationen**            | Eine [**Akku \_ Informations**](battery-information-str.md) Struktur.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Batterymanufacturedate**        | Eine [**Akku \_ Herstellungs \_ Datums**](battery-manufacture-date-str.md) Struktur.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Batterymanufacturename**        | Eine auf **null** endenden Unicode-Zeichenfolge, die den Namen des Herstellers des Akkus enthält.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Akku serialNumber**           | Eine mit **null** beendete Unicode-Zeichenfolge, die die Seriennummer des Akkus enthält.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Akku Temperatur**            | Ein **ulong** -Wert, der die aktuelle Temperatur des Akkus in Zehntel Grad Kelvin enthält.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Batteryuniqueid**               | Eine mit **null** beendete Unicode-Zeichenfolge, die den Akku eindeutig identifiziert. Dieser Wert kann verwendet werden, um einen bestimmten Akku zu verfolgen. Im Fall von intelligenten Akkus ist diese ID die Verkettung aus dem Namen des Herstellers, dem Gerätenamen, dem Erstellungsdatum und der druckbaren Darstellung der Seriennummer. Dieser Wert sollte nicht für den Benutzer angezeigt werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Die Größe des Ausgabepuffers in Bytes. Abhängig von der Informationsebene der angeforderten Daten kann dies ein Puffer mit variabler Größe sein.

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

Einige Informationen zu Akkus sind optional oder für einige Akkus bedeutungslos. Wenn der jeweilige angeforderte Datentyp für den aktuellen Akku nicht verfügbar ist, wird **die \_ Fehler \_ Funktion "ungültig** " zurückgegeben.

Alle Anforderungen für Akku Informationen werden mit dem Status der **Fehler \_ Datei \_ nicht \_ gefunden** , wenn das Element " **batterytag** " der Anforderung nicht mit der des aktuellen Akku Tags identisch ist. Dadurch wird sichergestellt, dass die zurückgegebenen Akku Informationen mit denen des angeforderten Akkus übereinstimmen. (Weitere Informationen finden Sie unter [Akku-Tags](battery-information.md) .)

## <a name="remarks"></a>Bemerkungen

Diese Akku-ioctl Ruft eine Vielzahl von Informationen für den Akku ab. Die Eingabeparameter Struktur, die [**Akku \_ Abfrage \_ Informationen**](battery-query-information-str.md), gibt den Typ der Informationen an, die zurückgegeben werden sollen, und wann die Akku Informationen zurückgegeben werden sollen. Der Datentyp und der Inhalt des Ausgabepuffers variieren basierend auf den angeforderten Daten.

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

[**Akku \_ Abfrage \_ Informationen**](battery-query-information-str.md)
</dt> <dt>

[**\_Skalierung von Akku Berichten \_**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[**IOCTL \_ Akku \_ Query- \_ Status**](ioctl-battery-query-status.md)
</dt> <dt>

[**IOCTL \_ Akku \_ - \_ abfragetag**](ioctl-battery-query-tag.md)
</dt> <dt>

[**IOCTL- \_ Akku \_ Satz \_ Informationen**](ioctl-battery-set-information.md)
</dt> </dl>

 

