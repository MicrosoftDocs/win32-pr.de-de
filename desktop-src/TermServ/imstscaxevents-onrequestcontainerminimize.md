---
title: Imstscaxevents onrequestcontainerminimum-Methode
description: Wird aufgerufen, wenn der Benutzer auf der Verbindungs Leiste im Vollbildmodus auf die Schaltfläche Minimieren drückt. Das Auslösen dieses Ereignisses ist eine Anforderung, dass die Containeranwendung sich selbst minimiert.
ms.assetid: fc052f9b-cf59-4d5a-ba39-571627b72f2a
ms.tgt_platform: multiple
keywords:
- Onrequestcontainerminimi-Methode Remotedesktopdienste
- Onrequestcontainerminimi-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onrequestcontainerminimi-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestContainerMinimize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85387e3b156eed29dc7068eac84280be521a934e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392022"
---
# <a name="imstscaxeventsonrequestcontainerminimize-method"></a><span data-ttu-id="07d5b-107">Imstscaxevents:: onrequestcontainerminimum-Methode</span><span class="sxs-lookup"><span data-stu-id="07d5b-107">IMsTscAxEvents::OnRequestContainerMinimize method</span></span>

<span data-ttu-id="07d5b-108">Wird aufgerufen, wenn der Benutzer auf der Verbindungs Leiste im Vollbildmodus auf die Schaltfläche **minimieren** drückt.</span><span class="sxs-lookup"><span data-stu-id="07d5b-108">Called when the user presses the **Minimize** button on the connection bar in full-screen mode.</span></span> <span data-ttu-id="07d5b-109">Das Auslösen dieses Ereignisses ist eine Anforderung, dass die Containeranwendung sich selbst minimiert.</span><span class="sxs-lookup"><span data-stu-id="07d5b-109">The firing of this event is a request that the container application minimize itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d5b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="07d5b-110">Syntax</span></span>


```C++
void OnRequestContainerMinimize();
```



## <a name="parameters"></a><span data-ttu-id="07d5b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="07d5b-111">Parameters</span></span>

<span data-ttu-id="07d5b-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="07d5b-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07d5b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07d5b-113">Return value</span></span>

<span data-ttu-id="07d5b-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="07d5b-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="07d5b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07d5b-115">Remarks</span></span>

<span data-ttu-id="07d5b-116">Diese Methode wird nur aufgerufen, wenn der im Container behandelte Vollbildmodus aktiviert ist. Weitere Informationen finden Sie unter [**imstscadvancedsettings::p UT \_ containerhandledfullscreen**](imstscadvancedsettings-containerhandledfullscreen.md) .</span><span class="sxs-lookup"><span data-stu-id="07d5b-116">This method will only be called if the container-handled full-screen mode is enabled - see [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="07d5b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07d5b-117">Requirements</span></span>



| <span data-ttu-id="07d5b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07d5b-118">Requirement</span></span> | <span data-ttu-id="07d5b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="07d5b-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07d5b-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07d5b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="07d5b-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07d5b-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="07d5b-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07d5b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="07d5b-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07d5b-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="07d5b-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="07d5b-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="07d5b-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07d5b-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="07d5b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="07d5b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07d5b-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07d5b-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="07d5b-128">IID</span><span class="sxs-lookup"><span data-stu-id="07d5b-128">IID</span></span><br/>                      | <span data-ttu-id="07d5b-129">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="07d5b-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="07d5b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07d5b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d5b-131">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="07d5b-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





