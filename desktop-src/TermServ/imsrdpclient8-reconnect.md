---
title: IMsRdpClient8 Reconnect-Methode
description: Stellt erneut eine Verbindung mit der Remote Sitzung mit der neuen Desktop Breite und-Höhe her.
ms.assetid: A2C4101D-780A-4973-B87C-025D9140C4BC
ms.tgt_platform: multiple
keywords:
- Reconnect-Methode Remotedesktopdienste
- Reconnect-Methode Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, Methode zum erneuten Verbinden
- Reconnect-Methode Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, Methode zum erneuten Verbinden
- Reconnect-Methode Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, Methode zum erneuten Verbinden
topic_type:
- apiref
api_name:
- IMsRdpClient8.Reconnect
- IMsRdpClient9.Reconnect
- IMsRdpClient10.Reconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d62072c56852af6be2965ce63aecf4634de87d11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519247"
---
# <a name="imsrdpclient8reconnect-method"></a><span data-ttu-id="8c3c9-110">IMsRdpClient8:: Reconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="8c3c9-110">IMsRdpClient8::Reconnect method</span></span>

<span data-ttu-id="8c3c9-111">Stellt erneut eine Verbindung mit der Remote Sitzung mit der neuen Desktop Breite und-Höhe her.</span><span class="sxs-lookup"><span data-stu-id="8c3c9-111">Reconnects to the remote session with the new desktop width and height.</span></span> <span data-ttu-id="8c3c9-112">Das-Steuerelement muss bereits mit einer Remote Sitzung verbunden sein, damit diese Methode erfolgreich ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="8c3c9-112">The control must already be connected to a remote session for this method to succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c3c9-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c3c9-113">Syntax</span></span>


```C++
HRESULT Reconnect(
  [in]          ULONG                  ulWidth,
  [in]          ULONG                  ulHeight,
  [out, retval] ControlReconnectStatus *pReconnectStatus
);
```



## <a name="parameters"></a><span data-ttu-id="8c3c9-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c3c9-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c3c9-115">*ulwidth* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c3c9-115">*ulWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3c9-116">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="8c3c9-116">Type: **ULONG**</span></span>

<span data-ttu-id="8c3c9-117">Die neue Breite des Desktops in Pixel.</span><span class="sxs-lookup"><span data-stu-id="8c3c9-117">The new desktop width, in pixels.</span></span> <span data-ttu-id="8c3c9-118">Informationen zu Wert Einschränkungen finden Sie in der [**desktopwidth**](imstscax-desktopwidth.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8c3c9-118">See the [**DesktopWidth**](imstscax-desktopwidth.md) property for value restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="8c3c9-119">*ulheight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c3c9-119">*ulHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3c9-120">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="8c3c9-120">Type: **ULONG**</span></span>

<span data-ttu-id="8c3c9-121">Die neue Höhe des Desktops in Pixel.</span><span class="sxs-lookup"><span data-stu-id="8c3c9-121">The new desktop height, in pixels.</span></span> <span data-ttu-id="8c3c9-122">Informationen zu Wert Einschränkungen finden Sie in der [**desktopheight**](imstscax-desktopheight.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8c3c9-122">See the [**DesktopHeight**](imstscax-desktopheight.md) property for value restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="8c3c9-123">*preconnectstatus* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8c3c9-123">*pReconnectStatus* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8c3c9-124">Typ: \**[**controlreconnectstatus**](controlreconnectstatus.md) \** _</span><span class="sxs-lookup"><span data-stu-id="8c3c9-124">Type: \**[**ControlReconnectStatus**](controlreconnectstatus.md)\** _</span></span>

<span data-ttu-id="8c3c9-125">Ein Zeiger auf eine [_ *controlreconnectstatus* \*](controlreconnectstatus.md) -Variable, die den Status des Vorgangs zum erneuten Verbinden empfängt.</span><span class="sxs-lookup"><span data-stu-id="8c3c9-125">A pointer to a [_ *ControlReconnectStatus*\*](controlreconnectstatus.md) variable that receives the status of the reconnect operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c3c9-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c3c9-126">Return value</span></span>

<span data-ttu-id="8c3c9-127">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8c3c9-127">Type: **HRESULT**</span></span>

<span data-ttu-id="8c3c9-128">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="8c3c9-128">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8c3c9-129">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8c3c9-129">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c3c9-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c3c9-130">Requirements</span></span>



| <span data-ttu-id="8c3c9-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c3c9-131">Requirement</span></span> | <span data-ttu-id="8c3c9-132">Wert</span><span class="sxs-lookup"><span data-stu-id="8c3c9-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c3c9-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c3c9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8c3c9-134">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8c3c9-134">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="8c3c9-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c3c9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8c3c9-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8c3c9-136">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="8c3c9-137">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="8c3c9-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="8c3c9-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c3c9-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8c3c9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="8c3c9-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c3c9-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c3c9-140"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8c3c9-141">IID</span><span class="sxs-lookup"><span data-stu-id="8c3c9-141">IID</span></span><br/>                      | <span data-ttu-id="8c3c9-142">IID \_ IMsRdpClient8 ist als 4247e044-9271-43a9-bc49-e2ad9e855d62 definiert.</span><span class="sxs-lookup"><span data-stu-id="8c3c9-142">IID\_IMsRdpClient8 is defined as 4247E044-9271-43A9-BC49-E2AD9E855D62</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8c3c9-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c3c9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c3c9-144">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="8c3c9-144">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="8c3c9-145">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="8c3c9-145">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="8c3c9-146">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="8c3c9-146">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="8c3c9-147">**Controlreconnectstatus**</span><span class="sxs-lookup"><span data-stu-id="8c3c9-147">**ControlReconnectStatus**</span></span>](controlreconnectstatus.md)
</dt> </dl>

 

 





