---
description: Die Reset-Methode der CIM \_ TapeDrive-Klasse fordert das Zurücksetzen des logischen Geräts an.
ms.assetid: 48097e0d-7986-46b9-884d-7534f3848dd7
ms.tgt_platform: multiple
title: Reset-Methode der CIM_TapeDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e5fd76d038e743ba5148f4c82555d50f0a5dde5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861623"
---
# <a name="reset-method-of-the-cim_tapedrive-class"></a><span data-ttu-id="58509-103">Reset-Methode der CIM \_ TapeDrive-Klasse</span><span class="sxs-lookup"><span data-stu-id="58509-103">Reset method of the CIM\_TapeDrive class</span></span>

<span data-ttu-id="58509-104">Die **Reset** -Methode der CIM \_ TapeDrive-Klasse fordert das Zurücksetzen des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="58509-104">The **Reset** method of the CIM\_TapeDrive class requests a reset of the logical device.</span></span> <span data-ttu-id="58509-105">Diese Methode wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="58509-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="58509-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="58509-106">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="58509-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="58509-107">Parameters</span></span>

<span data-ttu-id="58509-108">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="58509-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="58509-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58509-109">Return value</span></span>

<span data-ttu-id="58509-110">Gibt 0 (null) zurück, wenn die Anforderung erfolgreich ausgeführt wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und ein anderer Wert, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="58509-110">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="58509-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58509-111">Remarks</span></span>

<span data-ttu-id="58509-112">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="58509-112">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="58509-113">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="58509-113">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="58509-114">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="58509-114">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="58509-115">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="58509-115">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="58509-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58509-116">Requirements</span></span>



| <span data-ttu-id="58509-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58509-117">Requirement</span></span> | <span data-ttu-id="58509-118">Wert</span><span class="sxs-lookup"><span data-stu-id="58509-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58509-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58509-119">Minimum supported client</span></span><br/> | <span data-ttu-id="58509-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58509-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="58509-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58509-121">Minimum supported server</span></span><br/> | <span data-ttu-id="58509-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58509-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58509-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="58509-123">Namespace</span></span><br/>                | <span data-ttu-id="58509-124">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="58509-124">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="58509-125">MOF</span><span class="sxs-lookup"><span data-stu-id="58509-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58509-126"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="58509-126"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="58509-127">DLL</span><span class="sxs-lookup"><span data-stu-id="58509-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58509-128"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58509-128"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58509-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58509-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58509-130">CIM- \_ TapeDrive</span><span class="sxs-lookup"><span data-stu-id="58509-130">CIM\_TapeDrive</span></span>](reset-method-in-class-cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="58509-131">**CIM- \_ TapeDrive**</span><span class="sxs-lookup"><span data-stu-id="58509-131">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> </dl>

 

 




