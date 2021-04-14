---
title: Iamwmbufferpass-setnotify-Methode
description: Die setnotify-Methode wird von Anwendungen verwendet, um den WM-ASF-oder WM-ASF-Lesefilter mit einem Zeiger auf die iamwmbufferpasscallback-Schnittstelle der Anwendung bereitzustellen.
ms.assetid: b0fff344-a20c-4cfc-828b-c6fc49d990ea
keywords:
- Setnotify-Methode (Windows Media-Format)
- Setnotify-Methode Windows Media-Format, iamwmbufferpass-Schnittstelle
- Iamwmbufferpass-Schnittstelle Windows Media-Format, setnotify-Methode
topic_type:
- apiref
api_name:
- IAMWMBufferPass.SetNotify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9739952792fcfa49da1b5656db513c3af41a419c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390850"
---
# <a name="iamwmbufferpasssetnotify-method"></a><span data-ttu-id="5811c-106">Iamwmbufferpass:: setnotify-Methode</span><span class="sxs-lookup"><span data-stu-id="5811c-106">IAMWMBufferPass::SetNotify method</span></span>

<span data-ttu-id="5811c-107">Die **setnotify** -Methode wird von Anwendungen verwendet, um den WM-ASF-oder [WM-ASF-Lesefilter](wm-asf-reader-filter.md) mit einem Zeiger auf die [**iamwmbufferpasscallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) -Schnittstelle der Anwendung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5811c-107">The **SetNotify** method is used by applications to provide the WM ASF Writer or [WM ASF Reader](wm-asf-reader-filter.md) filter with a pointer to the application's [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5811c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5811c-108">Syntax</span></span>


```C++
HRESULT SetNotify(
  [in] IAMWMBufferPassCallback *pCallback
);
```



## <a name="parameters"></a><span data-ttu-id="5811c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5811c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5811c-110">*pCallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5811c-110">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5811c-111">Zeiger auf die **iamwmbufferpasscallback** -Schnittstelle der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5811c-111">Pointer to the application's **IAMWMBufferPassCallback** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5811c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5811c-112">Return value</span></span>

<span data-ttu-id="5811c-113">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="5811c-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="5811c-114">Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5811c-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5811c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5811c-115">Remarks</span></span>

<span data-ttu-id="5811c-116">Ruft diese Methode auf, bevor das Filter Diagramm in den Status "Run" versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="5811c-116">Call this method before putting the filter graph into the run state.</span></span>

## <a name="see-also"></a><span data-ttu-id="5811c-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5811c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5811c-118">**Iamwmbufferpass-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5811c-118">**IAMWMBufferPass Interface**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)
</dt> </dl>

 

 