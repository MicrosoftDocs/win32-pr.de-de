---
description: Bestimmt, wann WMI einen Ereignisconsumeranbieter freigeben soll.
ms.assetid: 93246826-8070-4e05-96f0-f773041ed1d4
ms.tgt_platform: multiple
title: __EventConsumerProviderCacheControl-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderCacheControl
- Root.__EventConsumerProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: f769427c77f6efdf9a521a63f7334d5d27416c04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373365"
---
# <a name="__eventconsumerprovidercachecontrol-class"></a>\_\_Eventconsumerprovidercachecontrol-Klasse

Die **\_ \_ eventconsumerprovidercachecontrol** -System Klasse bestimmt, wann WMI einen Ereignisconsumeranbieter freigeben soll. Die **\_ \_ eventconsumerprovidercachecontrol** -Klasse ist eine Singleton-Klasse. Sie befindet sich nur im \\ Root-Namespace.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[singleton]
class __EventConsumerProviderCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Member

Die **\_ \_ eventconsumerprovidercachecontrol** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ eventconsumerprovidercachecontrol** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Clearafter**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Das Zeitintervall, nach dem WMI einen Ereignisconsumeranbieter freigibt. Es kann bis zu einem doppelten Intervall dauern, bis der Anbieter entladen wurde. Die Uhrzeit liegt im [Intervall Format](interval-format.md)vor.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ eventconsumerprovidercachecontrol** -Klasse ist von [**\_ \_ CacheControl**](--cachecontrol.md)abgeleitet. Weitere Informationen zum Verwenden dieser Klasse finden Sie unter [Entladen eines Anbieters](unloading-a-provider.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Root<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> </dl>

 

 




