---
description: Steuert den Cache, wenn ein Eigenschaften Anbieter entladen wird.
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
ms.openlocfilehash: 1d153049a9635b4b77a1ad09ca0ee64835b9bcfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216324"
---
# <a name="__propertyprovidercachecontrol-class"></a>\_\_Propertyprovidercachecontrol-Klasse

Die **\_ \_ propertyprovidercachecontrol** -Klasse steuert den Cache, wenn ein Eigenschaften Anbieter entladen wird. Diese Klasse ist nur im \\ Root-Namespace vorhanden.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __PropertyProviderCacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Member

Die **\_ \_ propertyprovidercachecontrol** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ propertyprovidercachecontrol** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Clearafter**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Das Zeitintervall nach der Freigabe eines Eigenschaften Anbieters durch WMI. Die Uhrzeit liegt im Intervall Format vor.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ propertyprovidercachecontrol** -Klasse wird von [**\_ \_ CacheControl**](--cachecontrol.md)abgeleitet. Weitere Informationen finden Sie unter [Entladen eines Anbieters](unloading-a-provider.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> </dl>

 

 




