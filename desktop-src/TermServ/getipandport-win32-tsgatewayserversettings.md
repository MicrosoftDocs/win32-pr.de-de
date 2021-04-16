---
title: Getipandport-Methode der Win32_TSGatewayServerSettings-Klasse
description: Ruft die Abhör-IP-Adresse und die Portnummer für den angegebenen Transport ab.
ms.assetid: e12451c3-2641-49e1-bd35-f7cab37865ae
ms.tgt_platform: multiple
keywords:
- Getipandport-Methode Remotedesktopdienste
- Getipandport-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, getipandport-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260cc45961720ae8d175d4df3e84edc7a0c15c13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340458"
---
# <a name="getipandport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="db142-106">Getipandport-Methode der Win32-Klasse "t- \_ gatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="db142-106">GetIPAndPort method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="db142-107">Ruft die Abhör-IP-Adresse und die Portnummer für den angegebenen Transport ab.</span><span class="sxs-lookup"><span data-stu-id="db142-107">Obtains the listening IP address and port number for the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="db142-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="db142-108">Syntax</span></span>


```mof
uint32 GetIPAndPort(
  [in]  uint16 TransportType,
  [out] string IPAddress,
  [out] uint16 Port
);
```



## <a name="parameters"></a><span data-ttu-id="db142-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="db142-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db142-110">*TransportType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db142-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db142-111">Gibt den Transporttyp an.</span><span class="sxs-lookup"><span data-stu-id="db142-111">Specifies the transport type.</span></span> <span data-ttu-id="db142-112">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="db142-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="db142-113">0</span><span class="sxs-lookup"><span data-stu-id="db142-113">0</span></span>
</dt> <dd>

<span data-ttu-id="db142-114">RPC-über-HTTP-Transport.</span><span class="sxs-lookup"><span data-stu-id="db142-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="db142-115">1</span><span class="sxs-lookup"><span data-stu-id="db142-115">1</span></span>
</dt> <dd>

<span data-ttu-id="db142-116">HTTP-Transport.</span><span class="sxs-lookup"><span data-stu-id="db142-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="db142-117">2</span><span class="sxs-lookup"><span data-stu-id="db142-117">2</span></span>
</dt> <dd>

<span data-ttu-id="db142-118">UDP-Transport.</span><span class="sxs-lookup"><span data-stu-id="db142-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="db142-119">*IPAddress* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="db142-119">*IPAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db142-120">Eine Zeichenfolge, die die Abhör-IP-Adresse im Oktett-Format empfängt (z. b. "192.168.1.1").</span><span class="sxs-lookup"><span data-stu-id="db142-120">A string that receives the listening IP address, in octet form (for example, "192.168.1.1").</span></span>

</dd> <dt>

<span data-ttu-id="db142-121">*Port* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="db142-121">*Port* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db142-122">Gibt die Abhör Portnummer an.</span><span class="sxs-lookup"><span data-stu-id="db142-122">Specifies the listening port number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db142-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db142-123">Return value</span></span>

<span data-ttu-id="db142-124">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="db142-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="db142-125">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="db142-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="db142-126">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="db142-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="db142-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db142-127">Requirements</span></span>



| <span data-ttu-id="db142-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db142-128">Requirement</span></span> | <span data-ttu-id="db142-129">Wert</span><span class="sxs-lookup"><span data-stu-id="db142-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="db142-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db142-130">Minimum supported client</span></span><br/> | <span data-ttu-id="db142-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="db142-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="db142-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db142-132">Minimum supported server</span></span><br/> | <span data-ttu-id="db142-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="db142-133">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="db142-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="db142-134">Namespace</span></span><br/>                | <span data-ttu-id="db142-135">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="db142-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="db142-136">MOF</span><span class="sxs-lookup"><span data-stu-id="db142-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db142-137"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="db142-137"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="db142-138">DLL</span><span class="sxs-lookup"><span data-stu-id="db142-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db142-139"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db142-139"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="db142-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db142-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db142-141">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="db142-141">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





