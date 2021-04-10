---
title: show urlacl
description: Listet DACLs für die angegebene reservierte URL oder alle reservierten URLs auf.
ms.assetid: 8428583c-b420-408f-974f-670b6809fa3c
keywords:
- urlacl-http anzeigen
topic_type:
- apiref
api_name:
- show urlacl
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f86f7856e70a1be327297bb3fd4b892b3bf39789
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "103948271"
---
# <a name="show-urlacl"></a><span data-ttu-id="6a8ae-104">show urlacl</span><span class="sxs-lookup"><span data-stu-id="6a8ae-104">show urlacl</span></span>

<span data-ttu-id="6a8ae-105">Listet DACLs für die angegebene reservierte URL oder alle reservierten URLs auf.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-105">Lists DACLs for the specified reserved URL or all reserved URLs.</span></span>

``` syntax
show urlacl [url=]string
 
```

## <a name="parameters"></a><span data-ttu-id="6a8ae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a8ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a8ae-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[URL = \] \* \* \* Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="6a8ae-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[url=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="6a8ae-108">Gibt die voll qualifizierte URL an.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-108">Specifies the fully qualified URL.</span></span> <span data-ttu-id="6a8ae-109">Wenn nicht angegeben, werden alle URLs impliziert.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-109">If unspecified, implies all URLs.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="6a8ae-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6a8ae-110">Examples</span></span>

<span data-ttu-id="6a8ae-111">**urlacl-URL anzeigen =https://+:80/MyUrl**</span><span class="sxs-lookup"><span data-stu-id="6a8ae-111">**show urlacl url=https://+:80/MyUrl**</span></span>

<span data-ttu-id="6a8ae-112">**urlacl-URL anzeigen =https://www.contoso.com:80/MyUrl**</span><span class="sxs-lookup"><span data-stu-id="6a8ae-112">**show urlacl url=https://www.contoso.com:80/MyUrl**</span></span>

 

 




