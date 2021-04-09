---
description: Die Reset-Methode der CIM- \_ Klasse "magnetoopticaldrive" fordert eine zurück setzung des logischen Geräts an.
ms.assetid: a2a9d58a-2c20-4edc-8700-eebc7e5826f9
ms.tgt_platform: multiple
title: Reset-Methode der CIM_MagnetoOpticalDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MagnetoOpticalDrive.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 81d9830ddf684699d7339bbd436f87a3b6dd91b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958395"
---
# <a name="reset-method-of-the-cim_magnetoopticaldrive-class"></a><span data-ttu-id="396bc-103">Reset-Methode der CIM- \_ Klasse "magnedeopticaldrive"</span><span class="sxs-lookup"><span data-stu-id="396bc-103">Reset method of the CIM\_MagnetoOpticalDrive class</span></span>

<span data-ttu-id="396bc-104">Die **Reset** -Methode der CIM- \_ Klasse "magnetoopticaldrive" fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="396bc-104">The **Reset** method of the CIM\_MagnetoOpticalDrive class requests a reset of the logical device.</span></span> <span data-ttu-id="396bc-105">Diese Methode wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="396bc-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="396bc-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="396bc-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="396bc-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="396bc-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="396bc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="396bc-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="396bc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="396bc-109">Parameters</span></span>

<span data-ttu-id="396bc-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="396bc-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="396bc-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="396bc-111">Return value</span></span>

<span data-ttu-id="396bc-112">Gibt 0 (null) zurück, wenn die Anforderung erfolgreich ausgeführt wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und ein anderer Wert, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="396bc-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="396bc-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="396bc-113">Remarks</span></span>

<span data-ttu-id="396bc-114">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="396bc-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="396bc-115">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="396bc-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="396bc-116">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="396bc-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="396bc-117">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="396bc-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="396bc-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="396bc-118">Requirements</span></span>



| <span data-ttu-id="396bc-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="396bc-119">Requirement</span></span> | <span data-ttu-id="396bc-120">Wert</span><span class="sxs-lookup"><span data-stu-id="396bc-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="396bc-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="396bc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="396bc-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="396bc-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="396bc-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="396bc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="396bc-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="396bc-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="396bc-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="396bc-125">Namespace</span></span><br/>                | <span data-ttu-id="396bc-126">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="396bc-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="396bc-127">MOF</span><span class="sxs-lookup"><span data-stu-id="396bc-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="396bc-128"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="396bc-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="396bc-129">DLL</span><span class="sxs-lookup"><span data-stu-id="396bc-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="396bc-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="396bc-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="396bc-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="396bc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="396bc-132">CIM- \_ Magnet Laufwerk</span><span class="sxs-lookup"><span data-stu-id="396bc-132">CIM\_MagnetoOpticalDrive</span></span>](reset-method-in-class-cim-magnetoopticaldrive.md)
</dt> <dt>

[<span data-ttu-id="396bc-133">**CIM- \_ Magnet Laufwerk**</span><span class="sxs-lookup"><span data-stu-id="396bc-133">**CIM\_MagnetoOpticalDrive**</span></span>](cim-magnetoopticaldrive.md)
</dt> </dl>

 

 




