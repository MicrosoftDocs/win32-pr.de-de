---
title: Imsrdpclientsecuredsettings keyboardhuokmode (Eigenschaft)
description: Gibt die Einstellungen der Tastatur Umleitung an, die angeben, wie und wann die Windows-Tastenkombination angewendet werden soll (z. b. Alt + Tab).
ms.assetid: 16734580-9be9-476b-b8e7-1eca3ba24d61
ms.tgt_platform: multiple
keywords:
- Keyboardhuokmode-Eigenschaft Remotedesktopdienste
- Keyboardhuokmode-Eigenschaft Remotedesktopdienste, imsrdpclientsecuredsettings-Schnittstelle
- Imsrdpclientsecuredsettings-Schnittstelle Remotedesktopdienste, keyboardhuokmode-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.KeyboardHookMode
- IMsRdpClientSecuredSettings.get_KeyboardHookMode
- IMsRdpClientSecuredSettings.put_KeyboardHookMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 948069b689d8799a98805148017a204b719d7645
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391730"
---
# <a name="imsrdpclientsecuredsettingskeyboardhookmode-property"></a><span data-ttu-id="6d178-106">Imsrdpclientsecuredsettings:: keyboardhuokmode-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6d178-106">IMsRdpClientSecuredSettings::KeyboardHookMode property</span></span>

<span data-ttu-id="6d178-107">Gibt die Einstellungen der Tastatur Umleitung an, die angeben, wie und wann die Windows-Tastenkombination angewendet werden soll (z. b. Alt + Tab).</span><span class="sxs-lookup"><span data-stu-id="6d178-107">Specifies the keyboard redirection settings, which specify how and when to apply Windows keyboard shortcut (for example, ALT+TAB).</span></span>

<span data-ttu-id="6d178-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6d178-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d178-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d178-109">Syntax</span></span>


```C++
HRESULT put_KeyboardHookMode(
  [in]  LONG keyboardHookMode
);

HRESULT get_KeyboardHookMode(
  [out] LONG *pkeyboardHookMode
);
```



## <a name="property-value"></a><span data-ttu-id="6d178-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6d178-110">Property value</span></span>

<span data-ttu-id="6d178-111">Die neuen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="6d178-111">The new settings.</span></span> <span data-ttu-id="6d178-112">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="6d178-112">This parameter can be one of the following values.</span></span>

<dt>

<span data-ttu-id="6d178-113">0</span><span class="sxs-lookup"><span data-stu-id="6d178-113">0</span></span>
</dt> <dd>

<span data-ttu-id="6d178-114">Anwenden von Tastenkombinationen nur lokal auf dem Client Computer.</span><span class="sxs-lookup"><span data-stu-id="6d178-114">Apply key combinations only locally at the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="6d178-115">1</span><span class="sxs-lookup"><span data-stu-id="6d178-115">1</span></span>
</dt> <dd>

<span data-ttu-id="6d178-116">Anwenden von Tastenkombinationen auf dem Remote Server.</span><span class="sxs-lookup"><span data-stu-id="6d178-116">Apply key combinations at the remote server.</span></span>

</dd> <dt>

<span data-ttu-id="6d178-117">2</span><span class="sxs-lookup"><span data-stu-id="6d178-117">2</span></span>
</dt> <dd>

<span data-ttu-id="6d178-118">Anwenden von Tastenkombinationen auf den Remote Server, wenn der Client im Vollbildmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d178-118">Apply key combinations to the remote server only when the client is running in full-screen mode.</span></span> <span data-ttu-id="6d178-119">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="6d178-119">This is the default value.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="6d178-120">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="6d178-120">Error codes</span></span>

<span data-ttu-id="6d178-121">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="6d178-121">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d178-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d178-122">Remarks</span></span>

<span data-ttu-id="6d178-123">Diese Eigenschaften können nicht festgelegt werden, wenn das Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="6d178-123">These properties cannot be set when the control is connected.</span></span>

<span data-ttu-id="6d178-124">Weitere Informationen finden Sie unter [Bereitstellen der RDP-Client Sicherheit](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="6d178-124">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="6d178-125">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6d178-125">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d178-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d178-126">Requirements</span></span>



| <span data-ttu-id="6d178-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d178-127">Requirement</span></span> | <span data-ttu-id="6d178-128">Wert</span><span class="sxs-lookup"><span data-stu-id="6d178-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d178-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d178-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6d178-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d178-130">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="6d178-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d178-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6d178-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d178-132">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="6d178-133">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6d178-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="6d178-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d178-134"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="6d178-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6d178-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d178-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d178-136"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="6d178-137">IID</span><span class="sxs-lookup"><span data-stu-id="6d178-137">IID</span></span><br/>                      | <span data-ttu-id="6d178-138">IID \_ imsrdpclientsecuredsettings ist als 605befcf-39c1-45cc-a811-068fb7be346d definiert.</span><span class="sxs-lookup"><span data-stu-id="6d178-138">IID\_IMsRdpClientSecuredSettings is defined as 605befcf-39c1-45cc-a811-068fb7be346d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6d178-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d178-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d178-140">**Imsrdpclientsecuredsettings**</span><span class="sxs-lookup"><span data-stu-id="6d178-140">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





