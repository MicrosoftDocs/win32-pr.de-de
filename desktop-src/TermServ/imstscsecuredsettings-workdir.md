---
title: Imstscsecuredsettings WorkDir-Eigenschaft
description: Gibt das Arbeitsverzeichnis des Start Programms an.
ms.assetid: e67f7274-be47-42c4-9267-a05bb93e6725
ms.tgt_platform: multiple
keywords:
- WORKDIR-Eigenschaft Remotedesktopdienste
- WORKDIR-Eigenschaft Remotedesktopdienste, imstscsecuredsettings-Schnittstelle
- Imstscsecuredsettings-Schnittstelle Remotedesktopdienste, WorkDir-Eigenschaft
- WORKDIR-Eigenschaft Remotedesktopdienste, imsrdpclientsecuredsettings-Schnittstelle
- Imsrdpclientsecuredsettings-Schnittstelle Remotedesktopdienste, WorkDir-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.WorkDir
- IMsTscSecuredSettings.get_WorkDir
- IMsTscSecuredSettings.put_WorkDir
- IMsRdpClientSecuredSettings.WorkDir
- IMsRdpClientSecuredSettings.get_WorkDir
- IMsRdpClientSecuredSettings.put_WorkDir
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0a80b35ba682012150b4277d800bc4a3582e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344507"
---
# <a name="imstscsecuredsettingsworkdir-property"></a><span data-ttu-id="a48d2-108">Imstscsecuredsettings:: WorkDir-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a48d2-108">IMsTscSecuredSettings::WorkDir property</span></span>

<span data-ttu-id="a48d2-109">Gibt das Arbeitsverzeichnis des Start Programms an.</span><span class="sxs-lookup"><span data-stu-id="a48d2-109">Specifies the working directory of the start program.</span></span>

<span data-ttu-id="a48d2-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a48d2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a48d2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a48d2-111">Syntax</span></span>


```C++
HRESULT put_WorkDir(
  [in]  BSTR newVal
);

HRESULT get_WorkDir(
  [out] BSTR *pWorkDir
);
```



## <a name="property-value"></a><span data-ttu-id="a48d2-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a48d2-112">Property value</span></span>

<span data-ttu-id="a48d2-113">Das neue Arbeitsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="a48d2-113">The new working directory.</span></span> <span data-ttu-id="a48d2-114">Die maximale Länge dieser Zeichenfolge beträgt **Max. \_ Pfad**-1 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a48d2-114">The maximum length of this string is **MAX\_PATH**-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a48d2-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a48d2-115">Error codes</span></span>

<span data-ttu-id="a48d2-116">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a48d2-116">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a48d2-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a48d2-117">Remarks</span></span>

<span data-ttu-id="a48d2-118">Weitere Informationen finden Sie unter [Bereitstellen der RDP-Client Sicherheit](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="a48d2-118">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="a48d2-119">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a48d2-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a48d2-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a48d2-120">Requirements</span></span>



| <span data-ttu-id="a48d2-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a48d2-121">Requirement</span></span> | <span data-ttu-id="a48d2-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a48d2-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a48d2-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a48d2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a48d2-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a48d2-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="a48d2-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a48d2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a48d2-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a48d2-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a48d2-127">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a48d2-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="a48d2-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a48d2-128"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="a48d2-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a48d2-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a48d2-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a48d2-130"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="a48d2-131">IID</span><span class="sxs-lookup"><span data-stu-id="a48d2-131">IID</span></span><br/>                      | <span data-ttu-id="a48d2-132">IID \_ imstscsecuredsettings ist als c9d65442-a0f9-45b2-8f73-d61d2db8cbb6 definiert.</span><span class="sxs-lookup"><span data-stu-id="a48d2-132">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a48d2-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a48d2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a48d2-134">**Imsrdpclientsecuredsettings**</span><span class="sxs-lookup"><span data-stu-id="a48d2-134">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="a48d2-135">**Imstscsecuredsettings**</span><span class="sxs-lookup"><span data-stu-id="a48d2-135">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





