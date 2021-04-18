---
title: TaskService. newtask-Methode
description: Gibt für die Skripterstellung ein leeres Aufgaben Definitions Objekt zurück, das mit Einstellungen und Eigenschaften ausgefüllt und dann mithilfe der Task Folder. RegisterTaskDefinition-Methode registriert werden soll.
ms.assetid: 696d57fc-100a-43e6-a8d9-9ec89be40367
keywords:
- Newtask-Methode Taskplaner
- Newtask-Methode Taskplaner, Task Service-Objekt
- Task Service-Objekt Taskplaner, newtask-Methode
topic_type:
- apiref
api_name:
- TaskService.NewTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f5f10ce90861c76d0a751c54e8282269b7a8986
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345523"
---
# <a name="taskservicenewtask-method"></a><span data-ttu-id="cfdf2-106">TaskService. newtask-Methode</span><span class="sxs-lookup"><span data-stu-id="cfdf2-106">TaskService.NewTask method</span></span>

<span data-ttu-id="cfdf2-107">Gibt für die Skripterstellung ein leeres Aufgaben Definitions Objekt zurück, das mit Einstellungen und Eigenschaften ausgefüllt und dann mithilfe der [**Task Folder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) -Methode registriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cfdf2-107">For scripting, returns an empty task definition object to be filled in with settings and properties and then registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfdf2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfdf2-108">Syntax</span></span>


```VB
TaskService.NewTask( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="cfdf2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfdf2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfdf2-110">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfdf2-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfdf2-111">Dieser Parameter ist für die zukünftige Verwendung reserviert und muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cfdf2-111">This parameter is reserved for future use and must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfdf2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cfdf2-112">Return value</span></span>

<span data-ttu-id="cfdf2-113">Die Aufgabendefinition, die alle zum Erstellen einer neuen Aufgabe erforderlichen Informationen angibt.</span><span class="sxs-lookup"><span data-stu-id="cfdf2-113">The task definition that specifies all the information required to create a new task.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfdf2-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfdf2-114">Requirements</span></span>



| <span data-ttu-id="cfdf2-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfdf2-115">Requirement</span></span> | <span data-ttu-id="cfdf2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cfdf2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfdf2-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cfdf2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cfdf2-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfdf2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cfdf2-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cfdf2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cfdf2-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cfdf2-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cfdf2-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="cfdf2-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="cfdf2-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cfdf2-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cfdf2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="cfdf2-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfdf2-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfdf2-124"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





