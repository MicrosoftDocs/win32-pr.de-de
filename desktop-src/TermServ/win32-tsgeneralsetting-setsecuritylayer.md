---
title: Setsecuritylayer-Methode der Win32_TSGeneralSetting-Klasse
description: Die setsecuritylayer-Methode legt die Sicherheitsebene fest.
ms.assetid: 3b894494-2180-4f1d-8e67-a66c679d286c
ms.tgt_platform: multiple
keywords:
- Setsecuritylayer-Methode Remotedesktopdienste
- Setsecuritylayer-Methode Remotedesktopdienste, Win32_TSGeneralSetting-Klasse
- Win32_TSGeneralSetting-Klasse Remotedesktopdienste, setsecuritylayer-Methode
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetSecurityLayer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5e04c3f7e5a58ec8de345d570e36b35c7eb1e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956567"
---
# <a name="setsecuritylayer-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="f71e2-106">Setsecuritylayer-Methode der Win32- \_ Klasse "zgeneralsetting"</span><span class="sxs-lookup"><span data-stu-id="f71e2-106">SetSecurityLayer method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="f71e2-107">Die **setsecuritylayer** -Methode legt die Sicherheitsebene fest.</span><span class="sxs-lookup"><span data-stu-id="f71e2-107">The **SetSecurityLayer** method sets the security layer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f71e2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f71e2-108">Syntax</span></span>


```mof
uint32 SetSecurityLayer(
  [in] uint32 SecurityLayer
);
```



## <a name="parameters"></a><span data-ttu-id="f71e2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f71e2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f71e2-110">*Securitylayer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f71e2-110">*SecurityLayer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f71e2-111">Die festzulegende Sicherheitsebene.</span><span class="sxs-lookup"><span data-stu-id="f71e2-111">The security layer to set.</span></span> <span data-ttu-id="f71e2-112">Wenn die aktuelle Verschlüsselungs Stufe 1 ist, ist der Wert 2 für *securitylayer* ungültig.</span><span class="sxs-lookup"><span data-stu-id="f71e2-112">If the current Encryption Level is 1, then a value of 2 for *SecurityLayer* is not valid.</span></span>

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span data-ttu-id="f71e2-113"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP-Sicherheitsebene** (0)</span><span class="sxs-lookup"><span data-stu-id="f71e2-113"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP Security Layer** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f71e2-114">Bei der Kommunikation zwischen dem Server und dem Client wird die Native RDP-Verschlüsselung verwendet.</span><span class="sxs-lookup"><span data-stu-id="f71e2-114">Communication between the server and the client will use native RDP encryption.</span></span>

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="f71e2-115"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Aushandeln** (1)</span><span class="sxs-lookup"><span data-stu-id="f71e2-115"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f71e2-116">Die sicherste Ebene, die vom Client unterstützt wird, wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="f71e2-116">The most secure layer that is supported by the client will be used.</span></span> <span data-ttu-id="f71e2-117">Wenn unterstützt, wird SSL (TLS 1,0) verwendet.</span><span class="sxs-lookup"><span data-stu-id="f71e2-117">If supported, SSL (TLS 1.0) will be used.</span></span>

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span data-ttu-id="f71e2-118"><span id="SSL"></span><span id="ssl"></span>**SSL** (2)</span><span class="sxs-lookup"><span data-stu-id="f71e2-118"><span id="SSL"></span><span id="ssl"></span>**SSL** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f71e2-119">SSL (TLS 1,0) wird für die Server Authentifizierung sowie für die Verschlüsselung aller Daten verwendet, die zwischen dem Server und dem Client übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="f71e2-119">SSL (TLS 1.0) will be used for server authentication as well as for encrypting all data transferred between the server and the client.</span></span> <span data-ttu-id="f71e2-120">Diese Einstellung erfordert, dass der Server über ein SSL-kompatibles Zertifikat verfügt.</span><span class="sxs-lookup"><span data-stu-id="f71e2-120">This setting requires the server to have an SSL compatible certificate.</span></span> <span data-ttu-id="f71e2-121">Diese Einstellung ist nicht kompatibel mit dem **minverschlüsseltionlevel** -Wert 1.</span><span class="sxs-lookup"><span data-stu-id="f71e2-121">This setting is not compatible with a **MinEncryptionLevel** value of 1.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f71e2-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f71e2-122">Return value</span></span>

<span data-ttu-id="f71e2-123">Gibt bei Erfolg Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f71e2-123">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f71e2-124">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="f71e2-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f71e2-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f71e2-125">Remarks</span></span>

<span data-ttu-id="f71e2-126">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="f71e2-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f71e2-127">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="f71e2-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f71e2-128">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f71e2-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f71e2-129">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f71e2-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f71e2-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f71e2-130">Requirements</span></span>



| <span data-ttu-id="f71e2-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f71e2-131">Requirement</span></span> | <span data-ttu-id="f71e2-132">Wert</span><span class="sxs-lookup"><span data-stu-id="f71e2-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f71e2-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f71e2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f71e2-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f71e2-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f71e2-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f71e2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f71e2-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f71e2-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f71e2-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="f71e2-137">Namespace</span></span><br/>                | <span data-ttu-id="f71e2-138">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f71e2-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f71e2-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f71e2-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f71e2-140"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f71e2-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f71e2-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f71e2-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f71e2-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f71e2-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f71e2-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f71e2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f71e2-144">**Win32-Einstellung für "" \_**</span><span class="sxs-lookup"><span data-stu-id="f71e2-144">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> <dt>

[<span data-ttu-id="f71e2-145">**Setencryptionlevel**</span><span class="sxs-lookup"><span data-stu-id="f71e2-145">**SetEncryptionLevel**</span></span>](win32-tsgeneralsetting-setencryptionlevel.md)
</dt> </dl>

 

