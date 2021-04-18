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
# <a name="delete-timeout"></a><span data-ttu-id="6b95c-104">delete timeout</span><span class="sxs-lookup"><span data-stu-id="6b95c-104">delete timeout</span></span>

<span data-ttu-id="6b95c-105">Löscht ein globales Timeout und macht den HTTP.sys-Dienst auf die Standardwerte zurück.</span><span class="sxs-lookup"><span data-stu-id="6b95c-105">Deletes a global timeout and makes the HTTP.sys service revert to default values.</span></span>

``` syntax
delete timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
 
```

## <a name="parameters"></a><span data-ttu-id="6b95c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b95c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b95c-107"><span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype = \] {idleconnectiontimeout \| HeaderWaitTimeout}**</span><span class="sxs-lookup"><span data-stu-id="6b95c-107"><span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype=\]{idleconnectiontimeout\|headerwaittimeout}**</span></span>
</dt> <dd>

<span data-ttu-id="6b95c-108">Gibt den Typ der Einstellung für die Zeitüberschreitung an.</span><span class="sxs-lookup"><span data-stu-id="6b95c-108">Specifies the type of timeout setting.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="6b95c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b95c-109">Examples</span></span>

<span data-ttu-id="6b95c-110">**delete timeout timeouttype=idleconnectiontimeout**</span><span class="sxs-lookup"><span data-stu-id="6b95c-110">**delete timeout timeouttype=idleconnectiontimeout**</span></span>

<span data-ttu-id="6b95c-111">**delete timeout timeouttype=headerwaittimeout**</span><span class="sxs-lookup"><span data-stu-id="6b95c-111">**delete timeout timeouttype=headerwaittimeout**</span></span>

 

 




