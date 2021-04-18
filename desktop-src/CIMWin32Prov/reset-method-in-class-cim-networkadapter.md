---
description: Die Reset-Methode der CIM- \_ netzwerkadapterklasse fordert das Zurücksetzen des logischen Geräts an.
ms.assetid: ff4493b7-a9e1-4a39-a14a-05da75659d4e
ms.tgt_platform: multiple
title: Reset-Methode der CIM_NetworkAdapter-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkAdapter.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4159a4e3232b4cd709848df178d2238b409996a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523704"
---
# <a name="reset-method-of-the-cim_networkadapter-class"></a><span data-ttu-id="655e0-103">Reset-Methode der CIM \_ NetworkAdapter-Klasse</span><span class="sxs-lookup"><span data-stu-id="655e0-103">Reset method of the CIM\_NetworkAdapter class</span></span>

<span data-ttu-id="655e0-104">Die **Reset** -Methode der CIM- \_ netzwerkadapterklasse fordert das Zurücksetzen des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="655e0-104">The **Reset** method of the CIM\_NetworkAdapter class requests a reset of the logical device.</span></span> <span data-ttu-id="655e0-105">Diese Methode wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="655e0-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="655e0-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="655e0-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="655e0-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="655e0-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="655e0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="655e0-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="655e0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="655e0-109">Parameters</span></span>

<span data-ttu-id="655e0-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="655e0-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="655e0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="655e0-111">Return value</span></span>

<span data-ttu-id="655e0-112">Gibt 0 (null) zurück, wenn die Anforderung erfolgreich ausgeführt wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und ein anderer Wert, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="655e0-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="655e0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="655e0-113">Remarks</span></span>

<span data-ttu-id="655e0-114">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="655e0-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="655e0-115">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="655e0-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="655e0-116">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="655e0-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="655e0-117">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="655e0-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="655e0-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="655e0-118">Requirements</span></span>



| <span data-ttu-id="655e0-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="655e0-119">Requirement</span></span> | <span data-ttu-id="655e0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="655e0-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="655e0-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="655e0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="655e0-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="655e0-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="655e0-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="655e0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="655e0-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="655e0-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="655e0-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="655e0-125">Namespace</span></span><br/>                | <span data-ttu-id="655e0-126">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="655e0-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="655e0-127">MOF</span><span class="sxs-lookup"><span data-stu-id="655e0-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="655e0-128"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="655e0-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="655e0-129">DLL</span><span class="sxs-lookup"><span data-stu-id="655e0-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="655e0-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="655e0-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="655e0-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="655e0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="655e0-132">CIM- \_ Netzwerkadapter</span><span class="sxs-lookup"><span data-stu-id="655e0-132">CIM\_NetworkAdapter</span></span>](reset-method-in-class-cim-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="655e0-133">**CIM- \_ Netzwerkadapter**</span><span class="sxs-lookup"><span data-stu-id="655e0-133">**CIM\_NetworkAdapter**</span></span>](cim-networkadapter.md)
</dt> </dl>

 

 




