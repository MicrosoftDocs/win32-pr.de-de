---
description: Die getserializedsize-Methode berechnet die Puffergröße, die zum Speichern einer serialisierten iportabledevicevalues-Schnittstelle erforderlich ist.
ms.assetid: 12fa6ed1-ce3b-4c5d-920a-87ff693fe0ea
title: 'Iwpdserializer:: getserializedsize-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetSerializedSize
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7b50f7f6158145cd71125b5e5f26649712bb065b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355273"
---
# <a name="iwpdserializergetserializedsize-method"></a><span data-ttu-id="0b30f-103">Iwpdserializer:: getserializedsize-Methode</span><span class="sxs-lookup"><span data-stu-id="0b30f-103">IWpdSerializer::GetSerializedSize method</span></span>

<span data-ttu-id="0b30f-104">Die **getserializedsize** -Methode berechnet die Puffergröße, die zum Speichern einer serialisierten [**iportabledevicevalues**](iportabledevicevalues.md) -Schnittstelle erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0b30f-104">The **GetSerializedSize** method calculates the buffer size that is required to hold a serialized [**IPortableDeviceValues**](iportabledevicevalues.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b30f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b30f-105">Syntax</span></span>


```C++
HRESULT GetSerializedSize(
  [in]  IPortableDeviceValues *pSource,
  [out] DWORD                 *pdwSize
);
```



## <a name="parameters"></a><span data-ttu-id="0b30f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b30f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b30f-107">*psource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b30f-107">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b30f-108">Zeiger auf eine [**iportabletovicevalues**](iportabledevicevalues.md) -Schnittstelle, deren Größe Sie anfordern möchten.</span><span class="sxs-lookup"><span data-stu-id="0b30f-108">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface whose size you want to request.</span></span>

</dd> <dt>

<span data-ttu-id="0b30f-109">*pdwSize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0b30f-109">*pdwSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b30f-110">Zeiger auf ein **DWORD** , das die für die Serialisierung von *psource* erforderliche Puffergröße in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="0b30f-110">Pointer to a **DWORD** that indicates the buffer size that is required to serialize *pSource*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b30f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b30f-111">Return value</span></span>

<span data-ttu-id="0b30f-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="0b30f-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0b30f-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0b30f-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0b30f-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0b30f-114">Return code</span></span>                                                                                   | <span data-ttu-id="0b30f-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b30f-115">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0b30f-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0b30f-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0b30f-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b30f-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="0b30f-118"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="0b30f-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0b30f-119">Ein erforderliches Zeigerargument war **null**.</span><span class="sxs-lookup"><span data-stu-id="0b30f-119">A required pointer argument was **NULL**.</span></span><br/>                   |
| <dl> <span data-ttu-id="0b30f-120"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="0b30f-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0b30f-121">Es war nicht genügend Arbeitsspeicher verfügbar, um den Puffer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0b30f-121">There was not enough available memory to create the buffer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0b30f-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b30f-122">Requirements</span></span>



| <span data-ttu-id="0b30f-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b30f-123">Requirement</span></span> | <span data-ttu-id="0b30f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="0b30f-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b30f-125">Header</span><span class="sxs-lookup"><span data-stu-id="0b30f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0b30f-126"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b30f-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b30f-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0b30f-127">Library</span></span><br/> | <dl> <span data-ttu-id="0b30f-128"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b30f-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b30f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b30f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b30f-130">**Iwpdserializer-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0b30f-130">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




