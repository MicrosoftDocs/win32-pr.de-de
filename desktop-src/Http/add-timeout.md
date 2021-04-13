---
title: add timeout
description: Fügt dem HTTP.sys-Dienst ein globales Timeout hinzu.
ms.assetid: c59a64e2-36aa-4428-b727-df21f5632d0d
keywords:
- Timeout hinzufügen http
topic_type:
- apiref
api_name:
- add timeout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2637cb5db663ea36b15eb382a16b02b166e98f88
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "104389393"
---
# <a name="add-timeout"></a>add timeout

Fügt dem HTTP.sys-Dienst ein globales Timeout hinzu.

``` syntax
add timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
            [value=]u-short

 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype = \] {idleconnectiontimeout \| HeaderWaitTimeout}**
</dt> <dd>

Gibt den Typ des Timeouts für die-Einstellung an.

</dd> <dt>

<span id="_value__u-short"></span><span id="_VALUE__U-SHORT"></span>**\[Wert = \] * * * u-Short*
</dt> <dd>

Gibt den Wert des Timeouts (in Sekunden) an. Wenn der Wert hexadezimal ist, fügen Sie das Präfix 0x hinzu.

</dd> </dl>

## <a name="examples"></a>Beispiele

**add timeout timeouttype=idleconnectiontimeout value=120**

**add timeout timeouttype=headerwaittimeout value=0x40**

 

 




