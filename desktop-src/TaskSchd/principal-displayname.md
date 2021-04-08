---
title: Principal. Display Name (Eigenschaft)
description: Ruft bei der Skripterstellung den Namen des Prinzipals ab oder legt ihn fest.
ms.assetid: 73caf263-f597-4bea-ae89-32f9919d7a70
keywords:
- Display Name-Eigenschaft Taskplaner
- Display Name-Eigenschaft Taskplaner, Prinzipal Objekt
- Principal Object Taskplaner, Display Name-Eigenschaft
topic_type:
- apiref
api_name:
- Principal.DisplayName
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31a76ec9473bccb20ec484259ab8adfe26ad6441
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741873"
---
# <a name="principaldisplayname-property"></a><span data-ttu-id="60efd-106">Principal. Display Name (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="60efd-106">Principal.DisplayName property</span></span>

<span data-ttu-id="60efd-107">Ruft bei der Skripterstellung den Namen des Prinzipals ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="60efd-107">For scripting, gets or sets the name of the principal..</span></span>

## <a name="syntax"></a><span data-ttu-id="60efd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="60efd-108">Syntax</span></span>


```VB
Principal.DisplayName As String
```



## <a name="property-value"></a><span data-ttu-id="60efd-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="60efd-109">Property value</span></span>

<span data-ttu-id="60efd-110">Der Name des Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="60efd-110">The name of the principal.</span></span>

## <a name="remarks"></a><span data-ttu-id="60efd-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60efd-111">Remarks</span></span>

<span data-ttu-id="60efd-112">Beim Lesen oder Schreiben von XML für eine Aufgabe wird der Anzeige Name für einen Prinzipal im [**Display Name**](taskschedulerschema-displayname-principaltype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="60efd-112">When reading or writing XML for a task, the display name for a principal is specified in the [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="60efd-113">Beim Festlegen dieses Eigenschafts Werts kann der Wert aus Text bestehen, der aus einer DLL-Datei der Ressource abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="60efd-113">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="60efd-114">Eine spezialisierte Zeichenfolge wird verwendet, um auf den Text aus der Ressourcen Datei zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="60efd-114">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="60efd-115">Das Format der Zeichenfolge ist $ (@ \[ dll \] , \[ ResourceId \] ), wobei \[ dll \] der Pfad zur DLL-Datei, die die Ressource enthält, und \[ ResourceId der \] Bezeichner für den Ressourcen Text ist.</span><span class="sxs-lookup"><span data-stu-id="60efd-115">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="60efd-116">Wenn Sie diesen Eigenschafts Wert z. b. auf $ (@% systemroot% \\ system32 \\ResourceName.dll,-101) festlegen, wird die-Eigenschaft auf den Wert des Ressourcen Texts mit einem Bezeichner festgelegt, der in der Datei "% SystemRoot% System32ResourceName.dll" gleich-101 ist \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="60efd-116">For example, setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="60efd-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60efd-117">Requirements</span></span>



| <span data-ttu-id="60efd-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60efd-118">Requirement</span></span> | <span data-ttu-id="60efd-119">Wert</span><span class="sxs-lookup"><span data-stu-id="60efd-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60efd-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60efd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="60efd-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60efd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="60efd-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60efd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="60efd-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60efd-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="60efd-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="60efd-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="60efd-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="60efd-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="60efd-126">DLL</span><span class="sxs-lookup"><span data-stu-id="60efd-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60efd-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60efd-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60efd-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60efd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60efd-129">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="60efd-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="60efd-130">**Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="60efd-130">**Principal**</span></span>](principal.md)
</dt> </dl>

 

 





