---
title: Iwmdrmprovider-Methode "kreateobject" (wmdrmsdk. h)
description: Die Methode "kreateobject" Ruft einen Zeiger auf eine angegebene Schnittstelle ab und erstellt bei Bedarf das implementierende Objekt.
ms.assetid: d408f7f3-9e49-4747-ac8f-d39db31d1240
keywords:
- Methode "kreateobject" Windows Media Format
- Kreateobject-Methode Windows Media-Format, iwmdrmprovider-Schnittstelle
- Iwmdrmprovider-Schnittstelle Windows Media-Format, Methode "kreateobject"
topic_type:
- apiref
api_name:
- IWMDRMProvider.CreateObject
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c0422138391b0d6f5e38fbc81fd5141bd3d8535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356358"
---
# <a name="iwmdrmprovidercreateobject-method"></a><span data-ttu-id="5d376-106">Iwmdrmprovider:: kreateobject-Methode</span><span class="sxs-lookup"><span data-stu-id="5d376-106">IWMDRMProvider::CreateObject method</span></span>

<span data-ttu-id="5d376-107">Die Methode " **kreateobject** " Ruft einen Zeiger auf eine angegebene Schnittstelle ab und erstellt bei Bedarf das implementierende Objekt.</span><span class="sxs-lookup"><span data-stu-id="5d376-107">The **CreateObject** method retrieves a pointer to a specified interface, creating the implementing object if needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d376-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d376-108">Syntax</span></span>


```C++
HRESULT CreateObject(
  [in]  REFIID riid,
  [out] void   **ppvObject
);
```



## <a name="parameters"></a><span data-ttu-id="5d376-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d376-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d376-110">*riid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d376-110">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d376-111">Der Bezeichner der zu erstellenden Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5d376-111">Identifier of the interface to be created.</span></span> <span data-ttu-id="5d376-112">Legen Sie auf einen der folgenden Werte fest.</span><span class="sxs-lookup"><span data-stu-id="5d376-112">Set to one of the following values.</span></span>

-   <span data-ttu-id="5d376-113">IID \_ iwmdrmlicenabmanagement</span><span class="sxs-lookup"><span data-stu-id="5d376-113">IID\_IWMDRMLicenseManagement</span></span>
-   <span data-ttu-id="5d376-114">IID \_ iwmdrmlicensequery</span><span class="sxs-lookup"><span data-stu-id="5d376-114">IID\_IWMDRMLicenseQuery</span></span>
-   <span data-ttu-id="5d376-115">IID \_ iwmdrmnetreceiver</span><span class="sxs-lookup"><span data-stu-id="5d376-115">IID\_IWMDRMNetReceiver</span></span>
-   <span data-ttu-id="5d376-116">IID \_ iwmdrmnettransmitter</span><span class="sxs-lookup"><span data-stu-id="5d376-116">IID\_IWMDRMNetTransmitter</span></span>
-   <span data-ttu-id="5d376-117">IID \_ iwmdrmsecurity</span><span class="sxs-lookup"><span data-stu-id="5d376-117">IID\_IWMDRMSecurity</span></span>

</dd> <dt>

<span data-ttu-id="5d376-118">*ppvobject* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5d376-118">*ppvObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d376-119">Adresse eines Zeigers, der die Adresse der angeforderten Schnittstelle empfängt.</span><span class="sxs-lookup"><span data-stu-id="5d376-119">Address of a pointer that receives the address of the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d376-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d376-120">Return value</span></span>

<span data-ttu-id="5d376-121">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="5d376-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5d376-122">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5d376-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5d376-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5d376-123">Return code</span></span>                                                                          | <span data-ttu-id="5d376-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d376-124">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5d376-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5d376-125"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5d376-126">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d376-126">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5d376-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d376-127">Remarks</span></span>

<span data-ttu-id="5d376-128">Keine.</span><span class="sxs-lookup"><span data-stu-id="5d376-128">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d376-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d376-129">Requirements</span></span>



| <span data-ttu-id="5d376-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d376-130">Requirement</span></span> | <span data-ttu-id="5d376-131">Wert</span><span class="sxs-lookup"><span data-stu-id="5d376-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d376-132">Header</span><span class="sxs-lookup"><span data-stu-id="5d376-132">Header</span></span><br/>  | <dl> <span data-ttu-id="5d376-133"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d376-133"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d376-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5d376-134">Library</span></span><br/> | <dl> <span data-ttu-id="5d376-135"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d376-135"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d376-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d376-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d376-137">**Iwmdrmprovider-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5d376-137">**IWMDRMProvider Interface**</span></span>](iwmdrmprovider.md)
</dt> <dt>

[<span data-ttu-id="5d376-138">**Iwmdrmlicenabmanagement-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5d376-138">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> <dt>

[<span data-ttu-id="5d376-139">**Iwmdrmlicensequery-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5d376-139">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="5d376-140">**Iwmdrmnetreceiver-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5d376-140">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="5d376-141">**Iwmdrmnettransmitter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5d376-141">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> <dt>

[<span data-ttu-id="5d376-142">**Iwmdrmsecurity-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5d376-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





