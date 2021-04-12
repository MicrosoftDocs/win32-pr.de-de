---
description: Die wmireverttopolicyhelligkeit-Methode wird verwendet, um die Helligkeit auf die Richtlinien Einstellung zurückzusetzen. Diese Methode hat keine Auswirkung auf die als-Helligkeitseinstellungen.
ms.assetid: 9a520c3f-3563-4ef4-b397-14e487c8e8bb
title: Wmireverttopolicyhelligkeit-Methode der wmimonitorbrightnessmethods-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiRevertToPolicyBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 03e1ed74486c7a5a2f2c61dc858e715850ec516e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216520"
---
# <a name="wmireverttopolicybrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="56aec-104">Wmireverttopolicyhelligkeit-Methode der wmimonitorbrightnessmethods-Klasse</span><span class="sxs-lookup"><span data-stu-id="56aec-104">WmiRevertToPolicyBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="56aec-105">Die **wmireverttopolicyhelligkeit** -Methode wird verwendet, um die Helligkeit auf die Richtlinien Einstellung zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="56aec-105">The **WmiRevertToPolicyBrightness** method is used to revert the brightness to the policy setting.</span></span> <span data-ttu-id="56aec-106">Diese Methode hat keine Auswirkung auf die als-Helligkeitseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="56aec-106">This method has no effect on the ALS brightness settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="56aec-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="56aec-107">Syntax</span></span>


```mof
uint32 WmiRevertToPolicyBrightness();
```



## <a name="parameters"></a><span data-ttu-id="56aec-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="56aec-108">Parameters</span></span>

<span data-ttu-id="56aec-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="56aec-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="56aec-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56aec-110">Return value</span></span>

<span data-ttu-id="56aec-111">Gibt NULL (0) zurück, um den Erfolg anzugeben.</span><span class="sxs-lookup"><span data-stu-id="56aec-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="56aec-112">Jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="56aec-112">Any other number indicates an error.</span></span> <span data-ttu-id="56aec-113">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="56aec-113">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="56aec-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56aec-114">Requirements</span></span>



| <span data-ttu-id="56aec-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56aec-115">Requirement</span></span> | <span data-ttu-id="56aec-116">Wert</span><span class="sxs-lookup"><span data-stu-id="56aec-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56aec-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56aec-117">Minimum supported client</span></span><br/> | <span data-ttu-id="56aec-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56aec-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="56aec-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56aec-119">Minimum supported server</span></span><br/> | <span data-ttu-id="56aec-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56aec-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="56aec-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="56aec-121">Namespace</span></span><br/>                | <span data-ttu-id="56aec-122">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="56aec-122">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="56aec-123">MOF</span><span class="sxs-lookup"><span data-stu-id="56aec-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56aec-124"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="56aec-124"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="56aec-125">DLL</span><span class="sxs-lookup"><span data-stu-id="56aec-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56aec-126"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56aec-126"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56aec-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56aec-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56aec-128">**Wmimonitorbrightnessmethods**</span><span class="sxs-lookup"><span data-stu-id="56aec-128">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="56aec-129">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="56aec-129">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

