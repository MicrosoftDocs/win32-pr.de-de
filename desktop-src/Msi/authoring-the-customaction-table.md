---
description: Geben Sie Datensätze für die fünf benutzerdefinierten Beispiel Aktionen ein, die im vorherigen Abschnitt für die Tabelle CustomAction erstellt wurden. Weitere Informationen zum Auffüllen der CustomAction-Tabelle für diese Art von benutzerdefinierter Aktion finden Sie unter benutzerdefinierter Aktionstyp 1.
ms.assetid: 56828105-bd72-426d-833f-f756c577c77f
title: Erstellen der Tabelle "CustomAction"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fb7d8cf99a30200e6a5525e3516e2b888c1129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959509"
---
# <a name="authoring-the-customaction-table"></a><span data-ttu-id="36221-104">Erstellen der Tabelle "CustomAction"</span><span class="sxs-lookup"><span data-stu-id="36221-104">Authoring the CustomAction Table</span></span>

<span data-ttu-id="36221-105">Geben Sie Datensätze für die fünf benutzerdefinierten Beispiel Aktionen ein, die im vorherigen Abschnitt für die [Tabelle CustomAction](customaction-table.md)erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="36221-105">Enter records for the five sample custom actions created in the previous section to the [CustomAction Table](customaction-table.md).</span></span> <span data-ttu-id="36221-106">Weitere Informationen zum Auffüllen der CustomAction-Tabelle für diese Art von benutzerdefinierter Aktion finden Sie unter [benutzerdefinierter Aktionstyp 1](custom-action-type-1.md).</span><span class="sxs-lookup"><span data-stu-id="36221-106">For more information on how to populate the CustomAction table for this type of custom action see [Custom Action Type 1](custom-action-type-1.md).</span></span>

