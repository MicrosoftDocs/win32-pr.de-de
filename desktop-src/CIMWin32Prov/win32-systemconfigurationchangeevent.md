---
description: Win32 \_ SystemConfigurationChangeEvent&\# 8194; Die WMI-Klasse gibt an, dass die Geräteliste auf dem System aktualisiert wurde (ein Gerät wurde hinzugefügt oder entfernt oder die Konfiguration geändert).
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
ms.openlocfilehash: 63a0708f2e081ffc8c5fb359be1e57aacd1cd62bd1db1daee2063e66e2fb55c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751300"
---
# <a name="win32_systemconfigurationchangeevent-class"></a>Win32 \_ SystemConfigurationChangeEvent-Klasse

Die  [WMI-Klasse](../wmisdk/retrieving-a-class.md) **Win32 \_ SystemConfigurationChangeEvent** gibt an, dass die Geräteliste auf dem System aktualisiert wurde (ein Gerät wurde hinzugefügt oder entfernt oder die Konfiguration geändert). Ein Ereignis wird ausgelöst, und eine Instanz dieser Klasse wird erstellt, wenn die Meldung "DevMgrRefreshOn<*ComputerName*>" gesendet wird. Die genaue Änderung an der Geräteliste ist nicht in der Meldung enthalten, sodass eine Geräteaktualisierung erforderlich ist, um die aktuellen Systemeinstellungen abzurufen. Beispiele für betroffene Konfigurationsänderungen sind IRQ-Einstellungen, COM-Ports und BIOS-Versionen.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge sortiert.

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

Die **Win32 \_ SystemConfigurationChangeEvent-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ SystemConfigurationChangeEvent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages \| WM \_ DEVICECHANGE \| wParam", "Win32APIDevice Management Messages \| WM \_ SETTINGCHANGE")
</dt> </dl>

Typ der aufgetretenen Ereignisänderungsbenachrichtigung.

Diese Eigenschaft wird von [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md)geerbt.

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

**Konfiguration geändert** (1)


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

**Geräteankunft** (2)


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

**Geräteentfernung** (3)


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

**Andocken** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**\_SICHERHEITSBESCHREIBUNG**
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignisanbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird von [**\_ \_ Ereignis**](../wmisdk/--event.md)geerbt. Weitere Informationen zu Konstanten, die zum Festlegen dieser Sicherheitsbeschreibung verwendet werden, finden Sie unter [WMI-Sicherheitskonstanten.](../wmisdk/wmi-security-constants.md)

</dd> <dt>

**TIME \_ CREATED**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der den Zeitpunkt angibt, zu dem das Ereignis generiert wurde. Dies ist ein 64-Bit-Wert, der die Anzahl von 100-Nanosekunden-Intervallen nach dem 1. Januar 1601 darstellt. Die Informationen liegen im UTC-Format (Coordinated Universal Times) vor.

Diese Eigenschaft wird von [**\_ \_ Ereignis**](../wmisdk/--event.md)geerbt.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](../wmisdk/creating-a-wmi-script.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ SystemConfigurationChangeEvent-Klasse** wird von [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md)
</dt> <dt>

[Betriebssystemklassen](./operating-system-classes.md)
</dt> </dl>

 

 
