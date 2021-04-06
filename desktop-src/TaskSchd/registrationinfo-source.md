---
title: RegistrationInfo. Source (Eigenschaft)
description: Ruft bei der Skripterstellung ab oder legt fest, wo die Aufgabe aus stammt. Beispielsweise kann eine Aufgabe aus einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer stammen.
ms.assetid: b5bd987f-5c9f-4af0-99e2-aec92951f2be
keywords:
- Quell Eigenschaft Taskplaner
- Quell Eigenschaft Taskplaner, RegistrationInfo-Objekt
- RegistrationInfo-Objekt Taskplaner, Quell Eigenschaft
topic_type:
- apiref
api_name:
- RegistrationInfo.Source
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d360a20d1f0f4736db4dd6f136a579178a65ca70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742441"
---
# <a name="registrationinfosource-property"></a><span data-ttu-id="35b38-107">RegistrationInfo. Source (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="35b38-107">RegistrationInfo.Source property</span></span>

<span data-ttu-id="35b38-108">Ruft bei der Skripterstellung ab oder legt fest, wo die Aufgabe aus stammt.</span><span class="sxs-lookup"><span data-stu-id="35b38-108">For scripting, gets or sets where the task originated from.</span></span> <span data-ttu-id="35b38-109">Beispielsweise kann eine Aufgabe aus einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer stammen.</span><span class="sxs-lookup"><span data-stu-id="35b38-109">For example, a task may originate from a component, service, application, or user.</span></span>

## <a name="syntax"></a><span data-ttu-id="35b38-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="35b38-110">Syntax</span></span>


```VB
RegistrationInfo.Source As String
```



## <a name="property-value"></a><span data-ttu-id="35b38-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="35b38-111">Property value</span></span>

<span data-ttu-id="35b38-112">Der Ursprung der Aufgabe aus.</span><span class="sxs-lookup"><span data-stu-id="35b38-112">Where the task originated from.</span></span> <span data-ttu-id="35b38-113">Beispielsweise aus einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer.</span><span class="sxs-lookup"><span data-stu-id="35b38-113">For example, from a component, service, application, or user.</span></span>

## <a name="remarks"></a><span data-ttu-id="35b38-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35b38-114">Remarks</span></span>

<span data-ttu-id="35b38-115">Beim Lesen oder Schreiben von XML für eine Aufgabe werden die Informationen zur Task Quelle mithilfe des [**Quell**](taskschedulerschema-source-registrationinfotype-element.md) Elements des Taskplaner Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="35b38-115">When reading or writing XML for a task, the task source information is specified using the [**Source**](taskschedulerschema-source-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="35b38-116">Beim Festlegen dieses Eigenschafts Werts kann der Wert aus Text bestehen, der aus einer DLL-Datei der Ressource abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="35b38-116">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="35b38-117">Eine spezialisierte Zeichenfolge wird verwendet, um auf den Text aus der Ressourcen Datei zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="35b38-117">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="35b38-118">Das Format der Zeichenfolge ist $ (@ \[ dll \] , \[ ResourceId \] ), wobei \[ dll \] der Pfad zur DLL-Datei, die die Ressource enthält, und \[ ResourceId der \] Bezeichner für den Ressourcen Text ist.</span><span class="sxs-lookup"><span data-stu-id="35b38-118">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="35b38-119">Wenn z. b. der Wert dieser Eigenschaft auf $ (@% systemroot% \\ system32 \\ResourceName.dll,-101) festgelegt wird, wird die-Eigenschaft auf den Wert des Ressourcen Texts mit einem Bezeichner gleich-101 in der Datei% SystemRoot% \\ system32ResourceName.dll festgelegt \\ .</span><span class="sxs-lookup"><span data-stu-id="35b38-119">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="35b38-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35b38-120">Requirements</span></span>



| <span data-ttu-id="35b38-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35b38-121">Requirement</span></span> | <span data-ttu-id="35b38-122">Wert</span><span class="sxs-lookup"><span data-stu-id="35b38-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35b38-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35b38-123">Minimum supported client</span></span><br/> | <span data-ttu-id="35b38-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35b38-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="35b38-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35b38-125">Minimum supported server</span></span><br/> | <span data-ttu-id="35b38-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35b38-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="35b38-127">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="35b38-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="35b38-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="35b38-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="35b38-129">DLL</span><span class="sxs-lookup"><span data-stu-id="35b38-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35b38-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35b38-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35b38-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35b38-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35b38-132">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="35b38-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





