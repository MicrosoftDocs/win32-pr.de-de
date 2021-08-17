---
description: Die \_ \_ abstrakte Vertrauensnehmer-Systemklasse stellt einen Vertrauensnehmer dar. Es kann entweder ein Name oder eine SID (Bytearray) verwendet werden.
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
ms.openlocfilehash: ac1e80bceb3dc584a22e342780bbf32660276868e473ff33ff01d6c2ad65d504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131953"
---
# <a name="__trustee-class"></a>\_\_Vertrauensnehmerklasse

Die abstrakte [**\_ \_ Vertrauensnehmer-Systemklasse**](--securitydescriptor.md) stellt einen [*Vertrauensnehmer*](/windows/desktop/SecGloss/t-gly)dar. Es kann entweder ein Name oder eine SID (Bytearray) verwendet werden.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

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

Die **\_ \_ Vertrauensnehmerklasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ Vertrauensnehmerklasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Domain**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Domänenteil des Kontos.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Name-Teil des Kontos.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die SID des Vertrauensnehmers im binären Bytearrayformat.

</dd> <dt>

**SidLength**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Länge der SID in Bytes.

</dd> <dt>

**SidString**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die SID des Vertrauensnehmers im Zeichenfolgenformat, z.B. "S-1-1-0".

</dd> <dt>

**TIME \_ CREATED**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Uhrzeit im [CIM \_ DATETIME-Format,](cim-datetime.md) zu der der Sicherheitsdeskriptor erstellt wurde.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Klasse stellt Eigenschaften bereit, die von der [**\_ Win32-Vertrauensnehmerklasse**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) geerbt werden, die ein Member der [**Win32 \_ SecurityDescriptor-Klasse**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) ist. Weitere Informationen finden Sie unter [WMI-Sicherheitsbeschreibungsobjekte](wmi-security-descriptor-objects.md) und [Ändern der Zugriffssicherheit für sicherungsfähige Objekte.](changing-access-security-on-securable-objects.md) Weitere Informationen zu ACEs finden Sie unter [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> <dt>

[**\_Win32-Vertrauensnehmer**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
</dt> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> </dl>

 

