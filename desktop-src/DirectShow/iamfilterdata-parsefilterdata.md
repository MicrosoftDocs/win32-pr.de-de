---
description: Erfahren Sie mehr über die IAMFilterData::P arseFilterData-Methode, entpackt die binären Registrierungsdaten für einen Filter. Diese Schnittstelle ist veraltet.
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: IAMFilterData::P arseFilterData-Methode (File \_ Data.h)
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
ms.openlocfilehash: 9560280fa6f16699af907cdb5cf682b9c4bb1277
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989445"
---
# <a name="iamfilterdataparsefilterdata-method"></a><span data-ttu-id="475e4-104">IAMFilterData::P arseFilterData-Methode</span><span class="sxs-lookup"><span data-stu-id="475e4-104">IAMFilterData::ParseFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="475e4-105">Diese Schnittstelle ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="475e4-105">This interface has been deprecated.</span></span> <span data-ttu-id="475e4-106">Neue Anwendungen sollten sie nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="475e4-106">New applications should not use it.</span></span>

 

<span data-ttu-id="475e4-107">Die `ParseFilterData` -Methode entpackt die binären Registrierungsdaten für einen Filter.</span><span class="sxs-lookup"><span data-stu-id="475e4-107">The `ParseFilterData` method unpacks the binary registry data for a filter.</span></span>

<span data-ttu-id="475e4-108">Es gibt in der Regel keinen Grund, warum eine Anwendung diese Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="475e4-108">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="475e4-109">Die [**IFilterMapper2::EnumMatchingFilters-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) bietet eine bequemere Möglichkeit, auf die Filterregistrierungsdaten zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="475e4-109">The [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method provides a more convenient way to access the filter registry data.</span></span>

## <a name="syntax"></a><span data-ttu-id="475e4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="475e4-110">Syntax</span></span>


```C++
HRESULT ParseFilterData(
  [in]  BYTE  *rgbFilterData,
  [in]  ULONG cb,
  [out] BYTE  **prgbRegFilter2
);
```



## <a name="parameters"></a><span data-ttu-id="475e4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="475e4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="475e4-112">*rgbFilterData* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="475e4-112">*rgbFilterData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="475e4-113">Zeiger auf die binären Registrierungsdaten.</span><span class="sxs-lookup"><span data-stu-id="475e4-113">Pointer to the binary registry data.</span></span> <span data-ttu-id="475e4-114">Sie können diese Daten abrufen, indem Sie die Eigenschaft "FilterData" aus dem Filtermoniker abrufen.</span><span class="sxs-lookup"><span data-stu-id="475e4-114">You can get this data by retrieving the "FilterData" property from the filter moniker.</span></span> <span data-ttu-id="475e4-115">Die Daten werden als **SAFEARRAY von** Bytes (VT \_ UI1 \| VT \_ ARRAY) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="475e4-115">The data is stored as a **SAFEARRAY** of bytes (VT\_UI1 \| VT\_ARRAY).</span></span>

</dd> <dt>

<span data-ttu-id="475e4-116">*cb* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="475e4-116">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="475e4-117">Gibt die Größe der Binärdaten in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="475e4-117">Specifies the size of the binary data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="475e4-118">*prgbRegFilter2* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="475e4-118">*prgbRegFilter2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="475e4-119">Adresse einer Variablen, die einen Zeiger auf die entpackten Daten empfängt.</span><span class="sxs-lookup"><span data-stu-id="475e4-119">Address of a variable that receives a pointer to the unpacked data.</span></span> <span data-ttu-id="475e4-120">Wenn die Methode zurückgegeben wird, casten Sie diesen Zeiger in einen [**REGFILTER2-Typ,**](/windows/desktop/api/strmif/ns-strmif-regfilter2) um auf die Filterdaten zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="475e4-120">When the method returns, cast this pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) type to access the filter data.</span></span> <span data-ttu-id="475e4-121">Der Aufrufer muss den Arbeitsspeicher durch Aufrufen der **CoTaskMemFree-Methode** frei geben.</span><span class="sxs-lookup"><span data-stu-id="475e4-121">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="475e4-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="475e4-122">Return value</span></span>

<span data-ttu-id="475e4-123">Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="475e4-123">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="475e4-124">Bei einem Fehler wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="475e4-124">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="475e4-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="475e4-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="475e4-126">Der Header Header \_ "data.h" befindet sich im [Verzeichnis Mapper Sample (Mapperbeispiel)](mapper-sample.md) im Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="475e4-126">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="475e4-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="475e4-127">Requirements</span></span>



| <span data-ttu-id="475e4-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="475e4-128">Requirement</span></span> | <span data-ttu-id="475e4-129">Wert</span><span class="sxs-lookup"><span data-stu-id="475e4-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="475e4-130">Header</span><span class="sxs-lookup"><span data-stu-id="475e4-130">Header</span></span><br/> | <dl> <span data-ttu-id="475e4-131"><dt>Datei \_ "data.h"</dt></span><span class="sxs-lookup"><span data-stu-id="475e4-131"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="475e4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="475e4-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="475e4-133"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="475e4-133"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="475e4-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="475e4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="475e4-135">**IAMFilterData-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="475e4-135">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 




