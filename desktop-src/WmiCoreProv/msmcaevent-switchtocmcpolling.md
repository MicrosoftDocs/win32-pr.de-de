---
description: Stellt die Überprüfung der korrigierten Computer Überprüfung (CMC) dar, die vom Interrupt-Treiber zum Abrufen gewechselt werden soll. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
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
ms.openlocfilehash: f7d0d543dc36054550d4ddf6cc1a77ce80cf1647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343448"
---
# <a name="msmcaevent_switchtocmcpolling-class"></a>Msmcaevent \_ switchdecmcabruf-Klasse

Die **msmcaevent \_ switchdecmcabruf** -Klasse stellt die SMTP-Verarbeitung (korrigiert Machine Check) dar, die vom Interrupt-Treiber zum Abrufen gewechselt werden soll. In einigen Fällen fragt der Kernel die System Abstraktionsschicht (System Abstraktion Layer, SAL) nach einem beliebigen oder korrigierten Platt Formfehler (CPE) ab, der im vorherigen Abruf Intervall aufgetreten ist. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
class MSMCAEvent_SwitchToCMCPolling : WMIEvent
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Member

Die **msmcaevent \_ switchtocmcabruf** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **msmcaevent \_ switchdecmcabruf** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True**, wenn diese Instanz der-Klasse aktiv ist. andernfalls **false**.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Eindeutiger Bezeichner dieser Instanz der Klasse.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **msmcaevent \_ switchdecmcabruf** -Klasse wird von [**wmievent**](wmievent.md)abgeleitet.

Die System Abstraktionsschicht (System Abstraktion Layer, SAL) ist der Code, der auf Rom gebrannt ist, den das Betriebssystem aufruft, um Platt Form abhängige Vorgänge Sie ähnelt dem BIOS auf einer x86-Plattform. In Fällen, in denen die Plattform keine Interrupts für den Abruf von CMC oder CPE unterstützt, ruft das Betriebssystem jede Minute ab und überprüft, ob zuvor ein Fehler aufgetreten ist. Wenn die Plattform Interrupts unterstützt und das Betriebssystem innerhalb einer Minute eine benutzerdefinierte Menge an CMC-oder CPE-Abruf Vorgängen erhält, deaktiviert Sie die Unterbrechung und den Abruf Vorgang. Wenn der Benutzer die Anzahl der Umfragen nicht innerhalb einer Minute definiert, legt das System einen Standardwert auf 10 Umfragen pro Minute fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                         |
| Namespace<br/>                | WMI-Stammdatei \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WMI Core. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MSMCA-Klassen](msmca-classes.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

