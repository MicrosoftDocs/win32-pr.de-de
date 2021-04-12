---
title: IMsRdpClientAdvancedSettings6 enablekredsspsupport (Eigenschaft)
description: Gibt an, ob der Credential Security Service Provider (kredssp) für diese Verbindung aktiviert ist.
ms.assetid: 3BC8A265-7AEA-4C9C-9730-7710E1A3159D
ms.tgt_platform: multiple
keywords:
- Enablekredsspsupport-Eigenschaft Remotedesktopdienste
- Enablekredsspsupport-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, enablekredsspsupport (Eigenschaft)
- Enablekredsspsupport-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, enablekredsspsupport (Eigenschaft)
- Enablekredsspsupport-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, enablekredsspsupport (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.EnableCredSspSupport
- IMsRdpClientAdvancedSettings6.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings6.put_EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.put_EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.put_EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b73ad2b024cd0f8bbcafd6ba05be093c5953d54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517756"
---
# <a name="imsrdpclientadvancedsettings6enablecredsspsupport-property"></a><span data-ttu-id="bb6ad-110">IMsRdpClientAdvancedSettings6:: enablekredsspsupport (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bb6ad-110">IMsRdpClientAdvancedSettings6::EnableCredSspSupport property</span></span>

<span data-ttu-id="bb6ad-111">Gibt an, ob der Credential Security Service Provider (kredssp) für diese Verbindung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="bb6ad-111">Specifies whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span>

<span data-ttu-id="bb6ad-112">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="bb6ad-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb6ad-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb6ad-113">Syntax</span></span>


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a><span data-ttu-id="bb6ad-114">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="bb6ad-114">Property value</span></span>

<span data-ttu-id="bb6ad-115">Gibt an, ob "kredssp" für diese Verbindung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="bb6ad-115">Specifies whether CredSSP is enabled for this connection.</span></span> <span data-ttu-id="bb6ad-116">Legen Sie den Wert auf **Variant \_ true** fest, wenn Sie den Wert für "kredssp **" oder \_**</span><span class="sxs-lookup"><span data-stu-id="bb6ad-116">Set to **VARIANT\_TRUE** to enable CredSSP or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb6ad-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb6ad-117">Remarks</span></span>

<span data-ttu-id="bb6ad-118">Diese Eigenschaft wird nur von Remotedesktopverbindung 6,1-und 7,0-Clients unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bb6ad-118">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb6ad-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb6ad-119">Requirements</span></span>



| <span data-ttu-id="bb6ad-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb6ad-120">Requirement</span></span> | <span data-ttu-id="bb6ad-121">Wert</span><span class="sxs-lookup"><span data-stu-id="bb6ad-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb6ad-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb6ad-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bb6ad-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb6ad-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="bb6ad-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb6ad-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bb6ad-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb6ad-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="bb6ad-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="bb6ad-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="bb6ad-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb6ad-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="bb6ad-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bb6ad-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb6ad-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb6ad-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="bb6ad-130">IID</span><span class="sxs-lookup"><span data-stu-id="bb6ad-130">IID</span></span><br/>                      | <span data-ttu-id="bb6ad-131">IID \_ IMsRdpClientAdvancedSettings6 ist als 222c4b5d-45d9-4df0-a7c6-60cf9089d285 definiert.</span><span class="sxs-lookup"><span data-stu-id="bb6ad-131">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bb6ad-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb6ad-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb6ad-133">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="bb6ad-133">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="bb6ad-134">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="bb6ad-134">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="bb6ad-135">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="bb6ad-135">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





