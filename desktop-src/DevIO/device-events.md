---
description: Anwendungen, einschließlich Diensten, können sich registrieren, um Benachrichtigungen über Geräteereignisse zu empfangen.
ms.assetid: c89da4ac-57dd-4d95-ac86-3eb137dee0bc
title: Geräteereignisse (IoEvent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a44e6160ef3a59821e5d2b2a3d4e42ee1d14d5c2fb7deda689fb1c9c3186b428
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076254"
---
# <a name="device-events-ioeventh"></a>Geräteereignisse (IoEvent.h)

Anwendungen, einschließlich Diensten, können sich registrieren, um Benachrichtigungen über Geräteereignisse zu empfangen. Beispielsweise kann ein Katalogdienst Benachrichtigungen über volumes erhalten, die bereitgestellt oder aufgehoben werden, damit er die Pfade zu Dateien auf dem Volume anpassen kann. Das System benachrichtigt eine Anwendung, dass ein Geräteereignis aufgetreten ist, indem es der Anwendung eine [**WM \_ DEVICECHANGE-Nachricht**](wm-devicechange.md) sendet. Das System benachrichtigt einen Dienst, dass ein Geräteereignis aufgetreten ist, indem es die Ereignishandlerfunktion handlerex des [**Diensts aufruft.**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)

Um Geräteereignisbenachrichtigungen zu empfangen, rufen Sie die [**RegisterDeviceNotification-Funktion**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) mit einer [**DEV BROADCAST \_ \_ HANDLE-Struktur**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) auf. Achten Sie darauf, dass Sie **den \_ dbch-Handle-Member** auf das Gerätehand handle festlegen, das von der [**CreateFile-Funktion erhalten**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) wurde. Legen Sie außerdem den **dbch \_ devicetype-Member** auf **DBT \_ DEVTYP \_ HANDLE fest.** Die Funktion gibt ein Gerätebenachrichtigungshand handle zurück. Beachten Sie, dass dies nicht mit dem Volumehand handle identisch ist.

Wenn Ihre Anwendung eine Benachrichtigung empfängt und der Ereignistyp [DBT \_ CUSTOMEVENT](dbt-customevent.md)ist, haben Sie möglicherweise eines der in IoEvent.h definierten Geräteereignisse erhalten. Um zu ermitteln, ob eines dieser Ereignisse aufgetreten ist, verwenden Sie die folgenden Schritte.

1.  Behandeln Sie die Ereignisdaten als [**DEV \_ \_ BROADCAST-HDR-Struktur.**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) Stellen Sie sicher, **dass der dbch \_ devicetype-Member** auf **DBT \_ DEVTYP HANDLE festgelegt \_ ist.**
2.  Wenn **dbch \_ devicetype** **DBT \_ DEVTYP \_ HANDLE ist,** sind die Ereignisdaten tatsächlich ein Zeiger auf eine [**DEV BROADCAST \_ \_ HANDLE-Struktur.**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle)
3.  Vergleichen Sie **das dbch \_ eventguid-Mitglied** mit den **GUID-Dateien,** die in der folgenden Tabelle aufgeführt sind, mithilfe der [**IsEqualGUID-Funktion.**](/windows/win32/api/guiddef/nf-guiddef-isequalguid)

<dl> <dt>

<span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**EXKLUSIVE \_ \_ GUID-E/A-SPERRUNG \_ \_**
</dt> <dd> <dl> <dt>

bc56c139-7a10-47ee-a294-4c6a38f0149a
</dt> <dt>



Das CD-ROM-Gerät wurde für exklusiven Zugriff gesperrt.

**Windows Server 2003 und Windows XP:** Die Unterstützung für diesen Wert erfordert IMAPI 2.0. Weitere Informationen finden Sie unter [ImageMastering-API](/windows/desktop/imapi/portal).


</dt> </dl> </dd> <dt>

<span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**GUID \_ \_ E/A- EXKLUSIVE \_ \_ ENTSPERRUNG**
</dt> <dd> <dl> <dt>

a3b6d27d-5e35-4885-81e5-ee18c00ed779
</dt> <dt>



Ein CD-ROM-Gerät, das für exklusiven Zugriff gesperrt wurde, wurde entsperrt.

**Windows Server 2003 und Windows XP:** Die Unterstützung für diesen Wert erfordert IMAPI 2.0. Weitere Informationen finden Sie unter [ImageMastering-API](/windows/desktop/imapi/portal).


</dt> </dl> </dd> <dt>

<span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**\_ \_ GUID-E/A-GERÄT \_ WIRD \_ BEREIT**
</dt> <dd> <dl> <dt>

d07433f0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Das Medien spin-up ist in Bearbeitung.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**EXTERNE ANFORDERUNG DES \_ \_ GUID-E/A-GERÄTS \_ \_**
</dt> <dd> <dl> <dt>

d07433d0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Es gibt mehrere mögliche Ursachen für dieses Ereignis: Weitere Informationen finden Sie in der T10-MMC-Spezifikation des Befehls GET EVENT STATUS NOTIFICATION unter [https://www.t10.org/](https://www.t10.org/) .


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**GUID \_ IO \_ MEDIA \_ ARRIVAL**
</dt> <dd> <dl> <dt>

d07433c0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Dem Gerät wurden Wechselmedien hinzugefügt. Der **\_ dbch-Daten** member ist ein Zeiger auf eine [**CLASS MEDIA CHANGE \_ \_ \_ CONTEXT-Struktur.**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) Das **NewState-Member** stellt Statusinformationen zur Verfügung. Der Wert **MediaUnavailable** gibt beispielsweise an, dass das Medium nicht verfügbar ist (z. B. aufgrund einer aktiven Aufzeichnungssitzung).

**Windows XP:** Der **\_ dbch-Daten** member ist ein **ULONG-Wert,** der die Anzahl der Medienänderung seit dem Systemstart darstellt.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**\_ \_ GUID-E/A-MEDIENEJEKTIONSANFORDERUNG \_ \_**
</dt> <dd> <dl> <dt>

d07433d1-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Das Laufwerk des Wechselmediums hat vom Benutzer eine Anforderung zum Auswerfen des angegebenen Slots oder Mediums erhalten.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**ENTFERNEN VON \_ GUID-E/A-MEDIEN \_ \_**
</dt> <dd> <dl> <dt>

d07433c1-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Wechselmedien wurden vom Gerät entfernt oder sind nicht verfügbar. Der **\_ dbch-Daten** member ist ein Zeiger auf eine [**CLASS MEDIA CHANGE \_ \_ \_ CONTEXT-Struktur.**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) Das **NewState-Member** stellt Statusinformationen zur Verfügung. Der Wert **MediaUnavailable** gibt beispielsweise an, dass das Medium nicht verfügbar ist (z. B. aufgrund einer aktiven Aufzeichnungssitzung).

**Windows XP:** Der **\_ dbch-Daten** member ist ein **ULONG-Wert,** der die Anzahl der Medienänderung seit dem Systemstart darstellt.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**ÄNDERUNG DES \_ GUID-E/A-VOLUMES \_ \_**
</dt> <dd> <dl> <dt>

7373654a-812a-11d0-bec7-08002be2092f
</dt> <dt>



Die Volumebezeichnung wurde geändert.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**\_ \_ \_ GUID-E/A-VOLUMEÄNDERUNGSGRÖßE \_**
</dt> <dd> <dl> <dt>

3a1625be-ad03-49f1-8ef8-6bbac182d1fd
</dt> <dt>



Die Größe des Dateisystems auf dem Volume hat sich geändert.

**Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**\_GUID-E/A-VOLUME \_ \_ DISMOUNT**
</dt> <dd> <dl> <dt>

d16a55e8-1059-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Es wird versucht, die Bereitstellung des Volumes zu dismountieren. Sie sollten alle Handles für Dateien und Verzeichnisse auf dem Volume schließen. Diesem Ereignis wird nicht notwendigerweise ein GUID IO **\_ VOLUME \_ \_ LOCK-Ereignis** vorangehenden.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**FEHLER BEI DER BEREITSTELLUNG \_ DES GUID-E/A-VOLUMES \_ \_ \_**
</dt> <dd> <dl> <dt>

e3c5b178-105d-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Fehler beim Versuch, die Bereitstellung eines Volumes zu erhöhen. Dies liegt häufig daran, dass ein anderer Prozess nicht auf eine **\_ GUID-E/A-VOLUME-DISMOUNT-Benachrichtigung \_ \_** reagiert hat, indem er die ausstehenden Handles schließt. Da die Bereitstellung fehlgeschlagen ist, können Sie alle Handles für das betroffene Volume erneut öffnen.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**ÄNDERUNG DES STATUS DER \_ GUID-E/A-VOLUME-FVE \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

062998b2-ee1f-4b6a-b857-e76cbbe9a6da
</dt> <dt>



Der BitLocker-Laufwerkverschlüsselung des Volumes hat sich geändert. Dieses Ereignis wird signalisiert, wenn BitLocker aktiviert oder deaktiviert ist oder wenn die Verschlüsselung beginnt, endet, angehalten oder fortgesetzt wird.

**Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**\_GUID-E/A-VOLUMESPERRE \_ \_**
</dt> <dd> <dl> <dt>

50708874-c9af-11d1-8fef-00a0c9a06d32
</dt> <dt>



Ein anderer Prozess versucht, das Volume zu sperren. Sie sollten alle Handles für Dateien und Verzeichnisse auf dem Volume schließen.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**FEHLER BEI DER \_ GUID-E/A-VOLUMESPERRE \_ \_ \_**
</dt> <dd> <dl> <dt>

ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32
</dt> <dt>



Fehler beim Sperren eines Volumes. Dies liegt häufig daran, dass ein anderer Prozess nicht auf ein **GUID \_ IO VOLUME \_ \_ LOCK-Ereignis** reagieren konnte, indem seine ausstehenden Handles geschlossen wurden. Da die Sperre fehlgeschlagen ist, können Sie alle Handles für das betroffene Volume erneut öffnen.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**\_ \_ GUID-E/A-VOLUME-BEREITSTELLUNG \_**
</dt> <dd> <dl> <dt>

b5804878-1a96-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Das Volume wurde von einem anderen Prozess bereitgestellt. Sie können ein oder mehrere Handles öffnen.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**ÄNDERUNG DES \_ GUID-E/A-VOLUMENAMENS \_ \_ \_**
</dt> <dd> <dl> <dt>

2de97f83-4c06-11d2-a532-00609713055a
</dt> <dt>



Der Volumename wurde geändert.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**\_ \_ GUID-E/A-VOLUME \_ BENÖTIGT \_ CHKDSK**
</dt> <dd> <dl> <dt>

799a0960-0a0b-4e03-ad88-2fa7c6ce748a
</dt> <dt>



Ein Dateisystem hat eine Beschädigung auf dem Volume erkannt. Die Anwendung sollte CHKDSK auf dem Volume ausführen oder den Benutzer benachrichtigen, dies zu tun.

**Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**ÄNDERUNG DER PHYSISCHEN \_ KONFIGURATION DES GUID-E/A-VOLUMES \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

2de97f84-4c06-11d2-a532-00609713055a
</dt> <dt>



Das physische Makeup oder der aktuelle physische Zustand des Volumes wurde geändert.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**\_ \_ GUID-E/A-VOLUME, \_ DAS DAS \_ EJECT VORBEREITET**
</dt> <dd> <dl> <dt>

c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6
</dt> <dt>



Das Dateisystem bereitet den Datenträger vor, der ausjiziert werden soll. Beispielsweise beendet das Dateisystem einen Hintergrundformatierungsvorgang oder schließt die Sitzung auf Schreib-einmal-Medien.

**Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**ÄNDERUNG DER \_ EINDEUTIGEN ID DES GUID-E/A-VOLUMES \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

af39da42-6622-41f5-970b-139d092fa3d9
</dt> <dt>



Der eindeutige Bezeichner des Volumes wurde geändert. Weitere Informationen zum eindeutigen Bezeichner finden Sie unter [**IOCTL \_ MOUNTDEV \_ QUERY UNIQUE \_ \_ ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird erst Windows Server 2008 R2 und Windows 7 unterstützt.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**ENTSPERRUNG DES \_ GUID-E/A-VOLUMES \_ \_**
</dt> <dd> <dl> <dt>

9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32
</dt> <dt>



Das Volume wurde von einem anderen Prozess entsperrt. Sie können ein oder mehrere Handles öffnen.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**\_GUID-E/A-VOLUME \_ \_ WIRD \_ AUSGEGEBEN**
</dt> <dd> <dl> <dt>

873113ca-1486-4508-82ac-c3b2e5297aaa
</dt> <dt>



Die Medien werden ausgesägt. Dieses Ereignis wird gesendet, wenn ein Dateisystem feststellt, dass die Fehlerrate auf einem Volume zu hoch ist oder der Ersatzspeicherplatz des Fehlers fast erschöpft ist.

**Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Die EREIGNISSE **GUID \_ IO VOLUME \_ \_ DISMOUNT** und **GUID IO VOLUME \_ \_ \_ DISMOUNT \_ FAILED** sind verknüpft, ebenso wie die EREIGNISSE **GUID IO VOLUME \_ \_ \_ LOCK** und **GUID IO VOLUME LOCK \_ \_ \_ \_ FAILED.** Die EREIGNISSE **GUID \_ IO VOLUME \_ \_ DISMOUNT** und **GUID IO VOLUME \_ \_ \_ LOCK** deuten darauf hin, dass ein Vorgang versucht wird. Sie sollten auf die Ereignisbenachrichtigung reagieren und die ausgeführte Aktion aufzeichnen. Die Ereignisse **GUID \_ IO VOLUME \_ \_ DISMOUNT \_ FAILED** und **GUID IO VOLUME LOCK \_ \_ \_ \_ FAILED** geben an, dass der vorgangsversuch fehlgeschlagen ist. Anschließend können Sie Ihren Datensatz verwenden, um die Aktionen rückgängig zu machen, die Sie als Reaktion auf den Vorgang durchgeführt haben.

Der **dbch \_ hdevnotify-Member** der [**DEV BROADCAST \_ \_ HANDLE-Struktur**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) gibt das betroffene Gerät an. Beachten Sie, dass dies das von [**RegisterDeviceNotification zurückgegebene**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)Gerätebenachrichtigungshandle und kein Volumehandle ist. Um Vorgänge auf dem Volume auszuführen, ordnen Sie dieses Handle dem entsprechenden Volumehandle zu.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>IoEvent.h</dt> </dl> |



 

