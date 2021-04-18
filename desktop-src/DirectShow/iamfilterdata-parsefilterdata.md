---
description: Beachten Sie, dass diese Schnittstelle veraltet ist.
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: Iamfilterdata::P Ardie FilterData-Methode (fil \_ Data. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.ParseFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 18e1367813adff6b0debdfb698644731668bfc5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364898"
---
# <a name="iamfilterdataparsefilterdata-method"></a><span data-ttu-id="ae258-103">Iamfilterdata::P Ardie FilterData-Methode</span><span class="sxs-lookup"><span data-stu-id="ae258-103">IAMFilterData::ParseFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="ae258-104">Diese Schnittstelle ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="ae258-104">This interface has been deprecated.</span></span> <span data-ttu-id="ae258-105">Diese sollten von neuen Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae258-105">New applications should not use it.</span></span>

 

<span data-ttu-id="ae258-106">Die- `ParseFilterData` Methode entpackt die binären Registrierungsdaten für einen Filter.</span><span class="sxs-lookup"><span data-stu-id="ae258-106">The `ParseFilterData` method unpacks the binary registry data for a filter.</span></span>

<span data-ttu-id="ae258-107">Es gibt in der Regel keinen Grund dafür, dass eine Anwendung diese Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="ae258-107">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="ae258-108">Die [**IFilterMapper2:: enummatchingfilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) -Methode bietet eine bequeme Möglichkeit, auf die Filter Registrierungsdaten zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ae258-108">The [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method provides a more convenient way to access the filter registry data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae258-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae258-109">Syntax</span></span>


```C++
HRESULT ParseFilterData(
  [in]  BYTE  *rgbFilterData,
  [in]  ULONG cb,
  [out] BYTE  **prgbRegFilter2
);
```



## <a name="parameters"></a><span data-ttu-id="ae258-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae258-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae258-111">*rgbfilterdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae258-111">*rgbFilterData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae258-112">Zeiger auf die binären Registrierungsdaten.</span><span class="sxs-lookup"><span data-stu-id="ae258-112">Pointer to the binary registry data.</span></span> <span data-ttu-id="ae258-113">Sie können diese Daten abrufen, indem Sie die Eigenschaft "FilterData" aus dem filtermoniker abrufen.</span><span class="sxs-lookup"><span data-stu-id="ae258-113">You can get this data by retrieving the "FilterData" property from the filter moniker.</span></span> <span data-ttu-id="ae258-114">Die Daten werden als **SAFEARRAY** von Bytes (VT \_ UI1 \| VT \_ Array) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ae258-114">The data is stored as a **SAFEARRAY** of bytes (VT\_UI1 \| VT\_ARRAY).</span></span>

</dd> <dt>

<span data-ttu-id="ae258-115">*CB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae258-115">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae258-116">Gibt die Größe der Binärdaten in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="ae258-116">Specifies the size of the binary data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ae258-117">*prgbRegFilter2* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ae258-117">*prgbRegFilter2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae258-118">Adresse einer Variablen, die einen Zeiger auf die entpackten Daten empfängt.</span><span class="sxs-lookup"><span data-stu-id="ae258-118">Address of a variable that receives a pointer to the unpacked data.</span></span> <span data-ttu-id="ae258-119">Wenn die Methode zurückgegeben wird, wandeln Sie diesen Zeiger in einen [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) -Typ um, um auf die Filterdaten zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ae258-119">When the method returns, cast this pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) type to access the filter data.</span></span> <span data-ttu-id="ae258-120">Der Aufrufer muss den Speicher freigeben, indem er die **CoTaskMemFree** -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="ae258-120">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae258-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae258-121">Return value</span></span>

<span data-ttu-id="ae258-122">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="ae258-122">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="ae258-123">Bei einem Fehler wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ae258-123">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae258-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae258-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ae258-125">Der Header "fil \_ Data. h" befindet sich im Verzeichnis " [Mapper Sample](mapper-sample.md) " in der Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="ae258-125">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ae258-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae258-126">Requirements</span></span>



| <span data-ttu-id="ae258-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae258-127">Requirement</span></span> | <span data-ttu-id="ae258-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ae258-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae258-129">Header</span><span class="sxs-lookup"><span data-stu-id="ae258-129">Header</span></span><br/> | <dl> <span data-ttu-id="ae258-130"><dt>Fil- \_ Daten. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae258-130"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="ae258-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ae258-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="ae258-132"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae258-132"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ae258-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae258-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae258-134">**Iamfilterdata-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ae258-134">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 




