---
title: IMsRdpClientAdvancedSettings6 (Eigenschaft)
description: Gibt die Einstellung für die Vorverbindungs-BLOB (Festplatte) an, die vor der Verbindungs Herstellung mit dem Server verwendet werden soll. | IMsRdpClientAdvancedSettings6 (Eigenschaft)
ms.assetid: 3f3e6f09-2c26-44ab-9bcc-2636b71b57e2
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Platine-Eigenschaft
- Eigenschaften Remotedesktopdienste der Platine, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste, Eigenschaft ' PCB '
- Eigenschaften Remotedesktopdienste der Platine, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste, Eigenschaft ' PCB '
- Eigenschaften Remotedesktopdienste der Platine, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste, Eigenschaft ' PCB '
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.PCB
- IMsRdpClientAdvancedSettings6.get_PCB
- IMsRdpClientAdvancedSettings6.put_PCB
- IMsRdpClientAdvancedSettings7.PCB
- IMsRdpClientAdvancedSettings7.get_PCB
- IMsRdpClientAdvancedSettings7.put_PCB
- IMsRdpClientAdvancedSettings8.PCB
- IMsRdpClientAdvancedSettings8.get_PCB
- IMsRdpClientAdvancedSettings8.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da9cfa12ec944ea8f745ec3399c2a53f6b7c6b5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106371846"
---
# <a name="imsrdpclientadvancedsettings6pcb-property"></a><span data-ttu-id="db6ad-111">IMsRdpClientAdvancedSettings6::P CB-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="db6ad-111">IMsRdpClientAdvancedSettings6::PCB property</span></span>

<span data-ttu-id="db6ad-112">Gibt die Einstellung für die Vorverbindungs-BLOB (Festplatte) an, die vor der Verbindungs Herstellung mit dem Server verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="db6ad-112">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span>

<span data-ttu-id="db6ad-113">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="db6ad-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="db6ad-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="db6ad-114">Syntax</span></span>


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *pbstrPCB
);
```



## <a name="property-value"></a><span data-ttu-id="db6ad-115">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="db6ad-115">Property value</span></span>

<span data-ttu-id="db6ad-116">Gibt die BLOB-Einstellung an, die vor der Verbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="db6ad-116">Specifies the BLOB setting to use prior to connecting.</span></span>

## <a name="remarks"></a><span data-ttu-id="db6ad-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db6ad-117">Remarks</span></span>

<span data-ttu-id="db6ad-118">Diese Eigenschaft wird nur von Remotedesktopverbindung 6,1-und 7,0-Clients unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db6ad-118">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

<span data-ttu-id="db6ad-119">Der Server verwendet die BLOB-Einstellung, um den Ziel Prozess für die Verbindung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="db6ad-119">The server uses the BLOB setting to identify the target process for the connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="db6ad-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db6ad-120">Requirements</span></span>



| <span data-ttu-id="db6ad-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db6ad-121">Requirement</span></span> | <span data-ttu-id="db6ad-122">Wert</span><span class="sxs-lookup"><span data-stu-id="db6ad-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db6ad-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db6ad-123">Minimum supported client</span></span><br/> | <span data-ttu-id="db6ad-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="db6ad-124">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="db6ad-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db6ad-125">Minimum supported server</span></span><br/> | <span data-ttu-id="db6ad-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="db6ad-126">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="db6ad-127">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="db6ad-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="db6ad-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db6ad-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="db6ad-129">DLL</span><span class="sxs-lookup"><span data-stu-id="db6ad-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db6ad-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db6ad-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="db6ad-131">IID</span><span class="sxs-lookup"><span data-stu-id="db6ad-131">IID</span></span><br/>                      | <span data-ttu-id="db6ad-132">IID \_ IMsRdpClientAdvancedSettings6 ist als 222c4b5d-45d9-4df0-a7c6-60cf9089d285 definiert.</span><span class="sxs-lookup"><span data-stu-id="db6ad-132">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="db6ad-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db6ad-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db6ad-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="db6ad-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="db6ad-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="db6ad-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="db6ad-136">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="db6ad-136">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





