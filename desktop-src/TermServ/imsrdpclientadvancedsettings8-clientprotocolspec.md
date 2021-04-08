---
title: IMsRdpClientAdvancedSettings8 clientprotocolspec (Eigenschaft)
description: Gibt das Remote Desktop Protokoll an, das zwischen dem Client und dem Server verwendet wird.
ms.assetid: DD607D54-CAEA-43EE-94EB-F983AEA0CC1E
ms.tgt_platform: multiple
keywords:
- Clientprotocolspec-Eigenschaft Remotedesktopdienste
- Clientprotocolspec-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, clientprotocolspec-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings8.ClientProtocolSpec
- IMsRdpClientAdvancedSettings8.get_ClientProtocolSpec
- IMsRdpClientAdvancedSettings8.put_ClientProtocolSpec
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41e603f7587435b3701ec0511587286e1a38bcc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949563"
---
# <a name="imsrdpclientadvancedsettings8clientprotocolspec-property"></a><span data-ttu-id="52c90-106">IMsRdpClientAdvancedSettings8:: clientprotocolspec (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="52c90-106">IMsRdpClientAdvancedSettings8::ClientProtocolSpec property</span></span>

<span data-ttu-id="52c90-107">Gibt das Remote Desktop Protokoll an, das zwischen dem Client und dem Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="52c90-107">Specifies the remote desktop protocol used between the client and the server.</span></span>

<span data-ttu-id="52c90-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="52c90-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="52c90-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="52c90-109">Syntax</span></span>


```C++
HRESULT put_ClientProtocolSpec(
  [in]  ClientSpec ClientMode
);

HRESULT get_ClientProtocolSpec(
  [out] ClientSpec *pClientMode
);
```



## <a name="property-value"></a><span data-ttu-id="52c90-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="52c90-110">Property value</span></span>

<span data-ttu-id="52c90-111">Ein Wert der [**clientspec**](clientspec.md) -Enumeration, der das Remote Desktop Protokoll angibt, das zwischen dem Client und dem Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="52c90-111">A value of the [**ClientSpec**](clientspec.md) enumeration that specifies the remote desktop protocol used between the client and the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="52c90-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52c90-112">Requirements</span></span>



| <span data-ttu-id="52c90-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52c90-113">Requirement</span></span> | <span data-ttu-id="52c90-114">Wert</span><span class="sxs-lookup"><span data-stu-id="52c90-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52c90-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52c90-115">Minimum supported client</span></span><br/> | <span data-ttu-id="52c90-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="52c90-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="52c90-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52c90-117">Minimum supported server</span></span><br/> | <span data-ttu-id="52c90-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="52c90-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="52c90-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="52c90-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="52c90-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52c90-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="52c90-121">DLL</span><span class="sxs-lookup"><span data-stu-id="52c90-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52c90-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52c90-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52c90-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52c90-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52c90-124">**Clientspec**</span><span class="sxs-lookup"><span data-stu-id="52c90-124">**ClientSpec**</span></span>](clientspec.md)
</dt> <dt>

[<span data-ttu-id="52c90-125">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="52c90-125">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





