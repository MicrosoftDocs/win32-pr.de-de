---
description: Die getbufferfromiportabledevicevalues-Methode serialisiert eine übermittelte iportabledevicevalues-Schnittstelle zu einem zugeordneten Bytearray. Das zurückgegebene Bytearray wird dem Aufrufer zugeordnet und sollte vom Aufrufer mithilfe von "CoTaskMemFree" freigegeben werden.
ms.assetid: fd856394-9cb3-41cb-875b-1d490ca859df
title: 'Iwpdserializer:: getbufferfromiportabledevicevalues-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetBufferFromIPortableDeviceValues
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44f4e9e7011e6a4766183307e81ef7e783da899f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358221"
---
# <a name="iwpdserializergetbufferfromiportabledevicevalues-method"></a><span data-ttu-id="fa277-104">Iwpdserializer:: getbufferfromiportabledevicevalues-Methode</span><span class="sxs-lookup"><span data-stu-id="fa277-104">IWpdSerializer::GetBufferFromIPortableDeviceValues method</span></span>

<span data-ttu-id="fa277-105">Die **getbufferfromiportabledevicevalues** -Methode serialisiert eine übermittelte **iportabledevicevalues** -Schnittstelle zu einem zugeordneten Bytearray.</span><span class="sxs-lookup"><span data-stu-id="fa277-105">The **GetBufferFromIPortableDeviceValues** method serializes a submitted **IPortableDeviceValues** interface to an allocated byte array.</span></span> <span data-ttu-id="fa277-106">Das zurückgegebene Bytearray wird dem Aufrufer zugeordnet und sollte vom Aufrufer mithilfe von " **CoTaskMemFree**" freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fa277-106">The byte array returned is allocated for the caller and should be freed by the caller using **CoTaskMemFree**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa277-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa277-107">Syntax</span></span>


```C++
HRESULT GetBufferFromIPortableDeviceValues(
  [in]  IPortableDeviceValues *pSource,
  [out] BYTE                  **ppBuffer,
  [out] DWORD                 *pdwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="fa277-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa277-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa277-109">*psource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa277-109">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa277-110">Zeiger auf eine [**iportabledevicevalues**](iportabledevicevalues.md) -Schnittstelle, die serialisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa277-110">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface to serialize.</span></span>

</dd> <dt>

<span data-ttu-id="fa277-111">*ppbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fa277-111">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa277-112">Zeiger auf ein **Byte \* *_, das die serialisierten Daten enthält. Tragbare Windows-Geräte ordnet diesen Arbeitsspeicher zu. der Aufrufer muss ihn durch Aufrufen von _* CoTaskMemFree freigeben**.</span><span class="sxs-lookup"><span data-stu-id="fa277-112">Pointer to a \**BYTE\**_ that contains the serialized data. Windows Portable Devices allocates this memory; the caller must free it by calling _\* CoTaskMemFree\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="fa277-113">*pdwBufferSize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fa277-113">*pdwBufferSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa277-114">Zeiger auf ein **DWORD** , das die Größe des zugeordneten Puffers in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="fa277-114">Pointer to a **DWORD** that specifies the size of allocated buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa277-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa277-115">Return value</span></span>

<span data-ttu-id="fa277-116">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="fa277-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fa277-117">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fa277-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fa277-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fa277-118">Return code</span></span>                                                                                   | <span data-ttu-id="fa277-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa277-119">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fa277-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fa277-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fa277-121">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa277-121">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="fa277-122"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="fa277-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fa277-123">Ein erforderliches Zeigerargument war **null**.</span><span class="sxs-lookup"><span data-stu-id="fa277-123">A required pointer argument was **NULL**.</span></span><br/>                   |
| <dl> <span data-ttu-id="fa277-124"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="fa277-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fa277-125">Es war nicht genügend Arbeitsspeicher verfügbar, um den Puffer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fa277-125">There was not enough memory available to create the buffer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fa277-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa277-126">Requirements</span></span>



| <span data-ttu-id="fa277-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa277-127">Requirement</span></span> | <span data-ttu-id="fa277-128">Wert</span><span class="sxs-lookup"><span data-stu-id="fa277-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa277-129">Header</span><span class="sxs-lookup"><span data-stu-id="fa277-129">Header</span></span><br/>  | <dl> <span data-ttu-id="fa277-130"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa277-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa277-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fa277-131">Library</span></span><br/> | <dl> <span data-ttu-id="fa277-132"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa277-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa277-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa277-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa277-134">**Iwpdserializer-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="fa277-134">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




