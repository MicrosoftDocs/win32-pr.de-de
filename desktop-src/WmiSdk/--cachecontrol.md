---
description: Class ist die abstrakte Basisklasse für Klassen, mit denen bestimmt wird, wann WMI ein Component Object Model (com)-Objekt freigeben soll.
ms.assetid: 32631610-8c0e-4f04-b0b2-62e5f8e23ef4
ms.tgt_platform: multiple
title: __CacheControl-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CacheControl
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: fe5358630a7ac5eb48751135d39c2fd998196bf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373132"
---
# <a name="__cachecontrol-class"></a>\_\_CacheControl-Klasse

Die **\_ \_ CacheControl** -System Klasse ist die abstrakte Basisklasse für Klassen, mit denen bestimmt wird, wann WMI ein Component Object Model (com)-Objekt freigeben soll. Instanzen dieser Klasse werden nie erstellt. Die **\_ \_ CacheControl** -Klasse befindet sich nur im Root-Namespace. Weitere Informationen zum Verwenden dieser Klasse finden Sie unter [Entladen eines Anbieters](unloading-a-provider.md).

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[abstract]
class __CacheControl : __SystemClass
{
};
```

## <a name="members"></a>Member

Die **\_ \_ CacheControl** -Klasse definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ CacheControl** -Klasse wird von [**\_ \_ systemclass**](--systemclass.md)abgeleitet.

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
</dt> <dt>

[**\_\_Eventconsumerprovidercachecontrol**](--eventconsumerprovidercachecontrol.md)
</dt> <dt>

[**\_\_Eventprovidercachecontrol**](--eventprovidercachecontrol.md)
</dt> <dt>

[**\_\_EventSink Cache econtrol**](--eventsinkcachecontrol.md)
</dt> <dt>

[**\_\_Objectprovidercachecontrol**](--objectprovidercachecontrol.md)
</dt> <dt>

[\_\_Propertyprovidercachecontrol](--propertyprovidercachecontrol.md)
</dt> <dt>

[Entladen eines Anbieters](unloading-a-provider.md)
</dt> </dl>

 

