---
title: Msimtfiswindowgefilterte-Funktion
description: Die Funktion "msimtfiswindowgefiltertert" testet, ob das angegebene Fenster von "AIMM" gefiltert wird (aktiver Eingabemethoden-Manager).
ms.assetid: 1f5e98f1-3626-4aa5-b2da-b6bc48d02184
keywords:
- Msimtfiswindowgefiltertes Funktions Text Dienst-Framework
topic_type:
- apiref
api_name:
- MsimtfIsWindowFiltered
api_location:
- msimtf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70ad9bd9fb61c546ec3e2f1d96d5fc9cf932613a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105398"
---
# <a name="msimtfiswindowfiltered-function"></a><span data-ttu-id="f3721-104">Msimtfiswindowgefilterte-Funktion</span><span class="sxs-lookup"><span data-stu-id="f3721-104">MsimtfIsWindowFiltered function</span></span>

<span data-ttu-id="f3721-105">Die Funktion " **msimtfiswindowgefiltertert** " testet, ob das angegebene Fenster von "AIMM" gefiltert wird (aktiver Eingabemethoden-Manager).</span><span class="sxs-lookup"><span data-stu-id="f3721-105">The **MsimtfIsWindowFiltered** function tests if the given window is filtered by AIMM (Active Input Method Manager).</span></span>

## <a name="syntax"></a><span data-ttu-id="f3721-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3721-106">Syntax</span></span>


```C++
BOOL CALLBACK MsimtfIsWindowFiltered(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="f3721-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3721-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3721-108">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3721-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3721-109">Ein Fenster Handle, das getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3721-109">A window handle to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3721-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f3721-110">Return value</span></span>



| <span data-ttu-id="f3721-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f3721-111">Return code</span></span>                                                                          | <span data-ttu-id="f3721-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3721-112">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f3721-113"><dt>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="f3721-113"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="f3721-114">, Wenn dieses Fenster vom aktiven Eingabemethoden-Manager gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="f3721-114">If this window is filtered by Active Input Method Manager.</span></span><br/>     |
| <dl> <span data-ttu-id="f3721-115"><dt>**Alarm**</dt></span><span class="sxs-lookup"><span data-stu-id="f3721-115"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="f3721-116">, Wenn dieses Fenster nicht vom aktiven Eingabemethoden-Manager gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="f3721-116">If this window is not filtered by Active Input Method Manager.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f3721-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3721-117">Remarks</span></span>

<span data-ttu-id="f3721-118">Ein Fenster kann von iactiveimmapp:: filterclientwindows gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="f3721-118">A window can be filtered by IActiveIMMApp::FilterClientWindows.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3721-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3721-119">Requirements</span></span>



| <span data-ttu-id="f3721-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3721-120">Requirement</span></span> | <span data-ttu-id="f3721-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f3721-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3721-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3721-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f3721-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3721-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f3721-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3721-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f3721-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3721-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f3721-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f3721-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3721-127"><dt>Msimtf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3721-127"><dt>Msimtf.dll</dt></span></span> </dl> |



 

 





