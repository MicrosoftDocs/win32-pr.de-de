---
description: Die getiportabledevicevaluesfrombuffer-Methode deserialisiert ein Bytearray in eine iportabledevicevalues-Schnittstelle.
ms.assetid: 93bea711-74d5-407a-a707-a3abe47bc2cd
title: 'Iwpdserializer:: getiportabledevicevaluesfrombuffer-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetIPortableDeviceValuesFromBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 639a9455349e1d016b71d9c9717940695e9c0a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365902"
---
# <a name="iwpdserializergetiportabledevicevaluesfrombuffer-method"></a><span data-ttu-id="63906-103">Iwpdserializer:: getiportabledevicevaluesfrombuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="63906-103">IWpdSerializer::GetIPortableDeviceValuesFromBuffer method</span></span>

<span data-ttu-id="63906-104">Die **getiportabledevicevaluesfrombuffer** -Methode deserialisiert ein Bytearray in eine **iportabledevicevalues** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="63906-104">The **GetIPortableDeviceValuesFromBuffer** method deserializes a byte array to an **IPortableDeviceValues** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="63906-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="63906-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesFromBuffer(
  [in]  BYTE                  *pBuffer,
  [in]  DWORD                 dwInputBufferLength,
  [out] IPortableDeviceValues **ppParams
);
```



## <a name="parameters"></a><span data-ttu-id="63906-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="63906-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63906-107">*pbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63906-107">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63906-108">Zeiger auf den zu deserialisierenden Puffer.</span><span class="sxs-lookup"><span data-stu-id="63906-108">Pointer to the buffer to deserialize.</span></span>

</dd> <dt>

<span data-ttu-id="63906-109">*dwinputbufferlength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63906-109">*dwInputBufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63906-110">**DWORD** , das die Größe des Puffers in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="63906-110">**DWORD** that specifies the size of the buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="63906-111">*ppparameams* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="63906-111">*ppParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63906-112">Die Adresse einer Variablen, die einen Zeiger auf eine [**iportablede vicevalues**](iportabledevicevalues.md) -Schnittstelle empfängt, die aus dem Puffer erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="63906-112">Address of a variable that receives a pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface created from the buffer.</span></span> <span data-ttu-id="63906-113">Die Anwendung ist für das Aufrufen von **Release** auf der Schnittstelle verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="63906-113">The application is responsible for calling **Release** on the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63906-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63906-114">Return value</span></span>

<span data-ttu-id="63906-115">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="63906-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="63906-116">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="63906-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="63906-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="63906-117">Return code</span></span>                                                                                  | <span data-ttu-id="63906-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63906-118">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="63906-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="63906-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="63906-120">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63906-120">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="63906-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="63906-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="63906-122">Ein erforderliches Zeigerargument war **null**.</span><span class="sxs-lookup"><span data-stu-id="63906-122">A required pointer argument was **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="63906-123"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="63906-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="63906-124">Es ist ein nicht spezifizierter Konvertierungs Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="63906-124">An unspecified conversion error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="63906-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63906-125">Requirements</span></span>



| <span data-ttu-id="63906-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63906-126">Requirement</span></span> | <span data-ttu-id="63906-127">Wert</span><span class="sxs-lookup"><span data-stu-id="63906-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63906-128">Header</span><span class="sxs-lookup"><span data-stu-id="63906-128">Header</span></span><br/>  | <dl> <span data-ttu-id="63906-129"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="63906-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="63906-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="63906-130">Library</span></span><br/> | <dl> <span data-ttu-id="63906-131"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63906-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63906-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63906-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63906-133">**Iwpdserializer-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="63906-133">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




