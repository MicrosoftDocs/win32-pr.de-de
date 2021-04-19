---
description: Konfiguriert die Voreinstellung der Standardfunktionen.
ms.assetid: 0afcb25a-2499-4baa-82ad-0706164e2e72
title: 'IH323LineEx:: setdefaultcapabilitypreferrenz-Methode (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5604348eb80a3f423f6902f0a9a6e57204280c83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356383"
---
# <a name="ih323lineexsetdefaultcapabilitypreferrence-method"></a><span data-ttu-id="db050-103">IH323LineEx:: setdefaultcapabilitypreferrenz-Methode</span><span class="sxs-lookup"><span data-stu-id="db050-103">IH323LineEx::SetDefaultCapabilityPreferrence method</span></span>

<span data-ttu-id="db050-104">\[**Setdefaultcapabilityprefergenz** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="db050-104">\[**SetDefaultCapabilityPreferrence** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="db050-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="db050-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="db050-106">Die **setdefaultcapabilitypreferrenz** -Methode konfiguriert die Voreinstellung der Standardfunktionen.</span><span class="sxs-lookup"><span data-stu-id="db050-106">The **SetDefaultCapabilityPreferrence** method configures the preference of the default capabilities.</span></span> <span data-ttu-id="db050-107">Funktionen haben eine Standard Gewichtung von 100.</span><span class="sxs-lookup"><span data-stu-id="db050-107">Capabilities have a default weight of 100.</span></span> <span data-ttu-id="db050-108">Wenn die Anwendung eine höhere Gewichtung für eine Funktion angibt, erhält Sie während der H. 245-Aushandlung eine höhere Priorität.</span><span class="sxs-lookup"><span data-stu-id="db050-108">If the application specifies a higher weight for a capability, it will have a higher priority during the H.245 negotiation.</span></span> <span data-ttu-id="db050-109">Wenn die Anwendung die Gewichtung einer Funktion auf 0 festlegt, wird Sie in der H. 245-Aushandlung nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="db050-109">If the application sets the weight of a capability to 0, it will not be used in the H.245 negotiation.</span></span>

<span data-ttu-id="db050-110">Diese Methode ist kumulativ.</span><span class="sxs-lookup"><span data-stu-id="db050-110">This method is cumulative.</span></span> <span data-ttu-id="db050-111">Wenn diese Methode z. b. zuerst aufgerufen wird, um eine Funktion zu deaktivieren und erneut aufgerufen wird, um eine andere zu deaktivieren, werden beide Funktionen als Ergebnis dieser beiden Aufrufe deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="db050-111">For example, if this method is called first to disable a capability and is called again to disable another, both capabilities will be disabled as the result of these two calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="db050-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="db050-112">Syntax</span></span>


```C++
HRESULT SetDefaultCapabilityPreferrence(
  [in] DWORD           dwNumCaps,
  [in] H245_CAPABILITY *pCapabilities,
  [in] DWORD           *pWeights
);
```



## <a name="parameters"></a><span data-ttu-id="db050-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="db050-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db050-114">*dwnumcaps* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db050-114">*dwNumCaps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db050-115">Ein **DWORD** -Wert, der die Anzahl von Funktionen enthält, die mit dieser Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="db050-115">A **DWORD** value that contains the number of capabilities set with this method.</span></span>

</dd> <dt>

<span data-ttu-id="db050-116">*pfunktionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db050-116">*pCapabilities* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db050-117">Ein Array von Funktionen.</span><span class="sxs-lookup"><span data-stu-id="db050-117">An array of capabilities.</span></span> <span data-ttu-id="db050-118">Jedes Element des Arrays ist ein [**H245- \_**](h245-capability.md) Funktionswert.</span><span class="sxs-lookup"><span data-stu-id="db050-118">Each element of the array is an [**H245\_CAPABILITY**](h245-capability.md) value.</span></span>

</dd> <dt>

<span data-ttu-id="db050-119">*pgewichtungen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db050-119">*pWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db050-120">Ein Array von Gewichtungen, die den Funktionen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="db050-120">An array of weights associated with the capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db050-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db050-121">Return value</span></span>

<span data-ttu-id="db050-122">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="db050-122">This method can return one of these values.</span></span>



| <span data-ttu-id="db050-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="db050-123">Return code</span></span>                                                                                   | <span data-ttu-id="db050-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db050-124">Description</span></span>                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="db050-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="db050-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="db050-126">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="db050-126">Method succeeded.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="db050-127"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="db050-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="db050-128">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="db050-128">Insufficient memory exists to perform the operation.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="db050-129"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="db050-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="db050-130">Der *pcapability* -Parameter ist **null**, oder der *pgewichtungs* - **Parameter ist NULL**, oder sowohl *pcapability* als auch *pgewichtungen* sind **null**, oder das pcapability-Array enthält ein ungültiges H. 245-Funktions Objekt.</span><span class="sxs-lookup"><span data-stu-id="db050-130">The *pCapabilities* parameter is **NULL**, or the *pWeights* parameter is **NULL**, or both *pCapabilities* and *pWeights* are **NULL**, or the pCapabilities array contains an invalid H.245 capability object.</span></span><br/> |
| <dl> <span data-ttu-id="db050-131"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="db050-131"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="db050-132">Ein Element des *pgewichtungs* Arrays oder ein Element des *parrays* -Arrays konnte nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="db050-132">Unable to read an element of the *pWeights* array or an element of the *pCapabilities* array.</span></span><br/>                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="db050-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db050-133">Requirements</span></span>



| <span data-ttu-id="db050-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db050-134">Requirement</span></span> | <span data-ttu-id="db050-135">Wert</span><span class="sxs-lookup"><span data-stu-id="db050-135">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db050-136">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="db050-136">TAPI version</span></span><br/> | <span data-ttu-id="db050-137">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="db050-137">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="db050-138">Header</span><span class="sxs-lookup"><span data-stu-id="db050-138">Header</span></span><br/>       | <dl> <span data-ttu-id="db050-139"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="db050-139"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="db050-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="db050-140">Library</span></span><br/>      | <dl> <span data-ttu-id="db050-141"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db050-141"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="db050-142">DLL</span><span class="sxs-lookup"><span data-stu-id="db050-142">DLL</span></span><br/>          | <dl> <span data-ttu-id="db050-143"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db050-143"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




