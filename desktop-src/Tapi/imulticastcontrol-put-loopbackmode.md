---
description: Das put \_ loopbackmode legt den Multicast-Loopback Modus fest.
ms.assetid: 38b28529-224f-4624-bb5e-22fee500e8e6
title: Imulticastcontrol::p ut_LoopbackMode-Methode (confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5b5e51b3814b380cc06d9c960db1a4e4b9ecb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354732"
---
# <a name="imulticastcontrolput_loopbackmode-method"></a><span data-ttu-id="c7637-103">Imulticastcontrol::p UT \_ loopbackmode-Methode</span><span class="sxs-lookup"><span data-stu-id="c7637-103">IMulticastControl::put\_LoopbackMode method</span></span>

<span data-ttu-id="c7637-104">\[**Put \_ Loopbackmode** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c7637-104">\[**put\_LoopbackMode** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c7637-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="c7637-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c7637-106">Das **Put \_ loopbackmode** legt den Multicast-Loopback Modus fest.</span><span class="sxs-lookup"><span data-stu-id="c7637-106">The **put\_LoopbackMode** sets the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7637-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7637-107">Syntax</span></span>


```C++
HRESULT put_LoopbackMode(
  [in] MULTICAST_LOOPBACK_MODE mode
);
```



## <a name="parameters"></a><span data-ttu-id="c7637-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7637-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7637-109">*Modus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7637-109">*mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7637-110">[**Multicast \_ Der Loopback \_ Modus**](multicast-loopback-mode.md) -Deskriptor des neuen Loopback Modus.</span><span class="sxs-lookup"><span data-stu-id="c7637-110">[**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md) descriptor of the new loopback mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7637-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7637-111">Return value</span></span>

<span data-ttu-id="c7637-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c7637-112">This method can return one of these values.</span></span>



| <span data-ttu-id="c7637-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c7637-113">Return code</span></span>                                                                                  | <span data-ttu-id="c7637-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7637-114">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="c7637-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c7637-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c7637-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c7637-116">Method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="c7637-117"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="c7637-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c7637-118">Der *Mode* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7637-118">The *mode* parameter is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c7637-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7637-119">Requirements</span></span>



| <span data-ttu-id="c7637-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7637-120">Requirement</span></span> | <span data-ttu-id="c7637-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c7637-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7637-122">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="c7637-122">TAPI version</span></span><br/> | <span data-ttu-id="c7637-123">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c7637-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c7637-124">Header</span><span class="sxs-lookup"><span data-stu-id="c7637-124">Header</span></span><br/>       | <dl> <span data-ttu-id="c7637-125"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="c7637-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="c7637-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c7637-126">Library</span></span><br/>      | <dl> <span data-ttu-id="c7637-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7637-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c7637-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c7637-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="c7637-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7637-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c7637-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7637-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7637-131">**Imulticastcontrol**</span><span class="sxs-lookup"><span data-stu-id="c7637-131">**IMulticastControl**</span></span>](imulticastcontrol.md)
</dt> </dl>

 

 




