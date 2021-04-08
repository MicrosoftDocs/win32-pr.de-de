---
description: Vergleichen Sie das-Argument mit der aktiven Konfiguration des Sammlers.
ms.assetid: 8decb674-c905-4eb6-9f78-7bc7b99db908
ms.tgt_platform: multiple
title: Isconfigurationequal-Methode der Control-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.IsConfigurationEqual
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: fb471f144a39519f1f724db458b57b624db2846d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747785"
---
# <a name="isconfigurationequal-method-of-the-control-class"></a><span data-ttu-id="d1acb-103">Isconfigurationequal-Methode der Control-Klasse</span><span class="sxs-lookup"><span data-stu-id="d1acb-103">IsConfigurationEqual method of the Control class</span></span>

<span data-ttu-id="d1acb-104">Vergleichen Sie das-Argument mit der aktiven Konfiguration des Sammlers.</span><span class="sxs-lookup"><span data-stu-id="d1acb-104">Compare the argument with the active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1acb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1acb-105">Syntax</span></span>


```mof
Uint32 IsConfigurationEqual(
  [in] string Config
);
```



## <a name="parameters"></a><span data-ttu-id="d1acb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1acb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1acb-107">*Config* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1acb-107">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1acb-108">Die Konfiguration, die mit der aktiven Konfiguration verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1acb-108">The configuration to compare to the active configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1acb-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1acb-109">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="d1acb-110">0</span><span class="sxs-lookup"><span data-stu-id="d1acb-110">0</span></span>

<span data-ttu-id="d1acb-111">Fehler</span><span class="sxs-lookup"><span data-stu-id="d1acb-111">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d1acb-112">1</span><span class="sxs-lookup"><span data-stu-id="d1acb-112">1</span></span>

<span data-ttu-id="d1acb-113">Erfolg</span><span class="sxs-lookup"><span data-stu-id="d1acb-113">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1acb-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1acb-114">Requirements</span></span>



| <span data-ttu-id="d1acb-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1acb-115">Requirement</span></span> | <span data-ttu-id="d1acb-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d1acb-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1acb-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1acb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d1acb-118">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1acb-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d1acb-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1acb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d1acb-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d1acb-120">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="d1acb-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1acb-121">Namespace</span></span><br/>                | <span data-ttu-id="d1acb-122">Stammverzeichnis von \\ Microsoft \\ Windows \\ booteventcollector</span><span class="sxs-lookup"><span data-stu-id="d1acb-122">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="d1acb-123">MOF</span><span class="sxs-lookup"><span data-stu-id="d1acb-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1acb-124"><dt>Booteventcollector WMI. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d1acb-124"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1acb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d1acb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1acb-126"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d1acb-126"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="d1acb-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1acb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1acb-128">**Control**</span><span class="sxs-lookup"><span data-stu-id="d1acb-128">**Control**</span></span>](control.md)
</dt> </dl>

 

 




