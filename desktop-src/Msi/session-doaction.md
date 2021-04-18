---
description: Die doaction-Methode des Session-Objekts führt die Aktions Funktion aus, die dem angegebenen Namen entspricht.
ms.assetid: 6cff1cf1-1c8f-4c43-a687-e927e8573e55
title: Session. doaction-Methode (photobeschaffung. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.DoAction
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3084cfd51e7efbcfbfbc3cbcf2c9be21d8373d21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365482"
---
# <a name="sessiondoaction-method"></a><span data-ttu-id="7393f-103">Session. doaction-Methode</span><span class="sxs-lookup"><span data-stu-id="7393f-103">Session.DoAction method</span></span>

<span data-ttu-id="7393f-104">Die **doaction** -Methode des [**Session**](session-object.md) -Objekts führt die Aktions Funktion aus, die dem angegebenen Namen entspricht.</span><span class="sxs-lookup"><span data-stu-id="7393f-104">The **DoAction** method of the [**Session**](session-object.md) object executes the action function corresponding to the name supplied.</span></span> <span data-ttu-id="7393f-105">Wenn ein NULL-Aktionsname angegeben wird, verwendet die Engine den Großbuchstaben der [Action-Eigenschaft](action.md) als Aktion, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7393f-105">If a Null action name is supplied, the engine uses the uppercase value of the [ACTION property](action.md) as the action to perform.</span></span> <span data-ttu-id="7393f-106">Wenn kein Eigenschafts Wert definiert ist, wird die Standardaktion ausgeführt, die derzeit als install definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7393f-106">If no property value is defined, the default action is performed, currently defined as INSTALL.</span></span> <span data-ttu-id="7393f-107">Diese Methode gibt eine ganzzahlige Enumeration zurück.</span><span class="sxs-lookup"><span data-stu-id="7393f-107">This method returns an integer enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="7393f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7393f-108">Syntax</span></span>


```JScript
Session.DoAction(
  action
)
```



## <a name="parameters"></a><span data-ttu-id="7393f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7393f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7393f-110">*action*</span><span class="sxs-lookup"><span data-stu-id="7393f-110">*action*</span></span> 
</dt> <dd>

<span data-ttu-id="7393f-111">Erforderlicher Zeichen folgen Name der auszuführenden Aktion.</span><span class="sxs-lookup"><span data-stu-id="7393f-111">Required string name of the action to execute.</span></span> <span data-ttu-id="7393f-112">Groß-/Kleinschreibung wird beachtet,</span><span class="sxs-lookup"><span data-stu-id="7393f-112">Case-sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7393f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7393f-113">Return value</span></span>

<span data-ttu-id="7393f-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7393f-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7393f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7393f-115">Remarks</span></span>

<span data-ttu-id="7393f-116">Aktionen, die das System aktualisieren, z. b. die Aktionen " [InstallFiles](installfiles-action.md) " und " [schreiteregistryvalues](writeregistryvalues-action.md) ", können durch Aufrufen der **doaction** -Methode nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7393f-116">Actions that update the system, such as the [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions, cannot be run by calling the **DoAction** method.</span></span> <span data-ttu-id="7393f-117">Eine Ausnahme von dieser Regel ist, wenn die **doaction** -Methode von einer benutzerdefinierten Aktion aufgerufen wird, die in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) zwischen den [InstallInitialize](installinitialize-action.md) -und [InstallFinalize-Aktionen](installfinalize-action.md)geplant ist.</span><span class="sxs-lookup"><span data-stu-id="7393f-117">The exception to this rule is if the **DoAction** method is called from a custom action that is scheduled in the [InstallExecuteSequence table](installexecutesequence-table.md) between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize actions](installfinalize-action.md).</span></span> <span data-ttu-id="7393f-118">Aktionen, die das System nicht aktualisieren, z. b. [AppSearch](appsearch-action.md) oder [costinitialize](costinitialize-action.md), können aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7393f-118">Actions that do not update the system, such as [AppSearch](appsearch-action.md) or [CostInitialize](costinitialize-action.md), can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="7393f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7393f-119">Requirements</span></span>



| <span data-ttu-id="7393f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7393f-120">Requirement</span></span> | <span data-ttu-id="7393f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="7393f-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7393f-122">Version</span><span class="sxs-lookup"><span data-stu-id="7393f-122">Version</span></span><br/> | <span data-ttu-id="7393f-123">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7393f-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7393f-124">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7393f-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7393f-125">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="7393f-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7393f-126">Header</span><span class="sxs-lookup"><span data-stu-id="7393f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="7393f-127"><dt>Photoabruf. h</dt></span><span class="sxs-lookup"><span data-stu-id="7393f-127"><dt>Photoacquire.h</dt></span></span> </dl>                                                                                                                                                               |
| <span data-ttu-id="7393f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7393f-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="7393f-129"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7393f-129"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7393f-130">IID</span><span class="sxs-lookup"><span data-stu-id="7393f-130">IID</span></span><br/>     | <span data-ttu-id="7393f-131">IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7393f-131">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




