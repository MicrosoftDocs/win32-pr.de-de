---
description: Wird verwendet, um zu bestimmen, wann WMI einen Ereignisconsumeranbieter iwbemunboundobjectsink-Zeiger freigibt.
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
ms.openlocfilehash: 9d20e64fed1ee6ba5622d5e6a342a60485f53d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352298"
---
# <a name="__eventsinkcachecontrol-class"></a>\_\_EventSink Cache econtrol-Klasse

Die **\_ \_ EventSink Cache econtrol** -System Klasse wird verwendet, um zu bestimmen, wann WMI den [**iwbemunboundobjectsink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) -Zeiger eines Ereignis Verbraucher Anbieters freigibt. Die **\_ \_ EventSink Cache econtrol** -Klasse ist eine Singleton-Klasse. Sie befindet sich nur im \\ Root-Namespace.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[singleton]
class __EventSinkCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Member

Die **\_ \_ EventSink Cache econtrol** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ EventSink Cache econtrol** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Clearafter**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Das Zeitintervall, nach dem WMI einen Ereignis Anbieter freigibt. Es kann bis zu einem doppelten Intervall dauern, bis der Anbieter entladen wurde. Die Uhrzeit liegt im [Intervall Format](interval-format.md)vor.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ EventSink Cache econtrol** -Klasse ist von [**\_ \_ CacheControl**](--cachecontrol.md)abgeleitet. Weitere Informationen zum Verwenden dieser Klasse finden Sie unter [Entladen eines Anbieters](unloading-a-provider.md).

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

 

 




