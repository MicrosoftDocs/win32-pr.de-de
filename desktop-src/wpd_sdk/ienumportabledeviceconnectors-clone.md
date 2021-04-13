---
description: Erstellt eine Kopie der aktuellen ienumportabledebug Controller-Schnittstelle.
ms.assetid: 64274cb0-1f57-481d-914f-41238cbe2f1b
title: 'Ienumportabledeviceconnectors:: Clone-Methode (devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Clone
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 0e5273f1c400732c94c7c63918787f5e130a854d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348568"
---
# <a name="ienumportabledeviceconnectorsclone-method"></a><span data-ttu-id="acdd5-103">Ienumportabledeviceconnectors:: Clone-Methode</span><span class="sxs-lookup"><span data-stu-id="acdd5-103">IEnumPortableDeviceConnectors::Clone method</span></span>

<span data-ttu-id="acdd5-104">Die **Clone** -Methode erstellt eine Kopie der aktuellen [**ienumportabledeviceconnectors**](ienumportabledeviceconnectors.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="acdd5-104">The **Clone** method creates a copy of the current [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="acdd5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="acdd5-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPortableDeviceConnectors **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="acdd5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="acdd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acdd5-107">*ppum* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="acdd5-107">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acdd5-108">Die Adresse eines Zeigers auf eine [**ienumportabledebug Controller**](ienumportabledeviceconnectors.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="acdd5-108">The address of a pointer to an [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) interface.</span></span> <span data-ttu-id="acdd5-109">Diese Schnittstelle muss von der aufrufenden Anwendung freigegeben werden, wenn Sie damit abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="acdd5-109">The calling application must release this interface when it is done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acdd5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="acdd5-110">Return value</span></span>

<span data-ttu-id="acdd5-111">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="acdd5-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="acdd5-112">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="acdd5-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="acdd5-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="acdd5-113">Return code</span></span>                                                                          | <span data-ttu-id="acdd5-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="acdd5-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="acdd5-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="acdd5-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="acdd5-116">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="acdd5-116">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="acdd5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="acdd5-117">Requirements</span></span>



| <span data-ttu-id="acdd5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="acdd5-118">Requirement</span></span> | <span data-ttu-id="acdd5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="acdd5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acdd5-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="acdd5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="acdd5-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="acdd5-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="acdd5-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="acdd5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="acdd5-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="acdd5-123">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="acdd5-124">Header</span><span class="sxs-lookup"><span data-stu-id="acdd5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="acdd5-125"><dt>Devpkey. h; </dt> <dt>Portablede viceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="acdd5-125"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="acdd5-126">IDL</span><span class="sxs-lookup"><span data-stu-id="acdd5-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="acdd5-127"><dt>Portablede viceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="acdd5-127"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="acdd5-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="acdd5-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="acdd5-129"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="acdd5-129"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="acdd5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="acdd5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acdd5-131">**Ienumportablede viceconnectors**</span><span class="sxs-lookup"><span data-stu-id="acdd5-131">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




