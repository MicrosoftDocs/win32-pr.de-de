---
title: Imstscaxevents onremoteprogramview-Methode
description: Wird aufgerufen, wenn ein RemoteApp-Programm angezeigt wird.
ms.assetid: 24f5ea52-0c13-4024-9448-5c2c1896ca8b
ms.tgt_platform: multiple
keywords:
- Onremoteprogramview-Methode Remotedesktopdienste
- Onremoteprogramview-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onremoteprogramview-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 584e54c487ec24a3c165fdd5eb8e22f243e07f23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742112"
---
# <a name="imstscaxeventsonremoteprogramdisplayed-method"></a><span data-ttu-id="b6776-106">Imstscaxevents:: onremoteprogramview-Methode</span><span class="sxs-lookup"><span data-stu-id="b6776-106">IMsTscAxEvents::OnRemoteProgramDisplayed method</span></span>

<span data-ttu-id="b6776-107">Wird aufgerufen, wenn ein RemoteApp-Programm angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b6776-107">Called when a RemoteApp program is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6776-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6776-108">Syntax</span></span>


```C++
VOID OnRemoteProgramDisplayed(
  [in] VARIANT_BOOL vbDisplayed,
  [in] ULONG        uDisplayInformation
);
```



## <a name="parameters"></a><span data-ttu-id="b6776-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6776-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6776-110">*vbangezeigte* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6776-110">*vbDisplayed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6776-111">Gibt an, ob das RemoteApp-Programm angezeigt oder ausgeblendet wird.</span><span class="sxs-lookup"><span data-stu-id="b6776-111">Indicates whether the RemoteApp program is displayed or hidden.</span></span>

</dd> <dt>

<span data-ttu-id="b6776-112">*udisplayinformation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6776-112">*uDisplayInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6776-113">Die Anzeigeinformationen.</span><span class="sxs-lookup"><span data-stu-id="b6776-113">The display information.</span></span>

<dt>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>

<span data-ttu-id="b6776-114"><span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**Schiene \_ appdisplay \_ autoreconnct**</span><span class="sxs-lookup"><span data-stu-id="b6776-114"><span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**RAIL\_APPDISPLAY\_AUTORECONNECT**</span></span>


</dt> <dd>

<span data-ttu-id="b6776-115">Die automatische Wiederherstellung der Verbindung wird gerade ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b6776-115">Automatic reconnect is in progress.</span></span>

</dd> <dt>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>

<span data-ttu-id="b6776-116"><span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**Schiene \_ appdisplay \_ desktophooked**</span><span class="sxs-lookup"><span data-stu-id="b6776-116"><span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**RAIL\_APPDISPLAY\_DESKTOPHOOKED**</span></span>


</dt> <dd>

<span data-ttu-id="b6776-117">Der RemoteApp-Zähler wurde einfach auf NULL gesetzt.</span><span class="sxs-lookup"><span data-stu-id="b6776-117">The RemoteApp count just went to zero.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6776-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6776-118">Return value</span></span>

<span data-ttu-id="b6776-119">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b6776-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6776-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6776-120">Remarks</span></span>

<span data-ttu-id="b6776-121">Implementieren Sie diese Methode in der Ereignis Senke, um die Benachrichtigung zu erhalten, dass eine RemoteApp angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b6776-121">Implement this method in your event sink to receive notification that a RemoteApp has been displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6776-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6776-122">Requirements</span></span>



| <span data-ttu-id="b6776-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6776-123">Requirement</span></span> | <span data-ttu-id="b6776-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b6776-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6776-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6776-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b6776-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b6776-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b6776-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6776-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b6776-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6776-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b6776-129">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b6776-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="b6776-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6776-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b6776-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b6776-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6776-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6776-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b6776-133">IID</span><span class="sxs-lookup"><span data-stu-id="b6776-133">IID</span></span><br/>                      | <span data-ttu-id="b6776-134">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="b6776-134">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



 

 





