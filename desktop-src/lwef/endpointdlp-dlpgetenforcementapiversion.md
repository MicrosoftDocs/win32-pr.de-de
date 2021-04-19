---
description: Ruft die Version der Endpunkt-DLP-API (Data Loss Prevention) auf dem aktuellen Gerät ab.
title: DlpGetEnforcementApiVersion-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpGetEnforcementApiVersion
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d2b38b6bdcfd761b8ae3c90ee5d3b430767ad29c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495766"
---
# <a name="dlpgetenforcementapiversion-function"></a><span data-ttu-id="35cb2-103">DlpGetEnforcementApiVersion-Funktion</span><span class="sxs-lookup"><span data-stu-id="35cb2-103">DlpGetEnforcementApiVersion function</span></span>

<span data-ttu-id="35cb2-104">Ruft die Version der DLP-API (Data Loss Prevention) des Endpunkts auf dem aktuellen Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="35cb2-104">Retrieves the version of the endpoint Data Loss Prevention (DLP) API on the current device.</span></span>

## <a name="syntax"></a><span data-ttu-id="35cb2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="35cb2-105">Syntax</span></span>


```C++
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);
```



## <a name="parameters"></a><span data-ttu-id="35cb2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="35cb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35cb2-107">*MajorVersion* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="35cb2-107">*MajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35cb2-108">Ein **DWORD,** das die Hauptversionsnummer angibt.</span><span class="sxs-lookup"><span data-stu-id="35cb2-108">A **DWORD** specifying the major version number.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="35cb2-109">*MajorVersion* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="35cb2-109">*MajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35cb2-110">Ein **DWORD,** das die Nebenversionsnummer angibt.</span><span class="sxs-lookup"><span data-stu-id="35cb2-110">A **DWORD** specifying the minor version number.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="35cb2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35cb2-111">Return value</span></span>

<span data-ttu-id="35cb2-112">Gibt ein HRESULT zurück, einschließlich, aber nicht beschränkt auf die folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="35cb2-112">Returns an HRESULT including, but not limited to, the following values.</span></span>

| <span data-ttu-id="35cb2-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="35cb2-113">HRESULT</span></span> | <span data-ttu-id="35cb2-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="35cb2-114">Description</span></span> |
|---------|-------------|
| <span data-ttu-id="35cb2-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="35cb2-115">S_OK</span></span> | <span data-ttu-id="35cb2-116">Die Funktion wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="35cb2-116">The function completed successfully</span></span> |




## <a name="remarks"></a><span data-ttu-id="35cb2-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35cb2-117">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="35cb2-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="35cb2-118">Requirements</span></span>



| <span data-ttu-id="35cb2-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35cb2-119">Requirement</span></span>          |    <span data-ttu-id="35cb2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="35cb2-120">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35cb2-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35cb2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="35cb2-122">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="35cb2-122">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="35cb2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="35cb2-123">DLL</span></span><br/>                      | <span data-ttu-id="35cb2-124">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="35cb2-124">EndpointDlp.dll</span></span> |