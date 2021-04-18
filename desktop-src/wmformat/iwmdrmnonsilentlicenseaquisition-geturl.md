---
title: Iwmdrmnonsilentlicenseaquisition getURL-Methode (wmdrmsdk. h)
description: Die getURL-Methode ruft die URL ab, an die die Lizenz Herausforderung gesendet werden soll.
ms.assetid: f65f1984-74bc-4cd0-957e-930aa6a6f6a5
keywords:
- GetURL-Methode Windows Media-Format
- GetURL-Methode Windows Media-Format, iwmdrmnonsilentlicenseaquisition-Schnittstelle
- Iwmdrmnonsilentlicenseaquisition-Schnittstelle Windows Media-Format, getURL-Methode
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetURL
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79212d19d7dbf4a66e2b72dcbdeba9262a9aeddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364604"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongeturl-method"></a><span data-ttu-id="185ae-106">Iwmdrmnonsilentlicenseaquisition:: getURL-Methode</span><span class="sxs-lookup"><span data-stu-id="185ae-106">IWMDRMNonSilentLicenseAquisition::GetURL method</span></span>

<span data-ttu-id="185ae-107">Die **getURL** -Methode ruft die URL ab, an die die Lizenz Herausforderung gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="185ae-107">The **GetURL** method retrieves the URL to which the license challenge should be posted.</span></span>

## <a name="syntax"></a><span data-ttu-id="185ae-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="185ae-108">Syntax</span></span>


```C++
HRESULT GetURL(
  [out] BSTR *pbstrURL
);
```



## <a name="parameters"></a><span data-ttu-id="185ae-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="185ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="185ae-110">*pbstrinurl* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="185ae-110">*pbstrURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="185ae-111">Adresse einer Variablen, die die URL empfängt.</span><span class="sxs-lookup"><span data-stu-id="185ae-111">Address of a variable that receives the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="185ae-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="185ae-112">Return value</span></span>

<span data-ttu-id="185ae-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="185ae-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="185ae-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="185ae-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="185ae-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="185ae-115">Return code</span></span>                                                                          | <span data-ttu-id="185ae-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="185ae-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="185ae-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="185ae-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="185ae-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="185ae-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="185ae-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="185ae-119">Remarks</span></span>

<span data-ttu-id="185ae-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="185ae-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="185ae-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="185ae-121">Requirements</span></span>



| <span data-ttu-id="185ae-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="185ae-122">Requirement</span></span> | <span data-ttu-id="185ae-123">Wert</span><span class="sxs-lookup"><span data-stu-id="185ae-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="185ae-124">Header</span><span class="sxs-lookup"><span data-stu-id="185ae-124">Header</span></span><br/>  | <dl> <span data-ttu-id="185ae-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="185ae-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="185ae-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="185ae-126">Library</span></span><br/> | <dl> <span data-ttu-id="185ae-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="185ae-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="185ae-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="185ae-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="185ae-129">**Iwmdrmnonsilentlicenseaquisition-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="185ae-129">**IWMDRMNonSilentLicenseAquisition Interface**</span></span>](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





