---
description: Die getbuffervalue-Methode ruft einen Byte Array Wert (Typ VT \_ Vector \| VT \_ UI1) ab, der von einem Schlüssel angegeben wird.
ms.assetid: 18180a47-7d81-440b-b596-2516089a02bd
title: 'Iportabledevicevalues:: getbuffervalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e5b98bb412ed648cf6ac74ec457b1e6032c009ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371495"
---
# <a name="iportabledevicevaluesgetbuffervalue-method"></a><span data-ttu-id="56372-103">Iportabledevicevalues:: getbuffervalue-Methode</span><span class="sxs-lookup"><span data-stu-id="56372-103">IPortableDeviceValues::GetBufferValue method</span></span>

<span data-ttu-id="56372-104">Die **getbuffervalue** -Methode ruft einen **Byte Array** Wert (Typ VT \_ Vector \| VT \_ UI1) ab, der von einem Schlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="56372-104">The **GetBufferValue** method retrieves a **byte array** value (type VT\_VECTOR \| VT\_UI1) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="56372-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="56372-105">Syntax</span></span>


```C++
HRESULT GetBufferValue(
  [in]  REFPROPERTYKEY key,
  [out] BYTE           **ppValue,
  [out] DWORD          *pcbValue
);
```



## <a name="parameters"></a><span data-ttu-id="56372-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56372-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56372-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="56372-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56372-108">Ein **refpropertykey** -Schlüssel, der das abzurufende Element angibt.</span><span class="sxs-lookup"><span data-stu-id="56372-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="56372-109">*ppValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="56372-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56372-110">Zeiger auf den abgerufenen **Byte \* *_-Wert. Der Aufrufer ist dafür verantwortlich, den Arbeitsspeicher durch Aufrufen von _* CoTaskMemFree freizugeben**.</span><span class="sxs-lookup"><span data-stu-id="56372-110">Pointer to the retrieved \**BYTE\**_ value. The caller is responsible for freeing the memory by calling _\* CoTaskMemFree\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="56372-111">*pcbValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="56372-111">*pcbValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56372-112">Ein Zeiger auf die Größe von *ppValue* in Bytes.</span><span class="sxs-lookup"><span data-stu-id="56372-112">Pointer to the size of *ppValue*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56372-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56372-113">Return value</span></span>

<span data-ttu-id="56372-114">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="56372-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="56372-115">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="56372-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="56372-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="56372-116">Return code</span></span>                                                                                                            | <span data-ttu-id="56372-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56372-117">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="56372-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="56372-118"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="56372-119">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56372-119">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="56372-120"><dt>**DISP \_ E \_ typemismatch**</dt></span><span class="sxs-lookup"><span data-stu-id="56372-120"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="56372-121">Die von *Key* angegebene Eigenschaft ist kein  \* Bytetyp.</span><span class="sxs-lookup"><span data-stu-id="56372-121">The property specified by *key* is not a **BYTE**\* type.</span></span><br/> |
| <dl> <span data-ttu-id="56372-122"><dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt></span><span class="sxs-lookup"><span data-stu-id="56372-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="56372-123">Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="56372-123">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="56372-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56372-124">Remarks</span></span>

<span data-ttu-id="56372-125">Das Abrufen eines **null** -Puffers oder eines Puffers der Größe 0 wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="56372-125">Retrieving a **NULL** buffer or a zero-sized buffer is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="56372-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56372-126">Requirements</span></span>



| <span data-ttu-id="56372-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56372-127">Requirement</span></span> | <span data-ttu-id="56372-128">Wert</span><span class="sxs-lookup"><span data-stu-id="56372-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56372-129">Header</span><span class="sxs-lookup"><span data-stu-id="56372-129">Header</span></span><br/>  | <dl> <span data-ttu-id="56372-130"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="56372-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="56372-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="56372-131">Library</span></span><br/> | <dl> <span data-ttu-id="56372-132"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56372-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56372-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56372-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56372-134">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="56372-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="56372-135">**Iportabledebug:: setbuffervalue**</span><span class="sxs-lookup"><span data-stu-id="56372-135">**IPortableDeviceValues::SetBufferValue**</span></span>](iportabledevicevalues-setbuffervalue.md)
</dt> </dl>

 

 




