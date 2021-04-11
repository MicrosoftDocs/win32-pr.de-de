---
description: Tritt auf, wenn eine Windows Store-App aktiviert wird.
ms.assetid: CA0DB2D4-3417-48F5-8455-D87D0F323A1E
title: 'Icoreapplicationview:: aktiviertes Ereignis (Windows. applicationmodel. Core. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612f7110aa149396b18815afe664ee404c70fc52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214606"
---
# <a name="icoreapplicationviewactivated-event"></a><span data-ttu-id="9ebf4-103">Icoreapplicationview:: aktiviertes Ereignis</span><span class="sxs-lookup"><span data-stu-id="9ebf4-103">ICoreApplicationView::Activated event</span></span>

<span data-ttu-id="9ebf4-104">Tritt auf, wenn eine Windows Store-App aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="9ebf4-104">Occurs when a Windows Store app is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ebf4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ebf4-105">Syntax</span></span>


```C++
void Activated(
  [in] ITypedEventHandler<ICoreApplicationView*, IActivatedEventArgs*> handler
);
```



## <a name="parameters"></a><span data-ttu-id="9ebf4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ebf4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ebf4-107">*Handler* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ebf4-107">*handler* \[in\]</span></span>
<span data-ttu-id="9ebf4-108"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9ebf4-108"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="9ebf4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ebf4-109">Return value</span></span>

<span data-ttu-id="9ebf4-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9ebf4-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ebf4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ebf4-111">Remarks</span></span>

<span data-ttu-id="9ebf4-112">Die [**Exit**](/previous-versions//hh438368(v=vs.85)) -Methode kann nicht innerhalb des *Handlers* aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9ebf4-112">Do not call the [**Exit**](/previous-versions//hh438368(v=vs.85)) method from within *handler*.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ebf4-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ebf4-113">Requirements</span></span>



| <span data-ttu-id="9ebf4-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ebf4-114">Requirement</span></span> | <span data-ttu-id="9ebf4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9ebf4-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ebf4-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ebf4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9ebf4-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9ebf4-117">Windows 8</span></span><br/>                                                                                         |
| <span data-ttu-id="9ebf4-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ebf4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9ebf4-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9ebf4-119">Windows Server 2012</span></span><br/>                                                                               |
| <span data-ttu-id="9ebf4-120">Header</span><span class="sxs-lookup"><span data-stu-id="9ebf4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ebf4-121"><dt>Windows. applicationmodel. Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ebf4-121"><dt>Windows.ApplicationModel.Core.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ebf4-122">IDL</span><span class="sxs-lookup"><span data-stu-id="9ebf4-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9ebf4-123"><dt>Windows. applicationmodel. Core. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9ebf4-123"><dt>Windows.ApplicationModel.Core.idl</dt></span></span> </dl> |



 

 
