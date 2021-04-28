---
description: 'IFeedbackHubAppInfo::GetAumidFromAppListEntry-Methode: Diese API ist nicht für alle Apps verfügbar. Sofern Ihre App nicht speziell von Microsoft bereitgestellt wird, schlagen Aufrufe dieser APIs zur Laufzeit fehl.'
ms.assetid: F205911F-7AA3-464F-A408-3BF549E1112A
title: IFeedbackHubAppInfo::GetAumidFromAppListEntry-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IFeedbackHubAppInfo.GetAumidFromAppListEntry
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2da6b428db156ddf18483951701216942aebbeaf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089298"
---
# <a name="ifeedbackhubappinfogetaumidfromapplistentry-method"></a><span data-ttu-id="2bd9f-104">IFeedbackHubAppInfo::GetAumidFromAppListEntry-Methode</span><span class="sxs-lookup"><span data-stu-id="2bd9f-104">IFeedbackHubAppInfo::GetAumidFromAppListEntry method</span></span>

<span data-ttu-id="2bd9f-105">Diese API ist nicht für alle Apps verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2bd9f-105">This API is not available to all apps.</span></span> <span data-ttu-id="2bd9f-106">Sofern Ihre App nicht speziell von Microsoft bereitgestellt wird, schlagen Aufrufe dieser APIs zur Laufzeit fehl.</span><span class="sxs-lookup"><span data-stu-id="2bd9f-106">Unless your app is specially provisioned by Microsoft, calls to these APIs will fail at runtime.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bd9f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bd9f-107">Syntax</span></span>


```C++
virtual void GetAumidFromAppListEntry(
  [in, optional]  IUnknown *appListEntry,
  [out, optional] LPWSTR   *value
);
```



## <a name="parameters"></a><span data-ttu-id="2bd9f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bd9f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bd9f-109">*appListEntry* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="2bd9f-109">*appListEntry* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2bd9f-110">Diese API ist nicht für alle Apps verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2bd9f-110">This API is not available to all apps.</span></span> <span data-ttu-id="2bd9f-111">Sofern Ihre App nicht speziell von Microsoft bereitgestellt wird, schlagen Aufrufe dieser APIs zur Laufzeit fehl.</span><span class="sxs-lookup"><span data-stu-id="2bd9f-111">Unless your app is specially provisioned by Microsoft, calls to these APIs will fail at runtime.</span></span>

</dd> <dt>

<span data-ttu-id="2bd9f-112">*wert* \[ out, optional\]</span><span class="sxs-lookup"><span data-stu-id="2bd9f-112">*value* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2bd9f-113">Diese API ist nicht für alle Apps verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2bd9f-113">This API is not available to all apps.</span></span> <span data-ttu-id="2bd9f-114">Sofern Ihre App nicht speziell von Microsoft bereitgestellt wird, schlagen Aufrufe dieser APIs zur Laufzeit fehl.</span><span class="sxs-lookup"><span data-stu-id="2bd9f-114">Unless your app is specially provisioned by Microsoft, calls to these APIs will fail at runtime.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bd9f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2bd9f-115">Return value</span></span>

<span data-ttu-id="2bd9f-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2bd9f-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bd9f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2bd9f-117">Requirements</span></span>



| <span data-ttu-id="2bd9f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2bd9f-118">Requirement</span></span> | <span data-ttu-id="2bd9f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2bd9f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2bd9f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2bd9f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2bd9f-121">nur Windows 10 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bd9f-121">Windows 10 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2bd9f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2bd9f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2bd9f-123">Nur Windows Server \[ 2016-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bd9f-123">Windows Server 2016 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2bd9f-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2bd9f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bd9f-125">**IFeedbackHubAppInfo**</span><span class="sxs-lookup"><span data-stu-id="2bd9f-125">**IFeedbackHubAppInfo**</span></span>](ifeebackhubappinfo.md)
</dt> </dl>

 

 




