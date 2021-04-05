---
description: Löscht eine vorhandene Instanz einer Klasse aus dem Repository.
ms.assetid: 4389f831-a60e-4198-a55a-79189d10a38a
ms.tgt_platform: multiple
title: pragma Delta einstance
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
ms.openlocfilehash: 10d4c735f1e59533b57ae1814cfb8e36b2c1ad76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041889"
---
# <a name="pragma-deleteinstance"></a><span data-ttu-id="44649-103">pragma Delta einstance</span><span class="sxs-lookup"><span data-stu-id="44649-103">pragma deleteinstance</span></span>

<span data-ttu-id="44649-104">Der **pragma-Delta** Befehl löscht eine vorhandene Instanz einer Klasse aus dem Repository.</span><span class="sxs-lookup"><span data-stu-id="44649-104">The **pragma deleteinstance** command deletes an existing instance of a class from the repository.</span></span>

<span data-ttu-id="44649-105">Im folgenden wird die Syntax für diesen Befehl beschrieben:</span><span class="sxs-lookup"><span data-stu-id="44649-105">The following describes the syntax for this command:</span></span>


```mof
#pragma deleteinstance("InstanceId", [Flag])
```



<span data-ttu-id="44649-106">*InstanceId* ist ein eindeutiger Bezeichner der Instanz, die der MOF-Compiler aus dem aktuellen Namespace löscht.</span><span class="sxs-lookup"><span data-stu-id="44649-106">*InstanceId* is a unique identifier of the instance the MOF compiler deletes from the current namespace.</span></span>

<span data-ttu-id="44649-107">Das *\[ Flag \]* muss eines der folgenden Argumente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="44649-107">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="44649-108">Flag</span><span class="sxs-lookup"><span data-stu-id="44649-108">Flag</span></span>   | <span data-ttu-id="44649-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44649-109">Description</span></span>                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44649-110">fehlerhaft</span><span class="sxs-lookup"><span data-stu-id="44649-110">fail</span></span>   | <span data-ttu-id="44649-111">Bewirkt, dass der MOF-Compiler mit einer Fehlermeldung beendet wird, wenn die Klasse nicht bereits im Repository vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="44649-111">Causes the MOF compiler to quit with an error message if the class does not already exist in the repository.</span></span> |
| <span data-ttu-id="44649-112">"nofail"</span><span class="sxs-lookup"><span data-stu-id="44649-112">nofail</span></span> | <span data-ttu-id="44649-113">Bewirkt, dass der MOF-Compiler fortgesetzt wird, auch wenn die Klasse nicht bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="44649-113">Causes the MOF compiler to continue even if the class does not already exist.</span></span>                                |



 

## <a name="examples"></a><span data-ttu-id="44649-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44649-114">Examples</span></span>

<span data-ttu-id="44649-115">Im folgenden Beispiel wird gezeigt, wie dieser Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="44649-115">The following example shows how to use this command.</span></span>


```mof
#pragma deleteinstance(
    "MSFT_RisingFallingTemplate.id='TestRisingFallingCorrId'",
    nofail)
```



## <a name="requirements"></a><span data-ttu-id="44649-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44649-116">Requirements</span></span>



| <span data-ttu-id="44649-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44649-117">Requirement</span></span> | <span data-ttu-id="44649-118">Wert</span><span class="sxs-lookup"><span data-stu-id="44649-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="44649-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44649-119">Minimum supported client</span></span><br/> | <span data-ttu-id="44649-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44649-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="44649-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44649-121">Minimum supported server</span></span><br/> | <span data-ttu-id="44649-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44649-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44649-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44649-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44649-124">Präprozessorbefehle</span><span class="sxs-lookup"><span data-stu-id="44649-124">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




