---
title: IMsRdpClient9 syncsessiondisplaysettings-Methode
description: Synchronisiert Sitzungs Anzeigeeinstellungen.
ms.assetid: cc2c497f-665a-458d-895b-21dd21977890
ms.tgt_platform: multiple
keywords:
- Syncsessiondisplaysettings-Methode Remotedesktopdienste
- Syncsessiondisplaysettings-Methode Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, syncsessiondisplaysettings-Methode
- Syncsessiondisplaysettings-Methode Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, syncsessiondisplaysettings-Methode
topic_type:
- apiref
api_name:
- IMsRdpClient9.SyncSessionDisplaySettings
- IMsRdpClient10.SyncSessionDisplaySettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4429f966c00fb608416d541bec229defeca3e5b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949434"
---
# <a name="imsrdpclient9syncsessiondisplaysettings-method"></a><span data-ttu-id="6d684-108">IMsRdpClient9:: syncsessiondisplaysettings-Methode</span><span class="sxs-lookup"><span data-stu-id="6d684-108">IMsRdpClient9::SyncSessionDisplaySettings method</span></span>

<span data-ttu-id="6d684-109">Synchronisiert Sitzungs Anzeigeeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="6d684-109">Synchronizes session display settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d684-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d684-110">Syntax</span></span>


```C++
HRESULT SyncSessionDisplaySettings();
```



## <a name="parameters"></a><span data-ttu-id="6d684-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d684-111">Parameters</span></span>

<span data-ttu-id="6d684-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6d684-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d684-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d684-113">Return value</span></span>

<span data-ttu-id="6d684-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="6d684-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6d684-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6d684-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d684-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d684-116">Requirements</span></span>



| <span data-ttu-id="6d684-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d684-117">Requirement</span></span> | <span data-ttu-id="6d684-118">Wert</span><span class="sxs-lookup"><span data-stu-id="6d684-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d684-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d684-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6d684-120">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6d684-120">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="6d684-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d684-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6d684-122">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6d684-122">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="6d684-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6d684-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="6d684-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d684-124"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="6d684-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6d684-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d684-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d684-126"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="6d684-127">IID</span><span class="sxs-lookup"><span data-stu-id="6d684-127">IID</span></span><br/>                      | <span data-ttu-id="6d684-128">CLSID \_ MsRdpClient9 ist als 301b94ba-5d25-4a12-bffe-3b6e7a616585 definiert</span><span class="sxs-lookup"><span data-stu-id="6d684-128">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="6d684-129">CLSID \_ MsRdpClient9NotSafeForScripting ist als 8b918b82-7985-4c24-89df-c33ad2bbfbcd definiert.</span><span class="sxs-lookup"><span data-stu-id="6d684-129">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="6d684-130">IID \_ IMsRdpClient9 ist als 28904001-04b6-436C-a55b-0af1a0883dc9 definiert.</span><span class="sxs-lookup"><span data-stu-id="6d684-130">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6d684-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d684-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d684-132">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="6d684-132">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="6d684-133">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="6d684-133">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





