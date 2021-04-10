---
title: IMsRdpClientAdvancedSettings6 AuthenticationType (Eigenschaft)
description: Gibt den für diese Verbindung verwendeten Authentifizierungstyp an.
ms.assetid: A6DAAE0A-5045-4C2C-B065-AB5BFB39F955
ms.tgt_platform: multiple
keywords:
- AuthenticationType-Eigenschaft Remotedesktopdienste
- AuthenticationType-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste, AuthenticationType-Eigenschaft
- AuthenticationType-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste, AuthenticationType-Eigenschaft
- AuthenticationType-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste, AuthenticationType-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationType
- IMsRdpClientAdvancedSettings6.get_AuthenticationType
- IMsRdpClientAdvancedSettings7.AuthenticationType
- IMsRdpClientAdvancedSettings7.get_AuthenticationType
- IMsRdpClientAdvancedSettings8.AuthenticationType
- IMsRdpClientAdvancedSettings8.get_AuthenticationType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c59239570538b690866e499ee942b6635055c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103689"
---
# <a name="imsrdpclientadvancedsettings6authenticationtype-property"></a><span data-ttu-id="e394f-110">IMsRdpClientAdvancedSettings6:: AuthenticationType (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e394f-110">IMsRdpClientAdvancedSettings6::AuthenticationType property</span></span>

<span data-ttu-id="e394f-111">Gibt den für diese Verbindung verwendeten Authentifizierungstyp an.</span><span class="sxs-lookup"><span data-stu-id="e394f-111">Specifies the type of authentication used for this connection.</span></span>

<span data-ttu-id="e394f-112">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e394f-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e394f-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="e394f-113">Syntax</span></span>


```C++
HRESULT get_AuthenticationType(
  [out] UINT *puiAuthType
);
```



## <a name="property-value"></a><span data-ttu-id="e394f-114">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e394f-114">Property value</span></span>

<span data-ttu-id="e394f-115">Empfängt einen-Wert, der den für diese Verbindung verwendeten Authentifizierungstyp angibt.</span><span class="sxs-lookup"><span data-stu-id="e394f-115">Receives a value that specifies the type of authentication used for this connection.</span></span> <span data-ttu-id="e394f-116">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="e394f-116">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="e394f-117">0</span><span class="sxs-lookup"><span data-stu-id="e394f-117">0</span></span>
</dt> <dd>

<span data-ttu-id="e394f-118">Es wird keine Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="e394f-118">No authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="e394f-119">1</span><span class="sxs-lookup"><span data-stu-id="e394f-119">1</span></span>
</dt> <dd>

<span data-ttu-id="e394f-120">Die Zertifikat Authentifizierung wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="e394f-120">Certificate authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="e394f-121">2</span><span class="sxs-lookup"><span data-stu-id="e394f-121">2</span></span>
</dt> <dd>

<span data-ttu-id="e394f-122">Die Kerberos-Authentifizierung wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="e394f-122">Kerberos authentication is used.</span></span>

</dd> <dt>

<span data-ttu-id="e394f-123">3</span><span class="sxs-lookup"><span data-stu-id="e394f-123">3</span></span>
</dt> <dd>

<span data-ttu-id="e394f-124">Sowohl das Zertifikat als auch die Kerberos-Authentifizierung werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="e394f-124">Both certificate and Kerberos authentication are used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e394f-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e394f-125">Requirements</span></span>



| <span data-ttu-id="e394f-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e394f-126">Requirement</span></span> | <span data-ttu-id="e394f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="e394f-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e394f-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e394f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e394f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e394f-129">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="e394f-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e394f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e394f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e394f-131">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="e394f-132">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="e394f-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="e394f-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e394f-133"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e394f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e394f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e394f-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e394f-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e394f-136">IID</span><span class="sxs-lookup"><span data-stu-id="e394f-136">IID</span></span><br/>                      | <span data-ttu-id="e394f-137">IID \_ IMsRdpClientAdvancedSettings6 ist als 222c4b5d-45d9-4df0-a7c6-60cf9089d285 definiert.</span><span class="sxs-lookup"><span data-stu-id="e394f-137">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e394f-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e394f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e394f-139">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e394f-139">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e394f-140">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e394f-140">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e394f-141">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e394f-141">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





