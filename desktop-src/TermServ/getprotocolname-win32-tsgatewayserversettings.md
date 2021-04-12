---
title: Getprotocolname-Methode der Win32_TSGatewayServerSettings-Klasse
description: Gibt den Protokollnamen für den angegebenen Protokoll Index zurück.
ms.assetid: 6778cede-cc61-4e5d-9a29-ba88197fa8c6
ms.tgt_platform: multiple
keywords:
- Getprotocolname-Methode Remotedesktopdienste
- Getprotocolname-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, getprotocolname-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetProtocolName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81064581b209f047ac492faee6d442b082d038cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104331"
---
# <a name="getprotocolname-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="9a0d9-106">Getprotocolname-Methode der Win32- \_ Klasse "tgatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="9a0d9-106">GetProtocolName method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="9a0d9-107">Gibt den Protokollnamen für den angegebenen Protokoll Index zurück.</span><span class="sxs-lookup"><span data-stu-id="9a0d9-107">Returns the protocol name for the specified protocol index.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a0d9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a0d9-108">Syntax</span></span>


```mof
uint32 GetProtocolName(
  [in]  uint32 ProtocolId,
  [out] string ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="9a0d9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a0d9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a0d9-110">*Protokolid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a0d9-110">*ProtocolId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a0d9-111">Der Index des Protokoll Bezeichners.</span><span class="sxs-lookup"><span data-stu-id="9a0d9-111">Index of the protocol identifier.</span></span> <span data-ttu-id="9a0d9-112">Der Wert muss zwischen 0 (null) und dem Wert der **maxprotokolls** -Eigenschaft liegen.</span><span class="sxs-lookup"><span data-stu-id="9a0d9-112">The value must be between zero and the value of the **MaxProtocols** property.</span></span>

</dd> <dt>

<span data-ttu-id="9a0d9-113">*ProtocolName* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9a0d9-113">*ProtocolName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a0d9-114">Gibt den Namen des angegebenen Protokolls zurück.</span><span class="sxs-lookup"><span data-stu-id="9a0d9-114">Returns the name of the specified protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a0d9-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a0d9-115">Return value</span></span>

<span data-ttu-id="9a0d9-116">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="9a0d9-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9a0d9-117">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9a0d9-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9a0d9-118">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9a0d9-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9a0d9-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a0d9-119">Remarks</span></span>

<span data-ttu-id="9a0d9-120">Ein Protokoll wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9a0d9-120">One protocol is supported.</span></span>

<span data-ttu-id="9a0d9-121">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="9a0d9-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="9a0d9-122">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="9a0d9-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9a0d9-123">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="9a0d9-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9a0d9-124">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9a0d9-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9a0d9-125">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9a0d9-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a0d9-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a0d9-126">Requirements</span></span>



| <span data-ttu-id="9a0d9-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a0d9-127">Requirement</span></span> | <span data-ttu-id="9a0d9-128">Wert</span><span class="sxs-lookup"><span data-stu-id="9a0d9-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a0d9-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a0d9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9a0d9-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9a0d9-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9a0d9-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a0d9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9a0d9-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a0d9-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9a0d9-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="9a0d9-133">Namespace</span></span><br/>                | <span data-ttu-id="9a0d9-134">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9a0d9-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="9a0d9-135">MOF</span><span class="sxs-lookup"><span data-stu-id="9a0d9-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a0d9-136"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="9a0d9-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a0d9-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9a0d9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a0d9-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a0d9-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9a0d9-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a0d9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a0d9-140">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="9a0d9-140">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

