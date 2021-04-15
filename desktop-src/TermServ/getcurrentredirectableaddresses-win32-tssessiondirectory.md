---
title: Getcurrentredirectableadressen-Methode der Win32_TSSessionDirectory-Klasse
description: Ruft die derzeit konfigurierte Liste der für die Umleitung verfügbaren Adressen ab, die für die Umleitung verwendet werden können.
ms.assetid: 79f35d8f-b5f9-4b0f-bb7d-0d1ee3f02346
ms.tgt_platform: multiple
keywords:
- Getcurrentredirectableadressen-Methode Remotedesktopdienste
- Getcurrentredirectableadressen-Methode Remotedesktopdienste, Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste, getcurrentredirectableadressen-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetCurrentRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e6b4a859c77f449fb5a8f436be6e18c058ca59f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478894"
---
# <a name="getcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="3c8cb-106">Getcurrentredirectableadressen-Methode der Win32- \_ Klasse tssessiondirectory</span><span class="sxs-lookup"><span data-stu-id="3c8cb-106">GetCurrentRedirectableAddresses method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="3c8cb-107">Ruft die derzeit konfigurierte Liste der für die Umleitung verfügbaren Adressen ab, die für die Umleitung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3c8cb-107">Obtains the currently configured list of DNS eligible addresses that can be used for redirection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c8cb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c8cb-108">Syntax</span></span>


```mof
uint32 GetCurrentRedirectableAddresses(
  [out] uint32 fTokenRedirection,
  [out] string IPAddresses[]
);
```



## <a name="parameters"></a><span data-ttu-id="3c8cb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c8cb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c8cb-110">Kennzeichen *Umleitung* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3c8cb-110">*fTokenRedirection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c8cb-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c8cb-111">Type: **uint32**</span></span>

<span data-ttu-id="3c8cb-112">Ein Flag, das angibt, ob die Tokenumleitung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c8cb-112">A flag that indicates whether token redirection should be used.</span></span>

</dd> <dt>

<span data-ttu-id="3c8cb-113">*IP-Adressen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3c8cb-113">*IPAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c8cb-114">Typ: **Zeichen \[ \] Folge**</span><span class="sxs-lookup"><span data-stu-id="3c8cb-114">Type: **string\[\]**</span></span>

<span data-ttu-id="3c8cb-115">Ein Array der derzeit konfigurierten DNS-Adressen, die für die Umleitung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3c8cb-115">An array of the currently configured DNS eligible IP addresses that can be used for redirection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c8cb-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c8cb-116">Return value</span></span>

<span data-ttu-id="3c8cb-117">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c8cb-117">Type: **uint32**</span></span>

<span data-ttu-id="3c8cb-118">Gibt bei Erfolg 0 zurück. Andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3c8cb-118">Returns 0 on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="3c8cb-119">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="3c8cb-119">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c8cb-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c8cb-120">Remarks</span></span>

<span data-ttu-id="3c8cb-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="3c8cb-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3c8cb-122">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="3c8cb-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3c8cb-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3c8cb-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3c8cb-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3c8cb-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c8cb-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c8cb-125">Requirements</span></span>



| <span data-ttu-id="3c8cb-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c8cb-126">Requirement</span></span> | <span data-ttu-id="3c8cb-127">Wert</span><span class="sxs-lookup"><span data-stu-id="3c8cb-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c8cb-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c8cb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3c8cb-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3c8cb-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="3c8cb-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c8cb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3c8cb-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c8cb-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3c8cb-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="3c8cb-132">Namespace</span></span><br/>                | <span data-ttu-id="3c8cb-133">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3c8cb-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3c8cb-134">MOF</span><span class="sxs-lookup"><span data-stu-id="3c8cb-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c8cb-135"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3c8cb-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c8cb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3c8cb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c8cb-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c8cb-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c8cb-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c8cb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c8cb-139">**Win32- \_ tssessiondirectory**</span><span class="sxs-lookup"><span data-stu-id="3c8cb-139">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

