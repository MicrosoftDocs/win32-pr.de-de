---
description: Stellt die korrigierte CmC-Behandlung (Machine Check) dar, die vom Interrupttreiber zum Abruf umgeschaltet werden soll. Diese Klasse ist nur in 64-Bit-Systemen Windows verfügbar.
ms.assetid: c5e99e13-0f65-40bc-8863-b2ca7ea221df
title: MSMCAEvent_SwitchToCMCPolling-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SwitchToCMCPolling
- MSMCAEvent_SwitchToCMCPolling.Active
- MSMCAEvent_SwitchToCMCPolling.InstanceName
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: a8192dc83a50063b2aaabba2bf708053fadb8e094bfa1cab82b11b084f722a76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640940"
---
# <a name="msmcaevent_switchtocmcpolling-class"></a>MSMCAEvent \_ SwitchToCMCPolling-Klasse

Die **MSMCAEvent \_ SwitchToCMCPolling-Klasse** stellt die korrigierte CmC-Behandlung (Machine Check) dar, die vom Interrupttreiber zum Abruf umgeschaltet werden soll. In einigen Fällen wird die Systemabstraktionsschicht (SYSTEM Abstraction Layer, SAL) vom Kernel nach cmc- oder korrigierten Plattformfehlern (CPE) im vorherigen Abrufintervall abbestellen. Diese Klasse ist nur in 64-Bit-Systemen Windows verfügbar.

Die folgende Syntax wird durch Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
class MSMCAEvent_SwitchToCMCPolling : WMIEvent
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Member

Die **MSMCAEvent \_ SwitchToCMCPolling-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSMCAEvent \_ SwitchToCMCPolling-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**TRUE**, wenn diese Instanz der -Klasse aktiv ist; andernfalls **FALSE**.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Eindeutiger Bezeichner dieser Instanz der -Klasse.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **MSMCAEvent \_ SwitchToCMCPolling-Klasse** wird von [**WMIEvent abgeleitet.**](wmievent.md)

Die Systemabstraktionsschicht (SYSTEM Abstraction Layer, SAL) ist Code, der auf ROM glüht, den das Betriebssystem aufruft, um plattformabhängige Vorgänge durchzuführen. Dies ähnelt dem BIOS auf einer x86-Plattform. In Fällen, in denen die Plattform keine Unterbrechungen für CMC- oder CPE-Abrufe unterstützt, wird vom Betriebssystem jede Minute eine Abfrage ausgeführt, und es wird überprüft, ob zuvor ein Fehler aufgetreten ist. Wenn die Plattform Unterbrechungen unterstützt und das Betriebssystem innerhalb einer Minute eine benutzerdefinierte Menge von CMC- oder CPE-Abrufen erhält, deaktiviert sie den Interrupt und den Abruf. Wenn der Benutzer die Anzahl der Umfragen nicht innerhalb einer Minute definiert, legt das System standardmäßig 10 Umfragen pro Minute fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                         |
| Namespace<br/>                | Root \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MSMCA-Klassen](msmca-classes.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

