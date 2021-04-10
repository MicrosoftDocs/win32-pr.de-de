---
description: Löscht eine vorhandene Klasse und deren Instanzen aus dem Repository.
ms.assetid: 6f96d14a-16ab-4e83-a75f-5dbf162d1692
ms.tgt_platform: multiple
title: pragma deleteclass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0d3b5b1fa209be7fd472a87aec25a5e590d93c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868591"
---
# <a name="pragma-deleteclass"></a><span data-ttu-id="b7eef-103">pragma deleteclass</span><span class="sxs-lookup"><span data-stu-id="b7eef-103">pragma deleteclass</span></span>

<span data-ttu-id="b7eef-104">Der **pragma deleteclass** -Präprozessorbefehl löscht eine vorhandene Klasse und deren Instanzen aus dem Repository.</span><span class="sxs-lookup"><span data-stu-id="b7eef-104">The **pragma deleteclass** preprocessor command deletes an existing class and its instances from the repository.</span></span>

<span data-ttu-id="b7eef-105">Im folgenden wird die Syntax beschrieben:</span><span class="sxs-lookup"><span data-stu-id="b7eef-105">The following describes the syntax:</span></span>


```mof
#pragma deleteclass("ClassName", [Flag])
```



<span data-ttu-id="b7eef-106">*ClassName* ist der Name der Klasse, die der MOF-Compiler aus dem aktuellen Namespace löscht.</span><span class="sxs-lookup"><span data-stu-id="b7eef-106">*ClassName* is the name of the class that the MOF compiler deletes from the current namespace.</span></span>

<span data-ttu-id="b7eef-107">Das *\[ Flag \]* muss eines der folgenden Argumente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b7eef-107">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="b7eef-108">Flag</span><span class="sxs-lookup"><span data-stu-id="b7eef-108">Flag</span></span>   | <span data-ttu-id="b7eef-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7eef-109">Description</span></span>                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7eef-110">fehlerhaft</span><span class="sxs-lookup"><span data-stu-id="b7eef-110">fail</span></span>   | <span data-ttu-id="b7eef-111">Bewirkt, dass der MOF-Compiler mit einer Fehlermeldung beendet wird, wenn die Klasse nicht bereits im Repository vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b7eef-111">Causes the MOF compiler to quit with an error message if the class does not already exist in the repository.</span></span> |
| <span data-ttu-id="b7eef-112">"nofail"</span><span class="sxs-lookup"><span data-stu-id="b7eef-112">nofail</span></span> | <span data-ttu-id="b7eef-113">Bewirkt, dass der MOF-Compiler fortgesetzt wird, auch wenn die Klasse nicht bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b7eef-113">Causes the MOF compiler to continue even if the class does not already exist.</span></span>                                |



 

## <a name="examples"></a><span data-ttu-id="b7eef-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7eef-114">Examples</span></span>

<span data-ttu-id="b7eef-115">Im folgenden Beispiel wird gezeigt, wie dieser Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b7eef-115">The following example shows how to use this command.</span></span>


```mof
#pragma deleteclass("MyClass1",FAIL)
```



## <a name="requirements"></a><span data-ttu-id="b7eef-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7eef-116">Requirements</span></span>



| <span data-ttu-id="b7eef-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7eef-117">Requirement</span></span> | <span data-ttu-id="b7eef-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b7eef-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b7eef-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7eef-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b7eef-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7eef-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b7eef-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7eef-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b7eef-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7eef-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7eef-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7eef-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7eef-124">Präprozessorbefehle</span><span class="sxs-lookup"><span data-stu-id="b7eef-124">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




