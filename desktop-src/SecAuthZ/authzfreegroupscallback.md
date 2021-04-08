---
description: Eine Anwendungs definierte Funktion, die von der authzcomputegroupscallback-Funktion zugeordnete Arbeitsspeicher freigibt. Authzfregroupscallback ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.
ms.assetid: 5563311c-2bd1-4e96-ba0a-5a4225050f77
title: Authzfregroupscallback-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7d8942acbc67f122ea79f0b9e98793628b5f21f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760825"
---
# <a name="authzfreegroupscallback-callback-function"></a><span data-ttu-id="91955-104">Authzfregroupscallback-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="91955-104">AuthzFreeGroupsCallback callback function</span></span>

<span data-ttu-id="91955-105">Die **authzfregroupscallback** -Funktion ist eine Anwendungs definierte Funktion, die von der [**authzcomputegroupscallback**](authzcomputegroupscallback.md) -Funktion zugeordnete Arbeitsspeicher freigibt.</span><span class="sxs-lookup"><span data-stu-id="91955-105">The **AuthzFreeGroupsCallback** function is an application-defined function that frees memory allocated by the [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md) function.</span></span> <span data-ttu-id="91955-106">**Authzfregroupscallback** ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.</span><span class="sxs-lookup"><span data-stu-id="91955-106">**AuthzFreeGroupsCallback** is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="91955-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="91955-107">Syntax</span></span>


```C++
void CALLBACK AuthzFreeGroupsCallback(
  _In_ PSID_AND_ATTRIBUTES pSidAttrArray
);
```



## <a name="parameters"></a><span data-ttu-id="91955-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="91955-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91955-109">*psidattrarray* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91955-109">*pSidAttrArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91955-110">Ein Zeiger auf den von [**authzcomputegroupscallback**](authzcomputegroupscallback.md)zugeordneten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="91955-110">A pointer to memory allocated by [**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91955-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91955-111">Return value</span></span>

<span data-ttu-id="91955-112">Diese Rückruffunktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="91955-112">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91955-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91955-113">Remarks</span></span>

<span data-ttu-id="91955-114">Attribut Variablen müssen in Form eines Ausdrucks vorliegen, wenn Sie mit logischen Operatoren verwendet werden. Andernfalls werden Sie als UNKNOWN ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="91955-114">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="requirements"></a><span data-ttu-id="91955-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91955-115">Requirements</span></span>



| <span data-ttu-id="91955-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91955-116">Requirement</span></span> | <span data-ttu-id="91955-117">Wert</span><span class="sxs-lookup"><span data-stu-id="91955-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="91955-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91955-118">Minimum supported client</span></span><br/> | <span data-ttu-id="91955-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91955-119">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="91955-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91955-120">Minimum supported server</span></span><br/> | <span data-ttu-id="91955-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91955-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="91955-122">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="91955-122">Redistributable</span></span><br/>          | <span data-ttu-id="91955-123">Windows Server 2003-Verwaltungs Tools Pack unter Windows XP</span><span class="sxs-lookup"><span data-stu-id="91955-123">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="91955-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91955-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91955-125">Grundlegende Access Control Funktionen</span><span class="sxs-lookup"><span data-stu-id="91955-125">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="91955-126">**Authzcomputegroupscallback**</span><span class="sxs-lookup"><span data-stu-id="91955-126">**AuthzComputeGroupsCallback**</span></span>](authzcomputegroupscallback.md)
</dt> </dl>

 

 




