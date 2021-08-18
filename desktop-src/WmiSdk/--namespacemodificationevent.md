---
description: Meldet ein Namespaceänderungsereignis, bei dem es sich um einen Typ von systeminternem Ereignis handelt, das generiert wird, wenn ein Namespace geändert wird.
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
ms.openlocfilehash: 3243afe0a8cae34e83ad85e2d89a3becab8d07775ba3ec0c3283fd4ea8ed8bbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557813"
---
# <a name="__namespacemodificationevent-class"></a>\_\_NamespaceModificationEvent-Klasse

Die **\_ \_ NamespaceModificationEvent-Systemklasse** meldet ein Namespaceänderungsereignis, bei dem es sich um einen [Systemereignistyp](determining-the-type-of-event-to-receive.md) handelt, der generiert wird, wenn ein Namespace geändert wird.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

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

Die **\_ \_ NamespaceModificationEvent-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ NamespaceModificationEvent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**PreviousNamespace**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ Namespace**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kopie der ursprünglichen Version einer [**\_ \_ Namespace-Instanz.**](--namespace.md) Die **Name-Eigenschaft** dieser Instanz identifiziert den Namespace, der geändert wird.

</dd> <dt>

**\_SICHERHEITSBESCHREIBUNG**
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignisanbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird von [**\_ \_ Ereignis**](--event.md)geerbt.

</dd> <dt>

**\_SICHERHEITSBESCHREIBUNG** 
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, den der Ereignisanbieter verwendet, um die Benutzer zu bestimmen, die ein Ereignis empfangen können. Diese Eigenschaft wird von [**\_ \_ Ereignis**](--event.md)geerbt.

> [!Note]  
> Eine  NULL-Zugriffssteuerungsliste (Access Control List, ACL) in SECURITY [**\_ DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) gewährt jedem jederzeit unbegrenzten Zugriff. Weitere Informationen finden Sie unter [Erstellen eines Sicherheitsdeskriptors für ein neues Objekt.](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)

 

</dd> <dt>

**Targetnamespace**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ Namespace**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kopie der [**\_ \_ namespace-Instanz,**](--namespace.md) die geändert wird. Die **Name-Eigenschaft** der **\_ \_ Namespace-Instanz** gibt den Namespace an, der geändert wird. Diese Eigenschaft wird von der [**\_ \_ Klasse NamespaceOperationEvent**](--namespaceoperationevent.md)geerbt.

</dd> <dt>

**TIME \_ CREATED**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der die Zeit angibt, zu der ein Ereignis generiert wird. Dies ist ein 64-Bit-Wert, der die Anzahl von 100-Nanosekunden-Intervallen nach dem 1. Januar 1601 darstellt. Die Informationen haben das format koordinierte Weltzeit (UTC). Diese Eigenschaft wird von [**\_ \_ Ereignis**](--event.md)geerbt.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ NamespaceModificationEvent-Klasse** wird von [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md)abgeleitet.

Die einzigen Unterschiede zwischen dem Zielnamespace und dem vorherigen Namespace sind die Qualifizierer und Eigenschaften mit Ausnahme [**von Name**](--namespace.md).

Beachten Sie, dass die [**Name-Eigenschaft**](--namespace.md) einer **\_ \_ Namespace-Instanz** nicht geändert werden kann, da Namespaces nicht umbenannt werden können. Um den Namen eines Namespaces zu ändern, muss die **\_ \_ Namespace-Instanz** gelöscht und mit einem neuen Namen neu erstellt werden. Daher werden Namespaceänderungsereignisse generiert, wenn eine Änderung an anderen Qualifizierern und Eigenschaften als **Name** vorgenommen wird. Ein Namespaceänderungsereignis wird nicht generiert, wenn innerhalb des Namespace eine Änderung erfolgt. Ein Namespaceänderungsereignis wird nur generiert, wenn eine Namespaceinstanz geändert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_\_NamespaceOperationEvent**](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> </dl>

 

