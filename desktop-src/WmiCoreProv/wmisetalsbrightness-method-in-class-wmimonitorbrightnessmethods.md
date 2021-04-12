---
description: Wird verwendet, um den Umgebungs Wert des Umgebungslicht Sensors festzulegen.
ms.assetid: 8b3ec692-4043-42b3-8dd6-7a147620e382
title: Wmisegtalsbrightness-Methode der wmimonitorbrightnessmethods-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 0768917f9197b6ee3de52877e031acbbdc8f9aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218659"
---
# <a name="wmisetalsbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="bb991-103">Wmisegtalsbrightness-Methode der wmimonitorbrightnessmethods-Klasse</span><span class="sxs-lookup"><span data-stu-id="bb991-103">WmiSetALSBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="bb991-104">Die **wmisetalsbrightness** -Methode wird verwendet, um den Helligkeit-Wert des Umgebungslicht Sensors festzulegen.</span><span class="sxs-lookup"><span data-stu-id="bb991-104">The **WmiSetALSBrightness** method is used to set the ambient light sensor brightness value.</span></span> <span data-ttu-id="bb991-105">Wenn eine Überschreibung der aktiven Helligkeit mithilfe der [**wmisethelligkeit**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) -Methode festgelegt wurde, hat diese außer Kraft Setzung Vorrang vor der als-Helligkeit, die mithilfe dieser Methode festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bb991-105">If an active brightness override was established by using the [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) method, that override will take precedence over the ALS brightness set by using this method.</span></span> <span data-ttu-id="bb991-106">Damit eine aktivierte außer Kraft setzung der Helligkeit wirksam wird, muss die Helligkeit-Richtlinie mithilfe der [**wmireverttopolicybrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) -Methode wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="bb991-106">For an enabled ALS brightness override to take effect, the brightness policy has to be reverted by using the [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb991-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb991-107">Syntax</span></span>


```mof
uint32 WmiSetALSBrightness(
   uint8 Brightness
);
```



## <a name="parameters"></a><span data-ttu-id="bb991-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb991-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb991-109">*Helligkeit*</span><span class="sxs-lookup"><span data-stu-id="bb991-109">*Brightness*</span></span> 
</dt> <dd>

<span data-ttu-id="bb991-110">Die als-Helligkeit als Prozentsatz.</span><span class="sxs-lookup"><span data-stu-id="bb991-110">The ALS brightness as a percentage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb991-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb991-111">Return value</span></span>

<span data-ttu-id="bb991-112">Gibt NULL (0) zurück, um den Erfolg anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bb991-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="bb991-113">Jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="bb991-113">Any other number indicates an error.</span></span> <span data-ttu-id="bb991-114">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="bb991-114">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb991-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb991-115">Requirements</span></span>



| <span data-ttu-id="bb991-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb991-116">Requirement</span></span> | <span data-ttu-id="bb991-117">Wert</span><span class="sxs-lookup"><span data-stu-id="bb991-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb991-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb991-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bb991-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb991-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bb991-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb991-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bb991-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb991-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bb991-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="bb991-122">Namespace</span></span><br/>                | <span data-ttu-id="bb991-123">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="bb991-123">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="bb991-124">MOF</span><span class="sxs-lookup"><span data-stu-id="bb991-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb991-125"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bb991-125"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb991-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bb991-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb991-127"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb991-127"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb991-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb991-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb991-129">**Wmimonitorbrightnessmethods**</span><span class="sxs-lookup"><span data-stu-id="bb991-129">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="bb991-130">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="bb991-130">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

