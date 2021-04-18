---
title: delete timeout
description: Löscht ein globales Timeout und macht den HTTP.sys-Dienst auf die Standardwerte zurück.
ms.assetid: 5fcd5df4-023e-486d-b41a-639e210a128f
keywords:
- Timeout für Löschvorgang http
topic_type:
- apiref
api_name:
- delete timeout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6ee436e1eb7f545a74aa56f6c146afbd1c57066
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "106340675"
---
# <a name="delete-timeout"></a>delete timeout

Löscht ein globales Timeout und macht den HTTP.sys-Dienst auf die Standardwerte zurück.

``` syntax
delete timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype = \] {idleconnectiontimeout \| HeaderWaitTimeout}**
</dt> <dd>

Gibt den Typ der Einstellung für die Zeitüberschreitung an.

</dd> </dl>

## <a name="examples"></a>Beispiele

**delete timeout timeouttype=idleconnectiontimeout**

**delete timeout timeouttype=headerwaittimeout**

 

 




