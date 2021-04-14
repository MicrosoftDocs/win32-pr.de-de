---
title: Imstscaxevents onauthenticationwarningverworfen-Methode
description: Wird aufgerufen, nachdem ein ActiveX-Steuerelement ein Authentifizierungs Dialogfeld (z. b. das Dialogfeld Zertifikat Fehler) anzeigt.
ms.assetid: bf5dbe4a-9129-47b3-9808-ed09d9010099
ms.tgt_platform: multiple
keywords:
- Onauthenticationwarningverwerfen-Methode Remotedesktopdienste
- Onauthenticationwarningverwerfen-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onauthenticationwarningverworfen-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDismissed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86bdadfdbc8e0a1387a1f3aaf712188689d0f808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391873"
---
# <a name="imstscaxeventsonauthenticationwarningdismissed-method"></a><span data-ttu-id="f242b-106">Imstscaxevents:: onauthenticationwarningverwerfen-Methode</span><span class="sxs-lookup"><span data-stu-id="f242b-106">IMsTscAxEvents::OnAuthenticationWarningDismissed method</span></span>

<span data-ttu-id="f242b-107">Wird aufgerufen, nachdem ein ActiveX-Steuerelement ein Authentifizierungs Dialogfeld (z. b. das Dialogfeld Zertifikat Fehler) anzeigt.</span><span class="sxs-lookup"><span data-stu-id="f242b-107">Called after an ActiveX control displays an authentication dialog box (for example, the certificate error dialog box).</span></span>

## <a name="syntax"></a><span data-ttu-id="f242b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f242b-108">Syntax</span></span>


```C++
void OnAuthenticationWarningDismissed();
```



## <a name="parameters"></a><span data-ttu-id="f242b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f242b-109">Parameters</span></span>

<span data-ttu-id="f242b-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f242b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f242b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f242b-111">Return value</span></span>

<span data-ttu-id="f242b-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f242b-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f242b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f242b-113">Remarks</span></span>

<span data-ttu-id="f242b-114">Bei Bedarf kann die [**uiparameentwindowhandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) -Eigenschaft der [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) -Schnittstelle verwendet werden, um die in der [**onauthenticationwarningused**](imstscaxevents-onauthenticationwarningdisplayed.md) -Methode möglicherweise ausgeführten übergeordneten Objekte rückgängig zu machen.</span><span class="sxs-lookup"><span data-stu-id="f242b-114">If needed, the [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) property of the [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) interface can be used to revert any parenting that may have been done in the [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) method.</span></span>

<span data-ttu-id="f242b-115">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f242b-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f242b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f242b-116">Requirements</span></span>



| <span data-ttu-id="f242b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f242b-117">Requirement</span></span> | <span data-ttu-id="f242b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f242b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f242b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f242b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f242b-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f242b-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f242b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f242b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f242b-122">Windows Server 2008, Windows Server 2008 mit SP1</span><span class="sxs-lookup"><span data-stu-id="f242b-122">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="f242b-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f242b-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="f242b-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f242b-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f242b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f242b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f242b-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f242b-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f242b-127">IID</span><span class="sxs-lookup"><span data-stu-id="f242b-127">IID</span></span><br/>                      | <span data-ttu-id="f242b-128">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="f242b-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="f242b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f242b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f242b-130">**Onauthenticationwarningangezeigte**</span><span class="sxs-lookup"><span data-stu-id="f242b-130">**OnAuthenticationWarningDisplayed**</span></span>](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[<span data-ttu-id="f242b-131">**Uianentwindowhandle**</span><span class="sxs-lookup"><span data-stu-id="f242b-131">**UIParentWindowHandle**</span></span>](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[<span data-ttu-id="f242b-132">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="f242b-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





