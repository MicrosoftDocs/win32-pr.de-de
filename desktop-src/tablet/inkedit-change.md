---
description: Tritt auf, wenn sich der Inhalt des InkEdit-Steuer Elements ändert.
ms.assetid: 6c65fcca-c84a-414c-a4e5-c5fdffb13e51
title: InkEdit. Change-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1ad11ef335a397070001f1ae6be785d60fe9cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373254"
---
# <a name="inkeditchange-event"></a><span data-ttu-id="7e450-103">InkEdit. Change-Ereignis</span><span class="sxs-lookup"><span data-stu-id="7e450-103">InkEdit.Change event</span></span>

<span data-ttu-id="7e450-104">Tritt auf, wenn sich der Inhalt des [InkEdit](inkedit-control-reference.md) -Steuer Elements ändert.</span><span class="sxs-lookup"><span data-stu-id="7e450-104">Occurs when the content of the [InkEdit](inkedit-control-reference.md) control changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e450-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e450-105">Syntax</span></span>


```C++
void Change();
```



## <a name="parameters"></a><span data-ttu-id="7e450-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e450-106">Parameters</span></span>

<span data-ttu-id="7e450-107">Dieses Ereignis weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="7e450-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7e450-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e450-108">Return value</span></span>

<span data-ttu-id="7e450-109">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7e450-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e450-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e450-110">Remarks</span></span>

<span data-ttu-id="7e450-111">Dieses Ereignis tritt auf, wenn Eigenschaften, die sich auf den Inhalt des [InkEdit](inkedit-control-reference.md) -Steuer Elements auswirken, geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7e450-111">This event occurs whenever any properties that affect the contents of the [InkEdit](inkedit-control-reference.md) control change.</span></span>

<span data-ttu-id="7e450-112">Diese Ereignismethode wird in der **\_ iinkeditevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="7e450-112">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="7e450-113">Die **\_ iinkeditevents** -Schnittstelle implementiert die IDispatch-Schnittstelle mit dem Bezeichner " **DISPID \_ ieechange**".</span><span class="sxs-lookup"><span data-stu-id="7e450-113">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IeeChange**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e450-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e450-114">Requirements</span></span>



| <span data-ttu-id="7e450-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e450-115">Requirement</span></span> | <span data-ttu-id="7e450-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7e450-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e450-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e450-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7e450-118">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e450-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7e450-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e450-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7e450-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7e450-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7e450-121">Header</span><span class="sxs-lookup"><span data-stu-id="7e450-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e450-122"><dt>In "-. h" (auch als "gezeichneten \_ i. c" erforderlich)</dt></span><span class="sxs-lookup"><span data-stu-id="7e450-122"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7e450-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7e450-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="7e450-124"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e450-124"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7e450-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e450-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e450-126">InkEdit</span><span class="sxs-lookup"><span data-stu-id="7e450-126">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




