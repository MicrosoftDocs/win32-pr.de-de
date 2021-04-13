---
title: show cachestate
description: Listet alle Ressourcen und die zugehörigen Eigenschaften auf, die im HTTP-Antwort Cache zwischengespeichert werden, oder zeigt eine einzelne Ressource und die zugehörigen Eigenschaften an.
ms.assetid: 9daa445e-dd2f-4b73-8938-58df931c015b
keywords:
- Cache Estate http anzeigen
topic_type:
- apiref
api_name:
- show cachestate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 088a59eaa92db8ed9e8cbe59075d540507e51535
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313314"
---
# <a name="show-cachestate"></a><span data-ttu-id="40c93-104">show cachestate</span><span class="sxs-lookup"><span data-stu-id="40c93-104">show cachestate</span></span>

<span data-ttu-id="40c93-105">Listet alle Ressourcen und die zugehörigen Eigenschaften auf, die im HTTP-Antwort Cache zwischengespeichert werden, oder zeigt eine einzelne Ressource und die zugehörigen Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="40c93-105">Lists all resources and their associated properties that are cached in the HTTP response cache or displays a single resource and its associated properties.</span></span>

``` syntax
show cachestate [[url=]string]
 
```

## <a name="parameters"></a><span data-ttu-id="40c93-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="40c93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40c93-107"><span id="__url__string_"></span><span id="__URL__STRING_"></span>**\[\[URL = \] ***Zeichenfolge***\]**</span><span class="sxs-lookup"><span data-stu-id="40c93-107"><span id="__url__string_"></span><span id="__URL__STRING_"></span>**\[\[url=\]***string***\]**</span></span>
</dt> <dd>

<span data-ttu-id="40c93-108">Voll qualifizierte URL.</span><span class="sxs-lookup"><span data-stu-id="40c93-108">Fully qualified URL.</span></span> <span data-ttu-id="40c93-109">Wenn nicht angegeben, werden alle URLs impliziert.</span><span class="sxs-lookup"><span data-stu-id="40c93-109">If unspecified, implies all URLs.</span></span> <span data-ttu-id="40c93-110">Die URL kann auch ein Präfix für registrierte URLs sein.</span><span class="sxs-lookup"><span data-stu-id="40c93-110">The URL can also be a prefix to registered URLs.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="40c93-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40c93-111">Examples</span></span>

<span data-ttu-id="40c93-112">**cachestate-URL anzeigen =https://www.contoso.com:80/myresource**</span><span class="sxs-lookup"><span data-stu-id="40c93-112">**show cachestate url=https://www.contoso.com:80/myresource**</span></span>

 

 




