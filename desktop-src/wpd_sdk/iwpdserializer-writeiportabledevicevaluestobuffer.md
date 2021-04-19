---
description: Die Methode "Write teiportabledevicevaluestobuffer" serialisiert eine iportabledevicevalues-Schnittstelle zu einem vom Aufrufer zugeordneten Bytearray.
ms.assetid: 4d0108f1-563e-42df-897b-7cc0e9ff5b3a
title: 'Iwpdserializer:: Write-portabledevicevaluestobuffer-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.WriteIPortableDeviceValuesToBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f2a8f8b374f967f7231881d9e0eca6434e9c57e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370494"
---
# <a name="iwpdserializerwriteiportabledevicevaluestobuffer-method"></a><span data-ttu-id="eba7d-103">Iwpdserializer:: Write-portabledevicevaluestobuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="eba7d-103">IWpdSerializer::WriteIPortableDeviceValuesToBuffer method</span></span>

<span data-ttu-id="eba7d-104">Die Methode " **Write teiportabledevicevaluestobuffer** " serialisiert eine **iportabledevicevalues** -Schnittstelle zu einem vom Aufrufer zugeordneten Bytearray.</span><span class="sxs-lookup"><span data-stu-id="eba7d-104">The **WriteIPortableDeviceValuesToBuffer** method serializes an **IPortableDeviceValues** interface to a caller-allocated byte array.</span></span>

## <a name="syntax"></a><span data-ttu-id="eba7d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eba7d-105">Syntax</span></span>


```C++
HRESULT WriteIPortableDeviceValuesToBuffer(
  [in]  DWORD                 dwOutputBufferLength,
  [in]  IPortableDeviceValues *pResults,
  [out] BYTE                  *pBuffer,
  [out] DWORD                 *pdwBytesWritten
);
```



## <a name="parameters"></a><span data-ttu-id="eba7d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eba7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eba7d-107">*dwoutputbufferlength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eba7d-107">*dwOutputBufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eba7d-108">**DWORD** , das die Größe von *pbuffer* in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="eba7d-108">**DWORD** that specifies the size of *pBuffer*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="eba7d-109">*präsults* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eba7d-109">*pResults* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eba7d-110">Zeiger auf eine [**iportabledevicevalues**](iportabledevicevalues.md) -Schnittstelle, die serialisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="eba7d-110">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface to serialize.</span></span>

</dd> <dt>

<span data-ttu-id="eba7d-111">*pbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="eba7d-111">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eba7d-112">Zeiger auf einen vom Aufrufer zugewiesenen Puffer.</span><span class="sxs-lookup"><span data-stu-id="eba7d-112">Pointer to a caller-allocated buffer.</span></span> <span data-ttu-id="eba7d-113">Um die Größe des erforderlichen Puffers zu ermitteln, müssen Sie **getserializedsize** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="eba7d-113">To learn the size of the required buffer, call **GetSerializedSize**.</span></span>

</dd> <dt>

<span data-ttu-id="eba7d-114">*pdwbyteswritten* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="eba7d-114">*pdwBytesWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eba7d-115">Zeiger auf ein **DWORD** , das die Anzahl der Bytes angibt, die tatsächlich in den von dem Aufrufer zugewiesenen Puffer geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="eba7d-115">Pointer to a **DWORD** that indicates the number of bytes that was actually written to the caller-allocated buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eba7d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eba7d-116">Return value</span></span>

<span data-ttu-id="eba7d-117">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="eba7d-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="eba7d-118">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="eba7d-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="eba7d-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="eba7d-119">Return code</span></span>                                                                                   | <span data-ttu-id="eba7d-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eba7d-120">Description</span></span>                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="eba7d-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="eba7d-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="eba7d-122">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eba7d-122">The method succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="eba7d-123"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="eba7d-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="eba7d-124">Ein erforderliches Zeigerargument war **null**.</span><span class="sxs-lookup"><span data-stu-id="eba7d-124">A required pointer argument was **NULL**.</span></span><br/>      |
| <dl> <span data-ttu-id="eba7d-125"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="eba7d-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="eba7d-126">Der vom Aufrufer bereitgestellte Puffer war nicht groß genug.</span><span class="sxs-lookup"><span data-stu-id="eba7d-126">The caller-provided buffer was not big enough.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eba7d-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eba7d-127">Remarks</span></span>

<span data-ttu-id="eba7d-128">Diese Methode kopiert eine **iportabledevicevalues** -Schnittstelle in einen vorhandenen Puffer.</span><span class="sxs-lookup"><span data-stu-id="eba7d-128">This method copies an **IPortableDeviceValues** interface into an existing buffer.</span></span> <span data-ttu-id="eba7d-129">Wenn Sie einen neuen Puffer zuordnen möchten, verwenden Sie [**getbufferfromiportableendvicevalues**](iwpdserializer-getbufferfromiportabledevicevalues.md).</span><span class="sxs-lookup"><span data-stu-id="eba7d-129">If you want to allocate a new buffer, use [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eba7d-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eba7d-130">Requirements</span></span>



| <span data-ttu-id="eba7d-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eba7d-131">Requirement</span></span> | <span data-ttu-id="eba7d-132">Wert</span><span class="sxs-lookup"><span data-stu-id="eba7d-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eba7d-133">Header</span><span class="sxs-lookup"><span data-stu-id="eba7d-133">Header</span></span><br/>  | <dl> <span data-ttu-id="eba7d-134"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="eba7d-134"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="eba7d-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eba7d-135">Library</span></span><br/> | <dl> <span data-ttu-id="eba7d-136"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eba7d-136"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eba7d-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eba7d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eba7d-138">**Iwpdserializer-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="eba7d-138">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




