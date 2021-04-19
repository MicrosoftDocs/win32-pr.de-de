---
description: Steuert den Remote Zugriff auf nicht unterstützte Versionen von Windows.
ms.assetid: eb326bba-a011-4b9c-b4ee-fc08ae364f6f
ms.tgt_platform: multiple
title: __NTLMUser9X-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NTLMUser9X
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 79aa5153869c7337b6849e8c465dbbf8b36a0f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349650"
---
# <a name="__ntlmuser9x-class"></a>\_\_NTLMUser9X-Klasse

Die **\_ \_ NTLMUser9X** -System Klasse steuert den Remote Zugriff auf nicht unterstützte Versionen von Windows. Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __NTLMUser9X : __SecurityRelatedClass
{
  string Authority;
  sint32 Flags;
  sint32 Mask;
  string Name;
  sint32 Type;
};
```

## <a name="members"></a>Member

Die **\_ \_ NTLMUser9X** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ NTLMUser9X** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Autoritative Stelle**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Domäne, für die ein Benutzername gilt.

</dd> <dt>

**Flags**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Vererbungsflags.

<dt>

0
</dt> <dd>

Keine Vererbung.

</dd> <dt>

2
</dt> <dd>

Gilt für untergeordnete Namespaces, zusätzlich zur aktuellen.

</dd> </dl>

</dd> <dt>

**Mask**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Bitmaske, die Zugriffsrechte für den Namespace im WMI-Repository (Windows-Verwaltungsinstrumentation) angibt. Informationen zu Bitwerten finden Sie unter [**Namespace-Zugriffsrechte Konstanten**](namespace-access-rights-constants.md).

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Benutzername.

</dd> <dt>

**Type**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Zugriff ist zulässig.

<dt>

0
</dt> <dd>

Der Zugriff ist zulässig.

</dd> <dt>

2
</dt> <dd>

Zugriff verweigert.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ NTLMUser9X** -Klasse wird als Eingabeparameter für die Methoden " [**\_ \_ SystemSecurity:: Get9XUserList**](--systemsecurity-get9xuserlist.md) " und " [**\_ \_ SystemSecurity:: Set9XUserList**](--systemsecurity-set9xuserlist.md) " verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Securityrelatedclass**](/windows/desktop/WmiSdk/--securityrelatedclass)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

