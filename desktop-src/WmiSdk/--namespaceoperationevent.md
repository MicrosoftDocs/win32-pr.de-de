---
description: Eine Basisklasse für alle systeminternen Ereignisse, die sich auf einen Namespace beziehen.
ms.assetid: 168637b1-217e-4b6d-bd07-25127b9e9f6c
ms.tgt_platform: multiple
title: __NamespaceOperationEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b5293f97eed0716b3add1d5f06513d556355b157d8e594b1f9e55cb8df6ca7ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320622"
---
# <a name="__namespaceoperationevent-class"></a>\_\_NamespaceOperationEvent-Klasse

Die **\_ \_ NamespaceOperationEvent-Systemklasse** ist eine Basisklasse für alle systeminternen Ereignisse, die sich auf einen Namespace beziehen.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
class __NamespaceOperationEvent : __Event
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a>Member

Die **\_ \_ NamespaceOperationEvent-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ NamespaceOperationEvent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**\_SICHERHEITSBESCHREIBUNG**
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignisanbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird von [**\_ \_ Ereignis**](--event.md)geerbt.

</dd> <dt>

**Targetnamespace**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ Namespace**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Namespace, der vom Ereignis betroffen ist. Bei Erstellungsereignissen ist dies der neu erstellte Namespace. Bei Änderungsereignissen ist dies der geänderte Namespace. Bei Löschereignissen ist dies der gelöschte Namespace.

</dd> <dt>

**TIME \_ CREATED**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der den Zeitpunkt angibt, zu dem das Ereignis generiert wurde. Dies ist ein 64-Bit-Wert, der die Anzahl von 100-Nanosekunden-Intervallen nach dem 1. Januar 1601 darstellt. Die Informationen liegen im UTC-Format (Coordinated Universal Times) vor. Diese Eigenschaft wird von [**\_ \_ Ereignis**](--event.md)geerbt.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ NamespaceOperationEvent-Klasse** wird von [**\_ \_ Event**](--event.md)abgeleitet.

Instanzen dieser Klasse werden nicht erstellt. WMI erstellt Instanzen einer der folgenden Klassen, die von dieser Klasse abgeleitet werden:

[**\_\_NamespaceCreationEvent**](--namespacecreationevent.md)

[**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md)

[**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Ereignis**](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> <dt>

[Bestimmen des Typs des zu empfangenden Ereignisses](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

