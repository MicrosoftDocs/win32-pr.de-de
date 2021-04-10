---
title: IMsRdpDeviceCollection2 adddevicebyinstanceid-Methode
description: Fügt der Geräte Sammlung ein nicht aufgeführtes Gerät hinzu.
ms.assetid: 7ef200c5-b99e-40c9-80e1-0758ddfa0902
ms.tgt_platform: multiple
keywords:
- Adddevicebyinstanceid-Methode Remotedesktopdienste
- Adddevicebyinstanceid-Methode Remotedesktopdienste, IMsRdpDeviceCollection2-Schnittstelle
- IMsRdpDeviceCollection2 Interface Remotedesktopdienste, adddevicebyinstanceid-Methode
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.AddDeviceByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f817a5beb4d8762787c4bf2f8a3995d3918e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040124"
---
# <a name="imsrdpdevicecollection2adddevicebyinstanceid-method"></a><span data-ttu-id="b3612-106">IMsRdpDeviceCollection2:: adddevicebyinstanceid-Methode</span><span class="sxs-lookup"><span data-stu-id="b3612-106">IMsRdpDeviceCollection2::AddDeviceByInstanceId method</span></span>

<span data-ttu-id="b3612-107">Fügt der Geräte Sammlung ein nicht aufgeführtes Gerät hinzu.</span><span class="sxs-lookup"><span data-stu-id="b3612-107">Adds an unlisted device to the device collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3612-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3612-108">Syntax</span></span>


```C++
HRESULT AddDeviceByInstanceId(
  [in] RedirectDeviceType Type,
  [in] BSTR               InstanceId
);
```



## <a name="parameters"></a><span data-ttu-id="b3612-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3612-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3612-110">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3612-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3612-111">Type: **[ **redirectdevicetype**](redirectdevicetype.md)**</span><span class="sxs-lookup"><span data-stu-id="b3612-111">Type: **[**RedirectDeviceType**](redirectdevicetype.md)**</span></span>

<span data-ttu-id="b3612-112">Ein Wert der [**redirectdevicetype**](redirectdevicetype.md) -Enumeration, der den Typ des hinzugefügten Geräts angibt.</span><span class="sxs-lookup"><span data-stu-id="b3612-112">A value of the [**RedirectDeviceType**](redirectdevicetype.md) enumeration that specifies the type of device being added.</span></span>

</dd> <dt>

<span data-ttu-id="b3612-113">*InstanceId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3612-113">*InstanceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3612-114">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b3612-114">Type: **BSTR**</span></span>

<span data-ttu-id="b3612-115">Der Instanzbezeichner des hinzu zufügenden Geräts.</span><span class="sxs-lookup"><span data-stu-id="b3612-115">The instance identifier of the device to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3612-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3612-116">Return value</span></span>

<span data-ttu-id="b3612-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b3612-117">Type: **HRESULT**</span></span>

<span data-ttu-id="b3612-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b3612-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b3612-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b3612-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3612-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3612-120">Requirements</span></span>



| <span data-ttu-id="b3612-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3612-121">Requirement</span></span> | <span data-ttu-id="b3612-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b3612-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3612-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3612-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b3612-124">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b3612-124">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="b3612-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3612-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b3612-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b3612-126">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="b3612-127">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b3612-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="b3612-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3612-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b3612-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b3612-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3612-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3612-130"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3612-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3612-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3612-132">**Redirectde vicetype**</span><span class="sxs-lookup"><span data-stu-id="b3612-132">**RedirectDeviceType**</span></span>](redirectdevicetype.md)
</dt> <dt>

[<span data-ttu-id="b3612-133">**IMsRdpDeviceCollection2**</span><span class="sxs-lookup"><span data-stu-id="b3612-133">**IMsRdpDeviceCollection2**</span></span>](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





