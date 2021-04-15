---
title: Setportnumbers-Methode der Win32_TSGatewayResourceAuthorizationPolicy-Klasse
description: Legt die Portnummern fest, die über Remotedesktop Gateway (RD-Gateway) mit der Ressource verbunden werden können.
ms.assetid: f8237ec3-84dc-44f8-ad86-54c46be1fd03
ms.tgt_platform: multiple
keywords:
- Setportnumbers-Methode Remotedesktopdienste
- Setportnumbers-Methode Remotedesktopdienste, Win32_TSGatewayResourceAuthorizationPolicy-Klasse
- Win32_TSGatewayResourceAuthorizationPolicy-Klasse Remotedesktopdienste, setportnumbers-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetPortNumbers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b938435abab23e3ad27cf13dbe65e64b9ec859eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477721"
---
# <a name="setportnumbers-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="7bdcb-106">Setportnumbers-Methode der Win32-Klasse "t- \_ gatewayresourceauthorizationpolicy"</span><span class="sxs-lookup"><span data-stu-id="7bdcb-106">SetPortNumbers method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="7bdcb-107">Legt die Portnummern fest, die über Remotedesktop Gateway (RD-Gateway) mit der Ressource verbunden werden können.</span><span class="sxs-lookup"><span data-stu-id="7bdcb-107">Sets the port numbers that are allowed to connect to the resource through Remote Desktop Gateway (RD Gateway).</span></span>

## <a name="syntax"></a><span data-ttu-id="7bdcb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bdcb-108">Syntax</span></span>


```mof
uint32 SetPortNumbers(
  [in] string PortNumbers
);
```



## <a name="parameters"></a><span data-ttu-id="7bdcb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bdcb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bdcb-110">*Portnummern* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7bdcb-110">*PortNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bdcb-111">Liste von durch Semikolons getrennten Portnummern, die für diese Remotedesktop Ressourcen Autorisierungs Richtlinie (RD-RAP) zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="7bdcb-111">List of semicolon-separated port numbers that are allowed for this Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="7bdcb-112">Um eine beliebige Portnummer zuzulassen, legen Sie " \* " fest.</span><span class="sxs-lookup"><span data-stu-id="7bdcb-112">To allow any port number, set "\*".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bdcb-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7bdcb-113">Remarks</span></span>

<span data-ttu-id="7bdcb-114">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="7bdcb-114">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7bdcb-115">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="7bdcb-115">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7bdcb-116">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7bdcb-116">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7bdcb-117">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7bdcb-117">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7bdcb-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7bdcb-118">Requirements</span></span>



| <span data-ttu-id="7bdcb-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7bdcb-119">Requirement</span></span> | <span data-ttu-id="7bdcb-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7bdcb-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bdcb-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7bdcb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7bdcb-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7bdcb-122">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7bdcb-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7bdcb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7bdcb-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7bdcb-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="7bdcb-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="7bdcb-125">Namespace</span></span><br/>                | <span data-ttu-id="7bdcb-126">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="7bdcb-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="7bdcb-127">MOF</span><span class="sxs-lookup"><span data-stu-id="7bdcb-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7bdcb-128"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="7bdcb-128"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="7bdcb-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7bdcb-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bdcb-130"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bdcb-130"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="7bdcb-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bdcb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bdcb-132">**Win32- \_ faigatewayresourceauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="7bdcb-132">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

