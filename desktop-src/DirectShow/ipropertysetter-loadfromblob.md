---
description: Die loadfromblob-Methode lädt Eigenschafts Daten aus einem Persistenzformat.
ms.assetid: b314a844-2190-469a-a030-4494e2140ce6
title: 'Ipropertysetter:: loadfromblob-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadFromBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0a1e58aa5802e8fcb05c2464fc1f121ee1e86f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369974"
---
# <a name="ipropertysetterloadfromblob-method"></a><span data-ttu-id="7f820-103">Ipropertysetter:: loadfromblob-Methode</span><span class="sxs-lookup"><span data-stu-id="7f820-103">IPropertySetter::LoadFromBlob method</span></span>

> [!Note]  
> <span data-ttu-id="7f820-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="7f820-104">\[Deprecated.</span></span> <span data-ttu-id="7f820-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="7f820-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7f820-106">Die- `LoadFromBlob` Methode lädt Eigenschafts Daten aus einem Persistenzformat.</span><span class="sxs-lookup"><span data-stu-id="7f820-106">The `LoadFromBlob` method loads property data from a persistence format.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f820-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f820-107">Syntax</span></span>


```C++
HRESULT LoadFromBlob(
  [in] LONG cSize,
  [in] BYTE *pb
);
```



## <a name="parameters"></a><span data-ttu-id="7f820-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f820-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f820-109">*CSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f820-109">*cSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f820-110">Größe der Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="7f820-110">Size of the data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7f820-111">*PB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f820-111">*pb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f820-112">Ein Zeiger auf ein Bytearray, das die Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="7f820-112">Pointer to an array of bytes that contains the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f820-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f820-113">Return value</span></span>

<span data-ttu-id="7f820-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="7f820-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7f820-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7f820-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f820-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f820-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7f820-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="7f820-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7f820-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="7f820-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7f820-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7f820-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7f820-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f820-120">Requirements</span></span>



| <span data-ttu-id="7f820-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f820-121">Requirement</span></span> | <span data-ttu-id="7f820-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7f820-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f820-123">Header</span><span class="sxs-lookup"><span data-stu-id="7f820-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7f820-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7f820-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7f820-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7f820-125">Library</span></span><br/> | <dl> <span data-ttu-id="7f820-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="7f820-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f820-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f820-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f820-128">**Ipropertysetter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7f820-128">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="7f820-129">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="7f820-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




