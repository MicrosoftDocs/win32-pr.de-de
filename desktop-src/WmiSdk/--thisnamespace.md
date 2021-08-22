---
description: Enthält die Sicherheitsrechte für den Namespace in Form eines Sicherheitsdeskriptors.
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
ms.openlocfilehash: 02e92bd8cb1c1827af86d23320e7347baa08c395d32def8c9b8adea2fcfd35bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132023"
---
# <a name="__thisnamespace-class"></a>\_\_thisNAMESPACE-Klasse

Die **\_ \_ ThisNAMESPACE-Systemklasse** enthält die Sicherheitsrechte für den Namespace in Form eines Sicherheitsdeskriptors. Diese Klasse und eine einzelne Instanz befinden sich in allen Namespaces.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[singleton]
class __thisNAMESPACE : __SystemClass
{
  uint8 SECURITY_DESCRIPTOR[];
};
```

## <a name="members"></a>Member

Die **\_ \_ thisNAMESPACE-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ thisNAMESPACE-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**\_SICHERHEITSDESKRIPTOR**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Sicherheitsdeskriptor, der beschreibt, wer auf den Namespace zugreifen kann und wer aus dem Namespace lesen oder in diesen schreiben kann. Diese Eigenschaft wird vom Ereignis [**\_ \_ geerbt.**](--event.md) Weitere Informationen zum Format von Sicherheitsdeskriptoren finden Sie unter [Sicherheitsdeskriptoren](/windows/desktop/SecAuthZ/security-descriptors) im Abschnitt Sicherheit des Windows SDK.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Singletoninstanz **\_ \_ von thisNAMESPACE** ist schreibgeschützt. Verwenden Sie die Methoden der [**\_ \_ SystemSecurity-Klasse,**](--systemsecurity.md) um die Einstellungen der Sicherheitsbeschreibungseigenschaft zu ändern. Die **\_ \_ thisNAMESPACE-Klasse** wird von [**\_ \_ SystemClass ableiten.**](--systemclass.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> </dl>

 

