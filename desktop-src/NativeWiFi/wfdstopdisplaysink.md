---
description: Beendet den miracast-senkenmodus, deaktiviert die Auffindbarkeit und hebt die Registrierung des Rückrufs auf.
ms.assetid: 38AE60CB-F601-4C03-A725-9B802341B84B
title: WF-displaysink-Funktion (wsdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStopDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: d1ebaa9920ca7d38cff22cef6383b37065faa2ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347294"
---
# <a name="wfddisplaysinkstop-function"></a><span data-ttu-id="ba3fe-103">Wsddisplaysink-Funktion</span><span class="sxs-lookup"><span data-stu-id="ba3fe-103">WFDDisplaySinkStop function</span></span>

<span data-ttu-id="ba3fe-104">Beendet den miracast-senkenmodus, deaktiviert die Auffindbarkeit und hebt die Registrierung des Rückrufs auf.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-104">Stops the Miracast sink mode, turns off discoverability, and un-registers the callback.</span></span> <span data-ttu-id="ba3fe-105">Ihre APP sollte diese einmal beim Herunterfahren anrufen.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-105">Your app should call this once on shutdown.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba3fe-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba3fe-106">Syntax</span></span>


```C++
DWORD WINAPI WFDStopDisplaySink(void);
```



## <a name="parameters"></a><span data-ttu-id="ba3fe-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba3fe-107">Parameters</span></span>

<span data-ttu-id="ba3fe-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ba3fe-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba3fe-109">Return value</span></span>

<span data-ttu-id="ba3fe-110">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba3fe-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba3fe-111">Remarks</span></span>

<span data-ttu-id="ba3fe-112">Es wird erwartet, dass Ihre APP die Blockierung aller aktuell ausgeführten Rückrufe aufgehoben hat, bevor **wfdstopdisplaysink** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-112">It is expected that your app has unblocked any callbacks in progress before calling **WFDStopDisplaySink**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba3fe-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba3fe-113">Requirements</span></span>



| <span data-ttu-id="ba3fe-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba3fe-114">Requirement</span></span> | <span data-ttu-id="ba3fe-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ba3fe-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba3fe-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba3fe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ba3fe-117">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="ba3fe-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ba3fe-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba3fe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ba3fe-119">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba3fe-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ba3fe-120">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ba3fe-120">End of client support</span></span><br/>    | <span data-ttu-id="ba3fe-121">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ba3fe-121">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="ba3fe-122">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="ba3fe-122">End of server support</span></span><br/>    | <span data-ttu-id="ba3fe-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ba3fe-123">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="ba3fe-124">Header</span><span class="sxs-lookup"><span data-stu-id="ba3fe-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba3fe-125"><dt>WF-Senke. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba3fe-125"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="ba3fe-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ba3fe-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="ba3fe-127"><dt>Wifdisplay. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba3fe-127"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="ba3fe-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ba3fe-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba3fe-129"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba3fe-129"><dt>Wifidisplay.dll</dt></span></span> </dl> |



 

 




