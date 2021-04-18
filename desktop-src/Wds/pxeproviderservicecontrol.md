---
title: Pxeproviderservicecontrol-Rückruffunktion
description: Wird aufgerufen, wenn der WDS-Dienst einen Dienst Steuerungs Code empfängt.
ms.assetid: 180ddcda-d111-4c81-9177-db99cbf1449f
keywords:
- Pxeproviderservicecontrol-Rückruffunktion Windows-Bereitstellungs Dienste
topic_type:
- apiref
api_name:
- PxeProviderServiceControl
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c8a2c71b7b386254622758efa5f3dc5269a131d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338147"
---
# <a name="pxeproviderservicecontrol-callback-function"></a><span data-ttu-id="05e39-104">Pxeproviderservicecontrol-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="05e39-104">PxeProviderServiceControl callback function</span></span>

<span data-ttu-id="05e39-105">Wird aufgerufen, wenn der WDS-Dienst einen Dienst Steuerungs Code empfängt.</span><span class="sxs-lookup"><span data-stu-id="05e39-105">Called when a service control code is received by the WDS service.</span></span> <span data-ttu-id="05e39-106">Diese Rückruffunktion wird durch Aufrufen der [**pxeregistercallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) -Funktion registriert, wobei der *CallbackType* -Parameter auf **PXE \_ Callback \_ Service \_ Control** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="05e39-106">This callback function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_SERVICE\_CONTROL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="05e39-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="05e39-107">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderServiceControl(
  _In_ PVOID pContext,
       DWORD dwControl
);
```



## <a name="parameters"></a><span data-ttu-id="05e39-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="05e39-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05e39-109">*pContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05e39-109">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05e39-110">Der Kontextwert, der an die [**pxeregistercallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="05e39-110">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> <dt>

<span data-ttu-id="05e39-111">*dwcontrol*</span><span class="sxs-lookup"><span data-stu-id="05e39-111">*dwControl*</span></span> 
</dt> <dd>

<span data-ttu-id="05e39-112">Steuerelement Code.</span><span class="sxs-lookup"><span data-stu-id="05e39-112">Control code.</span></span> <span data-ttu-id="05e39-113">Eine Liste der möglichen Werte finden Sie unter dem *dwcontrol* -Parameter der [*handlerex*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="05e39-113">For the list of possible values, see the *dwControl* parameter of the [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05e39-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05e39-114">Return value</span></span>

<span data-ttu-id="05e39-115">Wenn der Anbieter erfolgreich heruntergefahren wurde, sollte der Rückruf einen **Fehler \_ Erfolg** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="05e39-115">If the provider shutdown succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="05e39-116">Im Falle eines Fehlers sollte ein entsprechender Fehlercode zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="05e39-116">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="05e39-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05e39-117">Requirements</span></span>



| <span data-ttu-id="05e39-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05e39-118">Requirement</span></span> | <span data-ttu-id="05e39-119">Wert</span><span class="sxs-lookup"><span data-stu-id="05e39-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="05e39-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05e39-120">Minimum supported client</span></span><br/> | <span data-ttu-id="05e39-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="05e39-121">None supported</span></span><br/>                                                          |
| <span data-ttu-id="05e39-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05e39-122">Minimum supported server</span></span><br/> | <span data-ttu-id="05e39-123">Windows Server 2008, Windows Server 2003 mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05e39-123">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="05e39-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05e39-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05e39-125">Server Funktionen der Windows-Bereitstellungs Dienste</span><span class="sxs-lookup"><span data-stu-id="05e39-125">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="05e39-126">**Pxeregistercallback**</span><span class="sxs-lookup"><span data-stu-id="05e39-126">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

