---
description: Enthält die Sicherheitsrechte für den Namespace in Form einer Sicherheits Beschreibung.
ms.assetid: 84e514f5-b114-4bfc-ab0b-9745f249168b
ms.tgt_platform: multiple
title: __thisNAMESPACE-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __thisNAMESPACE
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 440ccdf0eda794b5d648cae756f9a9c808eb2db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368967"
---
# <a name="__thisnamespace-class"></a>\_\_thisNamespace-Klasse

Die **\_ \_ thisNamespace** -System Klasse enthält die Sicherheitsrechte für den-Namespace in Form einer Sicherheits Beschreibung. Diese Klasse und eine einzelne Instanz befinden sich in allen Namespaces.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[singleton]
class __thisNAMESPACE : __SystemClass
{
  uint8 SECURITY_DESCRIPTOR[];
};
```

## <a name="members"></a>Member

Die **\_ \_ thisNamespace** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ thisNamespace** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Sicherheits \_ Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Sicherheits Deskriptor, der beschreibt, wer auf den Namespace zugreifen kann und wer in den Namespace lesen oder in diesen schreiben kann. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt. Weitere Informationen zum Format von Sicherheits Deskriptoren finden Sie unter [Sicherheits Deskriptoren](/windows/desktop/SecAuthZ/security-descriptors) im Abschnitt "Sicherheit" des Windows SDK.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Singleton-Instanz von **\_ \_ thisNamespace** ist schreibgeschützt. Verwenden Sie die Methoden der [**\_ \_ SystemSecurity**](--systemsecurity.md) -Klasse, um die Einstellungen der sicherheitsbeschreibungenschaft zu ändern. Die **\_ \_ thisNamespace** -Klasse wird von [**\_ \_ System Class**](--systemclass.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_System Class**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> </dl>

 

