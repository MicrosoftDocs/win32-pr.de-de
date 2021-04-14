---
title: Setmaxxresolution-Methode der Win32_TSClientSetting-Klasse
description: Legt die maxxresolution-Eigenschaft fest.
ms.assetid: c1e00bab-ab32-4cf6-8121-950184bd8a01
ms.tgt_platform: multiple
keywords:
- Setmaxxresolution-Methode Remotedesktopdienste
- Setmaxxresolution-Methode Remotedesktopdienste, Win32_TSClientSetting-Klasse
- Win32_TSClientSetting-Klasse Remotedesktopdienste, setmaxxresolution-Methode
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxXResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ab911fd66c7cf6b4f657d8f9e060eccee80675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476413"
---
# <a name="setmaxxresolution-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="bdc28-106">Setmaxxresolution-Methode der Win32- \_ Klasse tsclientsetting</span><span class="sxs-lookup"><span data-stu-id="bdc28-106">SetMaxXResolution method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="bdc28-107">Legt die **maxxresolution** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="bdc28-107">Sets the **MaxXResolution** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdc28-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdc28-108">Syntax</span></span>


```mof
uint32 SetMaxXResolution(
  [in] uint32 MaxXResolution
);
```



## <a name="parameters"></a><span data-ttu-id="bdc28-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdc28-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdc28-110">*Maxxresolution* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bdc28-110">*MaxXResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdc28-111">Die neue maximale X-Auflösung, die vom Server unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="bdc28-111">The new maximum X resolution supported by the server.</span></span> <span data-ttu-id="bdc28-112">Der Minimalwert ist 200 und der Höchstwert 4096.</span><span class="sxs-lookup"><span data-stu-id="bdc28-112">The minimum value is 200 and maximum value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdc28-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bdc28-113">Return value</span></span>

<span data-ttu-id="bdc28-114">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bdc28-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="bdc28-115">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="bdc28-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="bdc28-116">Die-Methode gibt einen Fehler zurück, wenn die Verbindungseinstellungen des Benutzers vom Server überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="bdc28-116">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdc28-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bdc28-117">Requirements</span></span>



| <span data-ttu-id="bdc28-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bdc28-118">Requirement</span></span> | <span data-ttu-id="bdc28-119">Wert</span><span class="sxs-lookup"><span data-stu-id="bdc28-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdc28-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bdc28-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bdc28-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bdc28-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="bdc28-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bdc28-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bdc28-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bdc28-123">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="bdc28-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="bdc28-124">Namespace</span></span><br/>                | <span data-ttu-id="bdc28-125">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="bdc28-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="bdc28-126">MOF</span><span class="sxs-lookup"><span data-stu-id="bdc28-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bdc28-127"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bdc28-127"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="bdc28-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bdc28-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdc28-129"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdc28-129"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdc28-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdc28-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdc28-131">**Win32- \_ tsclientsetting**</span><span class="sxs-lookup"><span data-stu-id="bdc28-131">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





