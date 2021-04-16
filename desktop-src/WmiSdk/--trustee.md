---
description: Die \_ \_ abstrakte System Klasse des Vertrauens nehmers stellt einen Vertrauens nehmer dar. Es kann entweder ein Name oder eine sid (Bytearray) verwendet werden.
ms.assetid: 92d17c7c-ebca-4dd0-80d8-6edd999ca394
ms.tgt_platform: multiple
title: __Trustee-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Trustee
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5c6ba04760e924ffe9d86916cffdb82ea2488219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530368"
---
# <a name="__trustee-class"></a>\_\_Treuhänder Klasse

Die [**\_ \_ abstrakte**](--securitydescriptor.md) System Klasse des Vertrauens nehmers [*stellt einen Vertrauens*](/windows/desktop/SecGloss/t-gly)nehmer dar. Es kann entweder ein Name oder eine sid (Bytearray) verwendet werden.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __Trustee
{
  string Domain;
  string Name;
  uint8  SID[];
  uint32 SidLength;
  string SidString;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Member

Die **\_ \_ Treuhänder** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ Treuhänder** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Domäne**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Domänen Teil des Kontos.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Namensteil des Kontos.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die SID des Vertrauens nehmers im binären Bytearray-Formular.

</dd> <dt>

**SidLength**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Länge der sid (in Bytes).

</dd> <dt>

**Sidstring**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die SID des Vertrauens nehmers im Zeichen folgen Format, z. b. "S-1-1-0".

</dd> <dt>

**\_Erstellungszeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Uhrzeit im [CIM- \_ DateTime](cim-datetime.md) -Format, als die Sicherheits Beschreibung erstellt wurde.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse stellt Eigenschaften bereit, die von der [**Win32- \_ Treuhänder**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) Klasse geerbt werden, die ein Member der [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Klasse ist. Weitere Informationen finden Sie unter [WMI-sicherheitsdeskriptorobjekte](wmi-security-descriptor-objects.md) und [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md). Weitere Informationen zu ACEs finden Sie unter [Access Control-Komponenten](/windows/desktop/SecAuthZ/access-control-components).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[**Win32- \_ Treuhänder**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
</dt> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> </dl>

 

