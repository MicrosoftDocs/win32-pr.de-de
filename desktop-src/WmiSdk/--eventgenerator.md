---
description: Fungiert als übergeordnete Klasse für Klassen, die die Generierung von Ereignissen steuern, z. b. Timer-Ereignisse.
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
ms.openlocfilehash: b40524405c3b284e7ec61414e36448cb37afeab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218657"
---
# <a name="__eventgenerator-class"></a>\_\_Eventgenerator-Klasse

Die **\_ \_ eventgenerator** -System Klasse ist eine abstrakte Basisklasse, die als übergeordnete Klasse für Klassen fungiert, die die Generierung von Ereignissen steuern, z. b. [Timer-Ereignisse](receiving-a-timed-or-repeating-event.md).

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[abstract]
class __EventGenerator : __IndicationRelated
{
};
```

## <a name="members"></a>Member

Die **\_ \_ eventgenerator** -Klasse definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ eventgenerator** -Klasse wird von " [**\_ \_ indicationrelated**](--indicationrelated.md)" abgeleitet, die keine Eigenschaften hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Indicationrelated**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> </dl>

 

