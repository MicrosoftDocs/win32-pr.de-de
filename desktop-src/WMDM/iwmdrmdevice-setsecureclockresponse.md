---
title: Iwmdrmdevice (setsecureclockresponse-Methode)
description: Die setsecureclockresponse-Methode legt die Antwort auf die sichere Uhr fest.
ms.assetid: 3f0a1487-d8c4-478d-bfb0-8d09931fd4b6
keywords:
- Setsecureclockresponse-Methode, Windows Media Device Manager
- Setsecureclockresponse-Methode Windows Media Device Manager, iwmdrmdevice-Schnittstelle
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager, setsecureclockresponse-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetSecureClockResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821aceda734aceb7a80774db05465f31213eec47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365928"
---
# <a name="iwmdrmdevicesetsecureclockresponse-method"></a><span data-ttu-id="53f2c-106">Iwmdrmdevice:: setsecureclockresponse-Methode</span><span class="sxs-lookup"><span data-stu-id="53f2c-106">IWMDRMDevice::SetSecureClockResponse method</span></span>

<span data-ttu-id="53f2c-107">Die **setsecureclockresponse** -Methode legt die Antwort auf die sichere Uhr fest.</span><span class="sxs-lookup"><span data-stu-id="53f2c-107">The **SetSecureClockResponse** method sets the secure clock response.</span></span>

## <a name="syntax"></a><span data-ttu-id="53f2c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="53f2c-108">Syntax</span></span>


```C++
HRESULT SetSecureClockResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a><span data-ttu-id="53f2c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="53f2c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53f2c-110">*pbresponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53f2c-110">*pbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53f2c-111">Die festzulegende sichere Uhr-Antwort.</span><span class="sxs-lookup"><span data-stu-id="53f2c-111">The secure clock response to be set.</span></span>

</dd> <dt>

<span data-ttu-id="53f2c-112">*cbresponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53f2c-112">*cbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53f2c-113">Die angegebene Größe der sicheren Uhr-Antwort in Bytes.</span><span class="sxs-lookup"><span data-stu-id="53f2c-113">The specified size of the secure clock response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53f2c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53f2c-114">Return value</span></span>

<span data-ttu-id="53f2c-115">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="53f2c-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="53f2c-116">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="53f2c-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="53f2c-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="53f2c-117">Return code</span></span>                                                                          | <span data-ttu-id="53f2c-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53f2c-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="53f2c-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="53f2c-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="53f2c-120">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="53f2c-120">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="53f2c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53f2c-121">Requirements</span></span>



| <span data-ttu-id="53f2c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53f2c-122">Requirement</span></span> | <span data-ttu-id="53f2c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="53f2c-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53f2c-124">Header</span><span class="sxs-lookup"><span data-stu-id="53f2c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="53f2c-125"><dt>Wmddrmsp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="53f2c-125"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="53f2c-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="53f2c-126">Library</span></span><br/> | <dl> <span data-ttu-id="53f2c-127"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53f2c-127"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53f2c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53f2c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f2c-129">**Getsecureclock**</span><span class="sxs-lookup"><span data-stu-id="53f2c-129">**GetSecureClock**</span></span>](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[<span data-ttu-id="53f2c-130">**Iwmdrmdevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="53f2c-130">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





