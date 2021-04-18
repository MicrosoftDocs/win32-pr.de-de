---
title: Setmaxyresolution-Methode der Win32_TSClientSetting-Klasse
description: Legt die maxyresolution-Eigenschaft fest.
ms.assetid: a8399c7c-6b3a-464f-8112-8838257ccf06
ms.tgt_platform: multiple
keywords:
- Setmaxyresolution-Methode Remotedesktopdienste
- Setmaxyresolution-Methode Remotedesktopdienste, Win32_TSClientSetting-Klasse
- Win32_TSClientSetting-Klasse Remotedesktopdienste, setmaxyresolution-Methode
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxYResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c85564e075865d993552e831869979fc6227af29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337330"
---
# <a name="setmaxyresolution-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="24bf2-106">Setmaxyresolution-Methode der Win32- \_ Klasse tsclientsetting</span><span class="sxs-lookup"><span data-stu-id="24bf2-106">SetMaxYResolution method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="24bf2-107">Legt die **maxyresolution** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="24bf2-107">Sets the **MaxYResolution** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="24bf2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="24bf2-108">Syntax</span></span>


```mof
uint32 SetMaxYResolution(
  [in] uint32 MaxYResolution
);
```



## <a name="parameters"></a><span data-ttu-id="24bf2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="24bf2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24bf2-110">*Maxyresolution* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24bf2-110">*MaxYResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24bf2-111">Die neue maximale Y-Auflösung, die vom Server unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="24bf2-111">The new maximum Y resolution supported by the server.</span></span> <span data-ttu-id="24bf2-112">Der Minimalwert ist 200 und der Höchstwert 2048.</span><span class="sxs-lookup"><span data-stu-id="24bf2-112">The minimum value is 200 and the maximum value is 2048.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24bf2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24bf2-113">Return value</span></span>

<span data-ttu-id="24bf2-114">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="24bf2-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="24bf2-115">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="24bf2-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="24bf2-116">Die-Methode gibt einen Fehler zurück, wenn die Verbindungseinstellungen des Benutzers vom Server überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="24bf2-116">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="24bf2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24bf2-117">Requirements</span></span>



| <span data-ttu-id="24bf2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24bf2-118">Requirement</span></span> | <span data-ttu-id="24bf2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="24bf2-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24bf2-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="24bf2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="24bf2-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="24bf2-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="24bf2-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="24bf2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="24bf2-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="24bf2-123">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="24bf2-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="24bf2-124">Namespace</span></span><br/>                | <span data-ttu-id="24bf2-125">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="24bf2-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="24bf2-126">MOF</span><span class="sxs-lookup"><span data-stu-id="24bf2-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24bf2-127"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="24bf2-127"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="24bf2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="24bf2-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24bf2-129"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24bf2-129"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24bf2-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24bf2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24bf2-131">**Win32- \_ tsclientsetting**</span><span class="sxs-lookup"><span data-stu-id="24bf2-131">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





