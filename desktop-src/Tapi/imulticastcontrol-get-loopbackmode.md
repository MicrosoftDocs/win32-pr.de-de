---
description: Die get \_ loopbackmode-Methode ruft den Multicast-Loopback Modus ab.
ms.assetid: 2499c108-f70b-4afe-aa2b-2376c95b84bd
title: 'Imulticastcontrol:: get_LoopbackMode-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 203d68f5b620ddf5e5ce7a36e4f8b85820deab2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364927"
---
# <a name="imulticastcontrolget_loopbackmode-method"></a><span data-ttu-id="dd090-103">Imulticastcontrol:: get \_ loopbackmode-Methode</span><span class="sxs-lookup"><span data-stu-id="dd090-103">IMulticastControl::get\_LoopbackMode method</span></span>

<span data-ttu-id="dd090-104">\[**get \_ Loopbackmode** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dd090-104">\[**get\_LoopbackMode** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dd090-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="dd090-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="dd090-106">Die **get \_ loopbackmode** -Methode ruft den Multicast-Loopback Modus ab.</span><span class="sxs-lookup"><span data-stu-id="dd090-106">The **get\_LoopbackMode** method gets the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd090-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd090-107">Syntax</span></span>


```C++
HRESULT get_LoopbackMode(
  [out] MULTICAST_LOOPBACK_MODE *pMode
);
```



## <a name="parameters"></a><span data-ttu-id="dd090-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd090-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd090-109">*pmode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dd090-109">*pMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd090-110">Zeiger auf den [**Multicast- \_ Loopback \_ Modus**](multicast-loopback-mode.md) -Deskriptor des aktuellen Loopback Modus.</span><span class="sxs-lookup"><span data-stu-id="dd090-110">Pointer to the [**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md) descriptor of the current loopback mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd090-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd090-111">Return value</span></span>

<span data-ttu-id="dd090-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="dd090-112">This method can return one of these values.</span></span>



| <span data-ttu-id="dd090-113">Wert</span><span class="sxs-lookup"><span data-stu-id="dd090-113">Value</span></span>                                                                                        | <span data-ttu-id="dd090-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="dd090-114">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="dd090-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dd090-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="dd090-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dd090-116">Method succeeded.</span></span><br/>                   |
| <dl> <span data-ttu-id="dd090-117"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="dd090-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="dd090-118">Der *pmode* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="dd090-118">The *pMode* parameter is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dd090-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd090-119">Requirements</span></span>



| <span data-ttu-id="dd090-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd090-120">Requirement</span></span> | <span data-ttu-id="dd090-121">Wert</span><span class="sxs-lookup"><span data-stu-id="dd090-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd090-122">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="dd090-122">TAPI version</span></span><br/> | <span data-ttu-id="dd090-123">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="dd090-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="dd090-124">Header</span><span class="sxs-lookup"><span data-stu-id="dd090-124">Header</span></span><br/>       | <dl> <span data-ttu-id="dd090-125"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="dd090-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="dd090-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dd090-126">Library</span></span><br/>      | <dl> <span data-ttu-id="dd090-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd090-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="dd090-128">DLL</span><span class="sxs-lookup"><span data-stu-id="dd090-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="dd090-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd090-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="dd090-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd090-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd090-131">**Imulticastcontrol**</span><span class="sxs-lookup"><span data-stu-id="dd090-131">**IMulticastControl**</span></span>](imulticastcontrol.md)
</dt> </dl>

 

 




