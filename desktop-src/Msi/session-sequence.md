---
description: Die Sequence-Methode des Session-Objekts öffnet eine Abfrage für die angegebene Tabelle und ordnet die Aktionen nach den Zahlen in der Sequenz Spalte an.
ms.assetid: cde735b0-0b97-4c4f-adfc-f0321aafb012
title: Session. Sequence-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Sequence
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 18708b79bdce73b29f46b4d62a15ceb8003d9c9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362135"
---
# <a name="sessionsequence-method"></a><span data-ttu-id="d109e-103">Session. Sequence-Methode</span><span class="sxs-lookup"><span data-stu-id="d109e-103">Session.Sequence method</span></span>

<span data-ttu-id="d109e-104">Die **Sequence** -Methode des [**Session**](session-object.md) -Objekts öffnet eine Abfrage für die angegebene Tabelle und ordnet die Aktionen nach den Zahlen in der Sequenz Spalte an.</span><span class="sxs-lookup"><span data-stu-id="d109e-104">The **Sequence** method of the [**Session**](session-object.md) object opens a query on the specified table, ordering the actions by the numbers in the Sequence column.</span></span> <span data-ttu-id="d109e-105">Für jede abgerufene Zeile wird die [**doaction**](session-doaction.md) -Methode aufgerufen, vorausgesetzt, dass ein beliebiger angegebener Bedingungs Ausdruck nicht als false ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="d109e-105">For each row fetched, the [**DoAction**](session-doaction.md) method is called, provided that any supplied condition expression does not evaluate to False.</span></span> <span data-ttu-id="d109e-106">Gibt eine Enumeration msidoaction Status usenum zurück, wie in der [**doaction**](session-doaction.md) -Methode beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d109e-106">Returns an enumeration msiDoActionStatusEnum, as described in the [**DoAction**](session-doaction.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d109e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d109e-107">Syntax</span></span>


```JScript
Session.Sequence(
  table
)
```



## <a name="parameters"></a><span data-ttu-id="d109e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d109e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d109e-109">*Tabelle*</span><span class="sxs-lookup"><span data-stu-id="d109e-109">*table*</span></span> 
</dt> <dd>

<span data-ttu-id="d109e-110">Erforderlicher Zeichen folgen Name der Tabelle, die für die Sequenzierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d109e-110">Required string name of the table to use for sequencing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d109e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d109e-111">Return value</span></span>

<span data-ttu-id="d109e-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d109e-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d109e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d109e-113">Remarks</span></span>

<span data-ttu-id="d109e-114">Diese Methode wird normalerweise intern von Aktionen der obersten Ebene aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d109e-114">This method is normally called internally by top-level actions.</span></span>

<span data-ttu-id="d109e-115">Eine Aktions Sequenz mit Aktionen, die das System aktualisieren, z. b. die Aktionen " [InstallFiles](installfiles-action.md) " und " [schreiteregistryvalues](writeregistryvalues-action.md) ", kann nicht ausgeführt werden, indem die **Sequence** -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d109e-115">An action sequence containing actions that update the system, such as the [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions, cannot be run by calling the **Sequence** method.</span></span> <span data-ttu-id="d109e-116">Eine Ausnahme von dieser Regel ist, wenn die **Sequence** -Methode von einer benutzerdefinierten Aktion aufgerufen wird, die in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) zwischen den [InstallInitialize](installinitialize-action.md) -und [InstallFinalize-Aktionen](installfinalize-action.md)geplant ist.</span><span class="sxs-lookup"><span data-stu-id="d109e-116">The exception to this rule is if the **Sequence** method is called from a custom action that is scheduled in the [InstallExecuteSequence table](installexecutesequence-table.md) between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize actions](installfinalize-action.md).</span></span> <span data-ttu-id="d109e-117">Aktionen, die das System nicht aktualisieren, z. b. [AppSearch](appsearch-action.md) oder [costinitialize](costinitialize-action.md), können aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d109e-117">Actions that do not update the system, such as [AppSearch](appsearch-action.md) or [CostInitialize](costinitialize-action.md), can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="d109e-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d109e-118">Requirements</span></span>



| <span data-ttu-id="d109e-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d109e-119">Requirement</span></span> | <span data-ttu-id="d109e-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d109e-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d109e-121">Version</span><span class="sxs-lookup"><span data-stu-id="d109e-121">Version</span></span><br/> | <span data-ttu-id="d109e-122">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d109e-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d109e-123">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d109e-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d109e-124">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="d109e-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d109e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d109e-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="d109e-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d109e-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d109e-127">IID</span><span class="sxs-lookup"><span data-stu-id="d109e-127">IID</span></span><br/>     | <span data-ttu-id="d109e-128">IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d109e-128">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




