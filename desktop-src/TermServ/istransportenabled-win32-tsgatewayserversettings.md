---
title: Istransportenabled-Methode der Win32_TSGatewayServerSettings-Klasse
description: Bestimmt, ob der angegebene Transport aktiviert ist.
ms.assetid: 3f08a206-5800-4088-a113-bb3f0cc826f2
ms.tgt_platform: multiple
keywords:
- Istransportenabled-Methode Remotedesktopdienste
- Istransportenabled-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, istransportenabled-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsTransportEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da152499138f6c1aba1ff6477c719aa0e787deee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103522"
---
# <a name="istransportenabled-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="01d44-106">Istransportenabled-Methode der Win32-Klasse "t- \_ gatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="01d44-106">IsTransportEnabled method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="01d44-107">Bestimmt, ob der angegebene Transport aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="01d44-107">Determines whether the specified transport is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="01d44-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="01d44-108">Syntax</span></span>


```mof
uint32 IsTransportEnabled(
  [in]  uint16  TransportType,
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="01d44-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="01d44-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01d44-110">*TransportType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01d44-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01d44-111">Gibt den Transporttyp an.</span><span class="sxs-lookup"><span data-stu-id="01d44-111">Specifies the transport type.</span></span> <span data-ttu-id="01d44-112">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="01d44-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="01d44-113">0</span><span class="sxs-lookup"><span data-stu-id="01d44-113">0</span></span>
</dt> <dd>

<span data-ttu-id="01d44-114">RPC-über-HTTP-Transport.</span><span class="sxs-lookup"><span data-stu-id="01d44-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="01d44-115">1</span><span class="sxs-lookup"><span data-stu-id="01d44-115">1</span></span>
</dt> <dd>

<span data-ttu-id="01d44-116">HTTP-Transport.</span><span class="sxs-lookup"><span data-stu-id="01d44-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="01d44-117">2</span><span class="sxs-lookup"><span data-stu-id="01d44-117">2</span></span>
</dt> <dd>

<span data-ttu-id="01d44-118">UDP-Transport.</span><span class="sxs-lookup"><span data-stu-id="01d44-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="01d44-119">*Aktiviert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="01d44-119">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01d44-120">Ein **boolescher** Wert, der angibt, ob der Transport aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="01d44-120">A **boolean** value that indicates whether the transport is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01d44-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="01d44-121">Return value</span></span>

<span data-ttu-id="01d44-122">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="01d44-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="01d44-123">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="01d44-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="01d44-124">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="01d44-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01d44-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01d44-125">Requirements</span></span>



| <span data-ttu-id="01d44-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01d44-126">Requirement</span></span> | <span data-ttu-id="01d44-127">Wert</span><span class="sxs-lookup"><span data-stu-id="01d44-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="01d44-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="01d44-128">Minimum supported client</span></span><br/> | <span data-ttu-id="01d44-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="01d44-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="01d44-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="01d44-130">Minimum supported server</span></span><br/> | <span data-ttu-id="01d44-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="01d44-131">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="01d44-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="01d44-132">Namespace</span></span><br/>                | <span data-ttu-id="01d44-133">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="01d44-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="01d44-134">MOF</span><span class="sxs-lookup"><span data-stu-id="01d44-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01d44-135"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="01d44-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="01d44-136">DLL</span><span class="sxs-lookup"><span data-stu-id="01d44-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01d44-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01d44-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="01d44-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01d44-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01d44-139">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="01d44-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





