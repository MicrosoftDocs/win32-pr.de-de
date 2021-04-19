---
description: Meldet ein Namespace Lösch Ereignis, bei dem es sich um einen Typ eines systeminternen Ereignisses handelt, das generiert wird, wenn ein untergeordneter Namespace aus dem aktuellen Namespace entfernt wird.
ms.assetid: f7160a90-562d-40d9-9189-32aaabcd81d0
ms.tgt_platform: multiple
title: __NamespaceDeletionEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6e23f909718167760c02bbdb38e2a075d04bc516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373297"
---
# <a name="__namespacedeletionevent-class"></a>\_\_Namespacedeletionevent-Klasse

Die **\_ \_ Namespace** -System Klasse meldet ein Namespace Lösch Ereignis, bei dem es sich um einen Typ eines systeminternen [Ereignisses](determining-the-type-of-event-to-receive.md) handelt, das generiert wird, wenn ein untergeordneter Namespace aus dem aktuellen Namespace entfernt wird.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __NamespaceDeletionEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a>Member

Die **\_ \_ namespacedeletionevent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ namespacedeletionevent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Sicherheits \_ Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, den der Ereignis Anbieter verwendet, um die Benutzer zu ermitteln, die ein Ereignis empfangen können. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.

</dd> <dt>

**TargetNamespace**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ Namespace**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kopie der [**\_ \_ Namespace**](--namespace.md) Instanz, die gelöscht wird. Die **Name** -Eigenschaft der **\_ \_ Namespace** Instanz identifiziert den Namespace, der gelöscht wird. Diese Eigenschaft wird von [**\_ \_ namespaceoperationevent**](--namespaceoperationevent.md)geerbt.

</dd> <dt>

**\_Erstellungszeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der die Uhrzeit angibt, zu der ein Ereignis generiert wird. Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt. Die Informationen liegen im UTC-Format (koordinierte Weltzeit) vor. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ namespacedeletionevent** -Klasse wird von [**\_ \_ namespaceoperationevent**](--namespaceoperationevent.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Namespaceoperationevent**](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> </dl>

 

