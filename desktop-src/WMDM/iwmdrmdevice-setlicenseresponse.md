---
title: Iwmdrmdevice-SetLicenseResponse-Methode
description: Die SetLicenseResponse-Methode legt die Lizenz Antwort fest.
ms.assetid: 1ef3ba9d-d14c-4a20-92d6-0bcb604fd9e2
keywords:
- SetLicenseResponse-Methode, Windows Media Device Manager
- SetLicenseResponse-Methode Windows Media Device Manager, iwmdrmdevice-Schnittstelle
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager, SetLicenseResponse-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetLicenseResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f32a2d27fabe45081b13d658e49171af035b8cc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370057"
---
# <a name="iwmdrmdevicesetlicenseresponse-method"></a><span data-ttu-id="30b03-106">Iwmdrmdevice:: SetLicenseResponse-Methode</span><span class="sxs-lookup"><span data-stu-id="30b03-106">IWMDRMDevice::SetLicenseResponse method</span></span>

<span data-ttu-id="30b03-107">Die **SetLicenseResponse** -Methode legt die Lizenz Antwort fest.</span><span class="sxs-lookup"><span data-stu-id="30b03-107">The **SetLicenseResponse** method sets the license response.</span></span>

## <a name="syntax"></a><span data-ttu-id="30b03-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="30b03-108">Syntax</span></span>


```C++
HRESULT SetLicenseResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a><span data-ttu-id="30b03-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="30b03-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30b03-110">*pbresponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30b03-110">*pbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30b03-111">Gibt die festzulegende Antwort an.</span><span class="sxs-lookup"><span data-stu-id="30b03-111">Specifies the response to be set.</span></span>

</dd> <dt>

<span data-ttu-id="30b03-112">*cbresponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30b03-112">*cbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30b03-113">Die Größe der Antwort in Bytes.</span><span class="sxs-lookup"><span data-stu-id="30b03-113">Size of the response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30b03-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30b03-114">Return value</span></span>

<span data-ttu-id="30b03-115">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="30b03-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="30b03-116">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="30b03-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="30b03-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="30b03-117">Return code</span></span>                                                                          | <span data-ttu-id="30b03-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30b03-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="30b03-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="30b03-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="30b03-120">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="30b03-120">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="30b03-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30b03-121">Requirements</span></span>



| <span data-ttu-id="30b03-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30b03-122">Requirement</span></span> | <span data-ttu-id="30b03-123">Wert</span><span class="sxs-lookup"><span data-stu-id="30b03-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30b03-124">Header</span><span class="sxs-lookup"><span data-stu-id="30b03-124">Header</span></span><br/>  | <dl> <span data-ttu-id="30b03-125"><dt>Wmddrmsp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="30b03-125"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="30b03-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="30b03-126">Library</span></span><br/> | <dl> <span data-ttu-id="30b03-127"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30b03-127"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30b03-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30b03-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30b03-129">**Iwmdrmdevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="30b03-129">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





