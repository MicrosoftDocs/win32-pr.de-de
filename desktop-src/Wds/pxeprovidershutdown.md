---
title: Pxeprovidershutdown-Rückruffunktion
description: Wird aufgerufen, um den Anbieter herunterzufahren.
ms.assetid: 436d7428-18f9-4b73-b346-79c9a0738c31
keywords:
- Pxeprovidershutdown-Rückruffunktion Windows-Bereitstellungs Dienste
topic_type:
- apiref
api_name:
- PxeProviderShutdown
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17698c5fa1f6ce6bd5443d0244ebc6ce6082ec33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342428"
---
# <a name="pxeprovidershutdown-callback-function"></a><span data-ttu-id="a6d8c-104">Pxeprovidershutdown-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="a6d8c-104">PxeProviderShutdown callback function</span></span>

<span data-ttu-id="a6d8c-105">Wird aufgerufen, um den Anbieter herunterzufahren.</span><span class="sxs-lookup"><span data-stu-id="a6d8c-105">Called to shutdown the provider.</span></span> <span data-ttu-id="a6d8c-106">Diese Funktion wird durch Aufrufen der [**pxeregistercallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) -Funktion registriert, wobei der *CallbackType* -Parameter auf den **PXE- \_ Rückruf \_ herunter** Gefahren festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a6d8c-106">This function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_SHUTDOWN**.</span></span> <span data-ttu-id="a6d8c-107">Nachdem diese Funktion aufgerufen wurde, ist das an die [*pxeproviderinitialize*](pxeproviderinitialize.md) -Funktion weiter gegebene *hprovider* -Handle nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="a6d8c-107">After this function is called, the *hProvider* handle passed to the [*PxeProviderInitialize*](pxeproviderinitialize.md) function is no longer valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6d8c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6d8c-108">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderShutdown(
  _In_ PVOID pContext
);
```



## <a name="parameters"></a><span data-ttu-id="a6d8c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6d8c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6d8c-110">*pContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6d8c-110">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6d8c-111">Der Kontextwert, der an die [**pxeregistercallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a6d8c-111">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6d8c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6d8c-112">Return value</span></span>

<span data-ttu-id="a6d8c-113">Wenn der Anbieter erfolgreich heruntergefahren wurde, sollte der Rückruf einen **Fehler \_ Erfolg** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a6d8c-113">If the provider shutdown succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="a6d8c-114">Im Falle eines Fehlers sollte ein entsprechender Fehlercode zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a6d8c-114">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6d8c-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6d8c-115">Requirements</span></span>



| <span data-ttu-id="a6d8c-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6d8c-116">Requirement</span></span> | <span data-ttu-id="a6d8c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a6d8c-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a6d8c-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a6d8c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a6d8c-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a6d8c-119">None supported</span></span><br/>                                                          |
| <span data-ttu-id="a6d8c-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a6d8c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a6d8c-121">Windows Server 2008, Windows Server 2003 mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6d8c-121">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a6d8c-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6d8c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6d8c-123">Server Funktionen der Windows-Bereitstellungs Dienste</span><span class="sxs-lookup"><span data-stu-id="a6d8c-123">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="a6d8c-124">*Pxeproviderinitialize*</span><span class="sxs-lookup"><span data-stu-id="a6d8c-124">*PxeProviderInitialize*</span></span>](pxeproviderinitialize.md)
</dt> <dt>

[<span data-ttu-id="a6d8c-125">**Pxeregistercallback**</span><span class="sxs-lookup"><span data-stu-id="a6d8c-125">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

 





