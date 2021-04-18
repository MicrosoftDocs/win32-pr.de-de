---
title: Wmdrmkreateprotectedprovider-Funktion (wmdrmsdk. h)
description: Die wmdrmkreateprotectedprovider-Funktion erstellt eine Klassenfactory, die die anderen Objekte der erweiterten APIs für den Windows Media DRM-Client erstellen kann.
ms.assetid: 0882062f-48a2-43bc-8853-a8a3d6bc2f52
keywords:
- Wmdrmkreateprotectedprovider-Funktion Windows Media-Format
topic_type:
- apiref
api_name:
- WMDRMCreateProtectedProvider
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f046de906c7753fa200de5075cf2064721940b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365923"
---
# <a name="wmdrmcreateprotectedprovider-function"></a><span data-ttu-id="ca16e-104">Wmdrmkreateprotectedprovider-Funktion</span><span class="sxs-lookup"><span data-stu-id="ca16e-104">WMDRMCreateProtectedProvider function</span></span>

<span data-ttu-id="ca16e-105">Die **wmdrmkreateprotectedprovider** -Funktion erstellt eine Klassenfactory, die die anderen Objekte der erweiterten APIs für den Windows Media DRM-Client erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="ca16e-105">The **WMDRMCreateProtectedProvider** function creates a class factory that can create the other objects of the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="ca16e-106">Diese Funktion erfordert eine stubbibliothek von Microsoft und erstellt Objekte, die die geschützten DRM-Features unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ca16e-106">This function requires a stub library from Microsoft and creates objects that support the protected DRM features.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca16e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca16e-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProtectedProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a><span data-ttu-id="ca16e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca16e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca16e-109">*ppdrmprovider* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ca16e-109">*ppDRMProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca16e-110">Empfängt einen Zeiger auf die [**iwmdrmprovider**](iwmdrmprovider.md) -Schnittstelle des neu erstellten Objekts.</span><span class="sxs-lookup"><span data-stu-id="ca16e-110">Receives a pointer to the [**IWMDRMProvider**](iwmdrmprovider.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca16e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca16e-111">Return value</span></span>

<span data-ttu-id="ca16e-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="ca16e-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ca16e-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ca16e-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ca16e-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ca16e-114">Return code</span></span>                                                                          | <span data-ttu-id="ca16e-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca16e-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ca16e-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ca16e-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ca16e-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca16e-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ca16e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca16e-118">Remarks</span></span>

<span data-ttu-id="ca16e-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="ca16e-119">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca16e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca16e-120">Requirements</span></span>



| <span data-ttu-id="ca16e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca16e-121">Requirement</span></span> | <span data-ttu-id="ca16e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ca16e-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca16e-123">Header</span><span class="sxs-lookup"><span data-stu-id="ca16e-123">Header</span></span><br/> | <dl> <span data-ttu-id="ca16e-124"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca16e-124"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca16e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca16e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca16e-126">**Funktionen**</span><span class="sxs-lookup"><span data-stu-id="ca16e-126">**Functions**</span></span>](drm-functions.md)
</dt> <dt>

[<span data-ttu-id="ca16e-127">**Wmdrmkreateprovider**</span><span class="sxs-lookup"><span data-stu-id="ca16e-127">**WMDRMCreateProvider**</span></span>](wmdrmcreateprovider.md)
</dt> </dl>

 

 





