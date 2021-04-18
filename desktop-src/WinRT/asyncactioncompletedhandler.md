---
description: Stellt die Methode dar, die aufgerufen wird, wenn eine asynchrone Aktion abgeschlossen ist.
ms.assetid: B410E7C1-B108-4204-9AD1-663F7E05BBC3
title: Asyncactioncompletedhandler-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 639f5c39d0d9e4086009fd08bd0204f9f5f25060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347181"
---
# <a name="asyncactioncompletedhandler-interface"></a><span data-ttu-id="0d613-103">Asyncactioncompletedhandler-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0d613-103">AsyncActionCompletedHandler interface</span></span>

<span data-ttu-id="0d613-104">Stellt die Methode dar, die aufgerufen wird, wenn eine asynchrone Aktion abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="0d613-104">Represents the method that is called when an asynchronous action completes.</span></span>

## <a name="members"></a><span data-ttu-id="0d613-105">Member</span><span class="sxs-lookup"><span data-stu-id="0d613-105">Members</span></span>

<span data-ttu-id="0d613-106">Die **asyncactioncompletedhandler** -Schnittstelle erbt von [**iasyncinfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo).</span><span class="sxs-lookup"><span data-stu-id="0d613-106">The **AsyncActionCompletedHandler** interface inherits from [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo).</span></span> <span data-ttu-id="0d613-107">**Asyncactioncompletedhandler** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0d613-107">**AsyncActionCompletedHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="0d613-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="0d613-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0d613-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="0d613-109">Methods</span></span>

<span data-ttu-id="0d613-110">Die **asyncactioncompletedhandler** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0d613-110">The **AsyncActionCompletedHandler** interface has these methods.</span></span>



| <span data-ttu-id="0d613-111">Methode</span><span class="sxs-lookup"><span data-stu-id="0d613-111">Method</span></span>                                               | <span data-ttu-id="0d613-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d613-112">Description</span></span>                                                                                    |
|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d613-113">**Invoke**</span><span class="sxs-lookup"><span data-stu-id="0d613-113">**Invoke**</span></span>](asyncactioncompletedhandler-invoke.md) | <span data-ttu-id="0d613-114">Ruft die Methode auf, die aufgerufen wird, wenn die angegebene asynchrone Aktion abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="0d613-114">Invokes the method that is called when the specified asynchronous action completes.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0d613-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d613-115">Remarks</span></span>

<span data-ttu-id="0d613-116">Weisen Sie einer [**iasyncaction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) einen **asyncactioncompletedhandler** zu, um eine Benachrichtigung zu erhalten, wenn die asynchrone Aktion abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="0d613-116">Assign an **AsyncActionCompletedHandler** to an [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) to receive a notification when the asynchronous action completes.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d613-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d613-117">Requirements</span></span>



| <span data-ttu-id="0d613-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d613-118">Requirement</span></span> | <span data-ttu-id="0d613-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0d613-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d613-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d613-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0d613-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0d613-121">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="0d613-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d613-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0d613-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0d613-123">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="0d613-124">Header</span><span class="sxs-lookup"><span data-stu-id="0d613-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d613-125"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0d613-125"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d613-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d613-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d613-127">**IAsyncInfo**</span><span class="sxs-lookup"><span data-stu-id="0d613-127">**IAsyncInfo**</span></span>](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo)
</dt> </dl>

 

