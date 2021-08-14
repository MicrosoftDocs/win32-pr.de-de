---
description: Steuert den Cache, wenn ein Eigenschaftenanbieter entladen wird.
ms.assetid: 8fc7de7a-889c-4d53-97ea-a676879de1d3
ms.tgt_platform: multiple
title: __PropertyProviderCacheControl-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderCacheControl
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 33edad107859328e9a81a6c77c3c02e29e2ee3aebbbe411ee20fb438e51517a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110538"
---
# <a name="__propertyprovidercachecontrol-class"></a>\_\_PropertyProviderCacheControl-Klasse

Die **\_ \_ PropertyProviderCacheControl-Klasse** steuert den Cache, wenn ein Eigenschaftenanbieter entladen wird. Diese Klasse ist nur im \\ Stammnamespace vorhanden.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
class __PropertyProviderCacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Member

Die **\_ \_ PropertyProviderCacheControl-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ PropertyProviderCacheControl-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Zeitintervall nach der Freigabe eines Eigenschaftenanbieters durch WMI. Die Zeit liegt im Intervallformat vor.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ PropertyProviderCacheControl-Klasse** wird von [**\_ \_ CacheControl**](--cachecontrol.md)abgeleitet. Weitere Informationen finden Sie unter [Entladen eines Anbieters.](unloading-a-provider.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> </dl>

 

 




