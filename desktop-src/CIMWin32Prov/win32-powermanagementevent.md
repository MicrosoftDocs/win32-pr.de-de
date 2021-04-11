---
description: Das Win32- \_ powermanagementevent-&\# 32; Die WMI-Klasse stellt Energie Verwaltungs Ereignisse dar, die sich aus Energie Zustandsänderungen ergeben.
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
ms.openlocfilehash: e0e7dfa68646dbefb6d6b70218fe99830b44a0c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126841"
---
# <a name="win32_powermanagementevent-class"></a>Win32- \_ Klasse "powermanagementevent"

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ powermanagementevent** " stellt Energie Verwaltungs Ereignisse dar, die sich aus Energie Zustandsänderungen ergeben. Diese Zustandsänderungen sind entweder mit der Advanced Power Management (APM)-oder der Advanced Configuration and Power Interface (ACPI)-System Verwaltungs Protokolle verknüpft.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die Win32-Klasse " **\_ powermanagementevent** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ powermanagementevent** " verfügt über diese Eigenschaften.

<dl> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Energie Verwaltungs Ereignisse")
</dt> </dl>

Der Typ der Änderung im System Energiezustand.

<dt>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>Wechseln **in Suspend** (4)


</dt> <dd>

Der Computer ist zwar angehalten, scheint aber deaktiviert zu sein. Allerdings kann Sie als Reaktion auf verschiedene Ereignisse wie Benutzereingaben (z. b. bewegen der Maus oder Drücken einer Taste auf der Tastatur) als "erwacht" angezeigt werden. Während der Computer angehalten wird, wird der Stromverbrauch auf eine von mehreren Ebenen reduziert, je nachdem, wie das System verwendet werden soll. Je niedriger die Stromverbrauchs Ebene, desto länger dauert es, bis das System wieder in den Arbeitszustand wechselt. Wenn der Computer in den anhaltezustand wechselt, wird der Desktop gesperrt, und Sie müssen STRG + ALT + ENTF drücken und einen gültigen Benutzernamen und ein gültiges Kennwort angeben, um den Vorgang fortzusetzen.

</dd> <dt>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>Fortsetzen **von Suspend** (7)


</dt> <dd>

Gibt an, dass eine Nachricht zum Fortsetzen des Anhaltevorgangs gesendet wurde, sodass der Computer seinen regulären Energiezustand wiederherstellen kann.

</dd> <dt>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**Energie Status Änderung** (10)


</dt> <dd>

Gibt an, dass der Energiestatus des Computers geändert wird, z. b. ein Wechsel von Akku Strom in die Stromversorgung oder von einem Wechsel zu einer unterbrechungsfreien Stromversorgung. Das System leitet dieses Ereignis auch dann weiter, wenn die verbleibende Akkuleistung unter einen vom Benutzer festgelegten Wert sinkt oder sich um einen angegebenen Prozentsatz ändert.

</dd> <dt>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**OEM-Ereignis** (11)


</dt> <dd>

Gibt an, dass ein APM-BIOS (Advanced Power Management) ein OEM-Ereignis gesendet hat. Der Wert des Ereignisses wird in der Eigenschaft " **OEMEventCode** " aufgezeichnet. Da einige APM-BIOS-Implementierungen keine OEM-Ereignis Benachrichtigungen bereitstellen, wird dieses Ereignis möglicherweise nie auf einigen Computern übertragen. APM ist ein Legacy-Energie Verwaltungs Schema. Apm wird zwar weiterhin unterstützt, ist jedoch größtenteils durch ACPI abgelöst (Erweiterte Konfiguration und Energie Schnittstelle).

</dd> <dt>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**Automatisch** fortsetzen (18)


</dt> <dd>

Gibt an, dass der Computer als Reaktion auf ein Ereignis erwacht ist. Wenn das Systembenutzer Aktivitäten erkennt (z. b. einen Mausklick), wird die resumesuspend-Nachricht gesendet, sodass die Anwendungen wissen, dass Sie die vollständige Interaktivität mit dem Benutzer fortsetzen können.

</dd> </dl>

</dd> <dt>

**"OEMEventCode"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Energie Verwaltungs Ereignisse")
</dt> </dl>

Der vom Originalgerätehersteller (OEM) definierte System Energiezustand, wenn die **eventType** -Eigenschaft dieser Klasse auf 11 (OEM-Ereignis) festgelegt ist. Andernfalls wird diese Eigenschaft auf **null** festgelegt. OEM-Ereignisse werden generiert, wenn ein APM-BIOS ein APM-OEM-Ereignis signalisiert. OEM-Ereignis Codes liegen im Bereich 0x0200h-0x02ffh.

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

Die Win32-Klasse " **\_ powermanagementevent** " ist von " [**\_ \_ ExtrinsicEvent**](../wmisdk/--extrinsicevent.md)" abgeleitet.

Änderungen am Energiestatus weisen häufig darauf hin, dass ein Problem mit einem Computer oder mit einem anderen verwalteten Gerät aufgetreten ist. Wenn ein Server plötzlich von der Stromversorgung zu einer unterbrechungsfreien Stromversorgung wechselt, kann diese Änderung darauf hindeuten, dass ein elektrisches Problem aufgetreten ist, entweder mit dem Computer selbst oder mit dem elektrischen System in dem Raum, in dem der Computer aufbewahrt wird.

Administratoren müssen diese Änderungen im Energiestatus überwachen und sofort über solche Änderungen benachrichtigt werden. Dadurch können Sie Maßnahmen ergreifen, bevor das Gerät die Stromversorgung vollständig verliert. (Unterbrechungsfreie Stromversorgungssysteme können z. b. nur für 15 Minuten oder vor dem Herunterfahren ausgeführt werden.)

Die Win32-Klasse " **\_ powermanagementevent** " kann verwendet werden, um Änderungen des Energiestatus auf einem Computer zu überwachen. Diese Änderungen können einen Wechsel von einer Stromquelle zu einer anderen und eine Änderung des Energie Zustands des Computers (z. b. Eingabe oder Beenden des anhaltemodus) einschließen.

Die Win32-Klasse " **\_ powermanagementevent** " hat nur zwei Eigenschaften: EventType, mit dem der Typ des aufgetretenen Energie Änderungs Ereignisses angegeben wird, und "oemeventtype", der von einigen Originalgeräte Herstellern verwendet wird, um zusätzliche Energie Änderungs Ereignisse zu definieren.

Weitere Informationen zum reagieren auf Windows-Energie Ereignisse finden Sie im Artikel [überwachen und reagieren auf Windows powerevents mit PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) auf der Scripting Guy! .

## <a name="examples"></a>Beispiele

Das folgende VBScript überwacht die Änderungen des Energiestatus auf einem Computer.


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
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_ExtrinsicEvent**](../wmisdk/--extrinsicevent.md)
</dt> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> <dt>

[Überwachen von Änderungen im Energie Status des Computers](/previous-versions/tn-archive/ee176537(v=technet.10))
</dt> </dl>

 

 
