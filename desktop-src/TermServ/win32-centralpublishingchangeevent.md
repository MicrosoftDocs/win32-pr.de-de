---
title: Win32_CentralPublishingChangeEvent-Klasse
description: Ein Ereignis, das eine Änderung der zentralen RDV-Einstellungen darstellt.
ms.assetid: 95be015e-a185-4548-a7f7-a22b351a34c8
ms.tgt_platform: multiple
keywords:
- Win32_CentralPublishingChangeEvent-Remotedesktopdienste
- Win32_CentralPublishingChangeEvent klasse Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- Win32_CentralPublishingChangeEvent
- Win32_CentralPublishingChangeEvent.SECURITY_DESCRIPTOR
- Win32_CentralPublishingChangeEvent.TIME_CREATED
- Win32_CentralPublishingChangeEvent.TargetInstance
- Win32_CentralPublishingChangeEvent.OperationType
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bbc38d132920bd5ffcaa2208d8f1aa94c8629bb0c5399f6b8776654d078cd47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868520"
---
# <a name="win32_centralpublishingchangeevent-class"></a>Win32 \_ CentralPublishingChangeEvent-Klasse

Ein Ereignis, das eine Änderung der zentralen RDV-Einstellungen darstellt.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
class Win32_CentralPublishingChangeEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  object TargetInstance;
  uint32 OperationType;
};
```

## <a name="members"></a>Member

Die **Win32 \_ CentralPublishingChangeEvent-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ CentralPublishingChangeEvent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**OperationType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Vorgangstyp, der dem Ereignis entspricht.

<dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

**Erstellen** (0)


</dt> <dd></dd> <dt>

<span id="Modify"></span><span id="modify"></span><span id="MODIFY"></span>

**Ändern** (1)


</dt> <dd></dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>

**Löschen** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**\_SICHERHEITSDESKRIPTOR**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignisanbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird vom Ereignis [**\_ \_ geerbt.**](/windows/desktop/WmiSdk/--event) Weitere Informationen zu Konstanten, die zum Festlegen dieses Sicherheitsdeskriptors verwendet werden, finden Sie unter [WMI-Sicherheitskonst constants](/windows/desktop/WmiSdk/wmi-security-constants).

</dd> <dt>

**TargetInstance**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Objekt wurde durch den Vorgang geändert, der dem Ereignis entspricht.

</dd> <dt>

**ZEIT \_ ERSTELLT**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der den Zeitpunkt angibt, zu dem das Ereignis generiert wurde. Dies ist ein 64-Bit-Wert, der die Anzahl von 100-Nanosekunden-Intervallen nach dem 1. Januar 1601 darstellt. Die Informationen sind im UTC-Format (Coordinated Universal Times) angegeben. Diese Eigenschaft wird vom Ereignis [**\_ \_ geerbt.**](/windows/desktop/WmiSdk/--event)

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                           |
| Namespace<br/>                | Root \\ cimv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>Tscpub.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TscPubWmi.dll</dt> </dl> |



 

