---
description: Eine Anwendungs definierte Funktion, die eine Liste von Sicherheits-IDs (SIDs) erstellt, die für einen Client gelten. Authzcomputegroupscallback ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.
ms.assetid: c20a02a0-5303-4433-a484-5a89999b32b9
title: Authzcomputegroupscallback-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzComputeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 3728f8114d87d07ddb33dd77a6fda5db30d07cf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760830"
---
# <a name="authzcomputegroupscallback-callback-function"></a><span data-ttu-id="73b6b-104">Authzcomputegroupscallback-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="73b6b-104">AuthzComputeGroupsCallback callback function</span></span>

<span data-ttu-id="73b6b-105">Die **authzcomputegroupscallback** -Funktion ist eine Anwendungs definierte Funktion, die eine Liste von [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -IDs (SIDs) erstellt, die für einen Client gelten.</span><span class="sxs-lookup"><span data-stu-id="73b6b-105">The **AuthzComputeGroupsCallback** function is an application-defined function that creates a list of [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) that apply to a client.</span></span> <span data-ttu-id="73b6b-106">**Authzcomputegroupscallback** ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.</span><span class="sxs-lookup"><span data-stu-id="73b6b-106">**AuthzComputeGroupsCallback** is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="73b6b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="73b6b-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzComputeGroupsCallback(
  _In_  AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_  PVOID                       Args,
  _Out_ PSID_AND_ATTRIBUTES         *pSidAttrArray,
  _Out_ PDWORD                      pSidCount,
  _Out_ PSID_AND_ATTRIBUTES         *pRestrictedSidAttrArray,
  _Out_ PDWORD                      pRestrictedSidCount
);
```



## <a name="parameters"></a><span data-ttu-id="73b6b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="73b6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73b6b-109">" *hauthzclientcontext* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="73b6b-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73b6b-110">Ein Handle für einen Client Kontext.</span><span class="sxs-lookup"><span data-stu-id="73b6b-110">A handle to a client context.</span></span>

</dd> <dt>

<span data-ttu-id="73b6b-111">*Args* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73b6b-111">*Args* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73b6b-112">Daten, die im *dynamicgrouparser* -Parameter eines Aufrufes der [**authzinitializecontextfromauthzcontext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)-, [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)-oder [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) -Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="73b6b-112">Data passed in the *DynamicGroupArgs* parameter of a call to the [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext), [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid), or [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function.</span></span>

</dd> <dt>

<span data-ttu-id="73b6b-113">*psidattrarray* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="73b6b-113">*pSidAttrArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73b6b-114">Ein Zeiger auf eine Zeiger Variable, die die Adresse eines Arrays von [**sid \_ -und \_ Attribute-**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) Strukturen empfängt.</span><span class="sxs-lookup"><span data-stu-id="73b6b-114">A pointer to a pointer variable that receives the address of an array of [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) structures.</span></span> <span data-ttu-id="73b6b-115">Diese Strukturen stellen die Gruppen dar, zu denen der Client gehört.</span><span class="sxs-lookup"><span data-stu-id="73b6b-115">These structures represent the groups to which the client belongs.</span></span>

</dd> <dt>

<span data-ttu-id="73b6b-116">*psidcount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="73b6b-116">*pSidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73b6b-117">Die Anzahl der Strukturen in *psidattrarray*.</span><span class="sxs-lookup"><span data-stu-id="73b6b-117">The number of structures in *pSidAttrArray*.</span></span>

</dd> <dt>

<span data-ttu-id="73b6b-118">*prestrictedsidattrarray* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="73b6b-118">*pRestrictedSidAttrArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73b6b-119">Ein Zeiger auf eine Zeiger Variable, die die Adresse eines Arrays von [**sid \_ -und \_ Attribute-**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) Strukturen empfängt.</span><span class="sxs-lookup"><span data-stu-id="73b6b-119">A pointer to a pointer variable that receives the address of an array of [**SID\_AND\_ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) structures.</span></span> <span data-ttu-id="73b6b-120">Diese Strukturen stellen die Gruppen dar, von denen der Client beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="73b6b-120">These structures represent the groups from which the client is restricted.</span></span>

</dd> <dt>

<span data-ttu-id="73b6b-121">*prestrictedsidcount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="73b6b-121">*pRestrictedSidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73b6b-122">Die Anzahl der Strukturen in *psidrestrictedattrarray*.</span><span class="sxs-lookup"><span data-stu-id="73b6b-122">The number of structures in *pSidRestrictedAttrArray*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73b6b-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73b6b-123">Return value</span></span>

<span data-ttu-id="73b6b-124">Wenn die Funktion erfolgreich eine Liste von SIDs zurückgibt, ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="73b6b-124">If the function successfully returns a list of SIDs, the return value is **TRUE**.</span></span>

<span data-ttu-id="73b6b-125">Wenn die Funktion fehlschlägt, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="73b6b-125">If the function fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="73b6b-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73b6b-126">Remarks</span></span>

<span data-ttu-id="73b6b-127">Anwendungen können dem Client Kontext auch SIDs hinzufügen, indem Sie [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="73b6b-127">Applications can also add SIDs to the client context by calling [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext).</span></span>

<span data-ttu-id="73b6b-128">Attribut Variablen müssen in Form eines Ausdrucks vorliegen, wenn Sie mit logischen Operatoren verwendet werden. Andernfalls werden Sie als UNKNOWN ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="73b6b-128">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="requirements"></a><span data-ttu-id="73b6b-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73b6b-129">Requirements</span></span>



| <span data-ttu-id="73b6b-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73b6b-130">Requirement</span></span> | <span data-ttu-id="73b6b-131">Wert</span><span class="sxs-lookup"><span data-stu-id="73b6b-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="73b6b-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73b6b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="73b6b-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73b6b-133">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="73b6b-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73b6b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="73b6b-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73b6b-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="73b6b-136">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="73b6b-136">Redistributable</span></span><br/>          | <span data-ttu-id="73b6b-137">Windows Server 2003-Verwaltungs Tools Pack unter Windows XP</span><span class="sxs-lookup"><span data-stu-id="73b6b-137">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="73b6b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73b6b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73b6b-139">Grundlegende Access Control Funktionen</span><span class="sxs-lookup"><span data-stu-id="73b6b-139">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="73b6b-140">**AuthzAddSidsToContext**</span><span class="sxs-lookup"><span data-stu-id="73b6b-140">**AuthzAddSidsToContext**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)
</dt> <dt>

[<span data-ttu-id="73b6b-141">**Authzcachedaccesscheck**</span><span class="sxs-lookup"><span data-stu-id="73b6b-141">**AuthzCachedAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[<span data-ttu-id="73b6b-142">**Authzinitializecontextfromauthzcontext**</span><span class="sxs-lookup"><span data-stu-id="73b6b-142">**AuthzInitializeContextFromAuthzContext**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)
</dt> <dt>

[<span data-ttu-id="73b6b-143">**AuthzInitializeContextFromSid**</span><span class="sxs-lookup"><span data-stu-id="73b6b-143">**AuthzInitializeContextFromSid**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)
</dt> <dt>

[<span data-ttu-id="73b6b-144">**AuthzInitializeContextFromToken**</span><span class="sxs-lookup"><span data-stu-id="73b6b-144">**AuthzInitializeContextFromToken**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken)
</dt> <dt>

[<span data-ttu-id="73b6b-145">**Authzinitializeresourcemanager**</span><span class="sxs-lookup"><span data-stu-id="73b6b-145">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> <dt>

[<span data-ttu-id="73b6b-146">**SID \_ und \_ Attribute**</span><span class="sxs-lookup"><span data-stu-id="73b6b-146">**SID\_AND\_ATTRIBUTES**</span></span>](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes)
</dt> </dl>

 

