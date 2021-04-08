---
description: Der dynamische Qualifizierer gibt eine Klasse an, deren Instanzen dynamisch erstellt werden. Der Wert dieses Qualifizierers muss auf "true" festgelegt werden.
ms.assetid: 63286687-abbf-49f0-8061-3b47fba75806
ms.tgt_platform: multiple
title: Dynamischer Qualifizierer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dynamic
api_type:
- NA
api_location: ''
ms.openlocfilehash: f6530942859c8c3de571ba9ddb94e9b1ce78cc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864023"
---
# <a name="dynamic-qualifier"></a>Dynamischer Qualifizierer

Der **dynamische** Qualifizierer gibt eine Klasse an, deren Instanzen dynamisch erstellt werden. Der Wert dieses Qualifizierers muss auf " **true**" festgelegt werden.

Der **dynamische** Qualifizierer muss für alle Klassen angegeben werden, die Daten enthalten und für die Instanzen dynamisch erstellt werden. Der [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) wird normalerweise auch angegeben, um den für die Bereitstellung der Daten verantwortlichen Anbieter zu identifizieren.

Klassen, die nur Methoden enthalten, die implementieren müssen, erfordern nicht den **dynamischen** Qualifizierer. Nur der [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) ist erforderlich, um den Namen des Anbieters anzugeben, um die Implementierung bereitzustellen.

Alle Klassen, die von einer dynamischen Klasse abgeleitet werden, müssen dynamisch sein. Eine statische Klasse kann nicht von einer dynamischen Klasse abgeleitet werden.

Wenn **Dynamic** für eine Eigenschaft einer Instanz angegeben ist, muss auch der **propertycontext** -Qualifizierer angegeben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WMI-Standard Qualifizierer**](standard-wmi-qualifiers.md)
</dt> <dt>

[WMI Qualifizierer](wmi-qualifiers.md)
</dt> <dt>

[Fügen eines Qualifizierers](adding-a-qualifier.md)
</dt> </dl>

 

 




