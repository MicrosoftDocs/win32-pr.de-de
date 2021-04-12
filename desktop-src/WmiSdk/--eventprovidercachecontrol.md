---
description: Steuert, wann ein Ereignis Anbieter entladen wird.
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
ms.openlocfilehash: c54ec47b1f67d96816cf24a6b6e0108ee0b1de70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216904"
---
# <a name="__eventprovidercachecontrol-class"></a>\_\_Eventprovidercachecontrol-Klasse

Die **\_ \_ eventprovidercachecontrol** -System Klasse steuert, wann ein Ereignis Anbieter entladen wird. Sie befindet sich nur im \\ Root-Namespace.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[singleton]
class __EventProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Member

Die **\_ \_ eventprovidercachecontrol** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ eventprovidercachecontrol** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Clearafter**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Das Zeitintervall, nach dem Windows-Verwaltungsinstrumentation (WMI) einen Ereignis Anbieter freigibt. Die Uhrzeit liegt im [Intervall Format](interval-format.md)vor. Es kann bis zu einem doppelten Intervall dauern, bis der Anbieter entladen wurde.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ eventprovidercachecontrol** -Klasse ist von [**\_ \_ CacheControl**](--cachecontrol.md)abgeleitet.

Weitere Informationen zum Verwenden dieser Klasse finden Sie unter [Entladen eines Anbieters](unloading-a-provider.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Root<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_CacheControl**](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> </dl>

 

