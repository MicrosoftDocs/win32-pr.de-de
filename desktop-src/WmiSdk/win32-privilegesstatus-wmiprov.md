---
description: Win32 \_ privilegesstatus &\# 8194; Die WMI-Klasse meldet Informationen zu den Berechtigungen, die zum Ausführen eines Vorgangs erforderlich sind. Sie kann zurückgegeben werden, wenn ein Vorgang fehlgeschlagen ist oder wenn eine teilweise aufgefüllte Instanz zurückgegeben wurde.
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
ms.openlocfilehash: 658803be4e70849531bf52e7368e4e9cbcc2f0a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218473"
---
# <a name="win32_privilegesstatus-class-wmi"></a>Win32_PrivilegesStatus-Klasse (WMI)

Die **Win32 \_ privilegesstatus**-[WMI-Klasse](retrieving-a-class.md) meldet Informationen zu den Berechtigungen, die zum Ausführen eines Vorgangs erforderlich sind.    Sie kann zurückgegeben werden, wenn ein Vorgang fehlgeschlagen ist oder wenn eine teilweise aufgefüllte Instanz zurückgegeben wurde.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

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

Die **Win32 \_ privilegesstatus** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ privilegesstatus** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine beliebige benutzerdefinierte Zeichenfolge, die einen Fehler-oder Betriebsstatus beschreibt.

Diese Eigenschaft wird von " [**\_ \_ ExtendedStatus**](--extendedstatus.md)" geerbt.

</dd> <dt>

**Vorgang**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Vorgang, der zum Zeitpunkt eines Fehlers oder einer Anomalieerkennung stattfindet. In der Regel legt Windows-Verwaltungsinstrumentation (WMI) diese Eigenschaft auf den Namen einer com-API für die WMI-Methode fest, z. b. die folgende: [**IWbemServices:: kreateinstanceenum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).

Diese Eigenschaft wird von " [**\_ \_ ExtendedStatus**](--extendedstatus.md)" geerbt.

</dd> <dt>

**Parameter Info**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Parameter, die an einem Fehler oder einer Statusänderung beteiligt sind. Wenn eine Anwendung z. b. versucht, eine Klasse abzurufen, die nicht vorhanden ist, wird diese Eigenschaft auf den Namen der angreifenden Klasse festgelegt.

Diese Eigenschaft wird von " [**\_ \_ ExtendedStatus**](--extendedstatus.md)" geerbt.

</dd> <dt>

**PrivilegesNotHeld**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Auflisten der erforderlichen Zugriffsberechtigungen für einen Vorgang fehlt. Die Zugriffs Berechtigungs Typen finden Sie unter den Windows-Berechtigungen.

Beispiel: "SE \_ Shutdown \_ Name"

</dd> <dt>

**Privilegigesrequired**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Auflisten aller Berechtigungen, die zum Ausführen eines Vorgangs erforderlich sind. Dies schließt Werte aus der **PrivilegesNotHeld** -Eigenschaft ein.

Beispiel: "SE \_ Shutdown \_ Name"

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert den Anbieter, der einen Fehler oder eine Statusänderung auslöst oder meldet. Wenn ein Anbieter nicht beteiligt ist, wird diese Zeichenfolge auf "Windows-Verwaltung" festgelegt.

Diese Eigenschaft wird von " [**\_ \_ ExtendedStatus**](--extendedstatus.md)" geerbt.

</dd> <dt>

**Statuscode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Enthält einen Fehler-oder Informations Code für einen Vorgang. Dies kann ein beliebiger Wert sein, der vom Anbieter definiert wird. der Wert 0 (null) ist jedoch normalerweise reserviert, um den Erfolg anzugeben. Diese Eigenschaft wird von [**\_ \_ notifystatus**](--notifystatus.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32 \_ privilegesstatus** -Klasse wird von [**\_ \_ ExtendedStatus**](--extendedstatus.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                     |
| Namespace<br/>                | WMI-Stammdatei \\<br/>                                                               |
| MOF<br/>                      | <dl> <dt>WMI. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Erweiterdedstatus**](--extendedstatus.md)
</dt> </dl>

 

 




