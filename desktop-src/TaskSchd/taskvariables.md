---
title: TaskVariables-Objekt
description: Skript Objekt, das Task Variablen definiert, die als Parameter an Task Handler und externe ausführbare Dateien, die von Aufgaben gestartet werden, übermittelt werden können.
ms.assetid: 194babe0-16bd-4a78-af45-139c9c7eacbe
keywords:
- TaskVariables-Objekt Taskplaner
- TaskVariables-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- TaskVariables
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00fe20153b0d6d66ca6c7f263a8e76d5a4d480b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478351"
---
# <a name="taskvariables-object"></a><span data-ttu-id="64887-105">TaskVariables-Objekt</span><span class="sxs-lookup"><span data-stu-id="64887-105">TaskVariables object</span></span>

<span data-ttu-id="64887-106">Skript Objekt, das Task Variablen definiert, die als Parameter an Task Handler und externe ausführbare Dateien, die von Aufgaben gestartet werden, übermittelt werden können.</span><span class="sxs-lookup"><span data-stu-id="64887-106">Scripting object that defines task variables that can be passed as parameters to task handlers and external executables that are launched by tasks.</span></span>

## <a name="members"></a><span data-ttu-id="64887-107">Member</span><span class="sxs-lookup"><span data-stu-id="64887-107">Members</span></span>

<span data-ttu-id="64887-108">Das **taskVariables** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="64887-108">The **TaskVariables** object has these types of members:</span></span>

-   [<span data-ttu-id="64887-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="64887-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="64887-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="64887-110">Methods</span></span>

<span data-ttu-id="64887-111">Das **taskVariables** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="64887-111">The **TaskVariables** object has these methods.</span></span>



| <span data-ttu-id="64887-112">Methode</span><span class="sxs-lookup"><span data-stu-id="64887-112">Method</span></span>                                         | <span data-ttu-id="64887-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64887-113">Description</span></span>                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64887-114">**GetContext**</span><span class="sxs-lookup"><span data-stu-id="64887-114">**GetContext**</span></span>](taskvariables-getcontext.md) | <span data-ttu-id="64887-115">Wird verwendet, um den Kontext zwischen verschiedenen Schritten und Aufgaben zu teilen, die sich in derselben Auftrags Instanz befinden.</span><span class="sxs-lookup"><span data-stu-id="64887-115">Used to share the context between different steps and tasks that are in the same job instance.</span></span><br/> |
| [<span data-ttu-id="64887-116">**GetInput**</span><span class="sxs-lookup"><span data-stu-id="64887-116">**GetInput**</span></span>](taskvariables-getinput.md)     | <span data-ttu-id="64887-117">Ruft die Eingabevariablen für eine Aufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="64887-117">Gets the input variables for a task.</span></span><br/>                                                           |
| [<span data-ttu-id="64887-118">**SetOutput**</span><span class="sxs-lookup"><span data-stu-id="64887-118">**SetOutput**</span></span>](taskvariables-setoutput.md)   | <span data-ttu-id="64887-119">Legt die Ausgabevariablen für eine Aufgabe fest.</span><span class="sxs-lookup"><span data-stu-id="64887-119">Sets the output variables for a task.</span></span><br/>                                                          |



 

## <a name="requirements"></a><span data-ttu-id="64887-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64887-120">Requirements</span></span>



| <span data-ttu-id="64887-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64887-121">Requirement</span></span> | <span data-ttu-id="64887-122">Wert</span><span class="sxs-lookup"><span data-stu-id="64887-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64887-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64887-123">Minimum supported client</span></span><br/> | <span data-ttu-id="64887-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64887-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="64887-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64887-125">Minimum supported server</span></span><br/> | <span data-ttu-id="64887-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64887-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="64887-127">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="64887-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="64887-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="64887-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="64887-129">DLL</span><span class="sxs-lookup"><span data-stu-id="64887-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64887-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64887-130"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





