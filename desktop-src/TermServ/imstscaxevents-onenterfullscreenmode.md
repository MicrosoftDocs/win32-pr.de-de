---
title: Imstscaxevents onenterfullscreenmode-Methode
description: Wird aufgerufen, wenn der Client in den Vollbildmodus wechselt. Beispielsweise wird dieses Ereignis aufgerufen, wenn der Benutzer die Tastenkombination für den Vollbildmodus drückt (Strg + Alt + untbuggung).
ms.assetid: dc772492-59a2-4403-8b9a-0aff1801aa6f
ms.tgt_platform: multiple
keywords:
- Onenterfullscreenmode-Methode Remotedesktopdienste
- Onenterfullscreenmode-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onenterfullscreenmode-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnEnterFullScreenMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 226054fc7b1371bb088deb70ec9e87ea5a340b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956668"
---
# <a name="imstscaxeventsonenterfullscreenmode-method"></a><span data-ttu-id="31bb2-107">Imstscaxevents:: onenterfullscreenmode-Methode</span><span class="sxs-lookup"><span data-stu-id="31bb2-107">IMsTscAxEvents::OnEnterFullScreenMode method</span></span>

<span data-ttu-id="31bb2-108">Wird aufgerufen, wenn der Client in den Vollbildmodus wechselt.</span><span class="sxs-lookup"><span data-stu-id="31bb2-108">Called when the client enters full-screen mode.</span></span> <span data-ttu-id="31bb2-109">Beispielsweise wird dieses Ereignis aufgerufen, wenn der Benutzer die [Tasten](terminal-services-shortcut-keys.md) Kombination für den Vollbildmodus drückt (Strg + Alt + untbuggung).</span><span class="sxs-lookup"><span data-stu-id="31bb2-109">For example, this event is called when the user presses the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

## <a name="syntax"></a><span data-ttu-id="31bb2-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="31bb2-110">Syntax</span></span>


```C++
void OnEnterFullScreenMode();
```



## <a name="parameters"></a><span data-ttu-id="31bb2-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="31bb2-111">Parameters</span></span>

<span data-ttu-id="31bb2-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="31bb2-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="31bb2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31bb2-113">Return value</span></span>

<span data-ttu-id="31bb2-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="31bb2-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="31bb2-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31bb2-115">Remarks</span></span>

<span data-ttu-id="31bb2-116">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="31bb2-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31bb2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31bb2-117">Requirements</span></span>



| <span data-ttu-id="31bb2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31bb2-118">Requirement</span></span> | <span data-ttu-id="31bb2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="31bb2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31bb2-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31bb2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="31bb2-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31bb2-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="31bb2-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31bb2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="31bb2-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31bb2-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="31bb2-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="31bb2-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="31bb2-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31bb2-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="31bb2-126">DLL</span><span class="sxs-lookup"><span data-stu-id="31bb2-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31bb2-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31bb2-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="31bb2-128">IID</span><span class="sxs-lookup"><span data-stu-id="31bb2-128">IID</span></span><br/>                      | <span data-ttu-id="31bb2-129">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="31bb2-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="31bb2-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31bb2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31bb2-131">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="31bb2-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





