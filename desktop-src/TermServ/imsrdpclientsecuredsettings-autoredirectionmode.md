---
title: Imsrdpclientsecuredsettings audioredirectionmode-Eigenschaft
description: Gibt die audioumleitungs Einstellungen an, die angeben, ob Sounds oder Sounds auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) umgeleitet werden sollen.
ms.assetid: 6aa63a50-a714-4a9b-a4ec-c0551920467a
ms.tgt_platform: multiple
keywords:
- Audioredirectionmode-Eigenschaft Remotedesktopdienste
- Audioredirectionmode-Eigenschaft Remotedesktopdienste, imsrdpclientsecuredsettings-Schnittstelle
- Imsrdpclientsecuredsettings-Schnittstelle Remotedesktopdienste, audioredirectionmode-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.AudioRedirectionMode
- IMsRdpClientSecuredSettings.get_AudioRedirectionMode
- IMsRdpClientSecuredSettings.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 858342811ec97def95031ebed0605b5a81cf80fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519228"
---
# <a name="imsrdpclientsecuredsettingsaudioredirectionmode-property"></a><span data-ttu-id="83179-106">Imsrdpclientsecuredsettings:: audioredirectionmode-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="83179-106">IMsRdpClientSecuredSettings::AudioRedirectionMode property</span></span>

<span data-ttu-id="83179-107">Gibt die audioumleitungs Einstellungen an, die angeben, ob Sounds oder Sounds auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) umgeleitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="83179-107">Specifies the audio redirection settings, which specify whether to redirect sounds or play sounds at the Remote Desktop Session Host (RD Session Host) server.</span></span>

<span data-ttu-id="83179-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="83179-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="83179-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="83179-109">Syntax</span></span>


```C++
HRESULT put_AudioRedirectionMode(
  [in]  LONG audioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] LONG *paudioRedirectionMode
);
```



## <a name="property-value"></a><span data-ttu-id="83179-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="83179-110">Property value</span></span>

<span data-ttu-id="83179-111">Die neuen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="83179-111">The new settings.</span></span> <span data-ttu-id="83179-112">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="83179-112">This parameter can be one of the following values.</span></span>

<dt>

<span data-ttu-id="83179-113">0</span><span class="sxs-lookup"><span data-stu-id="83179-113">0</span></span>
</dt> <dd>

<span data-ttu-id="83179-114">Umleiten von Sounds an den Client.</span><span class="sxs-lookup"><span data-stu-id="83179-114">Redirect sounds to the client.</span></span> <span data-ttu-id="83179-115">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="83179-115">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="83179-116">1</span><span class="sxs-lookup"><span data-stu-id="83179-116">1</span></span>
</dt> <dd>

<span data-ttu-id="83179-117">Abspielen von Sounds auf dem Remote Computer.</span><span class="sxs-lookup"><span data-stu-id="83179-117">Play sounds at the remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="83179-118">2</span><span class="sxs-lookup"><span data-stu-id="83179-118">2</span></span>
</dt> <dd>

<span data-ttu-id="83179-119">Sound Umleitung deaktivieren; Spielen Sie keine Sounds auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="83179-119">Disable sound redirection; do not play sounds at the server.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="83179-120">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="83179-120">Error codes</span></span>

<span data-ttu-id="83179-121">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="83179-121">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="83179-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83179-122">Remarks</span></span>

<span data-ttu-id="83179-123">Diese Eigenschaften können nicht festgelegt werden, wenn das Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="83179-123">These properties cannot be set when the control is connected.</span></span>

<span data-ttu-id="83179-124">Weitere Informationen finden Sie unter [Bereitstellen der RDP-Client Sicherheit](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="83179-124">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="83179-125">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="83179-125">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83179-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83179-126">Requirements</span></span>



| <span data-ttu-id="83179-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83179-127">Requirement</span></span> | <span data-ttu-id="83179-128">Wert</span><span class="sxs-lookup"><span data-stu-id="83179-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83179-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="83179-129">Minimum supported client</span></span><br/> | <span data-ttu-id="83179-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83179-130">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="83179-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="83179-131">Minimum supported server</span></span><br/> | <span data-ttu-id="83179-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83179-132">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="83179-133">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="83179-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="83179-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83179-134"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="83179-135">DLL</span><span class="sxs-lookup"><span data-stu-id="83179-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83179-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83179-136"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="83179-137">IID</span><span class="sxs-lookup"><span data-stu-id="83179-137">IID</span></span><br/>                      | <span data-ttu-id="83179-138">IID \_ imsrdpclientsecuredsettings ist als 605befcf-39c1-45cc-a811-068fb7be346d definiert.</span><span class="sxs-lookup"><span data-stu-id="83179-138">IID\_IMsRdpClientSecuredSettings is defined as 605befcf-39c1-45cc-a811-068fb7be346d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="83179-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83179-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83179-140">**Imsrdpclientsecuredsettings**</span><span class="sxs-lookup"><span data-stu-id="83179-140">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





