---
description: Fügt eine MOF-Datei zur Liste der Dateien hinzu, die während der Wiederherstellung des Repository kompiliert wurden.
ms.assetid: 8901c04e-f8c1-45b0-b69d-e2ebc948f088
ms.tgt_platform: multiple
title: pragma-Auto Wiederherstellen
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
ms.openlocfilehash: 9bb1cfca44e0bc5437d05d721ffcd57203e5aa9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960436"
---
# <a name="pragma-autorecover"></a><span data-ttu-id="27112-103">pragma-Auto Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="27112-103">pragma autorecover</span></span>

<span data-ttu-id="27112-104">Der Präprozessorbefehl **pragma Auto Wiederherstellen** fügt eine MOF-Datei zur Liste der Dateien hinzu, die während der Wiederherstellung des Repository kompiliert wurden.</span><span class="sxs-lookup"><span data-stu-id="27112-104">The **pragma autorecover** preprocessor command adds a MOF file to the list of files compiled during repository recovery.</span></span> <span data-ttu-id="27112-105">Die Liste der **Auto Wiederherstellen** -MOF-Dateien wird in diesem Registrierungsschlüssel gespeichert:</span><span class="sxs-lookup"><span data-stu-id="27112-105">The list of **autorecover** MOF files is stored in this registry key:</span></span>

<span data-ttu-id="27112-106">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Auto Wiederherstellen-mufs**</span><span class="sxs-lookup"><span data-stu-id="27112-106">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**autorecover mofs**</span></span>

<span data-ttu-id="27112-107">WMI prüft die Integrität des WMI-Repository, wenn das Betriebssystem WMI startet.</span><span class="sxs-lookup"><span data-stu-id="27112-107">WMI checks the integrity of the WMI repository when the operating system starts WMI.</span></span> <span data-ttu-id="27112-108">Wenn das Repository beschädigt ist, erstellt WMI das Repository automatisch neu und kompiliert alle MOF-Dateien, die in diesem Schlüssel in der Registrierung aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="27112-108">If the repository is damaged, WMI automatically rebuilds the repository and recompiles any MOF files listed in this key in the registry.</span></span>

<span data-ttu-id="27112-109">Im folgenden wird die Syntax für den Pragma Auto Wiederherstellen-Befehl beschrieben:</span><span class="sxs-lookup"><span data-stu-id="27112-109">The following describes the syntax for the pragma autorecover command:</span></span>


```mof
#pragma autorecover
```



<span data-ttu-id="27112-110">Beachten Sie jedoch die folgenden Einschränkungen, wenn Sie diesen Befehl verwenden:</span><span class="sxs-lookup"><span data-stu-id="27112-110">However, you must observe the following restrictions when using this command:</span></span>

-   <span data-ttu-id="27112-111">WMI kann keine MOF-Dateien wiederherstellen, die sich auf einem Remote Computer befinden.</span><span class="sxs-lookup"><span data-stu-id="27112-111">WMI cannot recover MOF files located on a remote computer.</span></span>

    <span data-ttu-id="27112-112">Daher müssen sich die MOF-Dateien, die in diesem Registrierungsschlüssel aufgelistet sind, auf dem lokalen Computer befinden.</span><span class="sxs-lookup"><span data-stu-id="27112-112">Therefore, the MOF files listed in this registry key must reside on the local computer.</span></span>

-   <span data-ttu-id="27112-113">Sie können nicht die Befehls Zeilenschalter angeben, die der MOF-Compiler verwendet, wenn eine MOF-Datei von WMI wieder hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="27112-113">You cannot specify the command-line switches that the MOF compiler uses when WMI recovers a MOF file.</span></span>

    <span data-ttu-id="27112-114">Daher sollten Sie [pragma](-pragma.md) -Befehle in die MOF-Datei einschließen, die Befehls Zeilenschalter unnötig machen.</span><span class="sxs-lookup"><span data-stu-id="27112-114">Therefore, you should include [pragma](-pragma.md) commands in your MOF file that make command-line switches unnecessary.</span></span> <span data-ttu-id="27112-115">Im folgenden Beispiel wird ein allgemeiner Befehls Zeilenschalter beschrieben, der von WMI nicht verwendet wird, wenn eine MOF-Datei aus diesem Registrierungsschlüssel wieder hergestellt wird: " **mufcomp-n:root \\ Test mymof. mof".**</span><span class="sxs-lookup"><span data-stu-id="27112-115">The following example describes a common command-line switch that WMI does not use when recovering a MOF file from this registry key: **mofcomp -N:Root\\Test mymof.mof**</span></span>

    <span data-ttu-id="27112-116">Sie können den Namespace jedoch mit einem [pragma](-pragma.md) -Befehl in der MOF-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="27112-116">However, you can specify the namespace using a [pragma](-pragma.md) command in the MOF file.</span></span>

    ```mof
    #pragma namespace ("\\\\.\\Root\\test")
    ```

    

## <a name="requirements"></a><span data-ttu-id="27112-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27112-117">Requirements</span></span>



| <span data-ttu-id="27112-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27112-118">Requirement</span></span> | <span data-ttu-id="27112-119">Wert</span><span class="sxs-lookup"><span data-stu-id="27112-119">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="27112-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27112-120">Minimum supported client</span></span><br/> | <span data-ttu-id="27112-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27112-121">Windows Vista</span></span><br/>       |
| <span data-ttu-id="27112-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27112-122">Minimum supported server</span></span><br/> | <span data-ttu-id="27112-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27112-123">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="27112-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27112-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27112-125">Präprozessorbefehle</span><span class="sxs-lookup"><span data-stu-id="27112-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




