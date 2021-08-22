---
description: Class ist die abstrakte Basisklasse für Klassen, die verwendet werden, um zu bestimmen, wann WMI ein Component Object Model -Objekt (COM) freigeben soll.
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
ms.openlocfilehash: 429e973d83e1f213b011998c75dfbfabd81fb7bb4921f0f8b9f61bcedd6080c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051098"
---
# <a name="__cachecontrol-class"></a>\_\_CacheControl-Klasse

Die **\_ \_ CacheControl-Systemklasse** ist die abstrakte Basisklasse für Klassen, die verwendet werden, um zu bestimmen, wann WMI ein Component Object Model -Objekt (COM) freigeben soll. Instanzen dieser Klasse werden nie erstellt. Die **\_ \_ CacheControl-Klasse** befindet sich nur im Stammnamespace. Weitere Informationen zur Verwendung dieser Klasse finden Sie unter [Entladen eines Anbieters.](unloading-a-provider.md)

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[abstract]
class __CacheControl : __SystemClass
{
};
```

## <a name="members"></a>Member

Die **\_ \_ CacheControl-Klasse** definiert keine Member.

## <a name="remarks"></a>Hinweise

Die **\_ \_ CacheControl-Klasse** wird von [**\_ \_ SystemClass**](--systemclass.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> <dt>

[**\_\_EventConsumerProviderCacheControl**](--eventconsumerprovidercachecontrol.md)
</dt> <dt>

[**\_\_EventProviderCacheControl**](--eventprovidercachecontrol.md)
</dt> <dt>

[**\_\_EventSinkCacheControl**](--eventsinkcachecontrol.md)
</dt> <dt>

[**\_\_ObjectProviderCacheControl**](--objectprovidercachecontrol.md)
</dt> <dt>

[\_\_PropertyProviderCacheControl](--propertyprovidercachecontrol.md)
</dt> <dt>

[Entladen eines Anbieters](unloading-a-provider.md)
</dt> </dl>

 

