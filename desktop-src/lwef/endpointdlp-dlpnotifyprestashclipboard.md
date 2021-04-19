---
description: Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor ein Stash-Zwischenablagevorgang initiiert wird.
title: DlpNotifyPreStashClipboard-Funktion (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreStashClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 72ecabb2bbfb7517b52790c0d3b7c1ab8075dbd0
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495574"
---
# <a name="dlpnotifyprestashclipboard-function"></a><span data-ttu-id="0ce50-103">DlpNotifyPreStashClipboard-Funktion</span><span class="sxs-lookup"><span data-stu-id="0ce50-103">DlpNotifyPreStashClipboard function</span></span>

<span data-ttu-id="0ce50-104">Benachrichtigt das System, bevor ein Stash-Zwischenablagevorgang initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="0ce50-104">Notifies the system before a stash clipboard operation is initiated.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ce50-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ce50-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPreStashClipboard();
```



## <a name="parameters"></a><span data-ttu-id="0ce50-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ce50-106">Parameters</span></span>




## <a name="return-value"></a><span data-ttu-id="0ce50-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ce50-107">Return value</span></span>

<span data-ttu-id="0ce50-108">Gibt void zurück.</span><span class="sxs-lookup"><span data-stu-id="0ce50-108">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ce50-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ce50-109">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="0ce50-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0ce50-110">Requirements</span></span>



| <span data-ttu-id="0ce50-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ce50-111">Requirement</span></span>          |    <span data-ttu-id="0ce50-112">Wert</span><span class="sxs-lookup"><span data-stu-id="0ce50-112">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ce50-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ce50-113">Minimum supported client</span></span><br/> | <span data-ttu-id="0ce50-114">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="0ce50-114">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="0ce50-115">DLL</span><span class="sxs-lookup"><span data-stu-id="0ce50-115">DLL</span></span><br/>                      | <span data-ttu-id="0ce50-116">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="0ce50-116">EndpointDlp.dll</span></span> |