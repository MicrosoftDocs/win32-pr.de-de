---
description: 'IEnumPortableDeviceConnectors::Reset-Methode: Setzt die Enumerationssequenz auf den Anfang zurück.'
ms.assetid: 1df1ff95-06ae-4e5e-8064-17f832c5f0b3
title: IEnumPortableDeviceConnectors::Reset-Methode (Devpkey.h)
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
ms.openlocfilehash: 10a356fbb8591568a9f99d9b92d681a46754a960
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083207"
---
# <a name="ienumportabledeviceconnectorsreset-method"></a><span data-ttu-id="6ddaf-103">IEnumPortableDeviceConnectors::Reset-Methode</span><span class="sxs-lookup"><span data-stu-id="6ddaf-103">IEnumPortableDeviceConnectors::Reset method</span></span>

<span data-ttu-id="6ddaf-104">Die **Reset-Methode** setzt die Enumerationssequenz auf den Anfang zurück.</span><span class="sxs-lookup"><span data-stu-id="6ddaf-104">The **Reset** method resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ddaf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ddaf-105">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="6ddaf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ddaf-106">Parameters</span></span>

<span data-ttu-id="6ddaf-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6ddaf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6ddaf-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ddaf-108">Return value</span></span>

<span data-ttu-id="6ddaf-109">Die -Methode gibt ein **HRESULT zurück.**</span><span class="sxs-lookup"><span data-stu-id="6ddaf-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6ddaf-110">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6ddaf-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6ddaf-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6ddaf-111">Return code</span></span>                                                                          | <span data-ttu-id="6ddaf-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ddaf-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6ddaf-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6ddaf-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6ddaf-114">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ddaf-114">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6ddaf-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ddaf-115">Requirements</span></span>



| <span data-ttu-id="6ddaf-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ddaf-116">Requirement</span></span> | <span data-ttu-id="6ddaf-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6ddaf-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ddaf-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ddaf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6ddaf-119">Nur Windows \[ 7-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ddaf-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="6ddaf-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ddaf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6ddaf-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6ddaf-121">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="6ddaf-122">Header</span><span class="sxs-lookup"><span data-stu-id="6ddaf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ddaf-123"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="6ddaf-123"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="6ddaf-124">Idl</span><span class="sxs-lookup"><span data-stu-id="6ddaf-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6ddaf-125"><dt>Portabledeviceconnectapi.idl</dt></span><span class="sxs-lookup"><span data-stu-id="6ddaf-125"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="6ddaf-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6ddaf-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="6ddaf-127"><dt>PortableDeviceGuids.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ddaf-127"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="6ddaf-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6ddaf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ddaf-129">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="6ddaf-129">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




