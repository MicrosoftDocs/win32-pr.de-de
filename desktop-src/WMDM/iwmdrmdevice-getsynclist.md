---
title: Methode "iwmdrmdevice getsynclist"
description: Die getsynclist-Methode ruft die Lizenz Synchronisierungs Liste auf dem Gerät ab. Mit der Lizenz Synchronisierung kann der Host Computer aktualisierte Lizenzen gemäß den angegebenen Kriterien auf ein Gerät übertragen.
ms.assetid: 772ac03b-3339-4c5f-a8fc-1c216ec665b7
keywords:
- Getsynclist-Methode, Windows Media Device Manager
- Getsynclist-Methode Windows Media Device Manager, iwmdrmdevice-Schnittstelle
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager, getsynclist-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381d410bd938cb90855b182e62354d48e72f16d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356446"
---
# <a name="iwmdrmdevicegetsynclist-method"></a><span data-ttu-id="0eec8-107">Iwmdrmdevice:: getsynclist-Methode</span><span class="sxs-lookup"><span data-stu-id="0eec8-107">IWMDRMDevice::GetSyncList method</span></span>

<span data-ttu-id="0eec8-108">Die **getsynclist** -Methode ruft die Lizenz Synchronisierungs Liste auf dem Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="0eec8-108">The **GetSyncList** method retrieves the license synchronization list on the device.</span></span> <span data-ttu-id="0eec8-109">Mit der Lizenz Synchronisierung kann der Host Computer aktualisierte Lizenzen gemäß den angegebenen Kriterien auf ein Gerät übertragen.</span><span class="sxs-lookup"><span data-stu-id="0eec8-109">License synchronization allows the host computer to transfer updated licenses to a device according to the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eec8-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0eec8-110">Syntax</span></span>


```C++
HRESULT GetSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList
);
```



## <a name="parameters"></a><span data-ttu-id="0eec8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0eec8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0eec8-112">*cminzählthreshold* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0eec8-112">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0eec8-113">Schwellenwert für minimale Anzahl.</span><span class="sxs-lookup"><span data-stu-id="0eec8-113">Minimum count threshold.</span></span>

</dd> <dt>

<span data-ttu-id="0eec8-114">*cminhoursthreshold* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0eec8-114">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0eec8-115">Schwellenwert für minimale Stunden.</span><span class="sxs-lookup"><span data-stu-id="0eec8-115">Minimum hours threshold.</span></span>

</dd> <dt>

<span data-ttu-id="0eec8-116">*ppbsynclist* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0eec8-116">*ppbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0eec8-117">Abgerufene Lizenz Synchronisierungs Liste.</span><span class="sxs-lookup"><span data-stu-id="0eec8-117">Retrieved license synchronization list.</span></span>

</dd> <dt>

<span data-ttu-id="0eec8-118">*pcbsynclist* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0eec8-118">*pcbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0eec8-119">Größe der Lizenz Synchronisierungs Liste in Bytes.</span><span class="sxs-lookup"><span data-stu-id="0eec8-119">Size of the license synchronization list, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0eec8-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0eec8-120">Return value</span></span>

<span data-ttu-id="0eec8-121">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="0eec8-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0eec8-122">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0eec8-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0eec8-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0eec8-123">Return code</span></span>                                                                          | <span data-ttu-id="0eec8-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0eec8-124">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0eec8-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0eec8-125"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0eec8-126">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0eec8-126">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0eec8-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0eec8-127">Requirements</span></span>



| <span data-ttu-id="0eec8-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0eec8-128">Requirement</span></span> | <span data-ttu-id="0eec8-129">Wert</span><span class="sxs-lookup"><span data-stu-id="0eec8-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0eec8-130">Header</span><span class="sxs-lookup"><span data-stu-id="0eec8-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0eec8-131"><dt>Wmddrmsp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0eec8-131"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="0eec8-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0eec8-132">Library</span></span><br/> | <dl> <span data-ttu-id="0eec8-133"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0eec8-133"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0eec8-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0eec8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eec8-135">**Iwmdrmdevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0eec8-135">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





