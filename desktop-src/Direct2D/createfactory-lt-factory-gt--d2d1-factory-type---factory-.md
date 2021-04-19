---
title: D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, Factory)-Funktion (D2D1. h)
description: Erstellt ein Factory-Objekt, das zum Erstellen von Direct2D-Ressourcen verwendet werden kann. | D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, Factory)-Funktion (D2D1. h)
ms.assetid: c1c25d51-15ea-4075-a896-bd6501bf68c1
keywords:
- D2D1CreateFactory Factory-Funktion (D2D1_FACTORY_TYPE, Factory) Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03400cec8c838ba561a7eb504674e074d7b3199
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106373477"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typefactory-function"></a><span data-ttu-id="5af9b-105">D2D1CreateFactory <Factory> (D2D1 \_ Factory \_ Type, Factory \* \* )-Funktion</span><span class="sxs-lookup"><span data-stu-id="5af9b-105">D2D1CreateFactory<Factory>(D2D1\_FACTORY\_TYPE,Factory\*\*) Function</span></span>

<span data-ttu-id="5af9b-106">Erstellt ein Factory-Objekt, das zum Erstellen von Direct2D-Ressourcen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5af9b-106">Creates a factory object that can be used to create Direct2D resources.</span></span>

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __out Factory **factory
);
```

## <a name="template-parameters"></a><span data-ttu-id="5af9b-107">Vorlagenparameter</span><span class="sxs-lookup"><span data-stu-id="5af9b-107">Template Parameters</span></span>



| <span data-ttu-id="5af9b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5af9b-108">Parameter</span></span> | <span data-ttu-id="5af9b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5af9b-109">Description</span></span>                                                 |
|-----------|-------------------------------------------------------------|
| <span data-ttu-id="5af9b-110">*Schen*</span><span class="sxs-lookup"><span data-stu-id="5af9b-110">*Factory*</span></span> | <span data-ttu-id="5af9b-111">Der Typ des zu erstellenden [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) .</span><span class="sxs-lookup"><span data-stu-id="5af9b-111">The type of [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) to create.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="5af9b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5af9b-112">Parameters</span></span>



| <span data-ttu-id="5af9b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5af9b-113">Parameter</span></span>     | <span data-ttu-id="5af9b-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5af9b-114">Description</span></span>                                                                     |
|---------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="5af9b-115">*factoryType*</span><span class="sxs-lookup"><span data-stu-id="5af9b-115">*factoryType*</span></span> | <span data-ttu-id="5af9b-116">Das Threading Modell der Factory und der von ihr erstellten Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="5af9b-116">The threading model of the factory and the resources it creates.</span></span>                |
| <span data-ttu-id="5af9b-117">*Fabrik*</span><span class="sxs-lookup"><span data-stu-id="5af9b-117">*factory*</span></span>     | <span data-ttu-id="5af9b-118">Wenn diese Methode zurückgegeben wird, enthält Sie die Adresse eines Zeigers auf die neue Factory.</span><span class="sxs-lookup"><span data-stu-id="5af9b-118">When this method returns, contains the address of a pointer to the new factory.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="5af9b-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5af9b-119">Return Value</span></span>

<span data-ttu-id="5af9b-120">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5af9b-120">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5af9b-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5af9b-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="examples"></a><span data-ttu-id="5af9b-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5af9b-122">Examples</span></span>

<span data-ttu-id="5af9b-123">Im folgenden Beispiel wird eine Factory erstellt.</span><span class="sxs-lookup"><span data-stu-id="5af9b-123">The following example creates a factory.</span></span>


```C++
HRESULT DemoApp::CreateDeviceIndependentResources()
{
    HRESULT hr = S_OK;

    // Create a Direct2D factory.
    hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="5af9b-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5af9b-124">Requirements</span></span>



| <span data-ttu-id="5af9b-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5af9b-125">Requirement</span></span> | <span data-ttu-id="5af9b-126">Wert</span><span class="sxs-lookup"><span data-stu-id="5af9b-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5af9b-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5af9b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5af9b-128">Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="5af9b-128">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="5af9b-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5af9b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5af9b-130">Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="5af9b-130">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="5af9b-131">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="5af9b-131">Minimum supported phone</span></span><br/>  | <span data-ttu-id="5af9b-132">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="5af9b-132">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="5af9b-133">Header</span><span class="sxs-lookup"><span data-stu-id="5af9b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5af9b-134"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="5af9b-134"><dt>D2d1.h</dt></span></span> </dl>                                                        |
| <span data-ttu-id="5af9b-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5af9b-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="5af9b-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5af9b-136"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="5af9b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="5af9b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5af9b-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5af9b-138"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

