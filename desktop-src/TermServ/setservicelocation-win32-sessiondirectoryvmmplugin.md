---
title: Setservicelokation-Methode der Win32_SessionDirectoryVMMPlugin-Klasse
description: Legt den Dienst Speicherort für das Plug-in fest.
ms.assetid: e886a40b-9ea9-4159-a2ea-776160559410
ms.tgt_platform: multiple
keywords:
- Setservicelokation-Methode Remotedesktopdienste
- Setservicelokation-Methode Remotedesktopdienste, Win32_SessionDirectoryVMMPlugin-Klasse
- Win32_SessionDirectoryVMMPlugin-Klasse Remotedesktopdienste, setservicelokation-Methode
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetServiceLocation
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64c16a6bbe802052f53d28d4cd8cc2b9ab559b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518164"
---
# <a name="setservicelocation-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="0c2b3-106">Setservicelokation-Methode der Win32- \_ Klasse "sessiondirectoryvmmplugin"</span><span class="sxs-lookup"><span data-stu-id="0c2b3-106">SetServiceLocation method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="0c2b3-107">Legt den Dienst Speicherort für das Plug-in fest.</span><span class="sxs-lookup"><span data-stu-id="0c2b3-107">Sets the service location for the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c2b3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c2b3-108">Syntax</span></span>


```mof
uint32 SetServiceLocation(
  [in] string sServiceLocation
);
```



## <a name="parameters"></a><span data-ttu-id="0c2b3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c2b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c2b3-110">*sservicelokation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c2b3-110">*sServiceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c2b3-111">Der Dienst Speicherort, den das Plug-in kontaktieren soll.</span><span class="sxs-lookup"><span data-stu-id="0c2b3-111">The service location that the plug-in should contact.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c2b3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c2b3-112">Return value</span></span>

<span data-ttu-id="0c2b3-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0c2b3-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="0c2b3-114">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="0c2b3-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c2b3-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c2b3-115">Requirements</span></span>



| <span data-ttu-id="0c2b3-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c2b3-116">Requirement</span></span> | <span data-ttu-id="0c2b3-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0c2b3-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c2b3-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c2b3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0c2b3-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0c2b3-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0c2b3-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c2b3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0c2b3-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0c2b3-121">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="0c2b3-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="0c2b3-122">Namespace</span></span><br/>                | <span data-ttu-id="0c2b3-123">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0c2b3-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="0c2b3-124">MOF</span><span class="sxs-lookup"><span data-stu-id="0c2b3-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c2b3-125"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="0c2b3-125"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c2b3-126">DLL</span><span class="sxs-lookup"><span data-stu-id="0c2b3-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c2b3-127"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c2b3-127"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c2b3-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c2b3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c2b3-129">**Win32 \_ sessiondirector yvmmplugin**</span><span class="sxs-lookup"><span data-stu-id="0c2b3-129">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





