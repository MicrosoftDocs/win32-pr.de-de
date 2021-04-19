---
description: Die folgenden Klassen werden deklariert und mit Klassen Bezeichner (CLSIDs) in wmcodecdsp. h verknüpft.
ms.assetid: f82d92dc-fbce-4274-a10f-72fa8dd776cc
title: Klassen Bezeichner für den Inhaltsverzeichnis Tabelle (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5108855c687085e77ce36aa14b3424732e25572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346670"
---
# <a name="class-identifiers-for-table-of-contents-parser"></a><span data-ttu-id="7259c-103">Klassen Bezeichner für Inhaltsverzeichnis Tabelle</span><span class="sxs-lookup"><span data-stu-id="7259c-103">Class Identifiers for Table of Contents Parser</span></span>

<span data-ttu-id="7259c-104">Die folgenden Klassen werden deklariert und mit Klassen Bezeichner (CLSIDs) in wmcodecdsp. h verknüpft.</span><span class="sxs-lookup"><span data-stu-id="7259c-104">The following classes are declared and associated with class identifiers (CLSIDs) in wmcodecdsp.h.</span></span>



| <span data-ttu-id="7259c-105">Klassenname</span><span class="sxs-lookup"><span data-stu-id="7259c-105">Class name</span></span>       | <span data-ttu-id="7259c-106">Anzeigeobjekt Name</span><span class="sxs-lookup"><span data-stu-id="7259c-106">Friendly object name</span></span> |
|------------------|----------------------|
| <span data-ttu-id="7259c-107">Cchcentry</span><span class="sxs-lookup"><span data-stu-id="7259c-107">CTocEntry</span></span>        | <span data-ttu-id="7259c-108">Inhaltseintrag</span><span class="sxs-lookup"><span data-stu-id="7259c-108">TOC Entry</span></span>            |
| <span data-ttu-id="7259c-109">Cycentrylist</span><span class="sxs-lookup"><span data-stu-id="7259c-109">CTocEntryList</span></span>    | <span data-ttu-id="7259c-110">Inhaltsliste für Inhaltsverzeichnis</span><span class="sxs-lookup"><span data-stu-id="7259c-110">TOC Entry List</span></span>       |
| <span data-ttu-id="7259c-111">Cinhalts Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="7259c-111">CToc</span></span>             | <span data-ttu-id="7259c-112">INHALTSVERZEICHNIS</span><span class="sxs-lookup"><span data-stu-id="7259c-112">TOC</span></span>                  |
| <span data-ttu-id="7259c-113">Cdeccollection</span><span class="sxs-lookup"><span data-stu-id="7259c-113">CTocCollection</span></span>   | <span data-ttu-id="7259c-114">Inhalts Sammlung</span><span class="sxs-lookup"><span data-stu-id="7259c-114">TOC Collection</span></span>       |
| <span data-ttu-id="7259c-115">Cdecparser</span><span class="sxs-lookup"><span data-stu-id="7259c-115">CTocParser</span></span>       | <span data-ttu-id="7259c-116">Inhaltsverzeichnis</span><span class="sxs-lookup"><span data-stu-id="7259c-116">TOC Parser</span></span>           |
| <span data-ttu-id="7259c-117">Cdecgeneratordmo</span><span class="sxs-lookup"><span data-stu-id="7259c-117">CTocGeneratorDmo</span></span> | <span data-ttu-id="7259c-118">TOC-Generator</span><span class="sxs-lookup"><span data-stu-id="7259c-118">TOC Generator</span></span>        |



 

<span data-ttu-id="7259c-119">Die obige Tabelle enthält einen anzeigen Amen für jede Klasse.</span><span class="sxs-lookup"><span data-stu-id="7259c-119">The preceding table gives a friendly object name for each class.</span></span> <span data-ttu-id="7259c-120">In dieser Dokumentation werden diese anzeigen Amen verwendet, um auf Instanzen der Klassen zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="7259c-120">This documentation uses those friendly names to refer to instances of the classes.</span></span> <span data-ttu-id="7259c-121">Die Dokumentation bezieht sich z. b. auf eine Instanz der cycentry-Klasse als ein Inhalts Objekt.</span><span class="sxs-lookup"><span data-stu-id="7259c-121">For example, the documentation refers to an instance of the CTocEntry class as a TOC Entry object.</span></span>

<span data-ttu-id="7259c-122">Im Code können Sie **\_ \_ uuidof** verwenden, um auf die CLSIDs zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="7259c-122">In code, you can use **\_\_uuidof** to refer to the CLSIDs.</span></span> <span data-ttu-id="7259c-123">Beispielsweise können Sie den folgenden Code verwenden, um auf die CLSID für cycgeneratordmo zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="7259c-123">For example, you can use the following code to refer to the CLSID for CTocGeneratorDmo.</span></span>


```C++
__uuidof(CTocGeneratorDmo)
```



### <a name="clsid-constants-defined-in-wmcodecdsph"></a><span data-ttu-id="7259c-124">In "wmcodecdsp. h" definierte CLSID-Konstanten</span><span class="sxs-lookup"><span data-stu-id="7259c-124">CLSID Constants Defined in Wmcodecdsp.h</span></span>

<span data-ttu-id="7259c-125">Als Alternative zur Verwendung von **\_ \_ uuidof** können Sie Konstanten verwenden, um auf die CLSIDs zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="7259c-125">As an alternative to using **\_\_uuidof**, you can use constants to refer to the CLSIDs.</span></span> <span data-ttu-id="7259c-126">Die folgenden Konstanten sind in wmcodecdsp. h definiert.</span><span class="sxs-lookup"><span data-stu-id="7259c-126">The following constants are defined in wmcodecdsp.h</span></span>



| <span data-ttu-id="7259c-127">Klassenname</span><span class="sxs-lookup"><span data-stu-id="7259c-127">Class name</span></span>     | <span data-ttu-id="7259c-128">CLSID-Konstante</span><span class="sxs-lookup"><span data-stu-id="7259c-128">CLSID constant</span></span>        |
|----------------|-----------------------|
| <span data-ttu-id="7259c-129">Cchcentry</span><span class="sxs-lookup"><span data-stu-id="7259c-129">CTocEntry</span></span>      | <span data-ttu-id="7259c-130">CLSID \_ cumcentry</span><span class="sxs-lookup"><span data-stu-id="7259c-130">CLSID\_CTocEntry</span></span>      |
| <span data-ttu-id="7259c-131">Cycentrylist</span><span class="sxs-lookup"><span data-stu-id="7259c-131">CTocEntryList</span></span>  | <span data-ttu-id="7259c-132">CLSID \_ cycentrylist</span><span class="sxs-lookup"><span data-stu-id="7259c-132">CLSID\_CTocEntryList</span></span>  |
| <span data-ttu-id="7259c-133">Cinhalts Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="7259c-133">CToc</span></span>           | <span data-ttu-id="7259c-134">CLSID- \_ cinhalts</span><span class="sxs-lookup"><span data-stu-id="7259c-134">CLSID\_CToc</span></span>           |
| <span data-ttu-id="7259c-135">Cdeccollection</span><span class="sxs-lookup"><span data-stu-id="7259c-135">CTocCollection</span></span> | <span data-ttu-id="7259c-136">CLSID \_ cdeccollection</span><span class="sxs-lookup"><span data-stu-id="7259c-136">CLSID\_CTocCollection</span></span> |
| <span data-ttu-id="7259c-137">Cdecparser</span><span class="sxs-lookup"><span data-stu-id="7259c-137">CTocParser</span></span>     | <span data-ttu-id="7259c-138">CLSID \_ cdecparser</span><span class="sxs-lookup"><span data-stu-id="7259c-138">CLSID\_CTocParser</span></span>     |



 

### <a name="clsid-constants-defined-in-wmcodecdspuuidlib"></a><span data-ttu-id="7259c-139">In wmcodecdspuuid. lib definierte CLSID-Konstanten</span><span class="sxs-lookup"><span data-stu-id="7259c-139">CLSID Constants Defined in Wmcodecdspuuid.lib</span></span>

<span data-ttu-id="7259c-140">Die folgende CLSID-Konstante wird in wmcodecdsp. h deklariert, aber nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="7259c-140">The following CLSID constant is declared, but not defined, in wmcodecdsp.h.</span></span> <span data-ttu-id="7259c-141">Um Sie im Code zu verwenden, müssen Sie eine Verknüpfung mit wmcodecdspuuid. lib herstellen.</span><span class="sxs-lookup"><span data-stu-id="7259c-141">To use it in code, you must link against wmcodecdspuuid.lib.</span></span>



| <span data-ttu-id="7259c-142">Klassenname</span><span class="sxs-lookup"><span data-stu-id="7259c-142">Class name</span></span>       | <span data-ttu-id="7259c-143">CLSID-Konstante</span><span class="sxs-lookup"><span data-stu-id="7259c-143">CLSID constant</span></span>          |
|------------------|-------------------------|
| <span data-ttu-id="7259c-144">Cdecgeneratordmo</span><span class="sxs-lookup"><span data-stu-id="7259c-144">CTocGeneratorDmo</span></span> | <span data-ttu-id="7259c-145">CLSID \_ cdecgeneratordmo</span><span class="sxs-lookup"><span data-stu-id="7259c-145">CLSID\_CTocGeneratorDmo</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="7259c-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7259c-146">Requirements</span></span>



| <span data-ttu-id="7259c-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7259c-147">Requirement</span></span> | <span data-ttu-id="7259c-148">Wert</span><span class="sxs-lookup"><span data-stu-id="7259c-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7259c-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7259c-149">Minimum supported client</span></span><br/> | <span data-ttu-id="7259c-150">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7259c-150">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7259c-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7259c-151">Minimum supported server</span></span><br/> | <span data-ttu-id="7259c-152">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7259c-152">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7259c-153">Header</span><span class="sxs-lookup"><span data-stu-id="7259c-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="7259c-154"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7259c-154"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="7259c-155">DLL</span><span class="sxs-lookup"><span data-stu-id="7259c-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7259c-156"><dt>Wmvdspa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7259c-156"><dt>Wmvdspa.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7259c-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7259c-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7259c-158">Tabelle mit Inhalts parserobjekten</span><span class="sxs-lookup"><span data-stu-id="7259c-158">Table of Contents Parser Objects</span></span>](toc-parser-objects.md)
</dt> </dl>

 

 