[<span data-ttu-id="36221-107">Tabelle "CustomAction"</span><span class="sxs-lookup"><span data-stu-id="36221-107">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="36221-108">Aktion</span><span class="sxs-lookup"><span data-stu-id="36221-108">Action</span></span>            | <span data-ttu-id="36221-109">type</span><span class="sxs-lookup"><span data-stu-id="36221-109">Type</span></span>  | <span data-ttu-id="36221-110">`Source`</span><span class="sxs-lookup"><span data-stu-id="36221-110">Source</span></span>      | <span data-ttu-id="36221-111">Ziel</span><span class="sxs-lookup"><span data-stu-id="36221-111">Target</span></span>                |
|-------------------|-------|-------------|-----------------------|
| <span data-ttu-id="36221-112">Processaccounts</span><span class="sxs-lookup"><span data-stu-id="36221-112">ProcessAccounts</span></span>   | <span data-ttu-id="36221-113">1</span><span class="sxs-lookup"><span data-stu-id="36221-113">1</span></span>     | <span data-ttu-id="36221-114">Process.dll</span><span class="sxs-lookup"><span data-stu-id="36221-114">Process.dll</span></span> | <span data-ttu-id="36221-115">Processuseraccounts</span><span class="sxs-lookup"><span data-stu-id="36221-115">ProcessUserAccounts</span></span>   |
| <span data-ttu-id="36221-116">Nicht installaccounts</span><span class="sxs-lookup"><span data-stu-id="36221-116">UninstallAccounts</span></span> | <span data-ttu-id="36221-117">1</span><span class="sxs-lookup"><span data-stu-id="36221-117">1</span></span>     | <span data-ttu-id="36221-118">Process.dll</span><span class="sxs-lookup"><span data-stu-id="36221-118">Process.dll</span></span> | <span data-ttu-id="36221-119">Uninstalluseraccounts</span><span class="sxs-lookup"><span data-stu-id="36221-119">UninstallUserAccounts</span></span> |
| <span data-ttu-id="36221-120">CreateAccount</span><span class="sxs-lookup"><span data-stu-id="36221-120">CreateAccount</span></span>     | <span data-ttu-id="36221-121">11265</span><span class="sxs-lookup"><span data-stu-id="36221-121">11265</span></span> | <span data-ttu-id="36221-122">Create.dll</span><span class="sxs-lookup"><span data-stu-id="36221-122">Create.dll</span></span>  | <span data-ttu-id="36221-123">"Kreateuseraccount"</span><span class="sxs-lookup"><span data-stu-id="36221-123">CreateUserAccount</span></span>     |
| <span data-ttu-id="36221-124">RemoveAccount</span><span class="sxs-lookup"><span data-stu-id="36221-124">RemoveAccount</span></span>     | <span data-ttu-id="36221-125">11265</span><span class="sxs-lookup"><span data-stu-id="36221-125">11265</span></span> | <span data-ttu-id="36221-126">Remove.dll</span><span class="sxs-lookup"><span data-stu-id="36221-126">Remove.dll</span></span>  | <span data-ttu-id="36221-127">Removeuseraccount</span><span class="sxs-lookup"><span data-stu-id="36221-127">RemoveUserAccount</span></span>     |
| <span data-ttu-id="36221-128">Rollbackaccount</span><span class="sxs-lookup"><span data-stu-id="36221-128">RollbackAccount</span></span>   | <span data-ttu-id="36221-129">9473</span><span class="sxs-lookup"><span data-stu-id="36221-129">9473</span></span>  | <span data-ttu-id="36221-130">Remove.dll</span><span class="sxs-lookup"><span data-stu-id="36221-130">Remove.dll</span></span>  | <span data-ttu-id="36221-131">Removeuseraccount</span><span class="sxs-lookup"><span data-stu-id="36221-131">RemoveUserAccount</span></span>     |



 

<span data-ttu-id="36221-132">Der C++-Quellcode für die Dynamic-Link-Bibliotheken wird im Windows Installer SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="36221-132">The C++ source code for the dynamic-link libraries are provided in the Windows Installer SDK.</span></span> <span data-ttu-id="36221-133">Verwenden Sie "Process. cpp", um die Datei Process.dll zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="36221-133">Use Process.cpp to create the file Process.dll.</span></span> <span data-ttu-id="36221-134">Erstellen Sie die Datei Create.dll mit CREATE. cpp.</span><span class="sxs-lookup"><span data-stu-id="36221-134">Use Create.cpp to create the file Create.dll.</span></span> <span data-ttu-id="36221-135">Verwenden Sie Remove. cpp, um Remove.dll zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="36221-135">Use Remove.cpp to create Remove.dll.</span></span> <span data-ttu-id="36221-136">Fügen Sie diese Dynamic-Link Library-Dateien der Binär Tabelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="36221-136">Add these dynamic-link library files to the Binary table.</span></span>

[<span data-ttu-id="36221-137">Binäre Tabelle</span><span class="sxs-lookup"><span data-stu-id="36221-137">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="36221-138">Name</span><span class="sxs-lookup"><span data-stu-id="36221-138">Name</span></span>        | <span data-ttu-id="36221-139">Daten</span><span class="sxs-lookup"><span data-stu-id="36221-139">Data</span></span>            |
|-------------|-----------------|
| <span data-ttu-id="36221-140">Process.dll</span><span class="sxs-lookup"><span data-stu-id="36221-140">Process.dll</span></span> | <span data-ttu-id="36221-141">{*binäre Daten*}</span><span class="sxs-lookup"><span data-stu-id="36221-141">{*binary data*}</span></span> |
| <span data-ttu-id="36221-142">Create.dll</span><span class="sxs-lookup"><span data-stu-id="36221-142">Create.dll</span></span>  | <span data-ttu-id="36221-143">{*binäre Daten*}</span><span class="sxs-lookup"><span data-stu-id="36221-143">{*binary data*}</span></span> |
| <span data-ttu-id="36221-144">Remove.dll</span><span class="sxs-lookup"><span data-stu-id="36221-144">Remove.dll</span></span>  | <span data-ttu-id="36221-145">{*binäre Daten*}</span><span class="sxs-lookup"><span data-stu-id="36221-145">{*binary data*}</span></span> |



 

<span data-ttu-id="36221-146">Fügen Sie weiterhin [eine benutzerdefinierte customuseraccounts-Tabelle hinzu](adding-a-custom-customuseraccounts-table.md).</span><span class="sxs-lookup"><span data-stu-id="36221-146">Continue to [Adding a Custom CustomUserAccounts Table](adding-a-custom-customuseraccounts-table.md).</span></span>

 

 



