---
title: SetEncryptionLevel-Methode der Win32_TSGeneralSetting-Klasse
description: Die setencryptionlevel-Methode legt die Verschlüsselungs Stufe fest.
ms.assetid: 1822c4dc-bce6-489f-b21e-f96faffd2fa5
ms.tgt_platform: multiple
keywords:
- Setencryptionlevel-Methode Remotedesktopdienste
- Setencryptionlevel-Methode Remotedesktopdienste, Win32_TSGeneralSetting-Klasse
- Win32_TSGeneralSetting-Klasse Remotedesktopdienste, setencryptionlevel-Methode
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetEncryptionLevel
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1fbe727c75851bb13252d196e1fe7d599f881c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104595"
---
# <a name="setencryptionlevel-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="10b86-106">Setencryptionlevel-Methode der Win32- \_ Klasse "zgeneralsetting"</span><span class="sxs-lookup"><span data-stu-id="10b86-106">SetEncryptionLevel method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="10b86-107">Die **setencryptionlevel** -Methode legt die Verschlüsselungs Stufe fest.</span><span class="sxs-lookup"><span data-stu-id="10b86-107">The **SetEncryptionLevel** method sets the encryption level.</span></span>

## <a name="syntax"></a><span data-ttu-id="10b86-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="10b86-108">Syntax</span></span>


```mof
uint32 SetEncryptionLevel(
  [in] uint32 MinEncryptionLevel
);
```



## <a name="parameters"></a><span data-ttu-id="10b86-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="10b86-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10b86-110">*Minverschlüsselungslevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10b86-110">*MinEncryptionLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10b86-111">Die minimale Verschlüsselungs Stufe, die festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="10b86-111">The minimum encryption level to set.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="10b86-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="10b86-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="10b86-113">Niedriger Verschlüsselungs Grad.</span><span class="sxs-lookup"><span data-stu-id="10b86-113">Low level of encryption.</span></span> <span data-ttu-id="10b86-114">Nur vom Client an den Server gesendete Daten werden mithilfe der 56-Bit-Verschlüsselung verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="10b86-114">Only data sent from the client to the server is encrypted using 56-bit encryption.</span></span> <span data-ttu-id="10b86-115">Beachten Sie, dass die vom Server an den Client gesendeten Daten nicht verschlüsselt sind.</span><span class="sxs-lookup"><span data-stu-id="10b86-115">Note that data sent from the server to the client is not encrypted.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="10b86-116"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="10b86-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="10b86-117">Client kompatibles Verschlüsselungs Niveau</span><span class="sxs-lookup"><span data-stu-id="10b86-117">Client-compatible level of encryption.</span></span> <span data-ttu-id="10b86-118">Alle Daten, die vom Client an den Server und vom Server an den Client gesendet werden, werden mit der maximalen Schlüssel Stärke verschlüsselt, die vom Client unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="10b86-118">All data sent from client to server and from server to client is encrypted at the maximum key strength supported by the client.</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="10b86-119"><span id="3"></span>**€**</span><span class="sxs-lookup"><span data-stu-id="10b86-119"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="10b86-120">Hohes Maß an Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="10b86-120">High level of encryption.</span></span> <span data-ttu-id="10b86-121">Alle Daten, die vom Client an den Server und vom Server an den Client gesendet werden, werden mit starker 128-Bit-Verschlüsselung verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="10b86-121">All data sent from client to server and from server to client is encrypted using strong 128-bit encryption.</span></span> <span data-ttu-id="10b86-122">Clients, die diese Verschlüsselungs Stufe nicht unterstützen, können keine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="10b86-122">Clients that do not support this level of encryption cannot connect.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="10b86-123"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="10b86-123"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="10b86-124">Mit der PPS-kompatible Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="10b86-124">FIPS-compliant encryption.</span></span> <span data-ttu-id="10b86-125">Alle Daten, die vom Client an den Server und vom Server an den Client gesendet werden, werden verschlüsselt und mit den Federal Information Processing Standard (FI)-Verschlüsselungsalgorithmen mithilfe der Kryptografiemodule von Microsoft entschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="10b86-125">All data sent from client to server and from server to client is encrypted and decrypted with the Federal Information Processing Standard (FIPS) encryption algorithms using the Microsoft cryptographic modules.</span></span> <span data-ttu-id="10b86-126">Der Standardwert für "Sicherheitsanforderungen für kryptografische Module" ist "Standard".</span><span class="sxs-lookup"><span data-stu-id="10b86-126">FIPS is a standard entitled "Security Requirements for Cryptographic Modules".</span></span> <span data-ttu-id="10b86-127">In den Informationen zu den in der US-Regierung verwendeten Hardware-und Softwaremodulen werden die behördlichen Anforderungen für Hardware-und Software Kryptografiemodule beschrieben. 2001 140-2 1994 140-1</span><span class="sxs-lookup"><span data-stu-id="10b86-127">FIPS 140-1 (1994) and FIPS 140-2 (2001) describe government requirements for hardware and software cryptographic modules used within the U.S. government.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10b86-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10b86-128">Return value</span></span>

<span data-ttu-id="10b86-129">Gibt bei Erfolg Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="10b86-129">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="10b86-130">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="10b86-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="10b86-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10b86-131">Remarks</span></span>

<span data-ttu-id="10b86-132">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="10b86-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="10b86-133">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="10b86-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="10b86-134">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="10b86-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="10b86-135">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="10b86-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="10b86-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10b86-136">Requirements</span></span>



| <span data-ttu-id="10b86-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10b86-137">Requirement</span></span> | <span data-ttu-id="10b86-138">Wert</span><span class="sxs-lookup"><span data-stu-id="10b86-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10b86-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10b86-139">Minimum supported client</span></span><br/> | <span data-ttu-id="10b86-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10b86-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10b86-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10b86-141">Minimum supported server</span></span><br/> | <span data-ttu-id="10b86-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10b86-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10b86-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="10b86-143">Namespace</span></span><br/>                | <span data-ttu-id="10b86-144">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="10b86-144">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="10b86-145">MOF</span><span class="sxs-lookup"><span data-stu-id="10b86-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10b86-146"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="10b86-146"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="10b86-147">DLL</span><span class="sxs-lookup"><span data-stu-id="10b86-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10b86-148"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10b86-148"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10b86-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10b86-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10b86-150">**Win32-Einstellung für "" \_**</span><span class="sxs-lookup"><span data-stu-id="10b86-150">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> </dl>

 

