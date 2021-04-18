---
title: Setmaxmonitors-Methode der Win32_TSClientSetting-Klasse
description: Legt die maxmonitors-Eigenschaft fest.
ms.assetid: 1c8266e1-ff2b-4fbc-af70-6f7b4499d88c
ms.tgt_platform: multiple
keywords:
- Setmaxmonitors-Methode Remotedesktopdienste
- Setmaxmonitors-Methode Remotedesktopdienste, Win32_TSClientSetting-Klasse
- Win32_TSClientSetting-Klasse Remotedesktopdienste, setmaxmonitors-Methode
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxMonitors
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76cdbe29079f5006cbf596751bef73cda1e94e52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338349"
---
# <a name="setmaxmonitors-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="67d8b-106">Setmaxmonitors-Methode der Win32- \_ Klasse tsclientsetting</span><span class="sxs-lookup"><span data-stu-id="67d8b-106">SetMaxMonitors method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="67d8b-107">Legt die **maxmonitors** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="67d8b-107">Sets the **MaxMonitors** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="67d8b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="67d8b-108">Syntax</span></span>


```mof
uint32 SetMaxMonitors(
  [in] uint32 MaxMonitors
);
```



## <a name="parameters"></a><span data-ttu-id="67d8b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="67d8b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67d8b-110">*Maxmonitors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67d8b-110">*MaxMonitors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67d8b-111">Gibt die neue maximale Anzahl von Monitoren an, die vom Server unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="67d8b-111">Specifies the new maximum number of monitors supported by the server.</span></span> <span data-ttu-id="67d8b-112">Der Minimalwert ist 1, und der Maximalwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="67d8b-112">The minimum value is 1 and the maximum value is 10.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67d8b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67d8b-113">Return value</span></span>

<span data-ttu-id="67d8b-114">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="67d8b-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="67d8b-115">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="67d8b-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="67d8b-116">Die-Methode gibt einen Fehler zurück, wenn die Verbindungseinstellungen des Benutzers vom Server überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="67d8b-116">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="67d8b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67d8b-117">Requirements</span></span>



| <span data-ttu-id="67d8b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67d8b-118">Requirement</span></span> | <span data-ttu-id="67d8b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="67d8b-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67d8b-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67d8b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="67d8b-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="67d8b-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="67d8b-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67d8b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="67d8b-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="67d8b-123">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="67d8b-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="67d8b-124">Namespace</span></span><br/>                | <span data-ttu-id="67d8b-125">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="67d8b-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="67d8b-126">MOF</span><span class="sxs-lookup"><span data-stu-id="67d8b-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67d8b-127"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="67d8b-127"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="67d8b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="67d8b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67d8b-129"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67d8b-129"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67d8b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67d8b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67d8b-131">**Win32- \_ tsclientsetting**</span><span class="sxs-lookup"><span data-stu-id="67d8b-131">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





