---
description: Steuert den Remotezugriff auf nicht unterstützte Versionen von Windows.
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
ms.openlocfilehash: 2d05920b0936e8ff4de3eb338938e03e92edb4596efbf01f1064b6952a7df661
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320578"
---
# <a name="__ntlmuser9x-class"></a>\_\_NTLMUser9X-Klasse

Die **\_ \_ NTLMUser9X-Systemklasse** steuert den Remotezugriff auf nicht unterstützte Versionen von Windows. Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

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

Die **\_ \_ NTLMUser9X-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ NTLMUser9X-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Autoritative Stelle**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Domäne, für die ein Benutzername gilt.

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

Wenden Sie zusätzlich zum aktuellen Namespace auch auf untergeordnete Namespaces an.

</dd> </dl>

</dd> <dt>

**Mask**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Bitmaske, die Zugriffsrechte für den Namespace im WMI-Repository (Windows Management Instrumentation) angibt. Bitwerte finden Sie unter [**Namespace Access Rights Constants**](namespace-access-rights-constants.md).

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Benutzername.

</dd> <dt>

**Typ**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Zugriff zulässig.

<dt>

0
</dt> <dd>

Zugriff zulässig.

</dd> <dt>

2
</dt> <dd>

Zugriff verweigert:

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ NTLMUser9X-Klasse** wird als Eingabeparameter für die Methoden [**\_ \_ SystemSecurity::Get9XUserList**](--systemsecurity-get9xuserlist.md) und [**\_ \_ SystemSecurity::Set9XUserList**](--systemsecurity-set9xuserlist.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_\_SecurityRelatedClass**](/windows/desktop/WmiSdk/--securityrelatedclass)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

