---
title: Imsrdpclientadvancedsettings TransportType-Eigenschaft
description: Gibt den Transporttyp an, der vom Client verwendet wird.
ms.assetid: 752f5fbc-eb5a-48eb-8750-fc25c8a2f024
ms.tgt_platform: multiple
keywords:
- TransportType-Eigenschaft Remotedesktopdienste
- TransportType-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, TransportType-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.TransportType
- IMsRdpClientAdvancedSettings.get_TransportType
- IMsRdpClientAdvancedSettings.put_TransportType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0664e0c792725dc112baf786d63c5175eb450dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340763"
---
# <a name="imsrdpclientadvancedsettingstransporttype-property"></a><span data-ttu-id="68dc9-106">Imsrdpclientadvancedsettings:: TransportType-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="68dc9-106">IMsRdpClientAdvancedSettings::TransportType property</span></span>

<span data-ttu-id="68dc9-107">Gibt den Transporttyp an, der vom Client verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="68dc9-107">Specifies the transport type used by the client.</span></span> <span data-ttu-id="68dc9-108">Diese Eigenschaft wird vom Remotedesktop ActiveX-Steuerelement nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="68dc9-108">This property is not used by the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="68dc9-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="68dc9-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="68dc9-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="68dc9-110">Syntax</span></span>


```C++
HRESULT put_TransportType(
  [in]  LONG transportType
);

HRESULT get_TransportType(
  [out] LONG *ptransportType
);
```



## <a name="property-value"></a><span data-ttu-id="68dc9-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="68dc9-111">Property value</span></span>

<span data-ttu-id="68dc9-112">Legt den Transporttyp fest.</span><span class="sxs-lookup"><span data-stu-id="68dc9-112">Sets the transport type.</span></span> <span data-ttu-id="68dc9-113">Diese Methode kann erfolgreich ausgeführt werden, aber der festgelegte Wert wird nie vom Remotedesktop ActiveX-Steuerelement verwendet.</span><span class="sxs-lookup"><span data-stu-id="68dc9-113">This method may succeed, but the value set is never used by the Remote Desktop ActiveX control.</span></span>

## <a name="remarks"></a><span data-ttu-id="68dc9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68dc9-114">Remarks</span></span>

<span data-ttu-id="68dc9-115">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="68dc9-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68dc9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68dc9-116">Requirements</span></span>



| <span data-ttu-id="68dc9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68dc9-117">Requirement</span></span> | <span data-ttu-id="68dc9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="68dc9-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68dc9-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68dc9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="68dc9-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68dc9-120">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="68dc9-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68dc9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="68dc9-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68dc9-122">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="68dc9-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="68dc9-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="68dc9-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68dc9-124"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="68dc9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="68dc9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68dc9-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68dc9-126"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="68dc9-127">IID</span><span class="sxs-lookup"><span data-stu-id="68dc9-127">IID</span></span><br/>                      | <span data-ttu-id="68dc9-128">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="68dc9-128">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="68dc9-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68dc9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68dc9-130">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="68dc9-130">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





