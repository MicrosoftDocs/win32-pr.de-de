---
description: Wird verwendet, um den Umgebungslichtsensor-Helligkeits Zustand zu steuern.
ms.assetid: ff400d4e-be8c-450b-ad53-d43b0ab84ab3
title: Wmiantalsbrightnessstate-Methode der wmimonitorbrightnessmethods-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightnessState
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 593b007f75c7eb134de4bb4c9f83c7246e9a51b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352385"
---
# <a name="wmisetalsbrightnessstate-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="86849-103">Wmiantalsbrightnessstate-Methode der wmimonitorbrightnessmethods-Klasse</span><span class="sxs-lookup"><span data-stu-id="86849-103">WmiSetALSBrightnessState method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="86849-104">Die **wmiantalsbrightnessstate** -Methode wird verwendet, um den Umgebungszustand des hellen hell Sensors zu steuern.</span><span class="sxs-lookup"><span data-stu-id="86849-104">The **WmiSetALSBrightnessState** method is used to control the ambient light sensor brightness state.</span></span> <span data-ttu-id="86849-105">Wenn eine Überschreibung der aktiven Helligkeit mithilfe der [**wmisethelligkeit**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) -Methode festgelegt wurde, hat diese außer Kraft Setzung Vorrang vor der als-Helligkeit, die mithilfe dieser Methode festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="86849-105">If an active brightness override was established by using the [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) method, that override will take precedence over the ALS brightness set by using this method.</span></span> <span data-ttu-id="86849-106">Damit eine aktivierte außer Kraft setzung der Helligkeit wirksam wird, muss die Helligkeit-Richtlinie mithilfe der [**wmireverttopolicybrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) -Methode wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="86849-106">For an enabled ALS brightness override to take effect, the brightness policy has to be reverted by using the [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="86849-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="86849-107">Syntax</span></span>


```mof
uint32 WmiSetALSBrightnessState(
   boolean State
);
```



## <a name="parameters"></a><span data-ttu-id="86849-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="86849-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86849-109">*State*</span><span class="sxs-lookup"><span data-stu-id="86849-109">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="86849-110">ALS-Helligkeits Zustand.</span><span class="sxs-lookup"><span data-stu-id="86849-110">ALS brightness state.</span></span> <span data-ttu-id="86849-111">False deaktiviert die außer Kraft Setzung von als Helligkeit, und true aktiviert Sie.</span><span class="sxs-lookup"><span data-stu-id="86849-111">False disables the ALS brightness override and true enables it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86849-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86849-112">Return value</span></span>

<span data-ttu-id="86849-113">Gibt NULL (0) zurück, um den Erfolg anzugeben.</span><span class="sxs-lookup"><span data-stu-id="86849-113">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="86849-114">Jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="86849-114">Any other number indicates an error.</span></span> <span data-ttu-id="86849-115">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="86849-115">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="86849-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86849-116">Requirements</span></span>



| <span data-ttu-id="86849-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86849-117">Requirement</span></span> | <span data-ttu-id="86849-118">Wert</span><span class="sxs-lookup"><span data-stu-id="86849-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86849-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86849-119">Minimum supported client</span></span><br/> | <span data-ttu-id="86849-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86849-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="86849-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86849-121">Minimum supported server</span></span><br/> | <span data-ttu-id="86849-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86849-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="86849-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="86849-123">Namespace</span></span><br/>                | <span data-ttu-id="86849-124">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="86849-124">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="86849-125">MOF</span><span class="sxs-lookup"><span data-stu-id="86849-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86849-126"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="86849-126"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="86849-127">DLL</span><span class="sxs-lookup"><span data-stu-id="86849-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86849-128"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86849-128"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86849-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86849-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86849-130">**Wmimonitorbrightnessmethods**</span><span class="sxs-lookup"><span data-stu-id="86849-130">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="86849-131">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="86849-131">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

