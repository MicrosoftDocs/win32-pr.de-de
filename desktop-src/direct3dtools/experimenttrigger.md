---
description: Stellt Experiment auslöserinformationen dar.
MS-HAID: vspixengine.ExperimentTrigger
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Experiment auslöst-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAA67E5-9C43-4BCD-9388-63EF06AB1C0E
api_name:
- ExperimentTrigger
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bba350657cf738058ecd3f38d7284b72deda1c17
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860214"
---
# <a name="span-idvspixengineexperimenttriggerspanexperimenttrigger-structure"></a><span data-ttu-id="16cd4-103"><span id="vspixengine.experimenttrigger"></span>Experiment auslöst-Struktur</span><span class="sxs-lookup"><span data-stu-id="16cd4-103"><span id="vspixengine.experimenttrigger"></span>ExperimentTrigger structure</span></span>

<span data-ttu-id="16cd4-104">Stellt Experiment auslöserinformationen dar.</span><span class="sxs-lookup"><span data-stu-id="16cd4-104">Represents experiment trigger information.</span></span>

## <a name="syntax"></a><span data-ttu-id="16cd4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="16cd4-105">Syntax</span></span>


```C++
} ExperimentTrigger;
```

## <a name="members"></a><span data-ttu-id="16cd4-106">Member</span><span class="sxs-lookup"><span data-stu-id="16cd4-106">Members</span></span>

<span data-ttu-id="16cd4-107">**type**</span><span class="sxs-lookup"><span data-stu-id="16cd4-107">**type**</span></span>  
<span data-ttu-id="16cd4-108">Die Art von Experiment (Erfassung), die ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="16cd4-108">The kind of experiment (capture) triggered.</span></span>

<span data-ttu-id="16cd4-109">**key**</span><span class="sxs-lookup"><span data-stu-id="16cd4-109">**key**</span></span>  
<span data-ttu-id="16cd4-110">Wenn Type dem Typ experimenttriggertype:: Key entspricht, wird der Schlüssel verwendet, um die Erfassung zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="16cd4-110">When type is equal to EXPERIMENTTRIGGERTYPE::KEY, the key used to trigger capture.</span></span>

<span data-ttu-id="16cd4-111">**Framezahl**</span><span class="sxs-lookup"><span data-stu-id="16cd4-111">**frameNumber**</span></span>  
<span data-ttu-id="16cd4-112">Wenn Type dem Typ experimenttriggertype:: framenumber entspricht, wird die Frame Nummer, die die Erfassung auslöst, ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="16cd4-112">When type is equal to EXPERIMENTTRIGGERTYPE::FRAMENUMBER, the frame number that will trigger capture.</span></span>

<span data-ttu-id="16cd4-113">**capturecount**</span><span class="sxs-lookup"><span data-stu-id="16cd4-113">**captureCount**</span></span>  
<span data-ttu-id="16cd4-114">Die Anzahl der zu erfassenden sequenziellen Frames.</span><span class="sxs-lookup"><span data-stu-id="16cd4-114">The number of sequential frames to capture.</span></span>

<span data-ttu-id="16cd4-115">**Aktions-ID**</span><span class="sxs-lookup"><span data-stu-id="16cd4-115">**actionIID**</span></span>  
<span data-ttu-id="16cd4-116">Die ID des Aktions Ereignisses (Screenshot, Frame Erfassung usw.).</span><span class="sxs-lookup"><span data-stu-id="16cd4-116">The ID of the action event (screenshot, frame capture, etc).</span></span>

<span data-ttu-id="16cd4-117">**Action playload**</span><span class="sxs-lookup"><span data-stu-id="16cd4-117">**actionPlayload**</span></span>  
<span data-ttu-id="16cd4-118">Ein Zeiger auf die Nutzlast des Aktions Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="16cd4-118">A pointer to the action event payload.</span></span>

## <a name="requirements"></a><span data-ttu-id="16cd4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16cd4-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="16cd4-120">Header</span><span class="sxs-lookup"><span data-stu-id="16cd4-120">Header</span></span></p></td><td><span data-ttu-id="16cd4-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="16cd4-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



