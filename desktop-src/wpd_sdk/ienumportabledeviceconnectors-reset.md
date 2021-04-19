---
description: Setzt die Enumerationsfolge auf den Anfang zurück.
ms.assetid: 1df1ff95-06ae-4e5e-8064-17f832c5f0b3
title: 'Ienumportabledeviceconnectors:: Reset-Methode (devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Reset
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 3a6846ea928afb6cd52f20098cd100b94b3a564e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355436"
---
# <a name="ienumportabledeviceconnectorsreset-method"></a><span data-ttu-id="da9e8-103">Ienumportabledeviceconnectors:: Reset-Methode</span><span class="sxs-lookup"><span data-stu-id="da9e8-103">IEnumPortableDeviceConnectors::Reset method</span></span>

<span data-ttu-id="da9e8-104">Die **Reset** -Methode setzt die Enumerationsfolge auf den Anfang zurück.</span><span class="sxs-lookup"><span data-stu-id="da9e8-104">The **Reset** method resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="da9e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da9e8-105">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="da9e8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da9e8-106">Parameters</span></span>

<span data-ttu-id="da9e8-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="da9e8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="da9e8-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da9e8-108">Return value</span></span>

<span data-ttu-id="da9e8-109">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="da9e8-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="da9e8-110">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="da9e8-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="da9e8-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="da9e8-111">Return code</span></span>                                                                          | <span data-ttu-id="da9e8-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da9e8-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="da9e8-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="da9e8-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="da9e8-114">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da9e8-114">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="da9e8-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da9e8-115">Requirements</span></span>



| <span data-ttu-id="da9e8-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da9e8-116">Requirement</span></span> | <span data-ttu-id="da9e8-117">Wert</span><span class="sxs-lookup"><span data-stu-id="da9e8-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da9e8-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da9e8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="da9e8-119">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da9e8-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="da9e8-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da9e8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="da9e8-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="da9e8-121">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="da9e8-122">Header</span><span class="sxs-lookup"><span data-stu-id="da9e8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="da9e8-123"><dt>Devpkey. h; </dt> <dt>Portablede viceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="da9e8-123"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="da9e8-124">IDL</span><span class="sxs-lookup"><span data-stu-id="da9e8-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="da9e8-125"><dt>Portablede viceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="da9e8-125"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="da9e8-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="da9e8-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="da9e8-127"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da9e8-127"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="da9e8-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da9e8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da9e8-129">**Ienumportablede viceconnectors**</span><span class="sxs-lookup"><span data-stu-id="da9e8-129">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




