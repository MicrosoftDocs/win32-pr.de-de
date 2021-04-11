---
description: Ruft den Vorgang zum Anhalten der App ab.
ms.assetid: 33FCAED5-7568-4483-A643-A536B53F7003
title: 'Isuspendingeventargs:: suspendingoperation-Eigenschaft (Windows. applicationmodel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs.SuspendingOperation
- ISuspendingEventArgs.get_SuspendingOperation
- ISuspendingEventArgs.put_SuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e12ccbb372d7c712585766bba8d7921fae57a617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862612"
---
# <a name="isuspendingeventargssuspendingoperation-property"></a><span data-ttu-id="6266d-103">Isuspendingeventargs:: suspendingoperation (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6266d-103">ISuspendingEventArgs::SuspendingOperation property</span></span>

<span data-ttu-id="6266d-104">Ruft den Vorgang zum Anhalten der App ab.</span><span class="sxs-lookup"><span data-stu-id="6266d-104">Gets the app suspending operation.</span></span>

<span data-ttu-id="6266d-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6266d-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6266d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6266d-106">Syntax</span></span>


```C++
HRESULT put_SuspendingOperation();

HRESULT get_SuspendingOperation(
  [out, retval] ISuspendingOperation **value
);
```



## <a name="property-value"></a><span data-ttu-id="6266d-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6266d-107">Property value</span></span>

<span data-ttu-id="6266d-108">Der anhalten-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="6266d-108">The suspending operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="6266d-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6266d-109">Requirements</span></span>



| <span data-ttu-id="6266d-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6266d-110">Requirement</span></span> | <span data-ttu-id="6266d-111">Wert</span><span class="sxs-lookup"><span data-stu-id="6266d-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6266d-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6266d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="6266d-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6266d-113">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6266d-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6266d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="6266d-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6266d-115">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6266d-116">Header</span><span class="sxs-lookup"><span data-stu-id="6266d-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="6266d-117"><dt>Windows. applicationmodel. h</dt></span><span class="sxs-lookup"><span data-stu-id="6266d-117"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="6266d-118">IDL</span><span class="sxs-lookup"><span data-stu-id="6266d-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6266d-119"><dt>Windows. applicationmodel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6266d-119"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6266d-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6266d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6266d-121">**Isuspendingeventargs**</span><span class="sxs-lookup"><span data-stu-id="6266d-121">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> </dl>

 

 




