---
title: RegistrationInfo. Author-Eigenschaft
description: Ruft den Autor der Aufgabe für die Skripterstellung ab oder legt ihn fest.
ms.assetid: ba355a3b-cda3-4d4f-8504-f77f3d9eb21a
keywords:
- Eigenschaften Taskplaner erstellen
- Author-Eigenschaft Taskplaner, RegistrationInfo-Objekt
- RegistrationInfo-Objekt Taskplaner, Author-Eigenschaft
topic_type:
- apiref
api_name:
- RegistrationInfo.Author
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e7e940ff9da2cfccaa306ebf73080da2a28a091
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040058"
---
# <a name="registrationinfoauthor-property"></a><span data-ttu-id="19aad-106">RegistrationInfo. Author-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="19aad-106">RegistrationInfo.Author property</span></span>

<span data-ttu-id="19aad-107">Ruft den Autor der Aufgabe für die Skripterstellung ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="19aad-107">For scripting, gets or sets the author of the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="19aad-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="19aad-108">Syntax</span></span>


```VB
RegistrationInfo.Author As String
```



## <a name="property-value"></a><span data-ttu-id="19aad-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="19aad-109">Property value</span></span>

<span data-ttu-id="19aad-110">Der Autor der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="19aad-110">The author of the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="19aad-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19aad-111">Remarks</span></span>

<span data-ttu-id="19aad-112">Beim Lesen oder Schreiben von XML für eine Aufgabe wird der Aufgaben Autor mithilfe des [**Author**](taskschedulerschema-author-registrationinfotype-element.md) -Elements des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="19aad-112">When reading or writing XML for a task, the task author is specified using the [**Author**](taskschedulerschema-author-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="19aad-113">Beim Festlegen dieses Eigenschafts Werts kann der Wert aus Text bestehen, der aus einer DLL-Datei der Ressource abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="19aad-113">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="19aad-114">Eine spezialisierte Zeichenfolge wird verwendet, um auf den Text aus der Ressourcen Datei zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="19aad-114">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="19aad-115">Das Format der Zeichenfolge ist $ (@ \[ dll \] , \[ ResourceId \] ), wobei \[ dll \] der Pfad zur DLL-Datei, die die Ressource enthält, und \[ ResourceId der \] Bezeichner für den Ressourcen Text ist.</span><span class="sxs-lookup"><span data-stu-id="19aad-115">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="19aad-116">Wenn z. b. der Wert dieser Eigenschaft auf $ (@% systemroot% \\ system32 \\ResourceName.dll,-101) festgelegt wird, wird die-Eigenschaft auf den Wert des Ressourcen Texts mit einem Bezeichner gleich-101 in der Datei% SystemRoot% \\ system32ResourceName.dll festgelegt \\ .</span><span class="sxs-lookup"><span data-stu-id="19aad-116">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="19aad-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19aad-117">Requirements</span></span>



| <span data-ttu-id="19aad-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19aad-118">Requirement</span></span> | <span data-ttu-id="19aad-119">Wert</span><span class="sxs-lookup"><span data-stu-id="19aad-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19aad-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19aad-120">Minimum supported client</span></span><br/> | <span data-ttu-id="19aad-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19aad-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="19aad-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19aad-122">Minimum supported server</span></span><br/> | <span data-ttu-id="19aad-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19aad-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="19aad-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="19aad-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="19aad-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="19aad-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="19aad-126">DLL</span><span class="sxs-lookup"><span data-stu-id="19aad-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19aad-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19aad-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19aad-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19aad-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19aad-129">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="19aad-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





