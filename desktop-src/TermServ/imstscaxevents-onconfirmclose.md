---
title: Imstscaxevents onconfirmclose-Methode
description: Wird aufgerufen, wenn der Client die Methode "imsrdpclient RequestClose" aufruft.
ms.assetid: fb149fbc-9415-4c4c-8d4b-e22214ac38cb
ms.tgt_platform: multiple
keywords:
- Onconfirmclose-Methode Remotedesktopdienste
- Onconfirmclose-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onconfirmclose-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConfirmClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623196033e23a964857a6a604c7eca3904f32c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106485"
---
# <a name="imstscaxeventsonconfirmclose-method"></a><span data-ttu-id="56e97-106">Imstscaxevents:: onconfirmclose-Methode</span><span class="sxs-lookup"><span data-stu-id="56e97-106">IMsTscAxEvents::OnConfirmClose method</span></span>

<span data-ttu-id="56e97-107">Wird aufgerufen, wenn der Client die [**imsrdpclient:: RequestClose**](imsrdpclient-requestclose.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="56e97-107">Called when the client calls the [**IMsRdpClient::RequestClose**](imsrdpclient-requestclose.md) method.</span></span> <span data-ttu-id="56e97-108">Als Reaktion auf dieses Ereignis sollte der Benutzer aufgefordert werden, das Schließen der Verbindung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="56e97-108">In response to this event, the user should be prompted to confirm closing the connection.</span></span> <span data-ttu-id="56e97-109">Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="56e97-109">For more information, see the following Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="56e97-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="56e97-110">Syntax</span></span>


```C++
void OnConfirmClose(
  [out] VARIANT_BOOL *pfAllowClose
);
```



## <a name="parameters"></a><span data-ttu-id="56e97-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="56e97-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56e97-112">*pfallowclose* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="56e97-112">*pfAllowClose* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56e97-113">Wenn **Variant \_ true** ist, bedeutet der Standardwert, dass der Benutzer die Verbindung schließen möchte.</span><span class="sxs-lookup"><span data-stu-id="56e97-113">If **VARIANT\_TRUE**, the default, indicates that the user wants to close the connection.</span></span> <span data-ttu-id="56e97-114">Wenn **Variant \_ false** ist, wird angegeben, dass der Benutzer die Verbindung nicht schließen möchte.</span><span class="sxs-lookup"><span data-stu-id="56e97-114">If **VARIANT\_FALSE**, indicates that the user does not want to close the connection.</span></span> <span data-ttu-id="56e97-115">Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="56e97-115">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56e97-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56e97-116">Return value</span></span>

<span data-ttu-id="56e97-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="56e97-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="56e97-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56e97-118">Remarks</span></span>

<span data-ttu-id="56e97-119">Wenn eine Containeranwendung die [**imsrdpclient:: RequestClose**](imsrdpclient-requestclose.md) -Methode aufruft, gibt diese Methode einen Wert zurück, der angibt, ob der Container auf das Eintreten eines **onconfirmclose** -Ereignisses warten soll, bevor die Steuerelement Verbindung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="56e97-119">When a container application calls the [**IMsRdpClient::RequestClose**](imsrdpclient-requestclose.md) method, that method returns a value indicating whether the container should wait for an **OnConfirmClose** event to occur before closing the control connection.</span></span> <span data-ttu-id="56e97-120">Wenn **RequestClose** " **controlclosewaitforevents**" zurückgibt und der Benutzer verbunden ist und bei seiner Remotedesktopdienste Sitzung angemeldet ist, wird das **onconfirmclose** -Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="56e97-120">If **RequestClose** returns **controlCloseWaitForEvents**, and the user is connected and logged on to their Remote Desktop Services session, the **OnConfirmClose** event fires.</span></span> <span data-ttu-id="56e97-121">An diesem Punkt kann die Containeranwendung den Benutzer auffordern und Fragen, ob der Benutzer die Verbindung schließen möchte.</span><span class="sxs-lookup"><span data-stu-id="56e97-121">At that point the container application can prompt the user, asking whether the user wants to close the connection.</span></span> <span data-ttu-id="56e97-122">Wenn der Benutzer die Verbindung schließen möchte, sollte die Anwendung den Parameter *pfallowclose* auf **Variant \_ true** festlegen und das Schließen der Verbindung fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="56e97-122">If the user wants to close the connection, the application should set the *pfAllowClose* parameter to **VARIANT\_TRUE** and proceed with closing the connection.</span></span> <span data-ttu-id="56e97-123">Wenn der Benutzer nicht schließen möchte, sollte die Anwendung *pfallowclose* auf **Variant \_ false** festlegen und die Verbindung geöffnet lassen.</span><span class="sxs-lookup"><span data-stu-id="56e97-123">If the user does not want to close, the application should set *pfAllowClose* to **VARIANT\_FALSE** and leave the connection open.</span></span>

<span data-ttu-id="56e97-124">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="56e97-124">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="56e97-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56e97-125">Requirements</span></span>



| <span data-ttu-id="56e97-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56e97-126">Requirement</span></span> | <span data-ttu-id="56e97-127">Wert</span><span class="sxs-lookup"><span data-stu-id="56e97-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56e97-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56e97-128">Minimum supported client</span></span><br/> | <span data-ttu-id="56e97-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56e97-129">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="56e97-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56e97-130">Minimum supported server</span></span><br/> | <span data-ttu-id="56e97-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56e97-131">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="56e97-132">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="56e97-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="56e97-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56e97-133"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="56e97-134">DLL</span><span class="sxs-lookup"><span data-stu-id="56e97-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56e97-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56e97-135"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="56e97-136">IID</span><span class="sxs-lookup"><span data-stu-id="56e97-136">IID</span></span><br/>                      | <span data-ttu-id="56e97-137">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="56e97-137">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="56e97-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56e97-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56e97-139">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="56e97-139">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





