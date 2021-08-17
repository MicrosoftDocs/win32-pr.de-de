---
description: Ruft eine Vielzahl von Informationen für den Akku ab.
ms.assetid: 4cc89b89-ab33-47c2-8327-9627cbd1595e
title: IOCTL_BATTERY_QUERY_INFORMATION -Steuerelementcode (Poclass.h)
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
ms.openlocfilehash: a48514b81ddf5d8f7c0d84d4404eb01752413e73ade43db089fbb6dade673bc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143532"
---
# <a name="ioctl_battery_query_information-control-code"></a>IOCTL \_ BATTERY \_ QUERY \_ INFORMATION-Steuerungscode

Ruft eine Vielzahl von Informationen für den Akku ab.

Um diesen Vorgang durchzuführen, rufen Sie die [**Funktion DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) mit den folgenden Parametern auf.


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

*hDevice* 
</dt> <dd>

Ein Handle für den Akku, über den Informationen zurückgegeben werden sollen. Um ein Gerätehand handle abzurufen, rufen Sie die [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) auf.

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Der Steuerungscode für den Vorgang. Dieser Wert gibt den spezifischen Vorgang an, der ausgeführt werden soll, und den Typ des Geräts, auf dem er ausgeführt werden soll. Verwenden **Sie IOCTL \_ BATTERY QUERY \_ \_ INFORMATION** für diesen Vorgang.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Ein Zeiger auf eine [**BATTERY \_ QUERY \_ INFORMATION-Struktur.**](battery-query-information-str.md)

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Die Größe des Eingabepuffers in Bytes.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Ein Zeiger auf den Rückgabepuffer. Der Datentyp (und somit die Größe) des Rückgabepuffers hängt von den Informationen ab, die im **BATTERY \_ QUERY INFORMATION \_ \_ LEVEL-Member** der [**INPUT BATTERY QUERY \_ \_ INFORMATION-Struktur angefordert**](battery-query-information-str.md) werden.

Die folgende Tabelle zeigt die Von einer bestimmten Informationsebene zurückgegebenen Daten.



| Informationsebene                 | Zurückgegebene Daten                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **BatteryDeviceName**             | **Mit NULL** beendete Unicode-Zeichenfolge, die den Namen des Akkus angibt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **BatteryEstimatedTime**          | Ein **ULONG-Wert,** der die geschätzte Akkulaufzeit in Sekunden angibt. Wenn die im **AtRate-Member** der [**BATTERY \_ QUERY \_ INFORMATION-Struktur**](battery-query-information-str.md) bereitgestellte Entleerungsrate null ist, basiert diese Berechnung auf der aktuellen Entleerungsrate. Wenn **AtRate** ungleich 0 (null) ist, ist die zurückgegebene Zeit die erwartete Laufzeit für die gegebene Rate. Wenn die geschätzte Zeit unbekannt ist (z. B. wird der Akku nicht entladen, und **AtRate** ist 0 (null) ), **wird BATTERY UNKNOWN \_ \_ TIME** zurückgegeben. Beachten Sie, dass dieser Wert bei einigen Akkusystemen nicht sehr genau ist. Der Wert kann je nach aktuellem Energieverbrauch stark variieren, was von der Datenträgeraktivität und anderen Faktoren beeinflusst werden kann. Es gibt keinen Benachrichtigungsmechanismus für Änderungen an diesem Wert. |
| **BatteryGranularityInformation** | Ein Array variabler Länge von [**BATTERY \_ REPORTING \_ SCALE-Strukturen,**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) das die Berichtgranularität für die Akkukapazität enthält, die von [**IOCTL \_ BATTERY QUERY STATUS zurückgegeben \_ \_ wird.**](ioctl-battery-query-status.md) Mehrere Einträge werden zurückgegeben, wenn die Granularität von der aktuellen Kapazität des Akkus abhängt. Informationen zur Interpretation des Arrays von Einträgen finden Sie unter **BATTERY \_ REPORTING \_ SCALE.** Die Anzahl der Einträge wird durch die Größe des zurückgegebenen Puffers angegeben und kann als (*lpBytesReturned* /sizeof (**BATTERY REPORTING \_ \_ SCALE**)) berechnet werden. Die maximale Anzahl von Einträgen, die zurückgegeben werden, beträgt vier.                                                                                                |
| **BatteryInformation**            | Eine [**BATTERY \_ INFORMATION-Struktur.**](battery-information-str.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **BatteryManufactureDate**        | Eine [**BATTERY \_ MANUFACTURE \_ DATE-Struktur.**](battery-manufacture-date-str.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **BatteryManufactureName**        | **Mit NULL** beendete Unicode-Zeichenfolge, die den Namen des Herstellers des Akkus enthält.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **BatterySerialNumber**           | **Mit NULL** beendete Unicode-Zeichenfolge, die die Seriennummer des Akkus enthält.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **BatteryTemperature**            | Ein **ULONG,** das die aktuelle Temperatur des Akkus in 10-Grad-Grad-Kelvin enthält.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **BatteryUniqueID**               | **Mit NULL** beendete Unicode-Zeichenfolge, die den Akku eindeutig identifiziert. Dieser Wert kann zum Nachverfolgen eines bestimmten Akkus verwendet werden. Bei intelligenten Akkus ist diese ID die Verkettung des Herstellernamens, des Gerätenamens, des Herstellungsdatums und einer druckbaren Darstellung der Seriennummer. Dieser Wert soll dem Benutzer nicht angezeigt werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Die Größe des Ausgabepuffers in Bytes. Abhängig von der angeforderten Informationsebene der Daten kann dies ein Puffer mit unterschiedlicher Größe sein.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der im *lpOutBuffer-Puffer* zurückgegebenen Daten in Bytes empfängt.

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

Einige Informationen zu Akkus sind optional oder für einige Akkus bedeutungslos. Wenn der angeforderte Datentyp für den aktuellen Akku nicht verfügbar ist, wird **ERROR \_ INVALID \_ FUNCTION** zurückgegeben.

Alle Anforderungen für Akkuinformationen werden mit dem Status **\_ FEHLERDATEI \_ NICHT \_ GEFUNDEN** abgeschlossen, wenn das **BatteryTag-Element** der Anforderung nicht mit dem des aktuellen Akkutags übereinstimmen. Dadurch wird sichergestellt, dass die zurückgegebenen Akkuinformationen mit denen des angeforderten Akkus in Übereinstimmung sind. (Weitere [Informationen finden Sie unter Akkutags.)](battery-information.md)

## <a name="remarks"></a>Hinweise

Diese Akku-IOCTL ruft eine Vielzahl von Informationen für den Akku ab. Die Eingabeparameterstruktur [**BATTERY \_ QUERY \_ INFORMATION**](battery-query-information-str.md)gibt an, welche Art von Informationen zurückgegeben werden sollen und wann die Akkuinformationen zurückgegeben werden sollen. Der Datentyp und der Inhalt des Ausgabepuffers variieren basierend auf den angeforderten Daten.

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

[**\_ \_ AKKUABFRAGEINFORMATIONEN**](battery-query-information-str.md)
</dt> <dt>

[**BATTERY \_ REPORTING \_ SCALE**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[**IOCTL \_ BATTERY \_ QUERY \_ STATUS**](ioctl-battery-query-status.md)
</dt> <dt>

[**IOCTL \_ BATTERY \_ QUERY \_ TAG**](ioctl-battery-query-tag.md)
</dt> <dt>

[**\_IOCTL-AKKUSATZINFORMATIONEN \_ \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

