---
title: Imstscaxevents onreceivedtspublickey-Methode
description: Wird während der Verbindungs Sequenz aufgerufen, wenn der Client den öffentlichen Schlüssel vom Server abruft. Dieses Ereignis wird nur aufgerufen, wenn die notifytspublickey-Eigenschaft Variant \_ true ist.
ms.assetid: 1db98b8b-2f08-4252-ad8b-6764fa25b300
ms.tgt_platform: multiple
keywords:
- Onreceivedtspublickey-Methode Remotedesktopdienste
- Onreceivedtspublickey-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onreceivedtspublickey-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnReceivedTSPublicKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 337a9efabe48dee7a5a4194c3b796b95f35a0592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477433"
---
# <a name="imstscaxeventsonreceivedtspublickey-method"></a><span data-ttu-id="1d27e-107">Imstscaxevents:: onreceivedtspublickey-Methode</span><span class="sxs-lookup"><span data-stu-id="1d27e-107">IMsTscAxEvents::OnReceivedTSPublicKey method</span></span>

<span data-ttu-id="1d27e-108">Wird während der Verbindungs Sequenz aufgerufen, wenn der Client den öffentlichen Schlüssel vom Server abruft.</span><span class="sxs-lookup"><span data-stu-id="1d27e-108">Called during the connection sequence when the client retrieves the public key from the server.</span></span> <span data-ttu-id="1d27e-109">Dieses Ereignis wird nur aufgerufen, wenn die **notifytspublickey** -Eigenschaft **Variant \_ true** ist.</span><span class="sxs-lookup"><span data-stu-id="1d27e-109">This event is only called if the **NotifyTSPublicKey** property is **VARIANT\_TRUE**.</span></span> <span data-ttu-id="1d27e-110">Dies erfolgt nach dem [**onconnecting**](imstscaxevents-onconnecting.md)-Prozess, aber vor [**onauthenticationwarninganzeige**](imstscaxevents-onauthenticationwarningdisplayed.md) und [**onconnected**](imstscaxevents-onconnected.md).</span><span class="sxs-lookup"><span data-stu-id="1d27e-110">This is after [**OnConnecting**](imstscaxevents-onconnecting.md), but before [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) and [**OnConnected**](imstscaxevents-onconnected.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1d27e-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d27e-111">Syntax</span></span>


```C++
void OnReceivedTSPublicKey(
  [in]  BSTR         publicKey,
  [out] VARIANT_BOOL *pfContinueLogon
);
```



## <a name="parameters"></a><span data-ttu-id="1d27e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d27e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d27e-113">*PublicKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d27e-113">*publicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d27e-114">Enthält den öffentlichen Schlüssel des Remote Computers.</span><span class="sxs-lookup"><span data-stu-id="1d27e-114">Contains the public key of the remote machine.</span></span>

</dd> <dt>

<span data-ttu-id="1d27e-115">*pfcontinuelogon* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1d27e-115">*pfContinueLogon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d27e-116">Ein Zeiger auf eine **Variant- \_ boolesche** Variable, die empfängt, ob der Anmeldevorgang fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d27e-116">A pointer to a **VARIANT\_BOOL** variable that receives whether the logon process should continue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d27e-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d27e-117">Return value</span></span>

<span data-ttu-id="1d27e-118">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1d27e-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d27e-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d27e-119">Remarks</span></span>

<span data-ttu-id="1d27e-120">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="1d27e-120">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d27e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d27e-121">Requirements</span></span>



| <span data-ttu-id="1d27e-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d27e-122">Requirement</span></span> | <span data-ttu-id="1d27e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="1d27e-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d27e-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d27e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1d27e-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d27e-125">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1d27e-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d27e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1d27e-127">Windows Server 2008, Windows Server 2008 mit SP1</span><span class="sxs-lookup"><span data-stu-id="1d27e-127">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="1d27e-128">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="1d27e-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="1d27e-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d27e-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1d27e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1d27e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d27e-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d27e-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1d27e-132">IID</span><span class="sxs-lookup"><span data-stu-id="1d27e-132">IID</span></span><br/>                      | <span data-ttu-id="1d27e-133">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="1d27e-133">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="1d27e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d27e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d27e-135">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="1d27e-135">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





