---
title: delete cache
description: Leert den gesamten URL-Cache oder löscht Einträge entsprechend der angegebenen URL.
ms.assetid: 499ce0f9-01db-4648-89f7-1ecafd25a805
keywords:
- Cache löschen http
topic_type:
- apiref
api_name:
- delete cache
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f963d12812140d11923460235ef780a621ba3db5
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "106338235"
---
# <a name="delete-cache"></a><span data-ttu-id="5ed5d-104">delete cache</span><span class="sxs-lookup"><span data-stu-id="5ed5d-104">delete cache</span></span>

<span data-ttu-id="5ed5d-105">Leert den gesamten URL-Cache oder löscht Einträge entsprechend der angegebenen URL.</span><span class="sxs-lookup"><span data-stu-id="5ed5d-105">Flushes the entire URL cache or deletes entries according to the specified URL.</span></span>

``` syntax
delete cache [url=]string [[recursive=]{yes|no}]
 
```

## <a name="parameters"></a><span data-ttu-id="5ed5d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ed5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ed5d-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[URL = \] \* \* \* Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="5ed5d-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[url=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="5ed5d-108">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5ed5d-108">Required.</span></span> <span data-ttu-id="5ed5d-109">Gibt die voll qualifizierte URL an.</span><span class="sxs-lookup"><span data-stu-id="5ed5d-109">Specifies the fully qualified URL.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="5ed5d-110"><span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[rekursiv = \] {Yes \| No}**</span><span class="sxs-lookup"><span data-stu-id="5ed5d-110"><span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[recursive=\]{yes\|no}**</span></span>
</dt> <dd>

<span data-ttu-id="5ed5d-111">Wenn ja, werden alle Einträge unter der angegebenen URL entfernt.</span><span class="sxs-lookup"><span data-stu-id="5ed5d-111">If yes, removes all entries under the specified URL.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="5ed5d-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ed5d-112">Examples</span></span>

<span data-ttu-id="5ed5d-113">**Cache-URL löschen = https://www.contoso.com:80/myresource/ rekursiv = ja**</span><span class="sxs-lookup"><span data-stu-id="5ed5d-113">**delete cache url=https://www.contoso.com:80/myresource/ recursive=yes**</span></span>

 

 




