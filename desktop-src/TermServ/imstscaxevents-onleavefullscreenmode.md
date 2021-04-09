---
title: Imstscaxevents onleavefullscreenmode-Methode
description: Wird aufgerufen, wenn der Client den Vollbildmodus verlässt. Beispielsweise wird dieses Ereignis aufgerufen, wenn der Benutzer die Tastenkombination für den Vollbildmodus drückt (Strg + Alt + untbuggung).
ms.assetid: 95c5d427-b6e2-4a42-9816-b130ab533ac0
ms.tgt_platform: multiple
keywords:
- Onleavefullscreenmode-Methode Remotedesktopdienste
- Onleavefullscreenmode-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onleavefullscreenmode-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLeaveFullScreenMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4ee414f2dceba35a17ff86bce03c83d75aab48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040751"
---
# <a name="imstscaxeventsonleavefullscreenmode-method"></a><span data-ttu-id="153ed-107">Imstscaxevents:: onleavefullscreenmode-Methode</span><span class="sxs-lookup"><span data-stu-id="153ed-107">IMsTscAxEvents::OnLeaveFullScreenMode method</span></span>

<span data-ttu-id="153ed-108">Wird aufgerufen, wenn der Client den Vollbildmodus verlässt.</span><span class="sxs-lookup"><span data-stu-id="153ed-108">Called when the client leaves full-screen mode.</span></span> <span data-ttu-id="153ed-109">Beispielsweise wird dieses Ereignis aufgerufen, wenn der Benutzer die [Tasten](terminal-services-shortcut-keys.md) Kombination für den Vollbildmodus drückt (Strg + Alt + untbuggung).</span><span class="sxs-lookup"><span data-stu-id="153ed-109">For example, this event is called when the user presses the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

## <a name="syntax"></a><span data-ttu-id="153ed-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="153ed-110">Syntax</span></span>


```C++
void OnLeaveFullScreenMode();
```



## <a name="parameters"></a><span data-ttu-id="153ed-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="153ed-111">Parameters</span></span>

<span data-ttu-id="153ed-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="153ed-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="153ed-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="153ed-113">Return value</span></span>

<span data-ttu-id="153ed-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="153ed-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="153ed-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="153ed-115">Remarks</span></span>

<span data-ttu-id="153ed-116">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="153ed-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="153ed-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="153ed-117">Requirements</span></span>



| <span data-ttu-id="153ed-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="153ed-118">Requirement</span></span> | <span data-ttu-id="153ed-119">Wert</span><span class="sxs-lookup"><span data-stu-id="153ed-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="153ed-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="153ed-120">Minimum supported client</span></span><br/> | <span data-ttu-id="153ed-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="153ed-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="153ed-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="153ed-122">Minimum supported server</span></span><br/> | <span data-ttu-id="153ed-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="153ed-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="153ed-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="153ed-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="153ed-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="153ed-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="153ed-126">DLL</span><span class="sxs-lookup"><span data-stu-id="153ed-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="153ed-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="153ed-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="153ed-128">IID</span><span class="sxs-lookup"><span data-stu-id="153ed-128">IID</span></span><br/>                      | <span data-ttu-id="153ed-129">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="153ed-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="153ed-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="153ed-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="153ed-131">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="153ed-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





