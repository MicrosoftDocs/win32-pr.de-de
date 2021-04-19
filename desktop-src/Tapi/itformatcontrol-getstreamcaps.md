---
description: Die getstreamcaps-Methode ruft die Funktionen ab, die einem bestimmten Format Index zugeordnet sind.
ms.assetid: 4c375369-51d9-44ac-a8f0-c2a96fc10805
title: 'Itformatcontrol:: getstreamcaps-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1ccaf825912e53eafb5112f14ed369f999959a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367660"
---
# <a name="itformatcontrolgetstreamcaps-method"></a><span data-ttu-id="1df5a-103">Itformatcontrol:: getstreamcaps-Methode</span><span class="sxs-lookup"><span data-stu-id="1df5a-103">ITFormatControl::GetStreamCaps method</span></span>

<span data-ttu-id="1df5a-104">\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1df5a-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1df5a-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="1df5a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1df5a-106">Die **getstreamcaps** -Methode ruft die Funktionen ab, die einem bestimmten Format Index zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1df5a-106">The **GetStreamCaps** method retrieves the capabilities associated with a given format index.</span></span>

## <a name="syntax"></a><span data-ttu-id="1df5a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1df5a-107">Syntax</span></span>


```C++
HRESULT GetStreamCaps(
  [in]  DWORD                   dwIndex,
  [out] AM_MEDIA_TYPE           **ppMediaType,
  [out] TAPI_STREAM_CONFIG_CAPS *pStreamConfigCaps,
  [out] BOOL                    *pfEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="1df5a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1df5a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1df5a-109">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1df5a-109">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1df5a-110">Der Index des zu überprüfenden Formats.</span><span class="sxs-lookup"><span data-stu-id="1df5a-110">Index of the format being probed.</span></span>

</dd> <dt>

<span data-ttu-id="1df5a-111">*PpMediaType* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1df5a-111">*ppMediaType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1df5a-112">Zeiger auf einen **am \_ \_ Medientyp** Deskriptor des Terminal Formats.</span><span class="sxs-lookup"><span data-stu-id="1df5a-112">Pointer to an **AM\_MEDIA\_TYPE** descriptor of the terminal format.</span></span> <span data-ttu-id="1df5a-113">Weitere Informationen zu dem **\_ \_ Medientyp** finden Sie in der DirectX-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="1df5a-113">For more information on **AM\_MEDIA\_TYPE**, see the DirectX documentation.</span></span>

</dd> <dt>

<span data-ttu-id="1df5a-114">*pstreamconfigcaps* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1df5a-114">*pStreamConfigCaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1df5a-115">Eine [**TAPI-Daten \_ Strom- \_ config \_**](tapi-stream-config-caps.md) -Struktur, die ausführliche Informationen zu Stream-Funktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="1df5a-115">A [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure that gives detailed information concerning stream capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="1df5a-116">*pfaktivierte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1df5a-116">*pfEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1df5a-117">Gibt an, ob das mit dem aktuellen Index verknüpfte Format aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1df5a-117">Indicates whether the format associated with the current index is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1df5a-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1df5a-118">Return value</span></span>

<span data-ttu-id="1df5a-119">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1df5a-119">This method can return one of these values.</span></span>



| <span data-ttu-id="1df5a-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1df5a-120">Return code</span></span>                                                                                   | <span data-ttu-id="1df5a-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1df5a-121">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="1df5a-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1df5a-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1df5a-123">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1df5a-123">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1df5a-124"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="1df5a-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1df5a-125">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1df5a-125">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1df5a-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1df5a-126">Requirements</span></span>



| <span data-ttu-id="1df5a-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1df5a-127">Requirement</span></span> | <span data-ttu-id="1df5a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="1df5a-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1df5a-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="1df5a-129">TAPI version</span></span><br/> | <span data-ttu-id="1df5a-130">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="1df5a-130">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="1df5a-131">Header</span><span class="sxs-lookup"><span data-stu-id="1df5a-131">Header</span></span><br/>       | <dl> <span data-ttu-id="1df5a-132"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1df5a-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1df5a-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1df5a-133">Library</span></span><br/>      | <dl> <span data-ttu-id="1df5a-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1df5a-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="1df5a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1df5a-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="1df5a-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1df5a-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1df5a-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1df5a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df5a-138">**Itformatcontrol**</span><span class="sxs-lookup"><span data-stu-id="1df5a-138">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> <dt>

[<span data-ttu-id="1df5a-139">**TAPI \_ - \_ streamkonfigurationscaps \_**</span><span class="sxs-lookup"><span data-stu-id="1df5a-139">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




