---
title: Enabletransport-Methode der Win32_TSGatewayServerSettings-Klasse
description: Aktiviert oder deaktiviert den angegebenen Transport.
ms.assetid: 95c599d7-56c3-462a-9c7d-2ecf8fc55da1
ms.tgt_platform: multiple
keywords:
- Enabletransport-Methode Remotedesktopdienste
- Enabletransport-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, enabletransport-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableTransport
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a14e7ee94eb02e1358d66b9965ecc2323d5b773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342676"
---
# <a name="enabletransport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="4bc61-106">Enabletransport-Methode der Win32-Klasse "t- \_ gatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="4bc61-106">EnableTransport method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="4bc61-107">Aktiviert oder deaktiviert den angegebenen Transport.</span><span class="sxs-lookup"><span data-stu-id="4bc61-107">Enables or disables the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bc61-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bc61-108">Syntax</span></span>


```mof
uint32 EnableTransport(
  [in] uint16  TransportType,
  [in] boolean Enable
);
```



## <a name="parameters"></a><span data-ttu-id="4bc61-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bc61-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bc61-110">*TransportType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4bc61-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc61-111">Gibt den Transporttyp an.</span><span class="sxs-lookup"><span data-stu-id="4bc61-111">Specifies the transport type.</span></span> <span data-ttu-id="4bc61-112">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="4bc61-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="4bc61-113">0</span><span class="sxs-lookup"><span data-stu-id="4bc61-113">0</span></span>
</dt> <dd>

<span data-ttu-id="4bc61-114">RPC-über-HTTP-Transport.</span><span class="sxs-lookup"><span data-stu-id="4bc61-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="4bc61-115">1</span><span class="sxs-lookup"><span data-stu-id="4bc61-115">1</span></span>
</dt> <dd>

<span data-ttu-id="4bc61-116">HTTP-Transport.</span><span class="sxs-lookup"><span data-stu-id="4bc61-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="4bc61-117">2</span><span class="sxs-lookup"><span data-stu-id="4bc61-117">2</span></span>
</dt> <dd>

<span data-ttu-id="4bc61-118">UDP-Transport.</span><span class="sxs-lookup"><span data-stu-id="4bc61-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4bc61-119">*Aktivieren* \[ von in\]</span><span class="sxs-lookup"><span data-stu-id="4bc61-119">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc61-120">Gibt an, ob der Transport aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4bc61-120">Specifies if the transport is enabled or disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bc61-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4bc61-121">Return value</span></span>

<span data-ttu-id="4bc61-122">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="4bc61-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4bc61-123">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4bc61-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4bc61-124">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4bc61-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bc61-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4bc61-125">Requirements</span></span>



| <span data-ttu-id="4bc61-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4bc61-126">Requirement</span></span> | <span data-ttu-id="4bc61-127">Wert</span><span class="sxs-lookup"><span data-stu-id="4bc61-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bc61-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4bc61-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4bc61-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4bc61-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="4bc61-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4bc61-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4bc61-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4bc61-131">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="4bc61-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="4bc61-132">Namespace</span></span><br/>                | <span data-ttu-id="4bc61-133">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="4bc61-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="4bc61-134">MOF</span><span class="sxs-lookup"><span data-stu-id="4bc61-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4bc61-135"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="4bc61-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="4bc61-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4bc61-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bc61-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bc61-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="4bc61-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bc61-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bc61-139">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="4bc61-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





