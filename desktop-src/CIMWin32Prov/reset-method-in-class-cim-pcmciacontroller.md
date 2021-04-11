---
description: Die Reset-Methode der CIM \_ PCMCIAController-Klasse fordert das Zurücksetzen des logischen Geräts an.
ms.assetid: c58e3265-2849-4154-a03e-2e1cfa9e3d30
ms.tgt_platform: multiple
title: Reset-Methode der CIM_PCMCIAController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCMCIAController.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8576bc5c1ce291c355d2907761e5b342ea6f3bc9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214170"
---
# <a name="reset-method-of-the-cim_pcmciacontroller-class"></a><span data-ttu-id="ed079-103">Reset-Methode der CIM \_ PCMCIAController-Klasse</span><span class="sxs-lookup"><span data-stu-id="ed079-103">Reset method of the CIM\_PCMCIAController class</span></span>

<span data-ttu-id="ed079-104">Die **Reset** -Methode der CIM \_ PCMCIAController-Klasse fordert das Zurücksetzen des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="ed079-104">The **Reset** method of the CIM\_PCMCIAController class requests a reset of the logical device.</span></span> <span data-ttu-id="ed079-105">Diese Methode wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ed079-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ed079-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ed079-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ed079-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ed079-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ed079-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed079-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="ed079-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed079-109">Parameters</span></span>

<span data-ttu-id="ed079-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ed079-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ed079-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed079-111">Return value</span></span>

<span data-ttu-id="ed079-112">Gibt 0 (null) zurück, wenn die Anforderung erfolgreich ausgeführt wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und ein anderer Wert, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ed079-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed079-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed079-113">Remarks</span></span>

<span data-ttu-id="ed079-114">Diese Methode wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="ed079-114">This method is not implemented by WMI.</span></span> <span data-ttu-id="ed079-115">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="ed079-115">To use this method, you must implement it in your own provider.</span></span> <span data-ttu-id="ed079-116">Informationen zu WMI-Klassen, die von [**CIM- \_ PCMCIAController**](cim-pcmciacontroller.md)abgeleitet sind, finden Sie unter [Win32](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="ed079-116">For WMI classes derived from [**CIM\_PCMCIAController**](cim-pcmciacontroller.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ed079-117">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ed079-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ed079-118">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ed079-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed079-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed079-119">Requirements</span></span>



| <span data-ttu-id="ed079-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed079-120">Requirement</span></span> | <span data-ttu-id="ed079-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ed079-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed079-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed079-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ed079-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed079-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ed079-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed079-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ed079-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed079-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ed079-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed079-126">Namespace</span></span><br/>                | <span data-ttu-id="ed079-127">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ed079-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ed079-128">MOF</span><span class="sxs-lookup"><span data-stu-id="ed079-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed079-129"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ed079-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed079-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ed079-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed079-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed079-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed079-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed079-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed079-133">CIM \_ PCMCIAController</span><span class="sxs-lookup"><span data-stu-id="ed079-133">CIM\_PCMCIAController</span></span>](reset-method-in-class-cim-pcmciacontroller.md)
</dt> <dt>

[<span data-ttu-id="ed079-134">**CIM \_ PCMCIAController**</span><span class="sxs-lookup"><span data-stu-id="ed079-134">**CIM\_PCMCIAController**</span></span>](cim-pcmciacontroller.md)
</dt> </dl>

 

 




