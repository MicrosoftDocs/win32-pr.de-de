---
title: Imsrdpclienttransportsettings (gatewayhostname-Eigenschaft)
description: Gibt den Hostnamen des Remotedesktop Gateway-Servers (RD-Gateway) an.
ms.assetid: 34c4b3b7-3768-4d98-b1e8-7fcb8f9c758d
ms.tgt_platform: multiple
keywords:
- Gatewayhostname-Eigenschaft Remotedesktopdienste
- Gatewayhostname-Eigenschaft Remotedesktopdienste, imsrdpclienttransportsettings-Schnittstelle
- Imsrdpclienttransportsettings-Schnittstelle Remotedesktopdienste, gatewayhostname-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayHostname
- IMsRdpClientTransportSettings.get_GatewayHostname
- IMsRdpClientTransportSettings.put_GatewayHostname
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03835faf48fa8aba557f82da158fdba827a84831
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340447"
---
# <a name="imsrdpclienttransportsettingsgatewayhostname-property"></a><span data-ttu-id="a3dee-106">Imsrdpclienttransportsettings:: gatewayhostname-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a3dee-106">IMsRdpClientTransportSettings::GatewayHostname property</span></span>

<span data-ttu-id="a3dee-107">Gibt den Hostnamen des Remotedesktop Gateway-Servers (RD-Gateway) an.</span><span class="sxs-lookup"><span data-stu-id="a3dee-107">Specifies the host name of the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="a3dee-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a3dee-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3dee-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3dee-109">Syntax</span></span>


```C++
HRESULT put_GatewayHostname(
  [in]  BSTR newVal
);

HRESULT get_GatewayHostname(
  [out] BSTR *pProxyHostname
);
```



## <a name="property-value"></a><span data-ttu-id="a3dee-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a3dee-110">Property value</span></span>

<span data-ttu-id="a3dee-111">Eine Zeichenfolge, die den RD-Gateway Server-Hostnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="a3dee-111">A string that contains the RD Gateway server host name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a3dee-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a3dee-112">Error codes</span></span>

<span data-ttu-id="a3dee-113">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a3dee-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3dee-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3dee-114">Requirements</span></span>



| <span data-ttu-id="a3dee-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3dee-115">Requirement</span></span> | <span data-ttu-id="a3dee-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a3dee-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3dee-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3dee-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a3dee-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3dee-118">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="a3dee-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3dee-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a3dee-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3dee-120">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="a3dee-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a3dee-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="a3dee-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3dee-122"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a3dee-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a3dee-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3dee-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3dee-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a3dee-125">IID</span><span class="sxs-lookup"><span data-stu-id="a3dee-125">IID</span></span><br/>                      | <span data-ttu-id="a3dee-126">IID \_ imsrdpclienttransportsettings ist definiert als 720298c0-A099-46f 5-9F 82-96921bae4701</span><span class="sxs-lookup"><span data-stu-id="a3dee-126">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a3dee-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3dee-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3dee-128">**Imsrdpclienttransportsettings**</span><span class="sxs-lookup"><span data-stu-id="a3dee-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





