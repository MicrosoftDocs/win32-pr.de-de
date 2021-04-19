---
title: Pxeproviderinitialize-Rückruffunktion
description: Ein Export aus einer Anbieter-DLL (Dynamic Link Library), mit der der Anbieter initialisiert und für den Empfang von Client Anforderungen vorbereitet wird.
ms.assetid: 433b051c-9fde-4589-92e2-58d3774826ac
keywords:
- Pxeproviderinitialize-Rückruffunktion Windows-Bereitstellungs Dienste
topic_type:
- apiref
api_name:
- PxeProviderInitialize
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b8d8fed4c1cc91c2090b957894b4f6641adad32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342655"
---
# <a name="pxeproviderinitialize-callback-function"></a><span data-ttu-id="ff794-104">Pxeproviderinitialize-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="ff794-104">PxeProviderInitialize callback function</span></span>

<span data-ttu-id="ff794-105">Ein Export aus einer Anbieter-DLL (Dynamic Link Library), mit der der Anbieter initialisiert und für den Empfang von Client Anforderungen vorbereitet wird.</span><span class="sxs-lookup"><span data-stu-id="ff794-105">An export from a provider dynamic-link library (DLL) that initializes the provider and prepares it to receive client requests.</span></span> <span data-ttu-id="ff794-106">Anbieter müssen die *pxeproviderinitialize* -Funktion exportieren.</span><span class="sxs-lookup"><span data-stu-id="ff794-106">Providers are required to export the *PxeProviderInitialize* function.</span></span> <span data-ttu-id="ff794-107">Alle Rückrufe für den Anbieter müssen bei der Verarbeitung von *pxeproviderinitialize* mit einem Aufruf der [**pxeregistercallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) -Funktion registriert werden.</span><span class="sxs-lookup"><span data-stu-id="ff794-107">Any callbacks to the provider must be registered with a call to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function during the processing of *PxeProviderInitialize*.</span></span> <span data-ttu-id="ff794-108">Bei der Rückgabe dieser Funktion muss der Anbieter vollständig initialisiert und bereit sein, Client Anforderungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="ff794-108">On the return of this function, the provider must be fully initialized and ready to process client requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff794-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff794-109">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderInitialize(
  _In_ HANDLE hProvider,
  _In_ HKEY   hProviderKey
);
```



## <a name="parameters"></a><span data-ttu-id="ff794-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff794-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff794-111">*hprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff794-111">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff794-112">Handle für die Anbieter Instanz.</span><span class="sxs-lookup"><span data-stu-id="ff794-112">Handle to the provider instance.</span></span> <span data-ttu-id="ff794-113">Dieses Handle muss vom Anbieter gespeichert und bei nachfolgenden Aufrufen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ff794-113">This handle must be stored by the provider and used in any subsequent calls.</span></span> <span data-ttu-id="ff794-114">Dieses Handle ist gültig, bis die Rückruffunktion [*pxeprovidershutdown*](pxeprovidershutdown.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ff794-114">This handle is valid until the [*PxeProviderShutdown*](pxeprovidershutdown.md) callback function is called.</span></span>

</dd> <dt>

<span data-ttu-id="ff794-115">*hproviderkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff794-115">*hProviderKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff794-116">Handle für einen Registrierungsschlüssel, in dem Anbieter Konfigurationsinformationen gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ff794-116">Handle to a registry key where provider configuration information is to be stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff794-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff794-117">Return value</span></span>

<span data-ttu-id="ff794-118">Wenn die Anbieter Initialisierung erfolgreich ist, sollte der Rückruf einen **Fehler \_ Erfolg** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ff794-118">If the provider initialization succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="ff794-119">Im Falle eines Fehlers sollte ein entsprechender Fehlercode zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ff794-119">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff794-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff794-120">Requirements</span></span>



| <span data-ttu-id="ff794-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff794-121">Requirement</span></span> | <span data-ttu-id="ff794-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ff794-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ff794-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff794-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ff794-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ff794-124">None supported</span></span><br/>                                                          |
| <span data-ttu-id="ff794-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff794-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ff794-126">Windows Server 2008, Windows Server 2003 mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff794-126">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff794-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff794-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff794-128">Server Funktionen der Windows-Bereitstellungs Dienste</span><span class="sxs-lookup"><span data-stu-id="ff794-128">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="ff794-129">*Pxeprovidershutdown*</span><span class="sxs-lookup"><span data-stu-id="ff794-129">*PxeProviderShutdown*</span></span>](pxeprovidershutdown.md)
</dt> </dl>

 

 





