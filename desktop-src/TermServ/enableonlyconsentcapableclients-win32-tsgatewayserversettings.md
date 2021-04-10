---
title: Enableonlygenehmicapableclients-Methode der Win32_TSGatewayServerSettings-Klasse
description: Legt die onlygenehmicapableclients-Eigenschaft fest.
ms.assetid: abc91ea8-0f3c-4b7c-9091-3c8193e610da
ms.tgt_platform: multiple
keywords:
- Enableonlygenehmicapableclients-Methode Remotedesktopdienste
- Enableonlygenehmicapableclients-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, enableonlygenehmicapableclients-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableOnlyConsentCapableClients
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb671ccefe98cdc1b569bcde155071ef7cc0d9ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040334"
---
# <a name="enableonlyconsentcapableclients-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="89d8a-106">Enableonlygenehmicapableclients-Methode der Win32-Klasse "t- \_ gatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="89d8a-106">EnableOnlyConsentCapableClients method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="89d8a-107">Legt die **onlygenehmicapableclients** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="89d8a-107">Sets the **OnlyConsentCapableClients** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="89d8a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="89d8a-108">Syntax</span></span>


```mof
uint32 EnableOnlyConsentCapableClients(
  [in] boolean OnlyConsentCapableClients
);
```



## <a name="parameters"></a><span data-ttu-id="89d8a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="89d8a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89d8a-110">*Onlygenehmicapableclients* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89d8a-110">*OnlyConsentCapableClients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89d8a-111">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="89d8a-111">Type: **boolean**</span></span>

<span data-ttu-id="89d8a-112">Gibt den neuen Wert für die **onlygenehmicapableclients** -Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="89d8a-112">Specifies the new value for the **OnlyConsentCapableClients** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89d8a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89d8a-113">Return value</span></span>

<span data-ttu-id="89d8a-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="89d8a-114">Type: **uint32**</span></span>

<span data-ttu-id="89d8a-115">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="89d8a-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="89d8a-116">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="89d8a-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="89d8a-117">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="89d8a-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="89d8a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89d8a-118">Remarks</span></span>

<span data-ttu-id="89d8a-119">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="89d8a-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="89d8a-120">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="89d8a-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="89d8a-121">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="89d8a-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="89d8a-122">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="89d8a-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="89d8a-123">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="89d8a-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="89d8a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89d8a-124">Requirements</span></span>



| <span data-ttu-id="89d8a-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89d8a-125">Requirement</span></span> | <span data-ttu-id="89d8a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="89d8a-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="89d8a-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="89d8a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="89d8a-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="89d8a-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="89d8a-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="89d8a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="89d8a-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="89d8a-130">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="89d8a-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="89d8a-131">Namespace</span></span><br/>                | <span data-ttu-id="89d8a-132">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="89d8a-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="89d8a-133">MOF</span><span class="sxs-lookup"><span data-stu-id="89d8a-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89d8a-134"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="89d8a-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="89d8a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="89d8a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89d8a-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89d8a-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="89d8a-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89d8a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89d8a-138">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="89d8a-138">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

