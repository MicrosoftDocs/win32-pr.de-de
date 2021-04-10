---
description: Anwendungen, einschließlich Diensten, können sich registrieren, um Benachrichtigungen über Geräte Ereignisse zu empfangen.
ms.assetid: c89da4ac-57dd-4d95-ac86-3eb137dee0bc
title: Geräte Ereignisse (ioevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce58ba5dd21cdd505e945687603ddb54e77b2440
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214019"
---
# <a name="device-events-ioeventh"></a>Geräte Ereignisse (ioevent. h)

Anwendungen, einschließlich Diensten, können sich registrieren, um Benachrichtigungen über Geräte Ereignisse zu empfangen. Beispielsweise kann ein Katalog Dienst eine Benachrichtigung über Volumes erhalten, die bereitgestellt oder entfernt werden, sodass die Pfade zu Dateien auf dem Volume angepasst werden können. Das System benachrichtigt eine Anwendung, dass ein Geräte Ereignis aufgetreten ist, indem die Anwendung eine [**WM \_ devicechange**](wm-devicechange.md) -Nachricht gesendet hat. Das System benachrichtigt einen Dienst, dass ein Geräte Ereignis aufgetreten ist, indem er die [**Ereignishandlerfunktion handlerex**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)aufgerufen hat.

Um Geräte Ereignis Benachrichtigungen zu empfangen, müssen Sie die [**registerdevicenotifi-**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) Funktion mit einer Entwicklungs-und [**\_ Übertragungs \_ handle**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) -Struktur aufrufen. Stellen Sie sicher, dass Sie das **dbch- \_ handle** -Element auf das Geräte handle festlegen [**, das von der Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "Funktion" abgerufen wurde. Legen Sie außerdem den **dbch \_ den DeviceType "** -Member auf **DBT \_ \_ devtyphandle** fest. Die Funktion gibt ein Geräte Benachrichtigungs Handle zurück. Beachten Sie, dass dies nicht mit dem volumehandle identisch ist.

Wenn die Anwendung eine Benachrichtigung empfängt und der Ereignistyp [DBT \_ CustomEvent](dbt-customevent.md)ist, haben Sie möglicherweise eines der in ioevent. h definierten Geräte Ereignisse erhalten. Führen Sie die folgenden Schritte aus, um zu bestimmen, ob eines dieser Ereignisse aufgetreten ist.

1.  Behandeln Sie die Ereignisdaten als [**Entwicklungs \_ Broadcast- \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -Struktur. Vergewissern Sie sich, dass der **dbch- \_ den DeviceType "** -Member auf **DBT \_ \_ devtyphandle** festgelegt ist.
2.  Wenn **dbch \_ den DeviceType "** **DBT \_ devype \_ handle** ist, handelt es sich bei den Ereignisdaten tatsächlich um einen Zeiger auf eine [**dev-Broadcast- \_ \_ handle**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) -Struktur.
3.  Vergleichen Sie den Member **dbch \_ eventguid** mit der **GUID** s, die in der folgenden Tabelle unter Verwendung der [**isequalguid**](/windows/win32/api/guiddef/nf-guiddef-isequalguid) -Funktion aufgeführt ist.

<dl> <dt>

<span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**GUID \_ IO- \_ CDROM- \_ exklusiv \_ Sperre**
</dt> <dd> <dl> <dt>

bc56c139-7a10-47ee-a294-4c6a38f0149a
</dt> <dt>



Das CD-ROM-Gerät wurde für exklusiven Zugriff gesperrt.

**Windows Server 2003 und Windows XP:** Die Unterstützung für diesen Wert erfordert IMAPI 2,0. Weitere Informationen finden Sie unter [Image Mastering API](/windows/desktop/imapi/portal).


</dt> </dl> </dd> <dt>

<span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**GUID \_ IO- \_ CDROM- \_ exklusive \_ Sperre**
</dt> <dd> <dl> <dt>

a3b6d27d-5e35-4885-81e5-ee18c00ed779
</dt> <dt>



Ein CD-ROM-Gerät, das für den exklusiven Zugriff gesperrt war, wurde entsperrt.

**Windows Server 2003 und Windows XP:** Die Unterstützung für diesen Wert erfordert IMAPI 2,0. Weitere Informationen finden Sie unter [Image Mastering API](/windows/desktop/imapi/portal).


</dt> </dl> </dd> <dt>

<span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**GUID \_ IO- \_ Gerät \_ wird \_ vorbereitet**
</dt> <dd> <dl> <dt>

d07433f0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Das Medien-Spin-up wird ausgeführt.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**Externe GUID \_ IO- \_ Geräte \_ \_ Anforderung**
</dt> <dd> <dl> <dt>

d07433d0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Für dieses Ereignis gibt es mehrere mögliche Ursachen: Weitere Informationen finden Sie unter T10 MMC-Spezifikation des Befehls Get Event Status Notification unter [https://www.t10.org/](https://www.t10.org/) .


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**GUID \_ IO- \_ Medien \_ Ankunft**
</dt> <dd> <dl> <dt>

d07433c0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Das Wechselmedium wurde dem Gerät hinzugefügt. Der **dbch- \_ Datenmember** ist ein Zeiger auf eine Kontext Struktur zum [**Ändern von Klassen \_ Medien \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) . Der **newState** -Member stellt Statusinformationen bereit. Der Wert **medianicht** gibt z. b. an, dass das Medium nicht verfügbar ist (z. b. aufgrund einer aktiven Aufzeichnungs Sitzung).

**Windows XP:** Der **dbch- \_ Datenmember** ist ein **ulong** -Wert, der angibt, wie oft das Medium seit dem Systemstart geändert wurde.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**GUID \_ IO- \_ Medien- \_ eject- \_ Anforderung**
</dt> <dd> <dl> <dt>

d07433d1-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Das Laufwerk des Wechsel Datenträgers hat eine Anforderung vom Benutzer empfangen, um den angegebenen Slot oder die angegebenen Medien abzurufen.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**Entfernen von GUID \_ IO- \_ Medien \_**
</dt> <dd> <dl> <dt>

d07433c1-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Das Wechselmedium wurde vom Gerät entfernt oder ist nicht verfügbar. Der **dbch- \_ Datenmember** ist ein Zeiger auf eine Kontext Struktur zum [**Ändern von Klassen \_ Medien \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) . Der **newState** -Member stellt Statusinformationen bereit. Der Wert **medianicht** gibt z. b. an, dass das Medium nicht verfügbar ist (z. b. aufgrund einer aktiven Aufzeichnungs Sitzung).

**Windows XP:** Der **dbch- \_ Datenmember** ist ein **ulong** -Wert, der angibt, wie oft das Medium seit dem Systemstart geändert wurde.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**GUID \_ IO- \_ Volumen \_ Änderung**
</dt> <dd> <dl> <dt>

7373654a-812a-11D0-bec7-08002be2092f
</dt> <dt>



Die Volumebezeichnung wurde geändert.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**GUID \_ IO- \_ Größe des \_ volumewechsels \_**
</dt> <dd> <dl> <dt>

3a1625be-ad03-49f1-8ef8-6bbac182 d1fd
</dt> <dt>



Die Größe des Dateisystems auf dem Volume hat sich geändert.

**Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**Dismount der GUID \_ IO- \_ Volume aufheben \_**
</dt> <dd> <dl> <dt>

d16a55e8-1059-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Es wird versucht, das Volume aufzuheben. Schließen Sie alle Handles für Dateien und Verzeichnisse auf dem Volume. Diesem Ereignis wird nicht unbedingt ein **GUID \_ IO- \_ Volume \_ Lock** -Ereignis vorangestellt.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**Fehler beim Aufheben der Einbindung des GUID IO-Volumes. \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

e3c5b178-105d-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Fehler beim Entfernen eines Volumes. Dies liegt häufig daran, dass ein anderer Prozess nicht auf eine **GUID \_ IO-Volume zur \_ \_ Aufhebung** der Einbindung reagiert, indem er die ausstehenden Handles schließt. Da die Aufhebung der Einbindung fehlgeschlagen ist, können Sie alle Handles für das betroffene Volume erneut öffnen.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**GUID \_ IO \_ Volume \_ FVE- \_ Status \_ Änderung**
</dt> <dd> <dl> <dt>

062998b2-ee1f -4B6A-b857-e76cbbe9a6da
</dt> <dt>



Der BitLocker-Laufwerkverschlüsselung Status des Volumes wurde geändert. Dieses Ereignis wird signalisiert, wenn BitLocker aktiviert oder deaktiviert wird oder wenn die Verschlüsselung gestartet, beendet, angehalten oder fortgesetzt wird.

**Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**GUID \_ IO- \_ Volume- \_ Sperre**
</dt> <dd> <dl> <dt>

50708874-c9af-11d1-8fef-00a0c9a06d32
</dt> <dt>



Ein anderer Prozess versucht, das Volume zu sperren. Schließen Sie alle Handles für Dateien und Verzeichnisse auf dem Volume.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**GUID \_ IO- \_ Volume \_ Sperren \_**
</dt> <dd> <dl> <dt>

ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32
</dt> <dt>



Fehler beim Sperren eines Volumes. Dies liegt häufig daran, dass ein anderer Prozess nicht auf ein GUID-e/a- **\_ \_ Volume \_ Lock** -Ereignis reagieren konnte, indem er die ausstehenden Handles schließt Da bei der Sperre ein Fehler aufgetreten ist, können Sie alle Handles für das betroffene Volume erneut öffnen.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**GUID \_ IO- \_ Volume \_ einbinden**
</dt> <dd> <dl> <dt>

b5804878-1a96-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Das Volume wurde von einem anderen Prozess bereitgestellt. Sie können ein oder mehrere Handles dafür öffnen.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**GUID \_ IO- \_ Volumen \_ Namen \_ Änderung**
</dt> <dd> <dl> <dt>

2de9783-4c06-11d2-A532-00609713055a
</dt> <dt>



Der Volumename wurde geändert.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**GUID-e/a- \_ \_ Volume \_ benötigt \_ chkdsk**
</dt> <dd> <dl> <dt>

799a0960-0a0b-4e03-ad88-2fa7c6ce748a
</dt> <dt>



Ein Dateisystem hat Beschädigungen auf dem Volume erkannt. Die Anwendung sollte CHKDSK auf dem Volume ausführen oder den Benutzer benachrichtigen.

**Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**Änderung der \_ \_ \_ physischen \_ Konfiguration \_ des GUID IO-Volumes**
</dt> <dd> <dl> <dt>

2de9784-4c06-11d2-A532-00609713055a
</dt> <dt>



Die physische oder der aktuelle physische Zustand des Volumes hat sich geändert.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**GUID \_ IO- \_ Volume \_ Vorbereiten von \_ eject**
</dt> <dd> <dl> <dt>

c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6
</dt> <dt>



Das Dateisystem bereitet den abzurufenden Datenträger vor. Beispielsweise hält das Dateisystem einen Hintergrund Formatierungs Vorgang an oder schließt die Sitzung auf einem Write-Once-Medium.

**Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**\_ \_ \_ eindeutige \_ ID- \_ Änderung für GUID IO-Volume**
</dt> <dd> <dl> <dt>

af39da42-6622-41f5-970b-139d092fa3d9
</dt> <dt>



Der eindeutige Bezeichner des Volumes wurde geändert. Weitere Informationen zum eindeutigen Bezeichner finden Sie unter [**eindeutige IOCTL \_ mountdev- \_ Abfrage- \_ \_ ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird erst ab Windows Server 2008 R2 und Windows 7 unterstützt.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**GUID \_ IO \_ Volume \_ Unlock**
</dt> <dd> <dl> <dt>

9a8c3d68-d0cb-11d1-8fef -00a0c9a06d32
</dt> <dt>



Das Volume wurde von einem anderen Prozess entsperrt. Sie können ein oder mehrere Handles dafür öffnen.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**GUID \_ IO- \_ Volume wird \_ \_ ausgecheckt**
</dt> <dd> <dl> <dt>

873113ca-1486-4508-82ac-c3b2e5297aaa
</dt> <dt>



Das Medium wird ausgecheckt. Dieses Ereignis wird gesendet, wenn ein Dateisystem feststellt, dass die Fehlerrate eines Volumes zu hoch ist oder der Fehler Ersetzungs Speicher fast erschöpft ist.

**Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beim Aufheben der Einbindung von GUID-e/a- **\_ \_ \_ Volume** und GUID io-e/a- **\_ \_ Volume \_ \_** werden fehlerhafte Ereignisse zusammen mit der **GUID \_ IO \_ Volume \_ Lock** und dem **GUID io-e/a-Volume \_ \_ \_ gesperrt \_** Durch die **GUID \_ IO \_ Volume \_ Dismount** und **GUID \_ IO \_ Volume \_ Lock** -Ereignisse wird angegeben, dass versucht wird, einen Vorgang auszuführen. Sie sollten auf die Ereignis Benachrichtigung reagieren und die ausgeführte Aktion aufzeichnen. Fehler beim Aufheben der Einbindung des **GUID \_ IO \_ \_ \_** -Volumes und beim fehl **\_ \_ \_ \_ geschlagenen GUID** -e/a-Volumen Sperr Vorgang auf einen Fehler beim Versuch Anschließend können Sie mit Ihrem Datensatz die Aktionen rückgängig machen, die Sie als Reaktion auf den Vorgang durchgeführt haben.

Das **dbch \_ hdevnotify** -Mitglied der [**dev- \_ Broadcast- \_ handle**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) -Struktur gibt das betroffene Gerät an. Beachten Sie, dass es sich hierbei um das von [**registerdevicenotifizierung**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)zurückgegebene Geräte Benachrichtigungs Handle handelt, nicht um ein Volume Zum Ausführen von Vorgängen auf dem Volume ordnen Sie dieses handle dem entsprechenden volumehandle zu.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Ioevent. h</dt> </dl> |



 

