---
description: Win32 \_ PowerManagementEvent &\# 32; Die WMI-Klasse stellt Energieverwaltungsereignisse dar, die sich aus Energiezustandsänderungen ergeben.
ms.assetid: b5781805-87c7-4eaf-afbb-a1770fcff41c
ms.tgt_platform: multiple
title: Win32_PowerManagementEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PowerManagementEvent
- Win32_PowerManagementEvent.SECURITY_DESCRIPTOR
- Win32_PowerManagementEvent.TIME_CREATED
- Win32_PowerManagementEvent.EventType
- Win32_PowerManagementEvent.OEMEventCode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 536963be51d665b03af77bb81c7592b44d2a6eb5ddc449bfa82896dd7f7da9b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064420"
---
# <a name="win32_powermanagementevent-class"></a>Win32 \_ PowerManagementEvent-Klasse

Die **WMI-Klasse \_ Win32 PowerManagementEvent** stellt Energieverwaltungsereignisse dar, die sich aus Energiezustandsänderungen ergeben. [](../wmisdk/retrieving-a-class.md) Diese Zustandsänderungen sind entweder den Systemverwaltungsprotokollen Advanced Power Management (APM) oder Advanced Configuration and Power Interface (ACPI) zugeordnet.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[UUID("{86460B6B-E709-11d2-B139-00105A1F77A1}"), AMENDMENT]
class Win32_PowerManagementEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
  uint16 OEMEventCode;
};
```

## <a name="members"></a>Member

Die **Win32 \_ PowerManagementEvent-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ PowerManagementEvent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Energieverwaltungsereignisse") \|
</dt> </dl>

Typ der Änderung des Systemleistungszustands.

<dt>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>**Eingabe von "Suspend"** (4)


</dt> <dd>

Wenn der Computer angehalten ist, scheint er ausgeschaltet zu sein. Sie kann jedoch als Reaktion auf verschiedene Ereignisse "erweckt" werden, einschließlich Benutzereingaben (z. B. Bewegen der Maus oder Drücken einer Taste auf der Tastatur). Während der Computer angehalten ist, wird der Stromverbrauch je nach Verwendung des Systems auf eine von mehreren Ebenen reduziert. Desto geringer der Stromverbrauch, desto mehr Zeit benötigt das System, um in den Betriebszustand zurückzukehren. Wenn der Computer in den Zustand "Angehalten" eintritt, ist der Desktop gesperrt, und Sie müssen STRG+ALT+DELETE drücken und einen gültigen Benutzernamen und ein Kennwort angeben, um Vorgänge fortsetzen zu können.

</dd> <dt>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>**Fortsetzen von "Suspend"** (7)


</dt> <dd>

Gibt an, dass eine Nachricht Vom Angehalten fortsetzen gesendet wurde, sodass der Computer wieder in den normalen Energiezustand zurückkehren kann.

</dd> <dt>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**Energiestatusänderung** (10)


</dt> <dd>

Gibt eine Änderung des Energiestatus des Computers an, z. B. einen Wechsel vom Akkustrom zum Wechselstrom oder vom Wechselstrom in eine unterbrechungsfreie Stromversorgung. Das System leitet dieses Ereignis auch dann weiter, wenn die verbleibende Akkuleistung unter einen vom Benutzer festgelegten Wert sinkt oder sich um einen angegebenen Prozentsatz ändert.

</dd> <dt>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**OEM-Ereignis** (11)


</dt> <dd>

Gibt an, dass Advanced Power Management -BIOS (APM) ein OEM-Ereignis gesendet hat. Der Wert des Ereignisses wird in der **OEMEventCode-Eigenschaft** erfasst. Da einige APM-BIOS-Implementierungen keine OEM-Ereignisbenachrichtigungen bereitstellen, wird dieses Ereignis möglicherweise nie auf einigen Computern übertragen. APM ist ein älteres Energieverwaltungsschema. APM wird zwar weiterhin unterstützt, wurde jedoch größtenteils durch ACPI (Advanced Configuration and Power Interface) ersetzt.

</dd> <dt>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**Automatisch fortsetzen** (18)


</dt> <dd>

Gibt an, dass der Computer als Reaktion auf ein Ereignis wiedererweckt wurde. Wenn das System Benutzeraktivitäten erkennt (z. B. einen Mausklick), wird die ResumeSuspend-Nachricht übertragen, damit Anwendungen wissen, dass sie die vollständige Interaktivität mit dem Benutzer fortsetzen können.

</dd> </dl>

</dd> <dt>

**OEMEventCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Energieverwaltungsereignisse") \|
</dt> </dl>

Vom Originalgerätehersteller (Original Equipment Manufacturer, OEM) definierter Systemleistungszustand, wenn die **EventType-Eigenschaft** dieser Klasse auf 11 (OEM-Ereignis) festgelegt ist; Andernfalls wird diese Eigenschaft auf **NULL festgelegt.** OEM-Ereignisse werden generiert, wenn ein APM-BIOS ein APM-OEM-Ereignis signalisiert. OEM-Ereigniscodes liegen im Bereich von 0x0200h bis 0x02FFH.

</dd> <dt>

**\_SICHERHEITSDESKRIPTOR**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignisanbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird vom Ereignis [**\_ \_ geerbt.**](../wmisdk/--event.md) Weitere Informationen zu Konstanten, die zum Festlegen dieses Sicherheitsdeskriptors verwendet werden, finden Sie unter [WMI-Sicherheitskonst constants](../wmisdk/wmi-security-constants.md).

</dd> <dt>

**ZEIT \_ ERSTELLT**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der den Zeitpunkt angibt, zu dem das Ereignis generiert wurde. Dies ist ein 64-Bit-Wert, der die Anzahl von 100-Nanosekunden-Intervallen nach dem 1. Januar 1601 darstellt. Die Informationen sind im UTC-Format (Coordinated Universal Times) angegeben.

Diese Eigenschaft wird vom Ereignis [**\_ \_ geerbt.**](../wmisdk/--event.md)

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](../wmisdk/creating-a-wmi-script.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ PowerManagementEvent-Klasse** wird von [**\_ \_ ExtrinsicEvent abgeleitet.**](../wmisdk/--extrinsicevent.md)

Änderungen am Energiestatus deuten häufig darauf hin, dass ein Problem mit einem Computer oder einem anderen verwalteten Gerät aufgetreten ist. Wenn ein Server plötzlich von der Stromversorgung zu einer unterbrechungsfreie Stromversorgung wechselt, kann diese Änderung darauf hindeuten, dass ein elektrisches Problem aufgetreten ist, entweder mit dem Computer selbst oder mit dem elektrischen System in dem Raum, in dem sich der Computer befindet.

Administratoren müssen diese Änderungen im Energiestatus überwachen und sofort über solche Änderungen benachrichtigt werden. Dies ermöglicht es ihnen, Maßnahmen zu ergreifen, bevor das Gerät die Stromversorgung vollständig verliert. (Unterbrechungsfreie Stromversorgungssysteme können z. B. nur 15 Minuten lang ausgeführt werden, bevor sie heruntergefahren werden.)

Die **Win32 \_ PowerManagementEvent-Klasse** kann verwendet werden, um Änderungen am Energiestatus auf einem Computer zu überwachen. Diese Änderungen können einen Wechsel von einer Stromquelle zu einer anderen sowie eine Änderung des Computerbetriebszustands (z. B. das Starten oder Beenden des Modus "Aussetzen") umfassen.

Die **Win32 \_ PowerManagementEvent-Klasse** verfügt nur über zwei Eigenschaften: EventType, der verwendet wird, um den Typ des aufgetretenen Stromänderungsereignisses anzugeben, und OEMEventType, der von einigen Originalgeräteherstellern verwendet wird, um zusätzliche Stromänderungsereignisse zu definieren.

Weitere Informationen zum Reagieren auf Windows Power Events finden Sie im Artikel Überwachen und Reagieren auf Windows [Power Events mit PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) unter Hey! Scripting Guy! .

## <a name="examples"></a>Beispiele

Das folgende VBScript überwacht Änderungen am Energiestatus auf einem Computer.


```VB
Set colMonitoredEvents = GetObject("winmgmts:")._
 ExecNotificationQuery("SELECT * FROM Win32_PowerManagementEvent")
Do
 Set strLatestEvent = colMonitoredEvents.NextEvent
 Wscript.Echo strLatestEvent.EventType
Loop
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_ExtrinsicEvent**](../wmisdk/--extrinsicevent.md)
</dt> <dt>

[Hardwareklassen des Computersystems](computer-system-hardware-classes.md)
</dt> <dt>

[Überwachen von Änderungen am Computerleistungsstatus](/previous-versions/tn-archive/ee176537(v=technet.10))
</dt> </dl>

 

 
