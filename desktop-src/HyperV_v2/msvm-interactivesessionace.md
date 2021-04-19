---
description: Stellt einen Zugriffs Steuerungs Eintrag (ACE) dar, der den Zugriff auf die interaktive Sitzung eines virtuellen Computers bestimmt.
ms.assetid: dfec83d6-8033-47b5-aa6f-fc7447a29f43
title: Msvm_InteractiveSessionACE-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InteractiveSessionACE
- Msvm_InteractiveSessionACE.Trustee
- Msvm_InteractiveSessionACE.AccessType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6c4b63e769b04092323cd2da7362ef6b156886b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355502"
---
# <a name="msvm_interactivesessionace-class"></a>MSVM \_ interactivesessionace-Klasse

Stellt einen *Zugriffs Steuerungs Eintrag* (ACE) dar, der den Zugriff auf die interaktive Sitzung eines virtuellen Computers bestimmt.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InteractiveSessionACE
{
  string Trustee;
  uint16 AccessType;
};
```

## <a name="members"></a>Member

Die **MSVM \_ interactivesessionace** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ interactivesessionace** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Access Type**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der ACE dem Vertrauens nehmer den Zugriff gewährt oder verweigert.

<dt>

<span id="Access_Allowed"></span><span id="access_allowed"></span><span id="ACCESS_ALLOWED"></span>

**Zugriff zulässig** (0)


</dt> <dd></dd> <dt>

<span id="Access_Denied"></span><span id="access_denied"></span><span id="ACCESS_DENIED"></span>

**Zugriff verweigert** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**Stiftungs**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert den Sicherheits Prinzipal, dem der ACE den Zugriff gewährt oder verweigert. Gültige Formate für diese Eigenschaft sind das Windows Sam-kompatible Benutzernamen Format und das Windows-SID-Zeichen folgen Format.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Getinteractivesessionacl**](getinteractivesessionacl-msvm-terminalservice.md)
</dt> </dl>

 

 




