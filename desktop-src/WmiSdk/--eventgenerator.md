---
description: Dient als übergeordnete Klasse für Klassen, die die Generierung von Ereignissen steuern, z. B. Timerereignisse.
ms.assetid: 381b06e7-2857-4932-9f52-f1d62efa8b79
ms.tgt_platform: multiple
title: __EventGenerator-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventGenerator
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0033bef55915865ba1945c9f17705ed40cd0d3db4cd572efd13cdadf99d4bbab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732902"
---
# <a name="__eventgenerator-class"></a>\_\_EventGenerator-Klasse

Die **\_ \_ EventGenerator-Systemklasse** ist eine abstrakte Basisklasse, die als übergeordnete Klasse für Klassen dient, die die Generierung von Ereignissen steuern, z. B. [Timerereignisse.](receiving-a-timed-or-repeating-event.md)

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[abstract]
class __EventGenerator : __IndicationRelated
{
};
```

## <a name="members"></a>Member

Die **\_ \_ EventGenerator-Klasse** definiert keine Member.

## <a name="remarks"></a>Hinweise

Die **\_ \_ EventGenerator-Klasse** wird von [**\_ \_ IndicationRelated**](--indicationrelated.md)abgeleitet, das über keine Eigenschaften verfügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_\_IndicationRelated**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> </dl>

 

