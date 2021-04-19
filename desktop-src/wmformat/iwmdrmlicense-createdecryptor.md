---
title: Iwmdrmlicense-Methode "deatedecryptor" (wmdrmsdk. h)
description: Die Methode "kreatedecryptor" erstellt mithilfe der Einstellungen der aktuellen Lizenz ein Entschlüsselungs-Objekt.
ms.assetid: 69b7f96b-a0d6-455e-8ef9-0faf9690cef1
keywords:
- Methode "Windows Media" der Methode "kreatedecryptor"
- Methode "deatedecryptor" Windows Media Format, iwmdrmlicense Interface
- Iwmdrmlicense-Schnittstelle Windows Media-Format, Methode "kreatedecryptor"
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e987e7ffa3390462889b128f390934f05e64cdff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353799"
---
# <a name="iwmdrmlicensecreatedecryptor-method"></a><span data-ttu-id="c602e-106">Iwmdrmlicense:: kreatedecryptor-Methode</span><span class="sxs-lookup"><span data-stu-id="c602e-106">IWMDRMLicense::CreateDecryptor method</span></span>

<span data-ttu-id="c602e-107">Die Methode " **kreatedecryptor** " erstellt mithilfe der Einstellungen der aktuellen Lizenz ein Entschlüsselungs-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c602e-107">The **CreateDecryptor** method creates a decryptor object using the settings of the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="c602e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c602e-108">Syntax</span></span>


```C++
HRESULT CreateDecryptor(
  [out] IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a><span data-ttu-id="c602e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c602e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c602e-110">*ppdecryptor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c602e-110">*ppDecryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c602e-111">Empfängt einen Zeiger auf die [**iwmdrmentschlüsseln**](iwmdrmdecrypt.md) -Schnittstelle des neu erstellten Objekts.</span><span class="sxs-lookup"><span data-stu-id="c602e-111">Receives a pointer to the [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c602e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c602e-112">Return value</span></span>

<span data-ttu-id="c602e-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="c602e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c602e-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c602e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c602e-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c602e-115">Return code</span></span>                                                                                                | <span data-ttu-id="c602e-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c602e-116">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="c602e-117"><dt>**NS \_ E \_ DRM- \_ RIV \_ zu \_ klein**</dt></span><span class="sxs-lookup"><span data-stu-id="c602e-117"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="c602e-118">Es wird eine aktualisierte Inhalts Sperr Liste benötigt.</span><span class="sxs-lookup"><span data-stu-id="c602e-118">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="c602e-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c602e-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="c602e-120">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c602e-120">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="c602e-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c602e-121">Remarks</span></span>

<span data-ttu-id="c602e-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="c602e-122">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="c602e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c602e-123">Requirements</span></span>



| <span data-ttu-id="c602e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c602e-124">Requirement</span></span> | <span data-ttu-id="c602e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c602e-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c602e-126">Header</span><span class="sxs-lookup"><span data-stu-id="c602e-126">Header</span></span><br/> | <dl> <span data-ttu-id="c602e-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="c602e-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c602e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c602e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c602e-129">**CreateEncryptor**</span><span class="sxs-lookup"><span data-stu-id="c602e-129">**CreateEncryptor**</span></span>](iwmdrmlicense-createencryptor.md)
</dt> <dt>

[<span data-ttu-id="c602e-130">**Iwmdrmlicense-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c602e-130">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





