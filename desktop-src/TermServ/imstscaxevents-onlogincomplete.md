---
title: Imstscaxevents onlogincomplete-Methode
description: Wird aufgerufen, wenn das Client Steuerelement nach der Anzeige des Windows-Anmelde Dialogfelds erfolgreich an einem Remotedesktop-Sitzungshost Server (RD-Sitzungshost) angemeldet ist.
ms.assetid: acb345a6-3153-4b8f-ac51-fe0c19fa750a
ms.tgt_platform: multiple
keywords:
- Onlogincomplete-Methode Remotedesktopdienste
- Onlogincomplete-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onlogincomplete-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLoginComplete
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74d6b63f74ed99c8af939bafdc8a55a41e33b404
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518056"
---
# <a name="imstscaxeventsonlogincomplete-method"></a><span data-ttu-id="70de4-106">Imstscaxevents:: onlogincomplete-Methode</span><span class="sxs-lookup"><span data-stu-id="70de4-106">IMsTscAxEvents::OnLoginComplete method</span></span>

<span data-ttu-id="70de4-107">Wird aufgerufen, wenn das Client Steuerelement nach der Anzeige des Windows-Anmelde Dialogfelds erfolgreich an einem Remotedesktop-Sitzungshost Server (RD-Sitzungshost) angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="70de4-107">Called when the client control has successfully logged on to a Remote Desktop Session Host (RD Session Host) server, following the display of the Windows Logon dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="70de4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="70de4-108">Syntax</span></span>


```C++
void OnLoginComplete();
```



## <a name="parameters"></a><span data-ttu-id="70de4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="70de4-109">Parameters</span></span>

<span data-ttu-id="70de4-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="70de4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="70de4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70de4-111">Return value</span></span>

<span data-ttu-id="70de4-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="70de4-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="70de4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70de4-113">Remarks</span></span>

<span data-ttu-id="70de4-114">Implementieren Sie diese Methode in der Ereignis Senke, um die Benachrichtigung zu erhalten, dass das Steuerelement die Anmeldung abgeschlossen hat</span><span class="sxs-lookup"><span data-stu-id="70de4-114">Implement this method in your event sink to receive notification that the control has completed logon.</span></span>

## <a name="examples"></a><span data-ttu-id="70de4-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70de4-115">Examples</span></span>

<span data-ttu-id="70de4-116">Im folgenden Beispiel wird gezeigt, wie dieses Ereignis mit Visual Basic Skriptcode behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="70de4-116">The following example shows how to handle this event by using Visual Basic Scripting code.</span></span> <span data-ttu-id="70de4-117">In diesem Beispiel wird davon ausgegangen, dass das Steuerelement Objekt den Namen "MsRdpClient" hat.</span><span class="sxs-lookup"><span data-stu-id="70de4-117">The assumption in this example is that your control object is named "MsRdpClient".</span></span>

<span data-ttu-id="70de4-118">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="70de4-118">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>


```VB
Sub MsRdpClient.OnLoginComplete()
    Msgbox("Login has completed")
End sub
```



## <a name="requirements"></a><span data-ttu-id="70de4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70de4-119">Requirements</span></span>



| <span data-ttu-id="70de4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70de4-120">Requirement</span></span> | <span data-ttu-id="70de4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="70de4-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70de4-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="70de4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="70de4-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70de4-123">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="70de4-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="70de4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="70de4-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70de4-125">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="70de4-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="70de4-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="70de4-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70de4-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="70de4-128">DLL</span><span class="sxs-lookup"><span data-stu-id="70de4-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70de4-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70de4-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="70de4-130">IID</span><span class="sxs-lookup"><span data-stu-id="70de4-130">IID</span></span><br/>                      | <span data-ttu-id="70de4-131">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="70de4-131">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="70de4-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70de4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70de4-133">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="70de4-133">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





