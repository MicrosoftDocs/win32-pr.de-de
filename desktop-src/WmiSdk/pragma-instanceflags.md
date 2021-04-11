---
description: Steuert die Art und Weise, in der Instanzen abhängig von den angegebenen Flags erstellt oder aktualisiert werden.
ms.assetid: 9932edf2-2e5f-4c5e-9889-f2be4af11bf2
ms.tgt_platform: multiple
title: pragma instanceflags
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
ms.openlocfilehash: acc05e201fcf153ab2156d4a360ce36b4539cd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218314"
---
# <a name="pragma-instanceflags"></a><span data-ttu-id="a7cca-103">pragma instanceflags</span><span class="sxs-lookup"><span data-stu-id="a7cca-103">pragma instanceflags</span></span>

<span data-ttu-id="a7cca-104">Der **pragma instanceflags** -Präprozessorbefehl steuert die Art und Weise, in der Instanzen abhängig von den angegebenen Flags erstellt oder aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a7cca-104">The **pragma instanceflags** preprocessor command controls the way instances are created or updated depending on the flags specified.</span></span>

<span data-ttu-id="a7cca-105">Im folgenden wird die Syntax beschrieben:</span><span class="sxs-lookup"><span data-stu-id="a7cca-105">The following describes the syntax:</span></span>


```mof
#pragma instanceflags ([Flag])
```



<span data-ttu-id="a7cca-106">Das *\[ Flag \]* muss eines der folgenden Argumente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a7cca-106">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="a7cca-107">Flag</span><span class="sxs-lookup"><span data-stu-id="a7cca-107">Flag</span></span>       | <span data-ttu-id="a7cca-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7cca-108">Description</span></span>                                                                                                |
|------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7cca-109">createonly</span><span class="sxs-lookup"><span data-stu-id="a7cca-109">createonly</span></span> | <span data-ttu-id="a7cca-110">Verhindert, dass der Compiler vorhandene Instanzen in der MOF-Datei ändert.</span><span class="sxs-lookup"><span data-stu-id="a7cca-110">Prevents the compiler from changing any existing instances in the MOF file.</span></span>                                |
| <span data-ttu-id="a7cca-111">updateonly</span><span class="sxs-lookup"><span data-stu-id="a7cca-111">updateonly</span></span> | <span data-ttu-id="a7cca-112">Verhindert, dass der Compiler neue Instanzen erstellt, wenn eine Instanz, die in der MOF-Datei angegeben ist, nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a7cca-112">Prevents the compiler from creating new instances if an instance specified in the MOF file does not exist.</span></span> |



 

## <a name="examples"></a><span data-ttu-id="a7cca-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7cca-113">Examples</span></span>

<span data-ttu-id="a7cca-114">Im folgenden Beispiel wird gezeigt, wie dieser Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a7cca-114">The following example shows how to use this command.</span></span>


```mof
#pragma instanceflags("createonly")
```



## <a name="requirements"></a><span data-ttu-id="a7cca-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7cca-115">Requirements</span></span>



| <span data-ttu-id="a7cca-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7cca-116">Requirement</span></span> | <span data-ttu-id="a7cca-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a7cca-117">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a7cca-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7cca-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a7cca-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7cca-119">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a7cca-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7cca-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a7cca-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7cca-121">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a7cca-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7cca-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7cca-123">Präprozessorbefehle</span><span class="sxs-lookup"><span data-stu-id="a7cca-123">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




