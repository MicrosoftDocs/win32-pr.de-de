---
title: Iwmdrmdevice-cleandatastore-Methode
description: Die cleandatastore-Methode startet das Bereinigen des DRM-Datenspeicher auf dem Gerät.
ms.assetid: aad99137-6d2b-4612-8014-9783035af929
keywords:
- Cleandatastore-Methode Windows Media Device Manager
- Cleandatastore-Methode Windows Media Device Manager, iwmdrmdevice-Schnittstelle
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager, cleandatastore-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice.CleanDataStore
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5aed9608a7428245edd84602ea5e7252861d938
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365160"
---
# <a name="iwmdrmdevicecleandatastore-method"></a><span data-ttu-id="8ffc2-106">Iwmdrmdevice:: cleandatastore-Methode</span><span class="sxs-lookup"><span data-stu-id="8ffc2-106">IWMDRMDevice::CleanDataStore method</span></span>

<span data-ttu-id="8ffc2-107">Die **cleandatastore** -Methode startet das Bereinigen des DRM-Datenspeicher auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="8ffc2-107">The **CleanDataStore** method starts the process of cleaning the DRM data store on the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ffc2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ffc2-108">Syntax</span></span>


```C++
HRESULT CleanDataStore(
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8ffc2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ffc2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ffc2-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ffc2-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffc2-111">Flags für die Speicher Bereinigungs Kriterien.</span><span class="sxs-lookup"><span data-stu-id="8ffc2-111">Flags for store cleaning criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ffc2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ffc2-112">Return value</span></span>

<span data-ttu-id="8ffc2-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="8ffc2-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8ffc2-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8ffc2-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8ffc2-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8ffc2-115">Return code</span></span>                                                                          | <span data-ttu-id="8ffc2-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ffc2-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8ffc2-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8ffc2-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8ffc2-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ffc2-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8ffc2-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ffc2-119">Requirements</span></span>



| <span data-ttu-id="8ffc2-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ffc2-120">Requirement</span></span> | <span data-ttu-id="8ffc2-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8ffc2-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ffc2-122">Header</span><span class="sxs-lookup"><span data-stu-id="8ffc2-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8ffc2-123"><dt>Wmddrmsp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8ffc2-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="8ffc2-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8ffc2-124">Library</span></span><br/> | <dl> <span data-ttu-id="8ffc2-125"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ffc2-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ffc2-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ffc2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ffc2-127">**Iwmdrmdevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8ffc2-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





