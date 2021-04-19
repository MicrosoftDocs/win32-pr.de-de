---
title: "\"Iwmdrmlicenabmanagement\" (storelicense-Methode) (wmdrmsdk. h)"
description: Die storelicense-Methode enthält eine Lizenz, die außerhalb des lokalen DRM-Subsystems im lokalen Lizenz Speicher generiert wurde.
ms.assetid: 2190ff8c-8969-4f03-9f90-331bff8f4da2
keywords:
- Storelicense-Methode Windows Media-Format
- Storelicense-Methode Windows Media-Format, iwmdrmlicensmanagement-Schnittstelle
- Iwmdrmlicenabmanagement-Schnittstelle Windows Media-Format, storelicense-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.StoreLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcfde6347e099ceb9fc168e1183cbd62c90f9b9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369979"
---
# <a name="iwmdrmlicensemanagementstorelicense-method"></a><span data-ttu-id="59028-106">Iwmdrmlicenabmanagement:: storelicense-Methode</span><span class="sxs-lookup"><span data-stu-id="59028-106">IWMDRMLicenseManagement::StoreLicense method</span></span>

<span data-ttu-id="59028-107">Die **storelicense** -Methode enthält eine Lizenz, die außerhalb des lokalen DRM-Subsystems im lokalen Lizenz Speicher generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="59028-107">The **StoreLicense** method includes a license that was generated outside of the local DRM subsystem in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="59028-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="59028-108">Syntax</span></span>


```C++
HRESULT StoreLicense(
  [in] BSTR bstrLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="59028-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="59028-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59028-110">*bstraulicenseresponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59028-110">*bstrLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59028-111">Lizenz Antwort Zeichenfolge, die decodiert und dem lokalen Lizenz Speicher hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="59028-111">License response string to be decoded and added to the local license store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59028-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59028-112">Return value</span></span>

<span data-ttu-id="59028-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="59028-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="59028-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="59028-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="59028-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="59028-115">Return code</span></span>                                                                          | <span data-ttu-id="59028-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59028-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="59028-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="59028-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="59028-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59028-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="59028-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59028-119">Remarks</span></span>

<span data-ttu-id="59028-120">Mit dieser Methode können Sie XMR-Lizenzen hinzufügen, die Sie im lokalen Lizenz Speicher erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="59028-120">You can use this method to add XMR licenses that you have created to the local license store.</span></span>

## <a name="requirements"></a><span data-ttu-id="59028-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59028-121">Requirements</span></span>



| <span data-ttu-id="59028-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59028-122">Requirement</span></span> | <span data-ttu-id="59028-123">Wert</span><span class="sxs-lookup"><span data-stu-id="59028-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59028-124">Header</span><span class="sxs-lookup"><span data-stu-id="59028-124">Header</span></span><br/>  | <dl> <span data-ttu-id="59028-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="59028-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="59028-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="59028-126">Library</span></span><br/> | <dl> <span data-ttu-id="59028-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59028-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59028-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59028-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59028-129">**Iwmdrmlicenabmanagement-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="59028-129">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





