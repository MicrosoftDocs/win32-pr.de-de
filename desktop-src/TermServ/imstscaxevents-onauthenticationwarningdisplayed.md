---
title: Imstscaxevents onauthenticationwarninggezeigte-Methode
description: Wird aufgerufen, bevor ein ActiveX-Steuerelement ein Authentifizierungs Dialogfeld (z. b. das Dialogfeld Zertifikat Fehler) anzeigt.
ms.assetid: ce307e5f-5e26-4041-bbd5-6871c0678da4
ms.tgt_platform: multiple
keywords:
- Onauthenticationwarningangezeigte-Methode Remotedesktopdienste
- Onauthenticationwarningangezeigte Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onauthenticationwarninggezeigte-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33307adf103536cce5841effe2843a7c48fda357
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103527"
---
# <a name="imstscaxeventsonauthenticationwarningdisplayed-method"></a><span data-ttu-id="00861-106">Imstscaxevents:: onauthenticationwarninggezeigte-Methode</span><span class="sxs-lookup"><span data-stu-id="00861-106">IMsTscAxEvents::OnAuthenticationWarningDisplayed method</span></span>

<span data-ttu-id="00861-107">Wird aufgerufen, bevor ein ActiveX-Steuerelement ein Authentifizierungs Dialogfeld (z. b. das Dialogfeld Zertifikat Fehler) anzeigt.</span><span class="sxs-lookup"><span data-stu-id="00861-107">Called before an ActiveX control displays an authentication dialog box (for example, the certificate error dialog box).</span></span>

## <a name="syntax"></a><span data-ttu-id="00861-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="00861-108">Syntax</span></span>


```C++
void OnAuthenticationWarningDisplayed();
```



## <a name="parameters"></a><span data-ttu-id="00861-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="00861-109">Parameters</span></span>

<span data-ttu-id="00861-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="00861-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="00861-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00861-111">Return value</span></span>

<span data-ttu-id="00861-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="00861-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="00861-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00861-113">Remarks</span></span>

<span data-ttu-id="00861-114">Bei Bedarf kann die [**uiparameentwindowhandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) -Eigenschaft der [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) -Schnittstelle verwendet werden, um sicherzustellen, dass das Dialogfeld für die modale Authentifizierung, das angezeigt wird, von einem angegebenen Fenster übergeordnet wird (Dies ist möglicherweise erforderlich, um zu verhindern, dass Benutzer andere Dialogfelder verwenden, während das Authentifizierungs Dialogfeld angezeigt wird).</span><span class="sxs-lookup"><span data-stu-id="00861-114">If needed, the [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) property of the [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) interface can be used to ensure that the modal authentication dialog to be displayed will be parented by a specified window (this may be necessary to prevent users from using other dialog boxes while the authentication dialog box is displayed).</span></span> <span data-ttu-id="00861-115">Standardmäßig ist das übergeordnete Element das Fenster "ActiveX-Steuerelement".</span><span class="sxs-lookup"><span data-stu-id="00861-115">By default, the parent is the ActiveX control window.</span></span>

<span data-ttu-id="00861-116">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="00861-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00861-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00861-117">Requirements</span></span>



| <span data-ttu-id="00861-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00861-118">Requirement</span></span> | <span data-ttu-id="00861-119">Wert</span><span class="sxs-lookup"><span data-stu-id="00861-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00861-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00861-120">Minimum supported client</span></span><br/> | <span data-ttu-id="00861-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00861-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="00861-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00861-122">Minimum supported server</span></span><br/> | <span data-ttu-id="00861-123">Windows Server 2008, Windows Server 2008 mit SP1</span><span class="sxs-lookup"><span data-stu-id="00861-123">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="00861-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="00861-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="00861-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00861-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="00861-126">DLL</span><span class="sxs-lookup"><span data-stu-id="00861-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00861-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00861-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="00861-128">IID</span><span class="sxs-lookup"><span data-stu-id="00861-128">IID</span></span><br/>                      | <span data-ttu-id="00861-129">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="00861-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="00861-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00861-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00861-131">**Onauthenticationwarningverworfen**</span><span class="sxs-lookup"><span data-stu-id="00861-131">**OnAuthenticationWarningDismissed**</span></span>](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[<span data-ttu-id="00861-132">**Uianentwindowhandle**</span><span class="sxs-lookup"><span data-stu-id="00861-132">**UIParentWindowHandle**</span></span>](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[<span data-ttu-id="00861-133">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="00861-133">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





