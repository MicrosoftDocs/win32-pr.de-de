---
description: Steuert, wann ein Klassen-oder Instanzanbieter entladen wird.
ms.assetid: 4cbeb820-8a65-4fab-97f1-2a973b2a4310
ms.tgt_platform: multiple
title: __ObjectProviderCacheControl-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderCacheControl
- Root.__ObjectProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 53cfaa69afead4f436879f128a4d42e50d36fe67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350098"
---
# <a name="__objectprovidercachecontrol-class"></a>\_\_Objectprovidercachecontrol-Klasse

Die System Klasse **\_ \_ objectprovidercachecontrol** steuert, wann ein Klassen-oder Instanzanbieter entladen wird. Sie befindet sich nur im \\ Root-Namespace.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[singleton]
class __ObjectProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Member

Die **\_ \_ objectprovidercachecontrol** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ objectprovidercachecontrol** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Clearafter**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Das Zeitintervall, nach dem WMI eine Instanz, Klasse oder einen Methoden Anbieter freigibt. Die Uhrzeit liegt im [Intervall Format](interval-format.md)vor.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ objectprovidercachecontrol** -Klasse ist von [**\_ \_ CacheControl**](--cachecontrol.md)abgeleitet. Weitere Informationen zum Verwenden dieser Klasse finden Sie unter [Entladen eines Anbieters](unloading-a-provider.md).

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
</dt> <dt>

[Empfangen von Ereignissen zu allen Zeitpunkten](receiving-events-at-all-times.md)
</dt> </dl>

 

