---
description: Überspringt die angegebene Anzahl von Geräten in der enumerationssequenz.
ms.assetid: 38b72b80-93f5-433e-977c-e3ee503daae5
title: 'Ienumportabledeviceconnectors:: Skip-Methode (devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Skip
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: c00daecccd12beee8e9e741c2906e47484fa6da3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042618"
---
# <a name="ienumportabledeviceconnectorsskip-method"></a><span data-ttu-id="4c938-103">Ienumportabledeviceconnectors:: Skip-Methode</span><span class="sxs-lookup"><span data-stu-id="4c938-103">IEnumPortableDeviceConnectors::Skip method</span></span>

<span data-ttu-id="4c938-104">Die **Skip** -Methode überspringt die angegebene Anzahl von Geräten in der enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="4c938-104">The **Skip** method skips the specified number of devices in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c938-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c938-105">Syntax</span></span>


```C++
HRESULT Skip(
  [in] UINT32 cConnectors
);
```



## <a name="parameters"></a><span data-ttu-id="4c938-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c938-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c938-107">*cconnectors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c938-107">*cConnectors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c938-108">Die Anzahl der zu über springenden Geräte.</span><span class="sxs-lookup"><span data-stu-id="4c938-108">The number of devices to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c938-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4c938-109">Return value</span></span>

<span data-ttu-id="4c938-110">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="4c938-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4c938-111">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4c938-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4c938-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4c938-112">Return code</span></span>                                                                             | <span data-ttu-id="4c938-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c938-113">Description</span></span>                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c938-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4c938-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="4c938-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4c938-115">The method succeeded.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="4c938-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4c938-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="4c938-117">Die angegebene Anzahl von Geräten konnte nicht übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="4c938-117">The specified number of devices could not be skipped.</span></span> <span data-ttu-id="4c938-118">Eine mögliche Ursache: der *cconnectors* -Parameter gibt mehr Geräte an, als Sie tatsächlich in der enumerationssequenz verbleiben.</span><span class="sxs-lookup"><span data-stu-id="4c938-118">One possible cause: The *cConnectors* parameter specifies more devices than actually remain in the enumeration sequence.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4c938-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c938-119">Requirements</span></span>



| <span data-ttu-id="4c938-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c938-120">Requirement</span></span> | <span data-ttu-id="4c938-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4c938-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c938-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4c938-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4c938-123">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c938-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="4c938-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4c938-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4c938-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c938-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                   |
| <span data-ttu-id="4c938-126">Header</span><span class="sxs-lookup"><span data-stu-id="4c938-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c938-127"><dt>Devpkey. h; </dt> <dt>Portablede viceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c938-127"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="4c938-128">IDL</span><span class="sxs-lookup"><span data-stu-id="4c938-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4c938-129"><dt>Portablede viceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4c938-129"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="4c938-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4c938-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="4c938-131"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c938-131"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="4c938-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c938-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c938-133">**Ienumportablede viceconnectors**</span><span class="sxs-lookup"><span data-stu-id="4c938-133">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




