---
description: Weist den MOF-Compiler an, eine MOF-Datei in sprachneutrale und sprachspezifische Versionen aufzuteilen.
ms.assetid: c1aec33c-b936-4cca-8fcd-7bd088af7116
ms.tgt_platform: multiple
title: pragma-Zusatz
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
ms.openlocfilehash: 1269ac1a96617b72852e687b2a38ce8d331ab3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753697"
---
# <a name="pragma-amendment"></a><span data-ttu-id="0a61c-103">pragma-Zusatz</span><span class="sxs-lookup"><span data-stu-id="0a61c-103">pragma amendment</span></span>

<span data-ttu-id="0a61c-104">Der Präprozessorbefehl " **pragma-Zusatz** " weist den MOF-Compiler an, eine MOF-Datei in sprachneutrale und sprachspezifische Versionen zu trennen.</span><span class="sxs-lookup"><span data-stu-id="0a61c-104">The **pragma amendment** preprocessor command directs the MOF compiler to separate a MOF file into language-neutral and language-specific versions.</span></span> <span data-ttu-id="0a61c-105">Die sprachspezifische MOF-Datei verschiebt geänderte Qualifizierer in einen Namespace für ein bestimmtes Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="0a61c-105">The language-specific MOF file moves amended qualifiers to a namespace for a specific locale.</span></span> <span data-ttu-id="0a61c-106">Anschließend kompilieren Sie die sprachspezifischen und sprach neutralen MOF-Dateien, um Klassen Informationen im WMI-Repository zu speichern.</span><span class="sxs-lookup"><span data-stu-id="0a61c-106">You then compile the language-specific and language-neutral MOF files to store class information in the WMI repository.</span></span>

## <a name="examples"></a><span data-ttu-id="0a61c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a61c-107">Examples</span></span>

<span data-ttu-id="0a61c-108">Im folgenden Beispiel wird gezeigt, wie eine MOF-Datei erstellt wird, die geänderte Qualifizierer enthält.</span><span class="sxs-lookup"><span data-stu-id="0a61c-108">The following example shows how to create a MOF file that contains amended qualifiers.</span></span> <span data-ttu-id="0a61c-109">Anschließend können Sie den MOF-Code mit dem folgenden Befehl kompilieren:</span><span class="sxs-lookup"><span data-stu-id="0a61c-109">You can then compile the MOF code with the following command:</span></span>

<span data-ttu-id="0a61c-110">**MUF Comp** **-MOF: lnmof. MOF** **-MFL: lsmof. MFL** **mastermof. MOF**</span><span class="sxs-lookup"><span data-stu-id="0a61c-110">**mofcomp** **-MOF:Lnmof.mof** **-MFL:Lsmof.mfl** **Mastermof.mof**</span></span>

<span data-ttu-id="0a61c-111">Der Befehl weist den MOF-Compiler an, zwei MOF-Dateien aus der ursprünglichen Datei "mastermof. mof" zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="0a61c-111">The command instructs the MOF compiler to produce two MOF files from the original Mastermof.mof file.</span></span> <span data-ttu-id="0a61c-112">Der MOF-Compiler erstellt eine sprachneutrale Version der MOF-Datei mit dem Namen lnmof. MOF, wobei alle sprachspezifischen Elemente entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="0a61c-112">The MOF compiler produces a language-neutral version of the MOF file, called Lnmof.mof, with all language-specific items removed.</span></span> <span data-ttu-id="0a61c-113">Der Compiler erstellt außerdem eine zweite sprachspezifische MOF-Datei mit dem Namen lsmof. MFL, die nur die Elemente enthält, die Sie lokalisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="0a61c-113">The compiler also creates a second, language-specific MOF file called Lsmof.mfl that contains only items that you must localize.</span></span>

> [!Note]  
> <span data-ttu-id="0a61c-114">Wenn Sie eine MOF-Datei mit dem **Zusatz** Qualifizierer oder dem **pragma-Zusatz** Befehl aufteilen, müssen Sie die **-MOF** -und die **-MFL-** Option angeben.</span><span class="sxs-lookup"><span data-stu-id="0a61c-114">When you are splitting a MOF file with the **amendment** qualifier or the **pragma amendment** command, you must specify the **-MOF** and **-MFL** options.</span></span> <span data-ttu-id="0a61c-115">Andernfalls generiert der Compiler keine Ausgabedateien.</span><span class="sxs-lookup"><span data-stu-id="0a61c-115">Otherwise, the compiler does not generate any output files.</span></span> <span data-ttu-id="0a61c-116">Sie müssen dann die beiden Ausgabedateien kompilieren, um die Klassen Informationen für WMI verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="0a61c-116">You must then compile the two output files to make the class information available to WMI.</span></span>

 


```mof
#pragma amendment ("MS_409")

[Description("Localized version of MyClass" for American English") :
    Amended, LOCALE(0x409)] 

Class myclass
{
     [DisplayName("User Name") : Amended,
     Description("The Name property contains the name of the user") : 
     Amended, key]
    string Name;

    uint64 Value; // non-localized value field

     [DisplayName("Time Stamp") : Amended,
     Description("This property shows when the object was created") : 
     Amended] 
    uint64 Timestamp;
};
```



## <a name="requirements"></a><span data-ttu-id="0a61c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a61c-117">Requirements</span></span>



| <span data-ttu-id="0a61c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a61c-118">Requirement</span></span> | <span data-ttu-id="0a61c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0a61c-119">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="0a61c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a61c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0a61c-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a61c-121">Windows Vista</span></span><br/>       |
| <span data-ttu-id="0a61c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a61c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0a61c-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a61c-123">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a61c-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a61c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a61c-125">Präprozessorbefehle</span><span class="sxs-lookup"><span data-stu-id="0a61c-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




