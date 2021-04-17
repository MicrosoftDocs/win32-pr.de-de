---
title: IMsRdpClient8 sendremoteaction-Methode
description: Bewirkt, dass eine Aktion in der Remote Sitzung ausgeführt wird.
ms.assetid: d6a43662-7e51-404a-a3f9-a8b51cbc69d1
ms.tgt_platform: multiple
keywords:
- Sendremoteaction-Methode Remotedesktopdienste
- Sendremoteaction-Methode Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, sendremoteaction-Methode
- Sendremoteaction-Methode Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, sendremoteaction-Methode
- Sendremoteaction-Methode Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10 Interface Remotedesktopdienste, sendremoteaction-Methode
topic_type:
- apiref
api_name:
- IMsRdpClient8.SendRemoteAction
- IMsRdpClient9.SendRemoteAction
- IMsRdpClient10.SendRemoteAction
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a28fc9695686402e0a8e98ed17fc1bc6a47939d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479302"
---
# <a name="imsrdpclient8sendremoteaction-method"></a><span data-ttu-id="2c74d-110">IMsRdpClient8:: sendremoteaction-Methode</span><span class="sxs-lookup"><span data-stu-id="2c74d-110">IMsRdpClient8::SendRemoteAction method</span></span>

<span data-ttu-id="2c74d-111">Bewirkt, dass eine Aktion in der Remote Sitzung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2c74d-111">Causes an action to be performed in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c74d-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c74d-112">Syntax</span></span>


```C++
HRESULT SendRemoteAction(
  [in] RemoteSessionActionType actionType
);
```



## <a name="parameters"></a><span data-ttu-id="2c74d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c74d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c74d-114">*Aktionstyp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c74d-114">*actionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c74d-115">Ein Wert der [**remotesessionaction Type**](remotesessionactiontype.md) -Enumeration, der die Aktion angibt, die an die Remote Sitzung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="2c74d-115">A value of the [**RemoteSessionActionType**](remotesessionactiontype.md) enumeration that specifies the action to send to the remote session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c74d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c74d-116">Return value</span></span>

<span data-ttu-id="2c74d-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2c74d-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2c74d-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2c74d-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c74d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c74d-119">Requirements</span></span>



| <span data-ttu-id="2c74d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c74d-120">Requirement</span></span> | <span data-ttu-id="2c74d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2c74d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c74d-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c74d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2c74d-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2c74d-123">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="2c74d-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c74d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2c74d-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2c74d-125">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="2c74d-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2c74d-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="2c74d-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c74d-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2c74d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2c74d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c74d-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c74d-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2c74d-130">IID</span><span class="sxs-lookup"><span data-stu-id="2c74d-130">IID</span></span><br/>                      | <span data-ttu-id="2c74d-131">IID \_ IMsRdpClient8 ist als 4247e044-9271-43a9-bc49-e2ad9e855d62 definiert.</span><span class="sxs-lookup"><span data-stu-id="2c74d-131">IID\_IMsRdpClient8 is defined as 4247E044-9271-43A9-BC49-E2AD9E855D62</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2c74d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c74d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c74d-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="2c74d-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="2c74d-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="2c74d-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="2c74d-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="2c74d-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





