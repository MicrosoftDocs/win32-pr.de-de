---
title: Setsslbridging-Methode der Win32_TSGatewayServerSettings-Klasse
description: Legt den Typ des SSL-Bridging fest, der vom Remotedesktop Gateway-Server (RD-Gateway) verwendet werden soll.
ms.assetid: 11885b8b-491e-4d90-b4d4-f0a0fbe68cb1
ms.tgt_platform: multiple
keywords:
- Setsslbridging-Methode Remotedesktopdienste
- Setsslbridging-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, setsslbridging-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetSslBridging
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77181fb8d8661ec7ea7dc0ce70532281fb9c1bde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392016"
---
# <a name="setsslbridging-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="22b13-106">Setsslbridging-Methode der Win32-Klasse "t- \_ gatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="22b13-106">SetSslBridging method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="22b13-107">Legt den Typ des SSL-Bridging fest, der vom Remotedesktop Gateway-Server (RD-Gateway) verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="22b13-107">Sets the type of SSL bridging to be used by the Remote Desktop Gateway (RD Gateway) server.</span></span> <span data-ttu-id="22b13-108">Dieser Wert wird in der **sslbridging** -Eigenschaft gespeichert.</span><span class="sxs-lookup"><span data-stu-id="22b13-108">This value is stored in the **SslBridging** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="22b13-109">Wenn der SSL-Bridging-Typ mit dieser Methode geändert wird, muss der RD-Gateway-Dienst neu gestartet werden, damit diese Änderung wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="22b13-109">When the SSL bridging type is changed with this method, the RD Gateway service must be restarted to make this change take effect.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="22b13-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="22b13-110">Syntax</span></span>


```mof
uint32 SetSslBridging(
  [in] uint32 SslBridging
);
```



## <a name="parameters"></a><span data-ttu-id="22b13-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="22b13-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22b13-112">*Sslbridging* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22b13-112">*SslBridging* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22b13-113">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22b13-113">Type: **uint32**</span></span>

<span data-ttu-id="22b13-114">Gibt den neuen SSL-Überbrückungs Wert an.</span><span class="sxs-lookup"><span data-stu-id="22b13-114">Specifies the new SSL bridging value.</span></span> <span data-ttu-id="22b13-115">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="22b13-115">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="22b13-116">0</span><span class="sxs-lookup"><span data-stu-id="22b13-116">0</span></span>
</dt> <dd>

<span data-ttu-id="22b13-117">Keine SSL-Überbrückung.</span><span class="sxs-lookup"><span data-stu-id="22b13-117">No SSL bridging.</span></span>

</dd> <dt>

<span data-ttu-id="22b13-118">1</span><span class="sxs-lookup"><span data-stu-id="22b13-118">1</span></span>
</dt> <dd>

<span data-ttu-id="22b13-119">HTTPS-zu-HTTP-Bridging.</span><span class="sxs-lookup"><span data-stu-id="22b13-119">HTTPS to HTTP bridging.</span></span>

</dd> <dt>

<span data-ttu-id="22b13-120">2</span><span class="sxs-lookup"><span data-stu-id="22b13-120">2</span></span>
</dt> <dd>

<span data-ttu-id="22b13-121">HTTPS-zu-HTTPS-Bridging.</span><span class="sxs-lookup"><span data-stu-id="22b13-121">HTTPS to HTTPS bridging.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22b13-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22b13-122">Return value</span></span>

<span data-ttu-id="22b13-123">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22b13-123">Type: **uint32**</span></span>

<span data-ttu-id="22b13-124">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="22b13-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="22b13-125">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="22b13-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="22b13-126">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="22b13-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="22b13-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22b13-127">Remarks</span></span>

<span data-ttu-id="22b13-128">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="22b13-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="22b13-129">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="22b13-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="22b13-130">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="22b13-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="22b13-131">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="22b13-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="22b13-132">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="22b13-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="22b13-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22b13-133">Requirements</span></span>



| <span data-ttu-id="22b13-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22b13-134">Requirement</span></span> | <span data-ttu-id="22b13-135">Wert</span><span class="sxs-lookup"><span data-stu-id="22b13-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="22b13-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22b13-136">Minimum supported client</span></span><br/> | <span data-ttu-id="22b13-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="22b13-137">None supported</span></span><br/>                                                                |
| <span data-ttu-id="22b13-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22b13-138">Minimum supported server</span></span><br/> | <span data-ttu-id="22b13-139">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="22b13-139">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="22b13-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="22b13-140">Namespace</span></span><br/>                | <span data-ttu-id="22b13-141">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="22b13-141">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="22b13-142">MOF</span><span class="sxs-lookup"><span data-stu-id="22b13-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22b13-143"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="22b13-143"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="22b13-144">DLL</span><span class="sxs-lookup"><span data-stu-id="22b13-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22b13-145"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22b13-145"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="22b13-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22b13-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22b13-147">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="22b13-147">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

