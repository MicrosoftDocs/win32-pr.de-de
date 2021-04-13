---
title: Die Methode "settenforcechannelbinding" der Win32_TSGatewayServerSettings-Klasse
description: Legt die enforcechannelbinding-Eigenschaft fest.
ms.assetid: 8bd64fe7-bad5-44e6-a309-10802d9a8bd4
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "settenforcechannelbinding"
- Die Methode "settenforcechannelbinding" Remotedesktopdienste, Win32_TSGatewayServerSettings Klasse
- Win32_TSGatewayServerSettings Klasse Remotedesktopdienste, Methode "settenforcechannelbinding"
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetEnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b236341f0fdac31f80f7e7d77aa12a4b22eb9731
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518026"
---
# <a name="setenforcechannelbinding-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="f18ec-106">Die Methode "settenforcechannelbinding" der Win32- \_ Klasse "tgatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="f18ec-106">SetEnforceChannelBinding method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="f18ec-107">Legt die **enforcechannelbinding** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="f18ec-107">Sets the **EnforceChannelBinding** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f18ec-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f18ec-108">Syntax</span></span>


```mof
uint32 SetEnforceChannelBinding(
  [in] boolean EnforceChannelBinding
);
```



## <a name="parameters"></a><span data-ttu-id="f18ec-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f18ec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f18ec-110">*Enforcechannelbinding* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f18ec-110">*EnforceChannelBinding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f18ec-111">Gibt den neuen **enforcechannelbinding** -Eigenschafts Wert an.</span><span class="sxs-lookup"><span data-stu-id="f18ec-111">Specifies the new **EnforceChannelBinding** property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f18ec-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f18ec-112">Return value</span></span>

<span data-ttu-id="f18ec-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="f18ec-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f18ec-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f18ec-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f18ec-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f18ec-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f18ec-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f18ec-116">Requirements</span></span>



| <span data-ttu-id="f18ec-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f18ec-117">Requirement</span></span> | <span data-ttu-id="f18ec-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f18ec-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f18ec-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f18ec-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f18ec-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f18ec-120">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f18ec-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f18ec-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f18ec-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f18ec-122">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="f18ec-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="f18ec-123">Namespace</span></span><br/>                | <span data-ttu-id="f18ec-124">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f18ec-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="f18ec-125">MOF</span><span class="sxs-lookup"><span data-stu-id="f18ec-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f18ec-126"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="f18ec-126"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="f18ec-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f18ec-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f18ec-128"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f18ec-128"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f18ec-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f18ec-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f18ec-130">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="f18ec-130">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





