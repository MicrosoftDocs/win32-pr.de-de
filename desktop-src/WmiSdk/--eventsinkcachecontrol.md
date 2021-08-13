---
description: Wird verwendet, um zu bestimmen, wann WMI den IWbemUnboundObjectSink-Zeiger eines Ereignisverbraucheranbieters frei gibt.
ms.assetid: f7b14efc-a2f7-4e99-8ec8-5b5af0743139
ms.tgt_platform: multiple
title: __EventSinkCacheControl-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventSinkCacheControl
- Root.__EventSinkCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: dc73e2cb740486ad08172c10233f4865709a87d9f1122f399002133687744094
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557914"
---
# <a name="__eventsinkcachecontrol-class"></a>\_\_EventSinkCacheControl-Klasse

Die **\_ \_ Systemklasse EventSinkCacheControl** wird verwendet, um zu bestimmen, wann WMI den [**IWbemUnboundObjectSink-Zeiger eines Ereignisverbraucheranbieters**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) frei gibt. Die **\_ \_ EventSinkCacheControl-Klasse** ist eine Singletonklasse. Sie befindet sich nur im \\ Stammnamespace.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[singleton]
class __EventSinkCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Member

Die **\_ \_ EventSinkCacheControl-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ EventSinkCacheControl-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Zeitintervall, nach dem WMI einen Ereignisanbieter frei gibt. Es kann bis zu zweimal das angegebene Intervall dauern, um den Anbieter zu entladen. Die Zeit hat das [Intervallformat](interval-format.md).

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ EventSinkCacheControl-Klasse** wird von [**\_ \_ CacheControl abgeleitet.**](--cachecontrol.md) Weitere Informationen zur Verwendung dieser Klasse finden Sie unter [Entladen eines Anbieters.](unloading-a-provider.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Root<br/>                |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> </dl>

 

 




