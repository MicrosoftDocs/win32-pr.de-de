---
title: SetDescription-Methode der Win32_TSGatewayResourceGroup-Klasse
description: Legt die Description-Eigenschaft für die Ressourcengruppe fest.
ms.assetid: ab1280c7-ce53-4807-9537-953b597dd636
ms.tgt_platform: multiple
keywords:
- SetDescription-Methode Remotedesktopdienste
- SetDescription-Methode Remotedesktopdienste, Win32_TSGatewayResourceGroup-Klasse
- Win32_TSGatewayResourceGroup-Klasse Remotedesktopdienste, setDescription-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetDescription
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d815cc5400a182f2dff3b982643d5e6bfd861002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346533"
---
# <a name="setdescription-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="ad5f7-106">SetDescription-Methode der Win32-Klasse "t- \_ gatewayresourcegroup"</span><span class="sxs-lookup"><span data-stu-id="ad5f7-106">SetDescription method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="ad5f7-107">Legt die **Description** -Eigenschaft für die Ressourcengruppe fest.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-107">Sets the **Description** property for the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad5f7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad5f7-108">Syntax</span></span>


```mof
uint32 SetDescription(
  [in] string Description
);
```



## <a name="parameters"></a><span data-ttu-id="ad5f7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad5f7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad5f7-110">*Beschreibung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad5f7-110">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad5f7-111">Beschreibung der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-111">Description of the resource group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad5f7-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad5f7-112">Return value</span></span>

<span data-ttu-id="ad5f7-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ad5f7-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ad5f7-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ad5f7-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ad5f7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad5f7-116">Remarks</span></span>

<span data-ttu-id="ad5f7-117">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ad5f7-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ad5f7-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ad5f7-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ad5f7-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ad5f7-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ad5f7-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad5f7-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad5f7-122">Requirements</span></span>



| <span data-ttu-id="ad5f7-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad5f7-123">Requirement</span></span> | <span data-ttu-id="ad5f7-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ad5f7-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad5f7-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad5f7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ad5f7-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad5f7-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ad5f7-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad5f7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ad5f7-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad5f7-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ad5f7-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad5f7-129">Namespace</span></span><br/>                | <span data-ttu-id="ad5f7-130">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="ad5f7-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="ad5f7-131">MOF</span><span class="sxs-lookup"><span data-stu-id="ad5f7-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad5f7-132"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="ad5f7-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad5f7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ad5f7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad5f7-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad5f7-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ad5f7-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad5f7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad5f7-136">**Win32-Datei " \_ zgatewayresourcegroup"**</span><span class="sxs-lookup"><span data-stu-id="ad5f7-136">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

