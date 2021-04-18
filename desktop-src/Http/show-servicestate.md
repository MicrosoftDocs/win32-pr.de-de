---
title: show servicestate
description: Zeigt eine Momentaufnahme des http-Dienes an.
ms.assetid: a50a3ef5-5e62-412e-a443-11d453778f70
keywords:
- SERVICESTATE ausgeführt wird anzeigen (http)
topic_type:
- apiref
api_name:
- show servicestate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f79bfdb946d286c31ce284efa09e75ad93c34438
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "106338234"
---
# <a name="show-servicestate"></a><span data-ttu-id="73fce-104">show servicestate</span><span class="sxs-lookup"><span data-stu-id="73fce-104">show servicestate</span></span>

<span data-ttu-id="73fce-105">Zeigt eine Momentaufnahme des http-Dienes an.</span><span class="sxs-lookup"><span data-stu-id="73fce-105">Shows a snapshot of the HTTP service.</span></span>

``` syntax
show servicestate [[view=]{session|requestq}] [[verbose=]{yes|no}]
 
```

## <a name="parameters"></a><span data-ttu-id="73fce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="73fce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73fce-107"><span id="__view___session_requestq__"></span><span id="__VIEW___SESSION_REQUESTQ__"></span>**\[\[View = \] {Session \| requestq}\]**</span><span class="sxs-lookup"><span data-stu-id="73fce-107"><span id="__view___session_requestq__"></span><span id="__VIEW___SESSION_REQUESTQ__"></span>**\[\[view=\]{session\|requestq}\]**</span></span>
</dt> <dd>

<span data-ttu-id="73fce-108">Anzeigen einer Momentaufnahme des http-Dienststatus basierend auf Server Sitzung oder Anforderungs Warteschlangen.</span><span class="sxs-lookup"><span data-stu-id="73fce-108">View snapshot of HTTP service state based on server session or request queues.</span></span>

</dd> <dt>

<span data-ttu-id="73fce-109"><span id="__verbose___yes_no__"></span><span id="__VERBOSE___YES_NO__"></span>**\[\[Verbose = \] {Yes \| No}\]**</span><span class="sxs-lookup"><span data-stu-id="73fce-109"><span id="__verbose___yes_no__"></span><span id="__VERBOSE___YES_NO__"></span>**\[\[verbose=\]{yes\|no}\]**</span></span>
</dt> <dd>

<span data-ttu-id="73fce-110">Ausführliche Informationen zu den Eigenschafts Informationen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="73fce-110">View verbose information showing property information too.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="73fce-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="73fce-111">Examples</span></span>

<span data-ttu-id="73fce-112">**SERVICESTATE ausgeführt wird View = Session anzeigen**</span><span class="sxs-lookup"><span data-stu-id="73fce-112">**show servicestate view=session**</span></span>

<span data-ttu-id="73fce-113">**SERVICESTATE ausgeführt wird View = requestq Verbose = Yes anzeigen**</span><span class="sxs-lookup"><span data-stu-id="73fce-113">**show servicestate view=requestq verbose=yes**</span></span>

 

 




