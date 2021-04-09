---
description: Legt die Anzeige Helligkeit eines Computermonitors fest.
ms.assetid: 900cf5fd-6888-4f0b-8e0b-01eeaaeeeb8f
title: Wmisethelligkeit-Methode der wmimonitorbrightnessmethods-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 599610b0d81de283d97ca347486c4adcbe0103dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042477"
---
# <a name="wmisetbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="53b06-103">Wmisethelligkeit-Methode der wmimonitorbrightnessmethods-Klasse</span><span class="sxs-lookup"><span data-stu-id="53b06-103">WmiSetBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="53b06-104">Die **wmisethelligkeit** -Methode legt die Anzeige Helligkeit eines Computermonitors fest.</span><span class="sxs-lookup"><span data-stu-id="53b06-104">The **WmiSetBrightness** method sets the display brightness of a computer monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="53b06-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="53b06-105">Syntax</span></span>


```mof
uint32 WmiSetBrightness(
   uint32 Timeout,
   uint8  Brightness
);
```



## <a name="parameters"></a><span data-ttu-id="53b06-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="53b06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53b06-107">*Timeout*</span><span class="sxs-lookup"><span data-stu-id="53b06-107">*Timeout*</span></span> 
</dt> <dd>

<span data-ttu-id="53b06-108">Timeout in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="53b06-108">Timeout, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="53b06-109">*Helligkeit*</span><span class="sxs-lookup"><span data-stu-id="53b06-109">*Brightness*</span></span> 
</dt> <dd>

<span data-ttu-id="53b06-110">Helligkeit in Prozent.</span><span class="sxs-lookup"><span data-stu-id="53b06-110">Brightness, in percent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53b06-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53b06-111">Return value</span></span>

<span data-ttu-id="53b06-112">Gibt NULL (0) zurück, um den Erfolg anzugeben.</span><span class="sxs-lookup"><span data-stu-id="53b06-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="53b06-113">Jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="53b06-113">Any other number indicates an error.</span></span> <span data-ttu-id="53b06-114">Weitere Informationen zu Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="53b06-114">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="examples"></a><span data-ttu-id="53b06-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53b06-115">Examples</span></span>

<span data-ttu-id="53b06-116">Eine ausführliche Erläuterung zum Abrufen und Festlegen der Helligkeit des Monitors finden Sie im Blogbeitrag [Verwenden von PowerShell zum melden und Festlegen von Monitor Helligkeit](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) .</span><span class="sxs-lookup"><span data-stu-id="53b06-116">For an extended discussion of retrieving and setting monitor brightness, see the Scripting Guy's [Use PowerShell to Report and Set Monitor Brightness](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) blog topic.</span></span>

<span data-ttu-id="53b06-117">Im folgenden PowerShell-Beispiel wird die Helligkeit des Monitors auf 50% festgelegt.</span><span class="sxs-lookup"><span data-stu-id="53b06-117">The following PowerShell sample sets the brightness of the monitor to 50%.</span></span>


```PowerShell
$brightness = 50
$delay = 5
$myMonitor = Get-WmiObject -Namespace root\wmi -Class WmiMonitorBrightnessMethods
$myMonitor.wmisetbrightness($delay, $brightness)
```



## <a name="requirements"></a><span data-ttu-id="53b06-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53b06-118">Requirements</span></span>



| <span data-ttu-id="53b06-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53b06-119">Requirement</span></span> | <span data-ttu-id="53b06-120">Wert</span><span class="sxs-lookup"><span data-stu-id="53b06-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53b06-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53b06-121">Minimum supported client</span></span><br/> | <span data-ttu-id="53b06-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53b06-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="53b06-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53b06-123">Minimum supported server</span></span><br/> | <span data-ttu-id="53b06-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53b06-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="53b06-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="53b06-125">Namespace</span></span><br/>                | <span data-ttu-id="53b06-126">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="53b06-126">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="53b06-127">MOF</span><span class="sxs-lookup"><span data-stu-id="53b06-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53b06-128"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="53b06-128"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="53b06-129">DLL</span><span class="sxs-lookup"><span data-stu-id="53b06-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53b06-130"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53b06-130"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53b06-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53b06-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53b06-132">**Wmimonitorbrightnessmethods**</span><span class="sxs-lookup"><span data-stu-id="53b06-132">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="53b06-133">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="53b06-133">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

