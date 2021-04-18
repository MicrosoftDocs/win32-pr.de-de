---
title: Iwmdrmdevice iswmdrmdevice-Methode
description: Die iswmdrmdevice-Methode bestimmt, ob das Gerät Windows Media DRM 10 für tragbare Geräte unterstützt.
ms.assetid: 247e7a77-e805-4848-893f-f5522c161232
keywords:
- Iswmdrmdevice-Methode, Windows Media Device Manager
- Iswmdrmdevice-Methode Windows Media Device Manager, iwmdrmdevice-Schnittstelle
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager, iswmdrmdevice-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice.IsWMDRMDevice
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9cb79598ea41a996748e383c8fdfc63364dd6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364926"
---
# <a name="iwmdrmdeviceiswmdrmdevice-method"></a><span data-ttu-id="db6e9-106">Iwmdrmdevice:: iswmdrmdevice-Methode</span><span class="sxs-lookup"><span data-stu-id="db6e9-106">IWMDRMDevice::IsWMDRMDevice method</span></span>

<span data-ttu-id="db6e9-107">Die **iswmdrmdevice** -Methode bestimmt, ob das Gerät Windows Media DRM 10 für tragbare Geräte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="db6e9-107">The **IsWMDRMDevice** method determines whether the device supports Windows Media DRM 10 for Portable Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="db6e9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="db6e9-108">Syntax</span></span>


```C++
HRESULT IsWMDRMDevice(
  [out] DWORD *pdwVersion
);
```



## <a name="parameters"></a><span data-ttu-id="db6e9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="db6e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db6e9-110">*pdwversion* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="db6e9-110">*pdwVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db6e9-111">Version von Windows Media DRM 10 für tragbare Geräte, die den Wert 0x00010000 bis haben.</span><span class="sxs-lookup"><span data-stu-id="db6e9-111">Version of Windows Media DRM 10 for Portable Devices, which has value of 0x00010000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db6e9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db6e9-112">Return value</span></span>

<span data-ttu-id="db6e9-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="db6e9-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="db6e9-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="db6e9-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="db6e9-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="db6e9-115">Return code</span></span>                                                                          | <span data-ttu-id="db6e9-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db6e9-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="db6e9-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="db6e9-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="db6e9-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="db6e9-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="db6e9-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db6e9-119">Requirements</span></span>



| <span data-ttu-id="db6e9-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db6e9-120">Requirement</span></span> | <span data-ttu-id="db6e9-121">Wert</span><span class="sxs-lookup"><span data-stu-id="db6e9-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db6e9-122">Header</span><span class="sxs-lookup"><span data-stu-id="db6e9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="db6e9-123"><dt>Wmddrmsp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="db6e9-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="db6e9-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="db6e9-124">Library</span></span><br/> | <dl> <span data-ttu-id="db6e9-125"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db6e9-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db6e9-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db6e9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db6e9-127">**Iwmdrmdevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="db6e9-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





