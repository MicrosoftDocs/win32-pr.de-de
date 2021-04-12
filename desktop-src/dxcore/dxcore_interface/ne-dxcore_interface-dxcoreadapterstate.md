---
title: DXCoreAdapterState
description: Definiert Konstanten, die Arten von DXCore-Adapter Zuständen angeben.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: e588b75360c141b52989aa14e88c886092af2647
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315560"
---
# <a name="dxcoreadapterstate-enum"></a><span data-ttu-id="01d87-103">Dxcoreadapterstate-Aufzählung</span><span class="sxs-lookup"><span data-stu-id="01d87-103">DXCoreAdapterState enum</span></span>

<span data-ttu-id="01d87-104">Definiert Konstanten, die Arten von DXCore-Adapter Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="01d87-104">Defines constants that specify kinds of DXCore adapter states.</span></span> <span data-ttu-id="01d87-105">Übergeben Sie eine dieser Konstanten an die [idxcoreadapter:: querystate](./nf-dxcore_interface-idxcoreadapter-querystate.md) -Methode, um das Adapter Zustands Element für eine Statusart abzurufen. übergeben Sie eine Konstante an die [idxcoreadapter:: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) -Methode, um die Informationen eines Adapters für ein Zustands Element festzulegen.</span><span class="sxs-lookup"><span data-stu-id="01d87-105">Pass one of these constants to the [IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) method to retrieve the adapter state item for a state kind; pass a constant to the [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) method to set an adapter's info for a state item.</span></span>

## <a name="syntax"></a><span data-ttu-id="01d87-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="01d87-106">Syntax</span></span>

```cpp
enum class DXCoreAdapterState : uint32_t
{
  IsDriverUpdateInProgress = 0,
  AdapterMemoryBudget = 1
};
```

## <a name="constants"></a><span data-ttu-id="01d87-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="01d87-107">Constants</span></span>

### <a name="isdriverupdateinprogress"></a><span data-ttu-id="01d87-108">Isdriverupdaterprogress</span><span class="sxs-lookup"><span data-stu-id="01d87-108">IsDriverUpdateInProgress</span></span>

<span data-ttu-id="01d87-109">Gibt den <em>isdriverupdateinprogress</em> -Adapter Status an, der `true` angibt, dass ein Treiberupdate auf dem Adapter initiiert, aber noch nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="01d87-109">Specifies the <em>IsDriverUpdateInProgress</em> adapter state, which when `true` indicates that a driver update has been initiated on the adapter but it has not yet completed.</span></span> <span data-ttu-id="01d87-110">Wenn das Treiberupdate bereits abgeschlossen wurde, wird der Adapter ungültig, und der [querystate](./nf-dxcore_interface-idxcoreadapter-querystate.md) -Rückruf gibt ein <b>HRESULT</b> <b>DXGI_ERROR_DEVICE_REMOVED</b>zurück.</span><span class="sxs-lookup"><span data-stu-id="01d87-110">If the driver update has already completed, then the adapter will have been invalidated, and your [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) call will return a <b>HRESULT</b> of <b>DXGI_ERROR_DEVICE_REMOVED</b>.</span></span>

<span data-ttu-id="01d87-111">Beim Aufrufen von [querystate](./nf-dxcore_interface-idxcoreadapter-querystate.md)hat das <em>isdriverupdateinprogress</em> -Zustands Element den Typ <b>uint8_t</b>, der einen booleschen Wert darstellt.</span><span class="sxs-lookup"><span data-stu-id="01d87-111">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>IsDriverUpdateInProgress</em> state item has type <b>uint8_t</b>, representing a Boolean value.</span></span>

<span data-ttu-id="01d87-112"><b>Wichtig</b>.</span><span class="sxs-lookup"><span data-stu-id="01d87-112"><b>Important</b>.</span></span> <span data-ttu-id="01d87-113">Dieses Zustands Element wird für [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md)nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="01d87-113">This state item is not supported for [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md).</span></span>

### <a name="adaptermemorybudget"></a><span data-ttu-id="01d87-114">Adaptermemorybudget</span><span class="sxs-lookup"><span data-stu-id="01d87-114">AdapterMemoryBudget</span></span>

<span data-ttu-id="01d87-115">Gibt den <em>adaptermemorybudget</em> -Adapter Status an, der das Arbeitsspeicher Budget des Adapters für den Adapter abruft oder anfordert.</span><span class="sxs-lookup"><span data-stu-id="01d87-115">Specifies the <em>AdapterMemoryBudget</em> adapter state, which retrieves or requests the adapter memory budget on the adapter.</span></span>

<span data-ttu-id="01d87-116">Beim Aufrufen von [querystate](./nf-dxcore_interface-idxcoreadapter-querystate.md)hat <em>der adaptermemorybudget</em> -Adapter Status den Typ <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">dxcoreadaptermemorybudgetnodesegmentgroup</a> für *inputstatedetails* und den Typ <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">dxcoreadaptermemorybudget</a> für *OUTPUTBUFFER*.</span><span class="sxs-lookup"><span data-stu-id="01d87-116">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> for *outputBuffer*.</span></span>

## <a name="see-also"></a><span data-ttu-id="01d87-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01d87-117">See also</span></span>

<span data-ttu-id="01d87-118">[Idxcoreadapter:: querystate](./nf-dxcore_interface-idxcoreadapter-querystate.md), [idxcoreadapter:: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="01d87-118">[IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>