---
description: Steuert, wann ein Ereignisanbieter entladen wird.
ms.assetid: 7f11e521-d0f6-4c3c-8bfe-ceed2d106ed3
ms.tgt_platform: multiple
title: __EventProviderCacheControl-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderCacheControl
- Root.__EventProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 9d027fec5aea132524924655047c0f0a8aa8605d1972c6f91b2c2315c5834ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557924"
---
# <a name="__eventprovidercachecontrol-class"></a>\_\_EventProviderCacheControl-Klasse

Die **\_ \_ Systemklasse EventProviderCacheControl** steuert, wann ein Ereignisanbieter entladen wird. Sie befindet sich nur im \\ Stammnamespace.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[singleton]
class __EventProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Member

Die **\_ \_ EventProviderCacheControl-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ EventProviderCacheControl-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Das Zeitintervall nach Windows WMI (Management Instrumentation) gibt einen Ereignisanbieter frei. Die Zeit hat das [Intervallformat](interval-format.md). Es kann bis zu zweimal das angegebene Intervall dauern, um den Anbieter zu entladen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ EventProviderCacheControl-Klasse** wird von [**\_ \_ CacheControl abgeleitet.**](--cachecontrol.md)

Weitere Informationen zur Verwendung dieser Klasse finden Sie unter [Entladen eines Anbieters.](unloading-a-provider.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Root<br/>                |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**\_\_CacheControl**](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> </dl>

 

