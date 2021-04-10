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
# <a name="device-events-ioeventh"></a><span data-ttu-id="05390-103">Geräte Ereignisse (ioevent. h)</span><span class="sxs-lookup"><span data-stu-id="05390-103">Device Events (IoEvent.h)</span></span>

<span data-ttu-id="05390-104">Anwendungen, einschließlich Diensten, können sich registrieren, um Benachrichtigungen über Geräte Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="05390-104">Applications, including services, can register to receive notification of device events.</span></span> <span data-ttu-id="05390-105">Beispielsweise kann ein Katalog Dienst eine Benachrichtigung über Volumes erhalten, die bereitgestellt oder entfernt werden, sodass die Pfade zu Dateien auf dem Volume angepasst werden können.</span><span class="sxs-lookup"><span data-stu-id="05390-105">For example, a catalog service can receive notice of volumes being mounted or dismounted so it can adjust the paths to files on the volume.</span></span> <span data-ttu-id="05390-106">Das System benachrichtigt eine Anwendung, dass ein Geräte Ereignis aufgetreten ist, indem die Anwendung eine [**WM \_ devicechange**](wm-devicechange.md) -Nachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="05390-106">The system notifies an application that a device event has occurred by sending the application a [**WM\_DEVICECHANGE**](wm-devicechange.md) message.</span></span> <span data-ttu-id="05390-107">Das System benachrichtigt einen Dienst, dass ein Geräte Ereignis aufgetreten ist, indem er die [**Ereignishandlerfunktion handlerex**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="05390-107">The system notifies a service that a device event has occurred by invoking the service's event handler function, [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span></span>

<span data-ttu-id="05390-108">Um Geräte Ereignis Benachrichtigungen zu empfangen, müssen Sie die [**registerdevicenotifi-**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) Funktion mit einer Entwicklungs-und [**\_ Übertragungs \_ handle**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) -Struktur aufrufen.</span><span class="sxs-lookup"><span data-stu-id="05390-108">To receive device event notices, call the [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) function with a [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure.</span></span> <span data-ttu-id="05390-109">Stellen Sie sicher, dass Sie das **dbch- \_ handle** -Element auf das Geräte handle festlegen [**, das von der Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "Funktion" abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="05390-109">Be sure to set the **dbch\_handle** member to the device handle obtained from the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="05390-110">Legen Sie außerdem den **dbch \_ den DeviceType "** -Member auf **DBT \_ \_ devtyphandle** fest.</span><span class="sxs-lookup"><span data-stu-id="05390-110">Also, set the **dbch\_devicetype** member to **DBT\_DEVTYP\_HANDLE**.</span></span> <span data-ttu-id="05390-111">Die Funktion gibt ein Geräte Benachrichtigungs Handle zurück.</span><span class="sxs-lookup"><span data-stu-id="05390-111">The function returns a device notification handle.</span></span> <span data-ttu-id="05390-112">Beachten Sie, dass dies nicht mit dem volumehandle identisch ist.</span><span class="sxs-lookup"><span data-stu-id="05390-112">Note that this is not the same as the volume handle.</span></span>

<span data-ttu-id="05390-113">Wenn die Anwendung eine Benachrichtigung empfängt und der Ereignistyp [DBT \_ CustomEvent](dbt-customevent.md)ist, haben Sie möglicherweise eines der in ioevent. h definierten Geräte Ereignisse erhalten.</span><span class="sxs-lookup"><span data-stu-id="05390-113">When your application receives notification, if the event type is [DBT\_CUSTOMEVENT](dbt-customevent.md), you may have received one of the device events defined in IoEvent.h.</span></span> <span data-ttu-id="05390-114">Führen Sie die folgenden Schritte aus, um zu bestimmen, ob eines dieser Ereignisse aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="05390-114">To determine if one of these events has occurred, use the following steps.</span></span>

1.  <span data-ttu-id="05390-115">Behandeln Sie die Ereignisdaten als [**Entwicklungs \_ Broadcast- \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="05390-115">Treat the event data as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span> <span data-ttu-id="05390-116">Vergewissern Sie sich, dass der **dbch- \_ den DeviceType "** -Member auf **DBT \_ \_ devtyphandle** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="05390-116">Verify that the **dbch\_devicetype** member is set to **DBT\_DEVTYP\_HANDLE**.</span></span>
2.  <span data-ttu-id="05390-117">Wenn **dbch \_ den DeviceType "** **DBT \_ devype \_ handle** ist, handelt es sich bei den Ereignisdaten tatsächlich um einen Zeiger auf eine [**dev-Broadcast- \_ \_ handle**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="05390-117">If **dbch\_devicetype** is **DBT\_DEVTYP\_HANDLE**, the event data is really a pointer to a [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure.</span></span>
3.  <span data-ttu-id="05390-118">Vergleichen Sie den Member **dbch \_ eventguid** mit der **GUID** s, die in der folgenden Tabelle unter Verwendung der [**isequalguid**](/windows/win32/api/guiddef/nf-guiddef-isequalguid) -Funktion aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="05390-118">Compare the **dbch\_eventguid** member to the **GUID** s listed in the following table using the [**IsEqualGUID**](/windows/win32/api/guiddef/nf-guiddef-isequalguid) function.</span></span>

<dl> <dt>

<span data-ttu-id="05390-119"><span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**GUID \_ IO- \_ CDROM- \_ exklusiv \_ Sperre**</span><span class="sxs-lookup"><span data-stu-id="05390-119"><span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**GUID\_IO\_CDROM\_EXCLUSIVE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-120">bc56c139-7a10-47ee-a294-4c6a38f0149a</span><span class="sxs-lookup"><span data-stu-id="05390-120">bc56c139-7a10-47ee-a294-4c6a38f0149a</span></span>
</dt> <dt>



<span data-ttu-id="05390-121">Das CD-ROM-Gerät wurde für exklusiven Zugriff gesperrt.</span><span class="sxs-lookup"><span data-stu-id="05390-121">The CD-ROM device has been locked for exclusive access.</span></span>

<span data-ttu-id="05390-122">**Windows Server 2003 und Windows XP:** Die Unterstützung für diesen Wert erfordert IMAPI 2,0.</span><span class="sxs-lookup"><span data-stu-id="05390-122">**Windows Server 2003 and Windows XP:** Support for this value requires IMAPI 2.0.</span></span> <span data-ttu-id="05390-123">Weitere Informationen finden Sie unter [Image Mastering API](/windows/desktop/imapi/portal).</span><span class="sxs-lookup"><span data-stu-id="05390-123">For more information, see [Image Mastering API](/windows/desktop/imapi/portal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-124"><span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**GUID \_ IO- \_ CDROM- \_ exklusive \_ Sperre**</span><span class="sxs-lookup"><span data-stu-id="05390-124"><span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**GUID\_IO\_CDROM\_EXCLUSIVE\_UNLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-125">a3b6d27d-5e35-4885-81e5-ee18c00ed779</span><span class="sxs-lookup"><span data-stu-id="05390-125">a3b6d27d-5e35-4885-81e5-ee18c00ed779</span></span>
</dt> <dt>



<span data-ttu-id="05390-126">Ein CD-ROM-Gerät, das für den exklusiven Zugriff gesperrt war, wurde entsperrt.</span><span class="sxs-lookup"><span data-stu-id="05390-126">A CD-ROM device that was locked for exclusive access has been unlocked.</span></span>

<span data-ttu-id="05390-127">**Windows Server 2003 und Windows XP:** Die Unterstützung für diesen Wert erfordert IMAPI 2,0.</span><span class="sxs-lookup"><span data-stu-id="05390-127">**Windows Server 2003 and Windows XP:** Support for this value requires IMAPI 2.0.</span></span> <span data-ttu-id="05390-128">Weitere Informationen finden Sie unter [Image Mastering API](/windows/desktop/imapi/portal).</span><span class="sxs-lookup"><span data-stu-id="05390-128">For more information, see [Image Mastering API](/windows/desktop/imapi/portal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-129"><span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**GUID \_ IO- \_ Gerät \_ wird \_ vorbereitet**</span><span class="sxs-lookup"><span data-stu-id="05390-129"><span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**GUID\_IO\_DEVICE\_BECOMING\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-130">d07433f0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="05390-130">d07433f0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="05390-131">Das Medien-Spin-up wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="05390-131">Media spin-up is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-132"><span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**Externe GUID \_ IO- \_ Geräte \_ \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="05390-132"><span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**GUID\_IO\_DEVICE\_EXTERNAL\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-133">d07433d0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="05390-133">d07433d0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="05390-134">Für dieses Ereignis gibt es mehrere mögliche Ursachen: Weitere Informationen finden Sie unter T10 MMC-Spezifikation des Befehls Get Event Status Notification unter [https://www.t10.org/](https://www.t10.org/) .</span><span class="sxs-lookup"><span data-stu-id="05390-134">There are several possible causes for this event; for more information, refer to T10 MMC specification of the GET EVENT STATUS NOTIFICATION Command, at [https://www.t10.org/](https://www.t10.org/).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-135"><span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**GUID \_ IO- \_ Medien \_ Ankunft**</span><span class="sxs-lookup"><span data-stu-id="05390-135"><span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**GUID\_IO\_MEDIA\_ARRIVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-136">d07433c0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="05390-136">d07433c0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="05390-137">Das Wechselmedium wurde dem Gerät hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="05390-137">Removable media has been added to the device.</span></span> <span data-ttu-id="05390-138">Der **dbch- \_ Datenmember** ist ein Zeiger auf eine Kontext Struktur zum [**Ändern von Klassen \_ Medien \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) .</span><span class="sxs-lookup"><span data-stu-id="05390-138">The **dbch\_data** member is a pointer to a [**CLASS\_MEDIA\_CHANGE\_CONTEXT**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) structure.</span></span> <span data-ttu-id="05390-139">Der **newState** -Member stellt Statusinformationen bereit.</span><span class="sxs-lookup"><span data-stu-id="05390-139">The **NewState** member provides status information.</span></span> <span data-ttu-id="05390-140">Der Wert **medianicht** gibt z. b. an, dass das Medium nicht verfügbar ist (z. b. aufgrund einer aktiven Aufzeichnungs Sitzung).</span><span class="sxs-lookup"><span data-stu-id="05390-140">For example, a value of **MediaUnavailable** indicates that the media is not available (for example, due to an active recording session).</span></span>

<span data-ttu-id="05390-141">**Windows XP:** Der **dbch- \_ Datenmember** ist ein **ulong** -Wert, der angibt, wie oft das Medium seit dem Systemstart geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="05390-141">**Windows XP:** The **dbch\_data** member is a **ULONG** value that represents the number of times that media has been changed since system startup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-142"><span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**GUID \_ IO- \_ Medien- \_ eject- \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="05390-142"><span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**GUID\_IO\_MEDIA\_EJECT\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-143">d07433d1-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="05390-143">d07433d1-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="05390-144">Das Laufwerk des Wechsel Datenträgers hat eine Anforderung vom Benutzer empfangen, um den angegebenen Slot oder die angegebenen Medien abzurufen.</span><span class="sxs-lookup"><span data-stu-id="05390-144">The removable media's drive has received a request from the user to eject the specified slot or media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-145"><span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**Entfernen von GUID \_ IO- \_ Medien \_**</span><span class="sxs-lookup"><span data-stu-id="05390-145"><span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**GUID\_IO\_MEDIA\_REMOVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-146">d07433c1-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="05390-146">d07433c1-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="05390-147">Das Wechselmedium wurde vom Gerät entfernt oder ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="05390-147">Removable media has been removed from the device or is unavailable.</span></span> <span data-ttu-id="05390-148">Der **dbch- \_ Datenmember** ist ein Zeiger auf eine Kontext Struktur zum [**Ändern von Klassen \_ Medien \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) .</span><span class="sxs-lookup"><span data-stu-id="05390-148">The **dbch\_data** member is a pointer to a [**CLASS\_MEDIA\_CHANGE\_CONTEXT**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) structure.</span></span> <span data-ttu-id="05390-149">Der **newState** -Member stellt Statusinformationen bereit.</span><span class="sxs-lookup"><span data-stu-id="05390-149">The **NewState** member provides status information.</span></span> <span data-ttu-id="05390-150">Der Wert **medianicht** gibt z. b. an, dass das Medium nicht verfügbar ist (z. b. aufgrund einer aktiven Aufzeichnungs Sitzung).</span><span class="sxs-lookup"><span data-stu-id="05390-150">For example, a value of **MediaUnavailable** indicates that the media is not available (for example, due to an active recording session).</span></span>

<span data-ttu-id="05390-151">**Windows XP:** Der **dbch- \_ Datenmember** ist ein **ulong** -Wert, der angibt, wie oft das Medium seit dem Systemstart geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="05390-151">**Windows XP:** The **dbch\_data** member is a **ULONG** value that represents the number of times that media has been changed since system startup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-152"><span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**GUID \_ IO- \_ Volumen \_ Änderung**</span><span class="sxs-lookup"><span data-stu-id="05390-152"><span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**GUID\_IO\_VOLUME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-153">7373654a-812a-11D0-bec7-08002be2092f</span><span class="sxs-lookup"><span data-stu-id="05390-153">7373654a-812a-11d0-bec7-08002be2092f</span></span>
</dt> <dt>



<span data-ttu-id="05390-154">Die Volumebezeichnung wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="05390-154">The volume label has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-155"><span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**GUID \_ IO- \_ Größe des \_ volumewechsels \_**</span><span class="sxs-lookup"><span data-stu-id="05390-155"><span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**GUID\_IO\_VOLUME\_CHANGE\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-156">3a1625be-ad03-49f1-8ef8-6bbac182 d1fd</span><span class="sxs-lookup"><span data-stu-id="05390-156">3a1625be-ad03-49f1-8ef8-6bbac182d1fd</span></span>
</dt> <dt>



<span data-ttu-id="05390-157">Die Größe des Dateisystems auf dem Volume hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="05390-157">The size of the file system on the volume has changed.</span></span>

<span data-ttu-id="05390-158">**Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05390-158">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-159"><span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**Dismount der GUID \_ IO- \_ Volume aufheben \_**</span><span class="sxs-lookup"><span data-stu-id="05390-159"><span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**GUID\_IO\_VOLUME\_DISMOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-160">d16a55e8-1059-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="05390-160">d16a55e8-1059-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="05390-161">Es wird versucht, das Volume aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="05390-161">An attempt to dismount the volume is in progress.</span></span> <span data-ttu-id="05390-162">Schließen Sie alle Handles für Dateien und Verzeichnisse auf dem Volume.</span><span class="sxs-lookup"><span data-stu-id="05390-162">You should close all handles to files and directories on the volume.</span></span> <span data-ttu-id="05390-163">Diesem Ereignis wird nicht unbedingt ein **GUID \_ IO- \_ Volume \_ Lock** -Ereignis vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="05390-163">This event will not necessarily be preceded by a **GUID\_IO\_VOLUME\_LOCK** event.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-164"><span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**Fehler beim Aufheben der Einbindung des GUID IO-Volumes. \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="05390-164"><span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**GUID\_IO\_VOLUME\_DISMOUNT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-165">e3c5b178-105d-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="05390-165">e3c5b178-105d-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="05390-166">Fehler beim Entfernen eines Volumes.</span><span class="sxs-lookup"><span data-stu-id="05390-166">An attempt to dismount a volume failed.</span></span> <span data-ttu-id="05390-167">Dies liegt häufig daran, dass ein anderer Prozess nicht auf eine **GUID \_ IO-Volume zur \_ \_ Aufhebung** der Einbindung reagiert, indem er die ausstehenden Handles schließt.</span><span class="sxs-lookup"><span data-stu-id="05390-167">This often happens because another process failed to respond to a **GUID\_IO\_VOLUME\_DISMOUNT** notice by closing its outstanding handles.</span></span> <span data-ttu-id="05390-168">Da die Aufhebung der Einbindung fehlgeschlagen ist, können Sie alle Handles für das betroffene Volume erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="05390-168">Because the dismount failed, you may reopen any handles to the affected volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-169"><span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**GUID \_ IO \_ Volume \_ FVE- \_ Status \_ Änderung**</span><span class="sxs-lookup"><span data-stu-id="05390-169"><span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**GUID\_IO\_VOLUME\_FVE\_STATUS\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-170">062998b2-ee1f -4B6A-b857-e76cbbe9a6da</span><span class="sxs-lookup"><span data-stu-id="05390-170">062998b2-ee1f-4b6a-b857-e76cbbe9a6da</span></span>
</dt> <dt>



<span data-ttu-id="05390-171">Der BitLocker-Laufwerkverschlüsselung Status des Volumes wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="05390-171">The volume's BitLocker Drive Encryption status has changed.</span></span> <span data-ttu-id="05390-172">Dieses Ereignis wird signalisiert, wenn BitLocker aktiviert oder deaktiviert wird oder wenn die Verschlüsselung gestartet, beendet, angehalten oder fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="05390-172">This event is signaled when BitLocker is enabled or disabled, or when encryption begins, ends, pauses, or resumes.</span></span>

<span data-ttu-id="05390-173">**Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05390-173">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-174"><span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**GUID \_ IO- \_ Volume- \_ Sperre**</span><span class="sxs-lookup"><span data-stu-id="05390-174"><span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**GUID\_IO\_VOLUME\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-175">50708874-c9af-11d1-8fef-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="05390-175">50708874-c9af-11d1-8fef-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="05390-176">Ein anderer Prozess versucht, das Volume zu sperren.</span><span class="sxs-lookup"><span data-stu-id="05390-176">Another process is attempting to lock the volume.</span></span> <span data-ttu-id="05390-177">Schließen Sie alle Handles für Dateien und Verzeichnisse auf dem Volume.</span><span class="sxs-lookup"><span data-stu-id="05390-177">You should close all handles to files and directories on the volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-178"><span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**GUID \_ IO- \_ Volume \_ Sperren \_**</span><span class="sxs-lookup"><span data-stu-id="05390-178"><span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**GUID\_IO\_VOLUME\_LOCK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-179">ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="05390-179">ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="05390-180">Fehler beim Sperren eines Volumes.</span><span class="sxs-lookup"><span data-stu-id="05390-180">An attempt to lock a volume failed.</span></span> <span data-ttu-id="05390-181">Dies liegt häufig daran, dass ein anderer Prozess nicht auf ein GUID-e/a- **\_ \_ Volume \_ Lock** -Ereignis reagieren konnte, indem er die ausstehenden Handles schließt</span><span class="sxs-lookup"><span data-stu-id="05390-181">This often happens because another process failed to respond to a **GUID\_IO\_VOLUME\_LOCK** event by closing its outstanding handles.</span></span> <span data-ttu-id="05390-182">Da bei der Sperre ein Fehler aufgetreten ist, können Sie alle Handles für das betroffene Volume erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="05390-182">Because the lock failed, you may reopen any handles to the affected volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-183"><span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**GUID \_ IO- \_ Volume \_ einbinden**</span><span class="sxs-lookup"><span data-stu-id="05390-183"><span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**GUID\_IO\_VOLUME\_MOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-184">b5804878-1a96-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="05390-184">b5804878-1a96-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="05390-185">Das Volume wurde von einem anderen Prozess bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="05390-185">The volume has been mounted by another process.</span></span> <span data-ttu-id="05390-186">Sie können ein oder mehrere Handles dafür öffnen.</span><span class="sxs-lookup"><span data-stu-id="05390-186">You may open one or more handles to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-187"><span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**GUID \_ IO- \_ Volumen \_ Namen \_ Änderung**</span><span class="sxs-lookup"><span data-stu-id="05390-187"><span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**GUID\_IO\_VOLUME\_NAME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-188">2de9783-4c06-11d2-A532-00609713055a</span><span class="sxs-lookup"><span data-stu-id="05390-188">2de97f83-4c06-11d2-a532-00609713055a</span></span>
</dt> <dt>



<span data-ttu-id="05390-189">Der Volumename wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="05390-189">The volume name has been changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-190"><span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**GUID-e/a- \_ \_ Volume \_ benötigt \_ chkdsk**</span><span class="sxs-lookup"><span data-stu-id="05390-190"><span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**GUID\_IO\_VOLUME\_NEED\_CHKDSK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-191">799a0960-0a0b-4e03-ad88-2fa7c6ce748a</span><span class="sxs-lookup"><span data-stu-id="05390-191">799a0960-0a0b-4e03-ad88-2fa7c6ce748a</span></span>
</dt> <dt>



<span data-ttu-id="05390-192">Ein Dateisystem hat Beschädigungen auf dem Volume erkannt.</span><span class="sxs-lookup"><span data-stu-id="05390-192">A file system has detected corruption on the volume.</span></span> <span data-ttu-id="05390-193">Die Anwendung sollte CHKDSK auf dem Volume ausführen oder den Benutzer benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="05390-193">The application should run CHKDSK on the volume or notify the user to do so.</span></span>

<span data-ttu-id="05390-194">**Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05390-194">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-195"><span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**Änderung der \_ \_ \_ physischen \_ Konfiguration \_ des GUID IO-Volumes**</span><span class="sxs-lookup"><span data-stu-id="05390-195"><span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**GUID\_IO\_VOLUME\_PHYSICAL\_CONFIGURATION\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-196">2de9784-4c06-11d2-A532-00609713055a</span><span class="sxs-lookup"><span data-stu-id="05390-196">2de97f84-4c06-11d2-a532-00609713055a</span></span>
</dt> <dt>



<span data-ttu-id="05390-197">Die physische oder der aktuelle physische Zustand des Volumes hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="05390-197">The physical makeup or current physical state of the volume has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-198"><span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**GUID \_ IO- \_ Volume \_ Vorbereiten von \_ eject**</span><span class="sxs-lookup"><span data-stu-id="05390-198"><span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**GUID\_IO\_VOLUME\_PREPARING\_EJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-199">c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6</span><span class="sxs-lookup"><span data-stu-id="05390-199">c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6</span></span>
</dt> <dt>



<span data-ttu-id="05390-200">Das Dateisystem bereitet den abzurufenden Datenträger vor.</span><span class="sxs-lookup"><span data-stu-id="05390-200">The file system is preparing the disc to be ejected.</span></span> <span data-ttu-id="05390-201">Beispielsweise hält das Dateisystem einen Hintergrund Formatierungs Vorgang an oder schließt die Sitzung auf einem Write-Once-Medium.</span><span class="sxs-lookup"><span data-stu-id="05390-201">For example, the file system is stopping a background formatting operation or closing the session on write-once media.</span></span>

<span data-ttu-id="05390-202">**Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05390-202">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-203"><span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**\_ \_ \_ eindeutige \_ ID- \_ Änderung für GUID IO-Volume**</span><span class="sxs-lookup"><span data-stu-id="05390-203"><span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**GUID\_IO\_VOLUME\_UNIQUE\_ID\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-204">af39da42-6622-41f5-970b-139d092fa3d9</span><span class="sxs-lookup"><span data-stu-id="05390-204">af39da42-6622-41f5-970b-139d092fa3d9</span></span>
</dt> <dt>



<span data-ttu-id="05390-205">Der eindeutige Bezeichner des Volumes wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="05390-205">The volume's unique identifier has been changed.</span></span> <span data-ttu-id="05390-206">Weitere Informationen zum eindeutigen Bezeichner finden Sie unter [**eindeutige IOCTL \_ mountdev- \_ Abfrage- \_ \_ ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).</span><span class="sxs-lookup"><span data-stu-id="05390-206">For more information about the unique identifier, see [**IOCTL\_MOUNTDEV\_QUERY\_UNIQUE\_ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).</span></span>

<span data-ttu-id="05390-207">**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Wert wird erst ab Windows Server 2008 R2 und Windows 7 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05390-207">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported until Windows Server 2008 R2 and Windows 7.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-208"><span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**GUID \_ IO \_ Volume \_ Unlock**</span><span class="sxs-lookup"><span data-stu-id="05390-208"><span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**GUID\_IO\_VOLUME\_UNLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-209">9a8c3d68-d0cb-11d1-8fef -00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="05390-209">9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="05390-210">Das Volume wurde von einem anderen Prozess entsperrt.</span><span class="sxs-lookup"><span data-stu-id="05390-210">The volume has been unlocked by another process.</span></span> <span data-ttu-id="05390-211">Sie können ein oder mehrere Handles dafür öffnen.</span><span class="sxs-lookup"><span data-stu-id="05390-211">You may open one or more handles to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="05390-212"><span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**GUID \_ IO- \_ Volume wird \_ \_ ausgecheckt**</span><span class="sxs-lookup"><span data-stu-id="05390-212"><span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**GUID\_IO\_VOLUME\_WEARING\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05390-213">873113ca-1486-4508-82ac-c3b2e5297aaa</span><span class="sxs-lookup"><span data-stu-id="05390-213">873113ca-1486-4508-82ac-c3b2e5297aaa</span></span>
</dt> <dt>



<span data-ttu-id="05390-214">Das Medium wird ausgecheckt. Dieses Ereignis wird gesendet, wenn ein Dateisystem feststellt, dass die Fehlerrate eines Volumes zu hoch ist oder der Fehler Ersetzungs Speicher fast erschöpft ist.</span><span class="sxs-lookup"><span data-stu-id="05390-214">The media is wearing out. This event is sent when a file system determines that the error rate on a volume is too high, or its defect replacement space is almost exhausted.</span></span>

<span data-ttu-id="05390-215">**Windows Server 2003 und Windows XP:** Dieser Wert wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05390-215">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05390-216">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05390-216">Remarks</span></span>

<span data-ttu-id="05390-217">Beim Aufheben der Einbindung von GUID-e/a- **\_ \_ \_ Volume** und GUID io-e/a- **\_ \_ Volume \_ \_** werden fehlerhafte Ereignisse zusammen mit der **GUID \_ IO \_ Volume \_ Lock** und dem **GUID io-e/a-Volume \_ \_ \_ gesperrt \_**</span><span class="sxs-lookup"><span data-stu-id="05390-217">The **GUID\_IO\_VOLUME\_DISMOUNT** and **GUID\_IO\_VOLUME\_DISMOUNT\_FAILED** events are related, as are the **GUID\_IO\_VOLUME\_LOCK** and **GUID\_IO\_VOLUME\_LOCK\_FAILED** event.</span></span> <span data-ttu-id="05390-218">Durch die **GUID \_ IO \_ Volume \_ Dismount** und **GUID \_ IO \_ Volume \_ Lock** -Ereignisse wird angegeben, dass versucht wird, einen Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="05390-218">The **GUID\_IO\_VOLUME\_DISMOUNT** and **GUID\_IO\_VOLUME\_LOCK** events indicate that an operation is being attempted.</span></span> <span data-ttu-id="05390-219">Sie sollten auf die Ereignis Benachrichtigung reagieren und die ausgeführte Aktion aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="05390-219">You should act on the event notification, and record the action taken.</span></span> <span data-ttu-id="05390-220">Fehler beim Aufheben der Einbindung des **GUID \_ IO \_ \_ \_** -Volumes und beim fehl **\_ \_ \_ \_ geschlagenen GUID** -e/a-Volumen Sperr Vorgang auf einen Fehler beim Versuch</span><span class="sxs-lookup"><span data-stu-id="05390-220">The **GUID\_IO\_VOLUME\_DISMOUNT\_FAILED** and **GUID\_IO\_VOLUME\_LOCK\_FAILED** events indicate that the attempted operation failed.</span></span> <span data-ttu-id="05390-221">Anschließend können Sie mit Ihrem Datensatz die Aktionen rückgängig machen, die Sie als Reaktion auf den Vorgang durchgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="05390-221">You may then use your record to undo the actions you made in response to the operation.</span></span>

<span data-ttu-id="05390-222">Das **dbch \_ hdevnotify** -Mitglied der [**dev- \_ Broadcast- \_ handle**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) -Struktur gibt das betroffene Gerät an.</span><span class="sxs-lookup"><span data-stu-id="05390-222">The **dbch\_hdevnotify** member of the [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure indicates the affected device.</span></span> <span data-ttu-id="05390-223">Beachten Sie, dass es sich hierbei um das von [**registerdevicenotifizierung**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)zurückgegebene Geräte Benachrichtigungs Handle handelt, nicht um ein Volume</span><span class="sxs-lookup"><span data-stu-id="05390-223">Note that this is the device notification handle returned by [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), not a volume handle.</span></span> <span data-ttu-id="05390-224">Zum Ausführen von Vorgängen auf dem Volume ordnen Sie dieses handle dem entsprechenden volumehandle zu.</span><span class="sxs-lookup"><span data-stu-id="05390-224">To perform operations on the volume, map this handle to the corresponding volume handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="05390-225">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05390-225">Requirements</span></span>



| <span data-ttu-id="05390-226">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05390-226">Requirement</span></span> | <span data-ttu-id="05390-227">Wert</span><span class="sxs-lookup"><span data-stu-id="05390-227">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="05390-228">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05390-228">Minimum supported client</span></span><br/> | <span data-ttu-id="05390-229">Windows XP</span><span class="sxs-lookup"><span data-stu-id="05390-229">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="05390-230">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05390-230">Minimum supported server</span></span><br/> | <span data-ttu-id="05390-231">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="05390-231">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="05390-232">Header</span><span class="sxs-lookup"><span data-stu-id="05390-232">Header</span></span><br/>                   | <dl> <span data-ttu-id="05390-233"><dt>Ioevent. h</dt></span><span class="sxs-lookup"><span data-stu-id="05390-233"><dt>IoEvent.h</dt></span></span> </dl> |



 

