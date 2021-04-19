---
description: Legt das Beispiel für die Medienstrom Quelle fest.
ms.assetid: a35c5e18-f307-4e40-bc92-f91aa9eb80ba
title: 'Imfmediastreamsourcesamplerequest:: setSample-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest.SetSample
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: bc3b2693a4690207f0b39d7f1b846e1e63069a8c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106366370"
---
# <a name="imfmediastreamsourcesamplerequestsetsample-method"></a><span data-ttu-id="2b108-103">Imfmediastreamsourcesamplerequest:: setSample-Methode</span><span class="sxs-lookup"><span data-stu-id="2b108-103">IMFMediaStreamSourceSampleRequest::SetSample method</span></span>

<span data-ttu-id="2b108-104">Legt das Beispiel für die Medienstrom Quelle fest.</span><span class="sxs-lookup"><span data-stu-id="2b108-104">Sets the sample for the media stream source.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b108-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b108-105">Syntax</span></span>


```C++
HRESULT SetSample(
  [in] IMFSample *value
);
```



## <a name="parameters"></a><span data-ttu-id="2b108-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b108-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b108-107">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b108-107">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b108-108">Das Beispiel für die Medienstrom Quelle.</span><span class="sxs-lookup"><span data-stu-id="2b108-108">The sample for the media stream source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b108-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b108-109">Return value</span></span>

<span data-ttu-id="2b108-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2b108-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2b108-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2b108-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b108-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b108-112">Requirements</span></span>



| <span data-ttu-id="2b108-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b108-113">Requirement</span></span> | <span data-ttu-id="2b108-114">Wert</span><span class="sxs-lookup"><span data-stu-id="2b108-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2b108-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b108-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2b108-116">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2b108-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="2b108-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b108-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2b108-118">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="2b108-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="2b108-119">IDL</span><span class="sxs-lookup"><span data-stu-id="2b108-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2b108-120"><dt>MFI. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2b108-120"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b108-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b108-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b108-122">**Imfmediastreamsourcesamplerequest**</span><span class="sxs-lookup"><span data-stu-id="2b108-122">**IMFMediaStreamSourceSampleRequest**</span></span>](imfmediastreamsourcesamplerequest.md)
</dt> </dl>

 

 




