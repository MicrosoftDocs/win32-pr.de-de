---
title: Die Methode "stipandport" der Win32_TSGatewayServerSettings-Klasse
description: Legt die Abhör-IP-Adresse und die Portnummer für den angegebenen Transport fest.
ms.assetid: f46f4660-31ce-4513-b93d-acd50b42ae0a
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "
- Remotedesktopdienste der Methode "" der Klasse "Win32_TSGatewayServerSettings"
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, Methode "".
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88870cce628a94ca34b38ccf315edc87a1a734b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517687"
---
# <a name="setipandport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="13e5e-106">Die Methode "stipandport" der Win32-Klasse "- \_ gatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="13e5e-106">SetIPAndPort method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="13e5e-107">Legt die Abhör-IP-Adresse und die Portnummer für den angegebenen Transport fest.</span><span class="sxs-lookup"><span data-stu-id="13e5e-107">Sets the listening IP address and port number for the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="13e5e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="13e5e-108">Syntax</span></span>


```mof
uint32 SetIPAndPort(
  [in] uint16  TransportType,
  [in] string  IPAddress,
  [in] uint16  Port,
  [in] boolean OverrideExisting
);
```



## <a name="parameters"></a><span data-ttu-id="13e5e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="13e5e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13e5e-110">*TransportType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13e5e-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13e5e-111">Gibt den Transporttyp an.</span><span class="sxs-lookup"><span data-stu-id="13e5e-111">Specifies the transport type.</span></span> <span data-ttu-id="13e5e-112">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="13e5e-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="13e5e-113">0</span><span class="sxs-lookup"><span data-stu-id="13e5e-113">0</span></span>
</dt> <dd>

<span data-ttu-id="13e5e-114">RPC-über-HTTP-Transport.</span><span class="sxs-lookup"><span data-stu-id="13e5e-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="13e5e-115">1</span><span class="sxs-lookup"><span data-stu-id="13e5e-115">1</span></span>
</dt> <dd>

<span data-ttu-id="13e5e-116">HTTP-Transport.</span><span class="sxs-lookup"><span data-stu-id="13e5e-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="13e5e-117">2</span><span class="sxs-lookup"><span data-stu-id="13e5e-117">2</span></span>
</dt> <dd>

<span data-ttu-id="13e5e-118">UDP-Transport.</span><span class="sxs-lookup"><span data-stu-id="13e5e-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="13e5e-119">*IPAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13e5e-119">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13e5e-120">Gibt die Abhör-IP-Adresse im Oktett-Format an (z. b. "192.168.1.1").</span><span class="sxs-lookup"><span data-stu-id="13e5e-120">Specifies the listening IP address, in octet form (for example, "192.168.1.1").</span></span>

</dd> <dt>

<span data-ttu-id="13e5e-121">*Port* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13e5e-121">*Port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13e5e-122">Gibt die Abhör Portnummer an.</span><span class="sxs-lookup"><span data-stu-id="13e5e-122">Specifies the listening port number.</span></span>

</dd> <dt>

<span data-ttu-id="13e5e-123">*Überschrieben* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13e5e-123">*OverrideExisting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13e5e-124">Gibt an, ob die vorhandene IP/Port-Bindung für http überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="13e5e-124">Indicates whether to override the existing IP/Port binding for HTTP.</span></span> <span data-ttu-id="13e5e-125">Dieser Parameter wird nur verwendet, wenn der *Transport Type* -Parameter 0 (RPC über HTTP) oder 1 (http) enthält.</span><span class="sxs-lookup"><span data-stu-id="13e5e-125">This parameter is only used if the *TransportType* parameter contains 0 (RPC over HTTP) or 1 (HTTP).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13e5e-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13e5e-126">Return value</span></span>

<span data-ttu-id="13e5e-127">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="13e5e-127">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="13e5e-128">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13e5e-128">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="13e5e-129">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="13e5e-129">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="13e5e-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13e5e-130">Requirements</span></span>



| <span data-ttu-id="13e5e-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13e5e-131">Requirement</span></span> | <span data-ttu-id="13e5e-132">Wert</span><span class="sxs-lookup"><span data-stu-id="13e5e-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="13e5e-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13e5e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="13e5e-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="13e5e-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="13e5e-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13e5e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="13e5e-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="13e5e-136">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="13e5e-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="13e5e-137">Namespace</span></span><br/>                | <span data-ttu-id="13e5e-138">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="13e5e-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="13e5e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="13e5e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13e5e-140"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="13e5e-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="13e5e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="13e5e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13e5e-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13e5e-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="13e5e-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13e5e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13e5e-144">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="13e5e-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





