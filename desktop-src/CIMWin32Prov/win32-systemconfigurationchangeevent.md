---
description: Das Win32 \_ systemconfigurationchangeevent-&\# 8194; WMI-Klasse gibt an, dass die Geräteliste im System aktualisiert wurde (ein Gerät wurde hinzugefügt oder entfernt, oder die Konfiguration wurde geändert).
ms.assetid: dce1e866-e739-4f90-9016-48b20ccfb75b
ms.tgt_platform: multiple
title: Win32_SystemConfigurationChangeEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemConfigurationChangeEvent
- Win32_SystemConfigurationChangeEvent.SECURITY_DESCRIPTOR
- Win32_SystemConfigurationChangeEvent.TIME_CREATED
- Win32_SystemConfigurationChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0bc479d3415906a6536c6df1d163056e94e2af76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127444"
---
# <a name="win32_systemconfigurationchangeevent-class"></a>Win32 \_ systemconfigurationchangeevent-Klasse

Die **Win32 \_ systemconfigurationchangeevent** [WMI-Klasse](../wmisdk/retrieving-a-class.md) gibt an, dass die Geräteliste im System aktualisiert wurde (ein Gerät wurde hinzugefügt oder entfernt, oder die Konfiguration wurde geändert). Ein Ereignis wird ausgelöst, und eine Instanz dieser Klasse wird erstellt, wenn die Meldung "devmgrerfrischendes on<*Computername*>" gesendet wird. Die genaue Änderung der Geräteliste ist nicht in der Nachricht enthalten. Daher ist eine Geräte Aktualisierung erforderlich, um die aktuellen Systemeinstellungen zu erhalten. Es folgen Beispiele für Änderungen an der Konfiguration, die sich auf die Einstellungen von "Iran", com-Ports und BIOS

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[UUID("76746942-D94B-47E2-BBA4-AFD2FDBA61"), AMENDMENT]
class Win32_SystemConfigurationChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a>Member

Die **Win32 \_ systemconfigurationchangeevent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ systemconfigurationchangeevent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages \| WM \_ devicechange \| wParam", "Win32APIDevice Management Messages \| WM \_ settingchange")
</dt> </dl>

Der Typ der Ereignis Änderungs Benachrichtigung, die aufgetreten ist.

Diese Eigenschaft wird von [**Win32 \_ devicechangeevent**](win32-devicechangeevent.md)geerbt.

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

**Konfiguration geändert** (1)


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

**Geräte Ankunft** (2)


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

**Entfernen von Geräten** (3)


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

**Andocken** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**Sicherheits \_ Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](../wmisdk/--event.md)geerbt. Weitere Informationen zu Konstanten, die verwendet werden, um diese Sicherheits Beschreibung festzulegen, finden Sie unter [WMI-Sicherheits Konstanten](../wmisdk/wmi-security-constants.md).

</dd> <dt>

**\_Erstellungszeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde. Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt. Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor.

Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](../wmisdk/--event.md)geerbt.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32 \_ systemconfigurationchangeevent** -Klasse wird von [**Win32 \_ devicechangeevent**](win32-devicechangeevent.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ devicechangeevent**](win32-devicechangeevent.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
