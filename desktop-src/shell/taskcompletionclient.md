---
description: Aktiviert die Aufgaben Vervollständigung.
ms.assetid: 323343D6-FC4A-4A5F-B065-DD72B6077F99
title: Taskcompletionclient-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: a823dc528ea189c70f44689ab69795eb3a430e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217684"
---
# <a name="taskcompletionclient-interface"></a><span data-ttu-id="928c7-103">Taskcompletionclient-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="928c7-103">TaskCompletionClient interface</span></span>

<span data-ttu-id="928c7-104">Aktiviert die Aufgaben Vervollständigung.</span><span class="sxs-lookup"><span data-stu-id="928c7-104">Enables task completion.</span></span>

## <a name="members"></a><span data-ttu-id="928c7-105">Member</span><span class="sxs-lookup"><span data-stu-id="928c7-105">Members</span></span>

<span data-ttu-id="928c7-106">Die **taskcompletionclient** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="928c7-106">The **TaskCompletionClient** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="928c7-107">**Taskcompletionclient** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="928c7-107">**TaskCompletionClient** also has these types of members:</span></span>

-   [<span data-ttu-id="928c7-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="928c7-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="928c7-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="928c7-109">Methods</span></span>

<span data-ttu-id="928c7-110">Die **taskcompletionclient** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="928c7-110">The **TaskCompletionClient** interface has these methods.</span></span>



| <span data-ttu-id="928c7-111">Methode</span><span class="sxs-lookup"><span data-stu-id="928c7-111">Method</span></span>                                                                    | <span data-ttu-id="928c7-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="928c7-112">Description</span></span>                            |
|:--------------------------------------------------------------------------|:---------------------------------------|
| [<span data-ttu-id="928c7-113">**Applytaskcompletion**</span><span class="sxs-lookup"><span data-stu-id="928c7-113">**ApplyTaskCompletion**</span></span>](taskcompletionclient-applytaskcompletion.md)   | <span data-ttu-id="928c7-114">Startet den Abschluss der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="928c7-114">Begins the task completion.</span></span><br/> |
| [<span data-ttu-id="928c7-115">**Revoketaskcompletion**</span><span class="sxs-lookup"><span data-stu-id="928c7-115">**RevokeTaskCompletion**</span></span>](taskcompletionclient-revoketaskcompletion.md) | <span data-ttu-id="928c7-116">Beendet den Abschluss der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="928c7-116">Ends the task completion.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="928c7-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="928c7-117">Remarks</span></span>

<span data-ttu-id="928c7-118">Die GUID für diese Schnittstelle lautet "E97D552D-9ae9-46aa-9151-D2DA4BBB5E96".</span><span class="sxs-lookup"><span data-stu-id="928c7-118">The GUID for this interface is "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96".</span></span>

<span data-ttu-id="928c7-119">Diese API ist veraltet und wird in zukünftigen Versionen von Windows möglicherweise nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="928c7-119">This API is deprecated and may not be available in future versions of Windows.</span></span> <span data-ttu-id="928c7-120">Apps sollten stattdessen die APIs im [**Windows. applicationmodel. extendedexecution**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) -Namespace verwenden.</span><span class="sxs-lookup"><span data-stu-id="928c7-120">Apps should use the APIs in the [**Windows.ApplicationModel.ExtendedExecution**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) namespace instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="928c7-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="928c7-121">Requirements</span></span>



| <span data-ttu-id="928c7-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="928c7-122">Requirement</span></span> | <span data-ttu-id="928c7-123">Wert</span><span class="sxs-lookup"><span data-stu-id="928c7-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="928c7-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="928c7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="928c7-125">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="928c7-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="928c7-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="928c7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="928c7-127">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="928c7-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="928c7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="928c7-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="928c7-129"><dt>ExecModelClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="928c7-129"><dt>ExecModelClient.dll</dt></span></span> </dl> |



 

 
