---
description: 'IFeedbackHubAppInfo::GetInstalledLegacyApps-Methode: Diese API ist nicht für alle Apps verfügbar. Sofern Ihre App nicht speziell von Microsoft bereitgestellt wird, schlagen Aufrufe dieser APIs zur Laufzeit fehl.'
ms.assetid: 84135D6F-8232-4CE5-AD38-D18823F0E174
title: IFeedbackHubAppInfo::GetInstalledLegacyApps-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IFeedbackHubAppInfo.GetInstalledLegacyApps
api_type:
- COM
api_location: ''
ms.openlocfilehash: 167be3846322a1b3aacdf752374b9b0089220963
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096698"
---
# <a name="ifeedbackhubappinfogetinstalledlegacyapps-method"></a><span data-ttu-id="88caa-104">IFeedbackHubAppInfo::GetInstalledLegacyApps-Methode</span><span class="sxs-lookup"><span data-stu-id="88caa-104">IFeedbackHubAppInfo::GetInstalledLegacyApps method</span></span>

<span data-ttu-id="88caa-105">Diese API ist nicht für alle Apps verfügbar.</span><span class="sxs-lookup"><span data-stu-id="88caa-105">This API is not available to all apps.</span></span> <span data-ttu-id="88caa-106">Sofern Ihre App nicht speziell von Microsoft bereitgestellt wird, schlagen Aufrufe dieser APIs zur Laufzeit fehl.</span><span class="sxs-lookup"><span data-stu-id="88caa-106">Unless your app is specially provisioned by Microsoft, calls to these APIs will fail at runtime.</span></span>

## <a name="syntax"></a><span data-ttu-id="88caa-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="88caa-107">Syntax</span></span>


```C++
virtual void GetInstalledLegacyApps(
  [out, optional] IObjectArray **result
);
```



## <a name="parameters"></a><span data-ttu-id="88caa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="88caa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88caa-109">*Ergebnis* \[ out, optional\]</span><span class="sxs-lookup"><span data-stu-id="88caa-109">*result* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="88caa-110">Diese API ist nicht für alle Apps verfügbar.</span><span class="sxs-lookup"><span data-stu-id="88caa-110">This API is not available to all apps.</span></span> <span data-ttu-id="88caa-111">Sofern Ihre App nicht speziell von Microsoft bereitgestellt wird, schlagen Aufrufe dieser APIs zur Laufzeit fehl.</span><span class="sxs-lookup"><span data-stu-id="88caa-111">Unless your app is specially provisioned by Microsoft, calls to these APIs will fail at runtime.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88caa-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88caa-112">Return value</span></span>

<span data-ttu-id="88caa-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="88caa-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="88caa-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88caa-114">Requirements</span></span>



| <span data-ttu-id="88caa-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88caa-115">Requirement</span></span> | <span data-ttu-id="88caa-116">Wert</span><span class="sxs-lookup"><span data-stu-id="88caa-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="88caa-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88caa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="88caa-118">nur Windows 10 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88caa-118">Windows 10 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="88caa-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88caa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="88caa-120">Nur Windows Server \[ 2016-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88caa-120">Windows Server 2016 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88caa-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="88caa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88caa-122">**IFeedbackHubAppInfo**</span><span class="sxs-lookup"><span data-stu-id="88caa-122">**IFeedbackHubAppInfo**</span></span>](ifeebackhubappinfo.md)
</dt> </dl>

 

 




