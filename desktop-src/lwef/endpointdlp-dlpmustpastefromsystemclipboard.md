---
description: Bestimmt, ob die App die Daten aus der Systemablage pullen muss, anstatt sie aus ihrem internen Cache zu entfernen.
title: DlpMustPasteFromSystemClipboard-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpMustPasteFromSystemClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 5863173b02cb5c63a2de46653c2d268464e82e65
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495729"
---
# <a name="dlpmustpastefromsystemclipboard-function"></a><span data-ttu-id="0d8a3-103">DlpMustPasteFromSystemClipboard-Funktion</span><span class="sxs-lookup"><span data-stu-id="0d8a3-103">DlpMustPasteFromSystemClipboard function</span></span>

<span data-ttu-id="0d8a3-104">Bestimmt, ob die App die Daten aus der Systemablage pullen muss, anstatt sie aus ihrem internen Cache zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="0d8a3-104">Determines whether the app must pull the data from the system clipboard rather than taking it from its internal cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d8a3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d8a3-105">Syntax</span></span>


```C++
BOOL WINAPI DlpMustPasteFromSystemClipboard();
```


## <a name="return-value"></a><span data-ttu-id="0d8a3-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d8a3-106">Return value</span></span>

<span data-ttu-id="0d8a3-107">TRUE, wenn der Aufruf in der Betriebssystem-Zwischenablage obligatorisch ist; andernfalls FALSE.</span><span class="sxs-lookup"><span data-stu-id="0d8a3-107">TRUE if calling into the OS clipboard is mandatory; otherwise, FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d8a3-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d8a3-108">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="0d8a3-109">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0d8a3-109">Requirements</span></span>



| <span data-ttu-id="0d8a3-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d8a3-110">Requirement</span></span>          |    <span data-ttu-id="0d8a3-111">Wert</span><span class="sxs-lookup"><span data-stu-id="0d8a3-111">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d8a3-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d8a3-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0d8a3-113">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="0d8a3-113">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="0d8a3-114">DLL</span><span class="sxs-lookup"><span data-stu-id="0d8a3-114">DLL</span></span><br/>                      | <span data-ttu-id="0d8a3-115">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="0d8a3-115">EndpointDlp.dll</span></span> |