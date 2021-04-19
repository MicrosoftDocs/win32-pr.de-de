---
description: Gibt an, dass das Ende des Mediendaten Stroms erreicht wurde.
ms.assetid: 6d6bffcc-aa3c-4825-9268-00dcd2a347e6
title: 'Imfmediasourceextension:: abtendofstream-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetEndOfStream
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9018d76ce13bf441ea98134eb751f9e472f6bca8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361764"
---
# <a name="imfmediasourceextensionsetendofstream-method"></a><span data-ttu-id="6394b-103">Imfmediasourceextension:: abtendofstream-Methode</span><span class="sxs-lookup"><span data-stu-id="6394b-103">IMFMediaSourceExtension::SetEndOfStream method</span></span>

<span data-ttu-id="6394b-104">Gibt an, dass das Ende des Mediendaten Stroms erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="6394b-104">Indicate that the end of the media stream has been reached.</span></span>

## <a name="syntax"></a><span data-ttu-id="6394b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6394b-105">Syntax</span></span>


```C++
HRESULT SetEndOfStream(
  [in] MF_MSE_ERROR error
);
```



## <a name="parameters"></a><span data-ttu-id="6394b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6394b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6394b-107">*Fehler* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6394b-107">*error* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6394b-108">Wird verwendet, um Fehlerinformationen zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="6394b-108">Used to pass error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6394b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6394b-109">Return value</span></span>

<span data-ttu-id="6394b-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="6394b-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6394b-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6394b-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6394b-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6394b-112">Requirements</span></span>



| <span data-ttu-id="6394b-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6394b-113">Requirement</span></span> | <span data-ttu-id="6394b-114">Wert</span><span class="sxs-lookup"><span data-stu-id="6394b-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6394b-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6394b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6394b-116">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="6394b-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6394b-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6394b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6394b-118">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6394b-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6394b-119">IDL</span><span class="sxs-lookup"><span data-stu-id="6394b-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6394b-120"><dt>MF mediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6394b-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6394b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6394b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6394b-122">**Imfmediasourceextension**</span><span class="sxs-lookup"><span data-stu-id="6394b-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> <dt>

[<span data-ttu-id="6394b-123">**MF- \_ MSE- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="6394b-123">**MF\_MSE\_ERROR**</span></span>](mf-mse-error.md)
</dt> </dl>

 

 




