---
title: Gettsaudioendpointenreeratorforsession-Rückruffunktion
description: Gibt einen Verweis auf einen audioendpunktenumerator für die angegebene Sitzungs-ID zurück.
ms.assetid: 9dd95ef7-f83f-43be-a8b2-e2b0e4a47a42
ms.tgt_platform: multiple
keywords:
- Gettsaudioendpointenreeratorforsession-Rückruffunktion Remotedesktopdienste
topic_type:
- apiref
api_name:
- GetTSAudioEndpointEnumeratorForSession
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6c09896fc4b35fcb0b6a01a7d592421dd5d5654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346334"
---
# <a name="gettsaudioendpointenumeratorforsession-callback-function"></a><span data-ttu-id="9b2f6-104">Gettsaudioendpointenreeratorforsession-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="9b2f6-104">GetTSAudioEndpointEnumeratorForSession callback function</span></span>

<span data-ttu-id="9b2f6-105">Gibt einen Verweis auf einen audioendpunktenumerator für die angegebene Sitzungs-ID zurück.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-105">Returns a reference to an audio endpoint enumerator for the specified session ID.</span></span> <span data-ttu-id="9b2f6-106">Consumer dieses audioendpunktenumerators, z. b. MMDevAPI.dll, rufen diese Funktion auf, um einen audioendpunktenumerator in einer Remotedesktopdienste Sitzung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-106">Consumers of this audio endpoint enumerator, such as MMDevAPI.dll, call this function to retrieve an audio endpoint enumerator in a Remote Desktop Services session.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b2f6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b2f6-107">Syntax</span></span>


```C++
HRESULT GetTSAudioEndpointEnumeratorForSession(
  _In_  DWORD               SessionId,
  _Out_ IMMDeviceEnumerator **ppEndpointEnumerator
);
```



## <a name="parameters"></a><span data-ttu-id="9b2f6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b2f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b2f6-109">*SessionID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9b2f6-109">*SessionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b2f6-110">Der Bezeichner der Remotedesktopdienste Sitzung.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-110">The identifier of the Remote Desktop Services session.</span></span>

</dd> <dt>

<span data-ttu-id="9b2f6-111">*ppendpointenreerator* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9b2f6-111">*ppEndpointEnumerator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b2f6-112">Die Adresse eines Zeigers auf eine [**immdeviceenumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-112">The address of a pointer to an [**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b2f6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9b2f6-113">Return value</span></span>

<span data-ttu-id="9b2f6-114">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-114">If the method succeeds, it returns **S\_OK**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b2f6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b2f6-115">Remarks</span></span>

<span data-ttu-id="9b2f6-116">Diese Funktion ist nicht in einer Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-116">This function is not defined in a header file.</span></span> <span data-ttu-id="9b2f6-117">Sie sollten diese Funktion in den benutzerdefinierten Endpunkt Enumerator implementieren und exportieren und die im Syntax Block weiter oben in diesem Thema gezeigte Signatur verwenden.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-117">You should implement and export this function in your custom endpoint enumerator and use the signature shown in the syntax block earlier in this topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b2f6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b2f6-118">Requirements</span></span>



| <span data-ttu-id="9b2f6-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b2f6-119">Requirement</span></span> | <span data-ttu-id="9b2f6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9b2f6-120">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="9b2f6-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b2f6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9b2f6-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9b2f6-122">None supported</span></span><br/>         |
| <span data-ttu-id="9b2f6-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b2f6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9b2f6-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9b2f6-124">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9b2f6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b2f6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b2f6-126">Implementieren eines benutzerdefinierten audioendpunkt-Enumerators</span><span class="sxs-lookup"><span data-stu-id="9b2f6-126">Implementing a Custom Audio Endpoint Enumerator</span></span>](implementing-an-audio-endpoint-enumerator.md)
</dt> <dt>

[<span data-ttu-id="9b2f6-127">**Immdeviceenumerator**</span><span class="sxs-lookup"><span data-stu-id="9b2f6-127">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> </dl>

 

