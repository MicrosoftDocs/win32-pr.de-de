---
title: DXCoreAdapterMemoryBudget
description: Beschreibt das Arbeitsspeicher Budget für einen Adapter.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2888b1480e3e394640a10bf0264403cd6c153e3b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474069"
---
# <a name="dxcoreadaptermemorybudget-structure"></a><span data-ttu-id="e6390-103">Dxcoreadaptermemorybudget-Struktur</span><span class="sxs-lookup"><span data-stu-id="e6390-103">DXCoreAdapterMemoryBudget structure</span></span>

<span data-ttu-id="e6390-104">Gibt den <em>adaptermemorybudget</em> -Adapter Status an, der das Arbeitsspeicher Budget des Adapters für den Adapter abruft oder anfordert.</span><span class="sxs-lookup"><span data-stu-id="e6390-104">Specifies the <em>AdapterMemoryBudget</em> adapter state, which retrieves or requests the adapter memory budget on the adapter.</span></span> <span data-ttu-id="e6390-105">Das festlegen (anfordern) eines Budgets gibt den mindestens erforderlichen physischen Speicher an, der in Byte für den Adapter reserviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6390-105">Setting (requesting) a budget represents the minimum required physical memory to reserve, in bytes, on the adapter.</span></span> <span data-ttu-id="e6390-106">Es wird empfohlen, dass Sie eine Adapter Reservierung festlegen, um die Menge an physischem Arbeitsspeicher anzugeben, die Ihre Anwendung nicht unterlassen kann.</span><span class="sxs-lookup"><span data-stu-id="e6390-106">We recommend that you set an adapter reservation in order to denote the amount of physical memory that your application can't go without.</span></span> <span data-ttu-id="e6390-107">Dieser Wert hilft dem Betriebssystem, die Auswirkungen von großen Speicherdruck Situationen schnell zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="e6390-107">This value helps the operating system (OS) to quickly minimize the impact of large memory-pressure situations.</span></span>

<span data-ttu-id="e6390-108">Beim Aufrufen von [querystate](./nf-dxcore_interface-idxcoreadapter-querystate.md)hat <em>der adaptermemorybudget</em> -Adapter Status den Typ <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">dxcoreadaptermemorybudgetnodesegmentgroup</a> für *inputstatedetails* und den Typ **dxcoreadaptermemorybudget** für *OUTPUTBUFFER*.</span><span class="sxs-lookup"><span data-stu-id="e6390-108">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type **DXCoreAdapterMemoryBudget** for *outputBuffer*.</span></span>

<span data-ttu-id="e6390-109">Beim Aufrufen [von SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md)hat der <em>adaptermemorybudget</em> -Adapter Status den Typ <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">dxcoreadaptermemorybudgetnodesegmentgroup</a> für *inputstatedetails*, und geben Sie **uint64_t** für *inputData* ein.</span><span class="sxs-lookup"><span data-stu-id="e6390-109">When calling [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type **uint64_t** for *inputData*.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6390-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6390-110">Syntax</span></span>

```cpp
struct DXCoreAdapterMemoryBudget
{
  uint64_t budget;
  uint64_t currentUsage;
  uint64_t availableForReservation;
  uint64_t currentReservation;
};
```

## <a name="members"></a><span data-ttu-id="e6390-111">Member</span><span class="sxs-lookup"><span data-stu-id="e6390-111">Members</span></span>

### <a name="budget"></a><span data-ttu-id="e6390-112">budget</span><span class="sxs-lookup"><span data-stu-id="e6390-112">budget</span></span>

<span data-ttu-id="e6390-113">Typ: **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="e6390-113">Type: **uint64_t**</span></span>

<span data-ttu-id="e6390-114">Gibt das vom Betriebssystem bereitgestellte Arbeitsspeicher Budget (in Byte) an, das Ihre Anwendung als Ziel hat.</span><span class="sxs-lookup"><span data-stu-id="e6390-114">Specifies the OS-provided adapter memory budget, in bytes, that your application should target.</span></span> <span data-ttu-id="e6390-115">Wenn *CurrentUsage* größer als das *Budget* ist, kann die Anwendung aufgrund der Hintergrund Aktivität durch das Betriebssystem zu einer ungenügenden oder Leistungseinbußen kommen, die anderen Anwendungen eine faire Verwendung des Adapter Speichers bereitstellen soll.</span><span class="sxs-lookup"><span data-stu-id="e6390-115">If *currentUsage* is greater than *budget*, then your application may incur stuttering or performance penalties due to background activity by the OS, which is intended to provide other applications with a fair usage of adapter memory.</span></span>

### <a name="currentusage"></a><span data-ttu-id="e6390-116">CurrentUsage</span><span class="sxs-lookup"><span data-stu-id="e6390-116">currentUsage</span></span>

<span data-ttu-id="e6390-117">Typ: **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="e6390-117">Type: **uint64_t**</span></span>

<span data-ttu-id="e6390-118">Gibt die Speicherauslastung des aktuellen Adapters für den Anwendungs Speicher in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="e6390-118">Specifies your applicaton's current adapter memory usage, in bytes.</span></span>

### <a name="availableforreservation"></a><span data-ttu-id="e6390-119">availableforreservierung</span><span class="sxs-lookup"><span data-stu-id="e6390-119">availableForReservation</span></span>

<span data-ttu-id="e6390-120">Typ: **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="e6390-120">Type: **uint64_t**</span></span>

<span data-ttu-id="e6390-121">Gibt die Größe des Adapter Speichers in Bytes an, der von der Anwendung für die Reservierung zur Verfügung gestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e6390-121">Specifies the amount of adapter memory, in bytes, that your application has available for reservation.</span></span> <span data-ttu-id="e6390-122">Um diesen Adapter Speicher zu reservieren, sollte Ihre Anwendung [idxcoreadapter:: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) aufrufen, wobei *State* auf [dxcoreadapterstate:: adaptermemorybudget](./ne-dxcore_interface-dxcoreadapterstate.md)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e6390-122">To reserve this adapter memory, your application should call [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) with *state* set to [DXCoreAdapterState::AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md).</span></span>

### <a name="currentreservation"></a><span data-ttu-id="e6390-123">currentreservation</span><span class="sxs-lookup"><span data-stu-id="e6390-123">currentReservation</span></span>

<span data-ttu-id="e6390-124">Typ: **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="e6390-124">Type: **uint64_t**</span></span>

<span data-ttu-id="e6390-125">Gibt die Größe des Adapter Speichers in Bytes an, der für Ihre Anwendung reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="e6390-125">Specifies the amount of adapter memory, in bytes, that is reserved by your application.</span></span> <span data-ttu-id="e6390-126">Das Betriebssystem verwendet die Reservierung als Hinweis, um den minimalen Arbeits Satz Ihrer Anwendung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="e6390-126">The OS uses the reservation as a hint to determine your application's minimum working set.</span></span> <span data-ttu-id="e6390-127">Die Anwendung sollte sicherstellen, dass die Speicherauslastung des Adapters zum erfüllen dieser Anforderung verkürzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e6390-127">Your application should attempt to ensure that its adapter memory usage can be trimmed to meet this requirement.</span></span>

## <a name="see-also"></a><span data-ttu-id="e6390-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6390-128">See also</span></span>

<span data-ttu-id="e6390-129">[DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="e6390-129">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>