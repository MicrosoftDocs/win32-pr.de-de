---
description: Benachrichtigt das System über die gewünschten Erzwingungsmodi für eine Reihe von DLP-Vorgängen (Endpoint Data Loss Prevention).
title: DlpInitializeEnforcementMode-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpInitializeEnforcementMode
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: cff3e1609f15f2cbbe6f6d9f76c6433ba3f4e5d7
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495730"
---
# <a name="dlpinitializeenforcementmode-function"></a><span data-ttu-id="22510-103">DlpInitializeEnforcementMode-Funktion</span><span class="sxs-lookup"><span data-stu-id="22510-103">DlpInitializeEnforcementMode function</span></span>

<span data-ttu-id="22510-104">Benachrichtigt das System über die gewünschten Erzwingungsmodi für eine Reihe von Endpunktvorgängen zur Verhinderung von Datenverlust (Data Loss Prevention, DLP).</span><span class="sxs-lookup"><span data-stu-id="22510-104">Notifies the system of the desired enforcement modes for a set of endpoint Data Loss Prevention (DLP) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="22510-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22510-105">Syntax</span></span>


```C++
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);
```



## <a name="parameters"></a><span data-ttu-id="22510-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22510-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22510-107">*Anzahl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="22510-107">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22510-108">Ein **DWORD,** das die Anzahl von Vorgängen angibt, die im *OperationEnforcement-Array* enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="22510-108">A **DWORD** specifying the number of operations included in the *OperationEnforcement* array.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="22510-109">*OperationEnforcement* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="22510-109">*OperationEnforcement* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22510-110">Ein Array von [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) Strukturen, die die Erzwingungsebene für einen Endpunkt-DLP-Vorgang angeben.</span><span class="sxs-lookup"><span data-stu-id="22510-110">An array of [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structures that specify the enforcement level for an endpoint DLP operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="22510-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22510-111">Return value</span></span>

<span data-ttu-id="22510-112">Gibt ein HRESULT zurück, einschließlich, aber nicht beschränkt auf die folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="22510-112">Returns an HRESULT including, but not limited to, the following values.</span></span>

| <span data-ttu-id="22510-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="22510-113">HRESULT</span></span> | <span data-ttu-id="22510-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22510-114">Description</span></span> |
|---------|-------------|
| <span data-ttu-id="22510-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="22510-115">S_OK</span></span> | <span data-ttu-id="22510-116">Die Funktion wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="22510-116">The function completed successfully</span></span> |
| <span data-ttu-id="22510-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="22510-117">E_INVALIDARG</span></span> | <span data-ttu-id="22510-118">Mindestens einer der Funktionsparameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="22510-118">One or more of the function parameters are invalid.</span></span> |
| <span data-ttu-id="22510-119">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="22510-119">E_OUTOFMEMORY</span></span> | <span data-ttu-id="22510-120">Fehler bei der Speicherbelegung für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="22510-120">Memory allocation for the operation failed.</span></span> |



## <a name="remarks"></a><span data-ttu-id="22510-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22510-121">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="22510-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="22510-122">Requirements</span></span>



| <span data-ttu-id="22510-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22510-123">Requirement</span></span>          |    <span data-ttu-id="22510-124">Wert</span><span class="sxs-lookup"><span data-stu-id="22510-124">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22510-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22510-125">Minimum supported client</span></span><br/> | <span data-ttu-id="22510-126">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="22510-126">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="22510-127">DLL</span><span class="sxs-lookup"><span data-stu-id="22510-127">DLL</span></span><br/>                      | <span data-ttu-id="22510-128">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="22510-128">EndpointDlp.dll</span></span> |