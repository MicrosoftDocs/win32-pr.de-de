---
title: IReferenceClock getTime-Methode
description: Die getTime-Methode ruft die aktuelle Verweis Zeit ab.
ms.assetid: 9bf5050a-ae09-4a72-a3f2-3df8339d99b9
keywords:
- GetTime-Methode Windows Media-Format
- GetTime-Methode Windows Media-Format, IReferenceClock-Schnittstelle
- IReferenceClock-Schnittstelle Windows Media-Format, GetTime-Methode
topic_type:
- apiref
api_name:
- IReferenceClock.GetTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c679ce0adbbc6cc7ddc014c12f1b0ace4be6b4b0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389344"
---
# <a name="ireferenceclockgettime-method"></a><span data-ttu-id="9db03-106">IReferenceClock:: getTime-Methode</span><span class="sxs-lookup"><span data-stu-id="9db03-106">IReferenceClock::GetTime method</span></span>

<span data-ttu-id="9db03-107">Die **GetTime** -Methode ruft die aktuelle Verweis Zeit ab.</span><span class="sxs-lookup"><span data-stu-id="9db03-107">The **GetTime** method retrieves the current reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="9db03-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9db03-108">Syntax</span></span>


```C++
HRESULT GetTime(
  [out] REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="9db03-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9db03-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9db03-110">*PTIME* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9db03-110">*pTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9db03-111">Ein Zeiger auf eine Variable, die die aktuelle Uhrzeit in 100-Nanosecond-Einheiten empfängt.</span><span class="sxs-lookup"><span data-stu-id="9db03-111">Pointer to a variable that receives the current time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9db03-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9db03-112">Return value</span></span>

<span data-ttu-id="9db03-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="9db03-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9db03-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9db03-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9db03-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9db03-115">Return code</span></span>                                                                               | <span data-ttu-id="9db03-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9db03-116">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="9db03-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9db03-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="9db03-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9db03-118">The method succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="9db03-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="9db03-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="9db03-120">Der *PTIME* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="9db03-120">The *pTime* parameter is **NULL**.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="9db03-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9db03-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9db03-122">**IReferenceClock-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="9db03-122">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





