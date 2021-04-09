---
description: Definieren Sie den Satz von Aktionen für den ioctl-Speicher für den ioctl-Speicher, der die \_ \_ \_ \_ \_ Attribute des
ms.assetid: ff688c9a-8669-4699-aab9-1e2e3a5c7fca
title: DEVICE_DATA_MANAGEMENT_SET_ACTION (winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524d1dbd2ecf09dbcfa66fa766089dde7cf04a0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861104"
---
# <a name="device_data_management_set_action"></a>Aktion für Geräte \_ Daten- \_ Verwaltungs \_ Gruppe \_

Bei den folgenden Konstanten Werten handelt es sich um den Satz möglicher Werte für den **\_ \_ \_ \_ Aktionstyp für die Gerätedaten Verwaltung** , der als **DWORD**-Typ definiert ist.

<dl> <dt>

<span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**Devicedsmaction \_ None**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Es wird keine Aktion ausgeführt.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**Devicedsmaction \_ Trim**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Eine Trim-Aktion wird ausgeführt.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**Devicedsmaction- \_ Benachrichtigung**
</dt> <dd> <dl> <dt>

2 \| **devicedsmaktionflag \_ nicht destruktiv** (0x80000002)
</dt> <dt>



Eine Benachrichtigungs Aktion wird ausgeführt. Die Parameter sind in einer [**Geräte- \_ DSM- \_ Benachrichtigungs \_ Parameter**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) -Struktur. Das **\_ nicht destruktiv devicedsmaktionflag** (0x80000000) ist ein Bitflag, das dem Treiber Stapel anzeigt, dass dieser Vorgang nicht destruktiv ist.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**Devicedsmaction \_ offloadread**
</dt> <dd> <dl> <dt>

3 \| **devicedsmaktionflag \_ nicht destruktiv** (0x80000003)
</dt> <dt>



Eine Auslagerungs Leseaktion wird ausgeführt. Die Parameter befinden sich in einer Struktur der AD- [**\_ \_ \_ Auslagerungs Lese \_ Parameter für Geräte**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) . Die Ausgabe befindet sich in einer [**Speicher \_ \_ Auslastungs \_ Ausgabe**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) Struktur. Das **\_ nicht destruktiv devicedsmaktionflag** (0x80000000) ist ein Bitflag, das dem Treiber Stapel anzeigt, dass dieser Vorgang nicht destruktiv ist.

**Windows 7 und Windows Server 2008 R2:** Dieser Wert wird vor Windows 8 und Windows Server 2012 nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**Devicedsmaction \_ offloadwrite**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Eine Auslagerungs Schreibaktion wird ausgeführt. Die Parameter befinden sich in einer [**Geräte- \_ DSM- \_ Offload- \_ Schreib \_ Parameter**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) Struktur. Die Ausgabe befindet sich in einer [**Speicher \_ Auslastungs- \_ Schreib \_ Ausgabe**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) Struktur.

**Windows 7 und Windows Server 2008 R2:** Dieser Wert wird vor Windows 8 und Windows Server 2012 nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**Devicedsmaction- \_ Zuordnung**
</dt> <dd> <dl> <dt>

5 \| **devicedsmaktionflag \_ nicht destruktiv** (0x80000005)
</dt> <dt>



Eine Zuordnungs Bitmap wird für den ersten Daten Satz Bereich zurückgegeben, der übergeben wird. Die Ausgabe befindet sich in [**einer \_ \_ \_ \_ Bereitstellungs \_ Zustands**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) Struktur für das Geräte Dataset lb. Das **\_ nicht destruktiv devicedsmaktionflag** (0x80000000) ist ein Bitflag, das dem Treiber Stapel anzeigt, dass dieser Vorgang nicht destruktiv ist.

**Windows 7 und Windows Server 2008 R2:** Dieser Wert wird vor Windows 8 und Windows Server 2012 nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**Devicedsmaction- \_ Reparatur**
</dt> <dd> <dl> <dt>

6 \| **devicedsmaktionflag \_ nicht destruktiv** (0x80000006)
</dt> <dt>



Eine Reparaturaktion wird ausgeführt. Das **\_ nicht destruktiv devicedsmaktionflag** (0x80000000) ist ein Bitflag, das dem Treiber Stapel anzeigt, dass dieser Vorgang nicht destruktiv ist.

**Windows 7 und Windows Server 2008 R2:** Dieser Wert wird vor Windows 8 und Windows Server 2012 nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**Devicedsmaction-Bereinigung \_**
</dt> <dd> <dl> <dt>

7 \| **devicedsmaktionflag \_ nicht destruktiv** (0x80000007)
</dt> <dt>



Eine Bereinigungsaktion wird ausgeführt. Das **\_ nicht destruktiv devicedsmaktionflag** (0x80000000) ist ein Bitflag, das dem Treiber Stapel anzeigt, dass dieser Vorgang nicht destruktiv ist.

**Windows 7 und Windows Server 2008 R2:** Dieser Wert wird vor Windows 8 und Windows Server 2012 nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**Devicedsmaction- \_ Resilienz**
</dt> <dd> <dl> <dt>

8 \| **devicedsmaktionflag \_ nicht destruktiv** (0x80000008)
</dt> <dt>



Eine resilienzaktion wird ausgeführt. Das **\_ nicht destruktiv devicedsmaktionflag** (0x80000000) ist ein Bitflag, das dem Treiber Stapel anzeigt, dass dieser Vorgang nicht destruktiv ist.

**Windows 7 und Windows Server 2008 R2:** Dieser Wert wird vor Windows 8 und Windows Server 2012 nicht unterstützt.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                                         |
| Header<br/>                   | <dl> <dt>Winioctl. h (Include Windows. h)</dt> </dl> |



 

 




