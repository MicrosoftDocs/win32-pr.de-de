---
title: Wmdrmkreateprovider-Funktion (wmdrmsdk. h)
description: Die wmdrmkreateprovider-Funktion erstellt eine Klassenfactory, die die anderen Objekte der erweiterten APIs für den Windows Media DRM-Client erstellen kann.
ms.assetid: 25ec2fbf-136a-4f40-b2d3-f35b42178c60
keywords:
- Wmdrmkreateprovider-Funktion Windows Media-Format
topic_type:
- apiref
api_name:
- WMDRMCreateProvider
api_location:
- Wmdrmsdk.dll
- Ext-MS-Win-mm-wmdrmsdk-l1-1-0.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cdf7a102d969ce916f8a5692d994c183305409a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370587"
---
# <a name="wmdrmcreateprovider-function"></a><span data-ttu-id="fa543-104">Wmdrmkreateprovider-Funktion</span><span class="sxs-lookup"><span data-stu-id="fa543-104">WMDRMCreateProvider function</span></span>

<span data-ttu-id="fa543-105">Die **wmdrmkreateprovider** -Funktion erstellt eine Klassenfactory, die die anderen Objekte der erweiterten APIs für den Windows Media DRM-Client erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="fa543-105">The **WMDRMCreateProvider** function creates a class factory that can create the other objects of the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="fa543-106">Diese Funktion erfordert keine stubbibliothek von Microsoft und erstellt Objekte, die die geschützten DRM-Funktionen nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fa543-106">This function does not require a stub library from Microsoft and creates objects that do not support the protected DRM features.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa543-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa543-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a><span data-ttu-id="fa543-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa543-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa543-109">*ppdrmprovider* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fa543-109">*ppDRMProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa543-110">Empfängt einen Zeiger auf die [**iwmdrmprovider**](iwmdrmprovider.md) -Schnittstelle des neu erstellten Objekts.</span><span class="sxs-lookup"><span data-stu-id="fa543-110">Receives a pointer to the [**IWMDRMProvider**](iwmdrmprovider.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa543-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa543-111">Return value</span></span>

<span data-ttu-id="fa543-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="fa543-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fa543-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fa543-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fa543-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fa543-114">Return code</span></span>                                                                          | <span data-ttu-id="fa543-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa543-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="fa543-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fa543-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fa543-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa543-117">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fa543-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa543-118">Requirements</span></span>



| <span data-ttu-id="fa543-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa543-119">Requirement</span></span> | <span data-ttu-id="fa543-120">Wert</span><span class="sxs-lookup"><span data-stu-id="fa543-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa543-121">Header</span><span class="sxs-lookup"><span data-stu-id="fa543-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fa543-122"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa543-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa543-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fa543-123">Library</span></span><br/> | <dl> <span data-ttu-id="fa543-124"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa543-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="fa543-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fa543-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="fa543-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa543-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa543-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa543-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa543-128">**Funktionen**</span><span class="sxs-lookup"><span data-stu-id="fa543-128">**Functions**</span></span>](drm-functions.md)
</dt> <dt>

[<span data-ttu-id="fa543-129">**Wmdrmkreateprotectedprovider**</span><span class="sxs-lookup"><span data-stu-id="fa543-129">**WMDRMCreateProtectedProvider**</span></span>](wmdrmcreateprotectedprovider.md)
</dt> </dl>

 

 





