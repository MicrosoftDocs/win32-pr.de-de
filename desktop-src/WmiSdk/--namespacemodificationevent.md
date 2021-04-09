---
description: Meldet ein Namespace-Änderungs Ereignis, bei dem es sich um einen Typ eines systeminternen Ereignisses handelt, das generiert wird, wenn ein Namespace geändert wird.
ms.assetid: 168505d7-4677-4f41-935e-149f22de2cb5
ms.tgt_platform: multiple
title: __NamespaceModificationEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceModificationEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5af5783d3ebfbfb4b7842cb86b1919f8dbed1365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759444"
---
# <a name="__namespacemodificationevent-class"></a>\_\_Namespacemodificationevent-Klasse

Die **\_ \_ namespacemodificationevent** -System Klasse meldet ein Namespace-Änderungs Ereignis, bei dem es sich um einen Typ eines systeminternen [Ereignisses](determining-the-type-of-event-to-receive.md) handelt, das generiert wird, wenn ein Namespace geändert wird.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __NamespaceModificationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace PreviousNamespace;
  uint8       SECURITY_DESCRIPTOR [];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a>Member

Die **\_ \_ namespacemodificationevent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ namespacemodificationevent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Previousnamespace**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ Namespace**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kopie der ursprünglichen Version einer [**\_ \_ Namespace**](--namespace.md) Instanz. Die **Name** -Eigenschaft dieser Instanz identifiziert den Namespace, der geändert wird.

</dd> <dt>

**Sicherheits \_ Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.

</dd> <dt>

**Sicherheits \_ Beschreibung** 
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, den der Ereignis Anbieter verwendet, um die Benutzer zu ermitteln, die ein Ereignis empfangen können. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.

> [!Note]  
> Eine Zugriffs Steuerungs Liste (Access Control List, ACL) für **null** in der [**Sicherheits \_ Beschreibung**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) gewährt allen Benutzern uneingeschränkten Zugriff. Weitere Informationen finden Sie unter [Erstellen einer Sicherheits Beschreibung für ein neues Objekt](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

</dd> <dt>

**TargetNamespace**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ Namespace**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kopie der geänderten [**\_ \_ Namespace**](--namespace.md) Instanz. Die **Name** -Eigenschaft der **\_ \_ Namespace** Instanz gibt den Namespace an, der geändert wird. Diese Eigenschaft wird von der Klasse [**\_ \_ namespaceoperationevent**](--namespaceoperationevent.md)geerbt.

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

Die **\_ \_ namespacemodificationevent** -Klasse wird von [**\_ \_ namespaceoperationevent**](--namespaceoperationevent.md)abgeleitet.

Die einzigen Unterschiede zwischen dem Ziel Namespace und dem vorherigen Namespace sind die Qualifizierer und Eigenschaften mit Ausnahme von [**Name**](--namespace.md).

Beachten Sie, dass die [**Name**](--namespace.md) -Eigenschaft einer **\_ \_ Namespace** Instanz nicht geändert werden kann, da Namespaces nicht umbenannt werden können. Um den Namen eines Namespace zu ändern, muss die **\_ \_ Namespace** Instanz gelöscht und mit einem neuen Namen neu erstellt werden. Daher werden Namespace Änderungs Ereignisse generiert, wenn eine Änderung an Qualifizierern und anderen Eigenschaften als **Name** auftritt. Ein Namespace-Änderungs Ereignis wird nicht generiert, wenn eine Art von Änderung im Namespace auftritt. Ein Namespace-Änderungs Ereignis wird nur generiert, wenn eine Namespace Instanz geändert wird.

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

 

