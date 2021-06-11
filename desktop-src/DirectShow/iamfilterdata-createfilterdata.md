---
description: Erfahren Sie mehr über die IAMFilterData::CreateFilterData-Methode, die binäre Registrierungsdaten für einen Filter erstellt. Diese Schnittstelle ist veraltet.
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: IAMFilterData::CreateFilterData-Methode (Eigenschaft \_ data.h)
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
ms.openlocfilehash: 0a0126266fc33dca030abad65ccf9f0d35f6e195
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989455"
---
# <a name="iamfilterdatacreatefilterdata-method"></a><span data-ttu-id="8264e-104">IAMFilterData::CreateFilterData-Methode</span><span class="sxs-lookup"><span data-stu-id="8264e-104">IAMFilterData::CreateFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="8264e-105">Diese Schnittstelle ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="8264e-105">This interface has been deprecated.</span></span> <span data-ttu-id="8264e-106">Neue Anwendungen sollten sie nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="8264e-106">New applications should not use it.</span></span>

 

<span data-ttu-id="8264e-107">Die `CreateFilterData` -Methode erstellt binäre Registrierungsdaten für einen Filter.</span><span class="sxs-lookup"><span data-stu-id="8264e-107">The `CreateFilterData` method creates binary registry data for a filter.</span></span> <span data-ttu-id="8264e-108">Diese Daten können als REG BINARY-Unterschlüssel namens FilterData unter dem CLSID-Schlüssel des Filters in die \_ Registrierung geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="8264e-108">This data can be written to the registry as a REG\_BINARY subkey named FilterData, under the filter's CLSID key.</span></span>

<span data-ttu-id="8264e-109">Es gibt in der Regel keinen Grund, warum eine Anwendung diese Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="8264e-109">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="8264e-110">Die [**IFilterMapper2::RegisterFilter-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) erstellt automatisch die Binärdaten und fügt sie dem richtigen Speicherort in der Registrierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="8264e-110">The [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method automatically creates the binary data and adds it to the correct location in the registry.</span></span> <span data-ttu-id="8264e-111">Weitere Informationen finden Sie unter [Registrieren von DirectShow-Filtern.](how-to-register-directshow-filters.md)</span><span class="sxs-lookup"><span data-stu-id="8264e-111">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8264e-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="8264e-112">Syntax</span></span>


```C++
HRESULT CreateFilterData(
  [in]  REGFILTER2 *prf2,
  [out] BYTE       **prgbFilterData,
  [out] ULONG      *pcb
);
```



## <a name="parameters"></a><span data-ttu-id="8264e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8264e-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8264e-114">*prf2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8264e-114">*prf2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8264e-115">Zeiger auf eine [**REGFILTER2-Struktur,**](/windows/desktop/api/strmif/ns-strmif-regfilter2) die die Filterinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="8264e-115">Pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) structure that contains the filter information.</span></span>

</dd> <dt>

<span data-ttu-id="8264e-116">*prgbFilterData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8264e-116">*prgbFilterData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8264e-117">Adresse einer Variablen, die einen Zeiger auf die Binärdaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="8264e-117">Address of a variable that receives a pointer to the binary data.</span></span> <span data-ttu-id="8264e-118">Die -Methode weist den Arbeitsspeicher für die Daten zu.</span><span class="sxs-lookup"><span data-stu-id="8264e-118">The method allocates the memory for the data.</span></span> <span data-ttu-id="8264e-119">Der Aufrufer muss den Arbeitsspeicher durch Aufrufen der **CoTaskMemFree-Methode** frei geben.</span><span class="sxs-lookup"><span data-stu-id="8264e-119">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> <dt>

<span data-ttu-id="8264e-120">*( )* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8264e-120">*pcb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8264e-121">Zeiger auf eine Variable, die die Größe der Binärdaten in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="8264e-121">Pointer to a variable that receives the size of the binary data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8264e-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8264e-122">Return value</span></span>

<span data-ttu-id="8264e-123">Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8264e-123">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="8264e-124">Bei einem Fehler wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8264e-124">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8264e-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8264e-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8264e-126">Die HeaderDatei \_ data.h befindet sich im [Verzeichnis Mapper Sample (Mapper-Beispiel)](mapper-sample.md) im Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8264e-126">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8264e-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8264e-127">Requirements</span></span>



| <span data-ttu-id="8264e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8264e-128">Requirement</span></span> | <span data-ttu-id="8264e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="8264e-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8264e-130">Header</span><span class="sxs-lookup"><span data-stu-id="8264e-130">Header</span></span><br/> | <dl> <span data-ttu-id="8264e-131"><dt>Datei \_ "Data.h"</dt></span><span class="sxs-lookup"><span data-stu-id="8264e-131"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="8264e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8264e-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="8264e-133"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8264e-133"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8264e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8264e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8264e-135">**IAMFilterData-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8264e-135">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 




