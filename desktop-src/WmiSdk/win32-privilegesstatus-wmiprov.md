---
description: Win32 \_ PrivilegesStatus &\# 8194; Die WMI-Klasse meldet Informationen zu Berechtigungen, die zum Abschließen eines Vorgangs erforderlich sind. Sie kann zurückgegeben werden, wenn ein Vorgang fehlgeschlagen ist oder eine teilweise aufgefüllte Instanz zurückgegeben wurde.
ms.assetid: 85bda855-1488-4d7a-99ed-798e9859fef7
ms.tgt_platform: multiple
title: Win32_PrivilegesStatus-Klasse (WMI)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrivilegesStatus
- Win32_PrivilegesStatus.Description
- Win32_PrivilegesStatus.Operation
- Win32_PrivilegesStatus.ParameterInfo
- Win32_PrivilegesStatus.ProviderName
- Win32_PrivilegesStatus.StatusCode
- Win32_PrivilegesStatus.PrivilegesNotHeld
- Win32_PrivilegesStatus.PrivilegesRequired
api_type:
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 97276023325dc4e2a460daefd35ee01104b5c0adf5c855f145e0f11c954eba1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757630"
---
# <a name="win32_privilegesstatus-class-wmi"></a>Win32_PrivilegesStatus-Klasse (WMI)

Die [WMI-Klasse](retrieving-a-class.md) **Win32 \_ PrivilegesStatus** meldet Informationen zu Berechtigungen, die zum Abschließen eines Vorgangs erforderlich sind.    Sie kann zurückgegeben werden, wenn ein Vorgang fehlgeschlagen ist oder eine teilweise aufgefüllte Instanz zurückgegeben wurde.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge sortiert.

## <a name="syntax"></a>Syntax

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}")]
class Win32_PrivilegesStatus : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string PrivilegesNotHeld[];
  string PrivilegesRequired[];
};
```

## <a name="members"></a>Member

Die **Win32 \_ PrivilegesStatus-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ PrivilegesStatus-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Jede benutzerdefinierte Zeichenfolge, die einen Fehler- oder Betriebsstatus beschreibt.

Diese Eigenschaft wird von [**\_ \_ ExtendedStatus**](--extendedstatus.md)geerbt.

</dd> <dt>

**Vorgang**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Vorgang, der zum Zeitpunkt eines Fehlers oder einer Anomalie stattfindet. In der Regel legt Windows Management Instrumentation (WMI) diese Eigenschaft auf den Namen einer COM-API für WMI-Methode fest, z. B.: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).

Diese Eigenschaft wird von [**\_ \_ ExtendedStatus**](--extendedstatus.md)geerbt.

</dd> <dt>

**Parameterinfo**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Parameter, die an einer Fehler- oder Statusänderung beteiligt sind. Wenn eine Anwendung beispielsweise versucht, eine klasse abzurufen, die nicht vorhanden ist, wird diese Eigenschaft auf den fehlerhaften Klassennamen festgelegt.

Diese Eigenschaft wird von [**\_ \_ ExtendedStatus**](--extendedstatus.md)geerbt.

</dd> <dt>

**PrivilegesNotHeld**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Listet die erforderlichen Zugriffsberechtigungen auf, die zum Abschließen eines Vorgangs fehlen. Die Zugriffsberechtigungstypen finden Sie unter Windows Berechtigungen.

Beispiel: "SE \_ SHUTDOWN \_ NAME"

</dd> <dt>

**BerechtigungenErforderlich**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Liste aller Berechtigungen, die zum Ausführen eines Vorgangs erforderlich sind. Dies schließt Werte aus der **PrivilegesNotHeld-Eigenschaft** ein.

Beispiel: "SE \_ SHUTDOWN \_ NAME"

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert den Anbieter, der einen Fehler oder eine Statusänderung verursacht oder meldet. Wenn kein Anbieter beteiligt ist, wird diese Zeichenfolge auf "Windows Management" festgelegt.

Diese Eigenschaft wird von [**\_ \_ ExtendedStatus**](--extendedstatus.md)geerbt.

</dd> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Enthält einen Fehler- oder Informationscode für einen Vorgang. Dies kann ein beliebiger Wert sein, der vom Anbieter definiert wird, aber der Wert 0 (null) ist in der Regel reserviert, um den Erfolg anzugeben. Diese Eigenschaft wird von [**\_ \_ NotifyStatus**](--notifystatus.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ PrivilegesStatus-Klasse** wird von [**\_ \_ ExtendedStatus**](--extendedstatus.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                     |
| Namespace<br/>                | \\Stamm-WMI<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Wmi.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_\_ExtendedStatus**](--extendedstatus.md)
</dt> </dl>

 

 




