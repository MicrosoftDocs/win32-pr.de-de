---
title: Win32_SessionBrokerTargetEvent-Klasse
description: Stellt eine Änderung an einem Sitzungs Broker Ziel dar.
ms.assetid: ee3ae0ed-eb8b-4777-9b9e-0e50722cf52a
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerTargetEvent-Klasse Remotedesktopdienste
- Win32_SessionBrokerTargetEvent Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTargetEvent
- Win32_SessionBrokerTargetEvent.SECURITY_DESCRIPTOR
- Win32_SessionBrokerTargetEvent.TIME_CREATED
- Win32_SessionBrokerTargetEvent.ChangeType
- Win32_SessionBrokerTargetEvent.PluginName
- Win32_SessionBrokerTargetEvent.TargetName
- Win32_SessionBrokerTargetEvent.FarmName
- Win32_SessionBrokerTargetEvent.Guid
- Win32_SessionBrokerTargetEvent.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d7f1cf6aab1c4497ce85cb93318c9ca79368853
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740704"
---
# <a name="win32_sessionbrokertargetevent-class"></a>Win32 \_ sessionbrokertargetevent-Klasse

Stellt eine Änderung an einem Sitzungs Broker Ziel dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class Win32_SessionBrokerTargetEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint32 ChangeType;
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a>Member

Die Win32-Klasse " **\_ sessionbrokertargetevent** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ sessionbrokertargetevent** " verfügt über diese Eigenschaften.

<dl> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die aufgetretene Änderung an. Dies kann einer der folgenden Werte sein:

<dt>

1 (0x1)
</dt> <dd>

Der Typ der Änderung ist nicht angegeben.

</dd> <dt>

2 (0x2)
</dt> <dd>

Die externe IP-Adresse hat sich geändert.

</dd> <dt>

4 (0x4)
</dt> <dd>

Die interne IP-Adresse hat sich geändert.

</dd> <dt>

8 (0x8)
</dt> <dd>

Das Ziel wurde verknüpft.

</dd> <dt>

16 (0x10)
</dt> <dd>

Das Ziel wurde entfernt.

</dd> <dt>

32 (0x20)
</dt> <dd>

Der Status des Ziels hat sich geändert.

</dd> <dt>

64 (0x40)
</dt> <dd>

Das Ziel befindet sich im Leerlauf.

</dd> </dl>

</dd> <dt>

**Umgebung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Umgebungsname. Bei einem Ziel eines virtuellen Computers (VM) kann dies der VM-hostname sein.

**Windows Server 2008 R2:** Diese Eigenschaft ist vor Windows Server 2012 nicht verfügbar.

</dd> <dt>

**Farmname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Farm, zu der das Ziel gehört.

**Windows Server 2008 R2:** Diese Eigenschaft ist vor Windows Server 2012 nicht verfügbar.

</dd> <dt>

**GUID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die GUID des Ziels.

**Windows Server 2008 R2:** Diese Eigenschaft ist vor Windows Server 2012 nicht verfügbar.

</dd> <dt>

**PluginName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Plug-ins.

**Windows Server 2008 R2:** Diese Eigenschaft ist vor Windows Server 2012 nicht verfügbar.

</dd> <dt>

**Sicherheits \_ Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](/windows/desktop/WmiSdk/--event)geerbt. Weitere Informationen zu Konstanten, die verwendet werden, um diese Sicherheits Beschreibung festzulegen, finden Sie unter [WMI-Sicherheits Konstanten](/windows/desktop/WmiSdk/wmi-security-constants).

</dd> <dt>

**TargetName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Ziels.

**Windows Server 2008 R2:** Diese Eigenschaft ist vor Windows Server 2012 nicht verfügbar.

</dd> <dt>

**\_Erstellungszeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde. Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt. Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](/windows/desktop/WmiSdk/--event)geerbt.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>"Tssdwmi. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

