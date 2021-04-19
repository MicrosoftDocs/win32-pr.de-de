---
description: Beachten Sie, dass diese Schnittstelle veraltet ist.
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: 'Iamfilterdata:: deatefilterdata-Methode (fil \_ Data. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.CreateFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 4c83f19de8e709f9890b23957f730fbbac12dd7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370034"
---
# <a name="iamfilterdatacreatefilterdata-method"></a><span data-ttu-id="2cb1b-103">Iamfilterdata:: kreatefilterdata-Methode</span><span class="sxs-lookup"><span data-stu-id="2cb1b-103">IAMFilterData::CreateFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="2cb1b-104">Diese Schnittstelle ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-104">This interface has been deprecated.</span></span> <span data-ttu-id="2cb1b-105">Diese sollten von neuen Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-105">New applications should not use it.</span></span>

 

<span data-ttu-id="2cb1b-106">Die- `CreateFilterData` Methode erstellt binäre Registrierungsdaten für einen Filter.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-106">The `CreateFilterData` method creates binary registry data for a filter.</span></span> <span data-ttu-id="2cb1b-107">Diese Daten können als reg \_ Binary-Unterschlüssel namens "FilterData" unter dem CLSID-Schlüssel des Filters in die Registrierung geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-107">This data can be written to the registry as a REG\_BINARY subkey named FilterData, under the filter's CLSID key.</span></span>

<span data-ttu-id="2cb1b-108">Es gibt in der Regel keinen Grund dafür, dass eine Anwendung diese Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-108">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="2cb1b-109">Die [**IFilterMapper2:: registerfilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) -Methode erstellt automatisch die Binärdaten und fügt Sie der richtigen Position in der Registrierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-109">The [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method automatically creates the binary data and adds it to the correct location in the registry.</span></span> <span data-ttu-id="2cb1b-110">Weitere Informationen finden Sie unter Vorgehens [Weise beim Registrieren von DirectShow-Filtern](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="2cb1b-110">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2cb1b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cb1b-111">Syntax</span></span>


```C++
HRESULT CreateFilterData(
  [in]  REGFILTER2 *prf2,
  [out] BYTE       **prgbFilterData,
  [out] ULONG      *pcb
);
```



## <a name="parameters"></a><span data-ttu-id="2cb1b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cb1b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cb1b-113">*prf2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2cb1b-113">*prf2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cb1b-114">Zeiger auf eine [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) -Struktur, die die Filter Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-114">Pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) structure that contains the filter information.</span></span>

</dd> <dt>

<span data-ttu-id="2cb1b-115">*prgbfilterdata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2cb1b-115">*prgbFilterData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cb1b-116">Adresse einer Variablen, die einen Zeiger auf die Binärdaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-116">Address of a variable that receives a pointer to the binary data.</span></span> <span data-ttu-id="2cb1b-117">Die-Methode ordnet den Arbeitsspeicher für die Daten zu.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-117">The method allocates the memory for the data.</span></span> <span data-ttu-id="2cb1b-118">Der Aufrufer muss den Speicher freigeben, indem er die **CoTaskMemFree** -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-118">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> <dt>

<span data-ttu-id="2cb1b-119">*Platine* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2cb1b-119">*pcb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cb1b-120">Ein Zeiger auf eine Variable, die die Größe der Binärdaten empfängt (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="2cb1b-120">Pointer to a variable that receives the size of the binary data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cb1b-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2cb1b-121">Return value</span></span>

<span data-ttu-id="2cb1b-122">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-122">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="2cb1b-123">Bei einem Fehler wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-123">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cb1b-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2cb1b-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2cb1b-125">Der Header "fil \_ Data. h" befindet sich im Verzeichnis " [Mapper Sample](mapper-sample.md) " in der Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="2cb1b-125">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2cb1b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2cb1b-126">Requirements</span></span>



| <span data-ttu-id="2cb1b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2cb1b-127">Requirement</span></span> | <span data-ttu-id="2cb1b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="2cb1b-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cb1b-129">Header</span><span class="sxs-lookup"><span data-stu-id="2cb1b-129">Header</span></span><br/> | <dl> <span data-ttu-id="2cb1b-130"><dt>Fil- \_ Daten. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cb1b-130"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="2cb1b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2cb1b-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="2cb1b-132"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cb1b-132"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2cb1b-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cb1b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cb1b-134">**Iamfilterdata-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2cb1b-134">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 




