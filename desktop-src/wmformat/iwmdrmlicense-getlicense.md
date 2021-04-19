---
title: Iwmdrmlicense GetLicense-Methode (wmdrmsdk. h)
description: Die GetLicense-Methode ruft die Lizenz als XML-oder XMR-Daten ab.
ms.assetid: 63317841-fd13-4e83-8b99-e3cab1405050
keywords:
- GetLicense-Methode Windows Media-Format
- GetLicense-Methode Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, GetLicense-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0692afb2ff127f9456e6da3c7546c67ae22ded
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361937"
---
# <a name="iwmdrmlicensegetlicense-method"></a><span data-ttu-id="487e2-106">Iwmdrmlicense:: GetLicense-Methode</span><span class="sxs-lookup"><span data-stu-id="487e2-106">IWMDRMLicense::GetLicense method</span></span>

<span data-ttu-id="487e2-107">Die **GetLicense** -Methode ruft die Lizenz als XML-oder XMR-Daten ab.</span><span class="sxs-lookup"><span data-stu-id="487e2-107">The **GetLicense** method retrieves the license as XML or XMR data.</span></span>

## <a name="syntax"></a><span data-ttu-id="487e2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="487e2-108">Syntax</span></span>


```C++
HRESULT GetLicense(
  [out] BYTE  **ppbLicense,
  [out] DWORD *pcbLicense,
  [out] DWORD *pdwLicenseType
);
```



## <a name="parameters"></a><span data-ttu-id="487e2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="487e2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="487e2-110">*ppblicense* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="487e2-110">*ppbLicense* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="487e2-111">Empfängt die Lizenz.</span><span class="sxs-lookup"><span data-stu-id="487e2-111">Receives the license.</span></span>

</dd> <dt>

<span data-ttu-id="487e2-112">*pcblicense* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="487e2-112">*pcbLicense* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="487e2-113">Empfängt die Größe der Lizenz.</span><span class="sxs-lookup"><span data-stu-id="487e2-113">Receives the size of the license.</span></span>

</dd> <dt>

<span data-ttu-id="487e2-114">*pdwlicensertype* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="487e2-114">*pdwLicenseType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="487e2-115">Empfängt den Typ der zurückgegebenen Lizenz.</span><span class="sxs-lookup"><span data-stu-id="487e2-115">Receives the type of the license returned.</span></span> <span data-ttu-id="487e2-116">Dieser Wert wird auf eine der Konstanten in der folgenden Tabelle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="487e2-116">This value is set to one of the constants in the following table.</span></span>



| <span data-ttu-id="487e2-117">Konstante</span><span class="sxs-lookup"><span data-stu-id="487e2-117">Constant</span></span>                  | <span data-ttu-id="487e2-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="487e2-118">Description</span></span>                            |
|---------------------------|----------------------------------------|
| <span data-ttu-id="487e2-119">WMDRM \_ - \_ Lizenztyp- \_ XML</span><span class="sxs-lookup"><span data-stu-id="487e2-119">WMDRM\_LICENSE\_TYPE\_XML</span></span> | <span data-ttu-id="487e2-120">Die abgerufene Lizenz wird als XML formatiert.</span><span class="sxs-lookup"><span data-stu-id="487e2-120">Retrieved license is formatted as XML.</span></span> |
| <span data-ttu-id="487e2-121">WMDRM \_ - \_ Lizenztyp \_ XMR</span><span class="sxs-lookup"><span data-stu-id="487e2-121">WMDRM\_LICENSE\_TYPE\_XMR</span></span> | <span data-ttu-id="487e2-122">Die abgerufene Lizenz ist als XMR formatiert.</span><span class="sxs-lookup"><span data-stu-id="487e2-122">Retrieved license is formatted as XMR.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="487e2-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="487e2-123">Return value</span></span>

<span data-ttu-id="487e2-124">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="487e2-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="487e2-125">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="487e2-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="487e2-126">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="487e2-126">Return code</span></span>                                                                          | <span data-ttu-id="487e2-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="487e2-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="487e2-128"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="487e2-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="487e2-129">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="487e2-129">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="487e2-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="487e2-130">Remarks</span></span>

<span data-ttu-id="487e2-131">Keine.</span><span class="sxs-lookup"><span data-stu-id="487e2-131">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="487e2-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="487e2-132">Requirements</span></span>



| <span data-ttu-id="487e2-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="487e2-133">Requirement</span></span> | <span data-ttu-id="487e2-134">Wert</span><span class="sxs-lookup"><span data-stu-id="487e2-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="487e2-135">Header</span><span class="sxs-lookup"><span data-stu-id="487e2-135">Header</span></span><br/>  | <dl> <span data-ttu-id="487e2-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="487e2-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="487e2-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="487e2-137">Library</span></span><br/> | <dl> <span data-ttu-id="487e2-138"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="487e2-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="487e2-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="487e2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="487e2-140">**Getliceneinproperty**</span><span class="sxs-lookup"><span data-stu-id="487e2-140">**GetLicenseProperty**</span></span>](iwmdrmlicense-getlicenseproperty.md)
</dt> <dt>

[<span data-ttu-id="487e2-141">**Iwmdrmlicense-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="487e2-141">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





