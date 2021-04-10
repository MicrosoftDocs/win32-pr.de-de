---
description: Eine abstrakte Basisklasse, von der alle Daten Klassen des MCA-Anbieters (Machine Check Architecture), wie z. b. msmcainfo \_ rawmcadata, abgeleitet werden. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: 22ec8343-fc4f-4b14-9354-26b5d6a6fe09
title: Msmcainfo-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 31fc35b1d680d900af929ea8a828bcb23d222f66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041718"
---
# <a name="msmcainfo-class"></a><span data-ttu-id="fa78e-104">Msmcainfo-Klasse</span><span class="sxs-lookup"><span data-stu-id="fa78e-104">MSMCAInfo class</span></span>

<span data-ttu-id="fa78e-105">Bei der **msmcainfo** -Klasse handelt es sich um eine abstrakte Basisklasse, von der alle Daten Klassen des MCA-Anbieters (Machine Check Architecture), wie z. b. [**msmcainfo \_ rawmcadata**](msmcainfo-rawmcadata.md), abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="fa78e-105">The **MSMCAInfo** class is an abstract base class from which all Machine Check Architecture (MCA) provider data classes, such as [**MSMCAInfo\_RawMCAData**](msmcainfo-rawmcadata.md), are derived.</span></span> <span data-ttu-id="fa78e-106">Der MCA-Anbieter verfügt auch über Ereignis Klassen, die von [**wmievent**](wmievent.md)abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="fa78e-106">The MCA provider also has event classes, derived from [**WMIEvent**](wmievent.md).</span></span> <span data-ttu-id="fa78e-107">Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fa78e-107">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="fa78e-108">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fa78e-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="fa78e-109">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="fa78e-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa78e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa78e-110">Syntax</span></span>

``` syntax
class MSMCAInfo
{
};
```

## <a name="members"></a><span data-ttu-id="fa78e-111">Member</span><span class="sxs-lookup"><span data-stu-id="fa78e-111">Members</span></span>

<span data-ttu-id="fa78e-112">Die **msmcainfo** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="fa78e-112">The **MSMCAInfo** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa78e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa78e-113">Requirements</span></span>



| <span data-ttu-id="fa78e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa78e-114">Requirement</span></span> | <span data-ttu-id="fa78e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="fa78e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa78e-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa78e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fa78e-117">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fa78e-117">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="fa78e-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa78e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fa78e-119">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fa78e-119">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="fa78e-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa78e-120">Namespace</span></span><br/>                | <span data-ttu-id="fa78e-121">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="fa78e-121">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="fa78e-122">MOF</span><span class="sxs-lookup"><span data-stu-id="fa78e-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa78e-123"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fa78e-123"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa78e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="fa78e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa78e-125"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa78e-125"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa78e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa78e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa78e-127">MSMCA-Klassen</span><span class="sxs-lookup"><span data-stu-id="fa78e-127">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="fa78e-128">**Msmcaevent- \_ Header**</span><span class="sxs-lookup"><span data-stu-id="fa78e-128">**MSMCAEvent\_Header**</span></span>](msmcaevent-header.md)
</dt> <dt>

[<span data-ttu-id="fa78e-129">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="fa78e-129">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

 




