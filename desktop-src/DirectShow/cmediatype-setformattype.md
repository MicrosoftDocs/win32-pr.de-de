---
description: Die setformattype-Methode gibt den Formattyp an.
ms.assetid: e8ed9190-7169-4d51-ace7-597f43ff083e
title: Cmediatype. setformattype-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormatType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7843c5a9788545909ef4297accfa342c08b71e88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362012"
---
# <a name="cmediatypesetformattype-method"></a><span data-ttu-id="ce212-103">Cmediatype. setformattype-Methode</span><span class="sxs-lookup"><span data-stu-id="ce212-103">CMediaType.SetFormatType method</span></span>

<span data-ttu-id="ce212-104">Die setformattype-Methode von ' ' gibt den Formattyp an.</span><span class="sxs-lookup"><span data-stu-id="ce212-104">The \`\`SetFormatType method specifies the format type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce212-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce212-105">Syntax</span></span>


```C++
void SetFormatType(
   const GUID *pformattype
);
```



## <a name="parameters"></a><span data-ttu-id="ce212-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce212-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce212-107">*pformattype*</span><span class="sxs-lookup"><span data-stu-id="ce212-107">*pformattype*</span></span> 
</dt> <dd>

<span data-ttu-id="ce212-108">Zeiger auf eine **GUID** , die den Formattyp angibt.</span><span class="sxs-lookup"><span data-stu-id="ce212-108">Pointer to a **GUID** that specifies the format type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce212-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce212-109">Return value</span></span>

<span data-ttu-id="ce212-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ce212-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce212-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce212-111">Remarks</span></span>

<span data-ttu-id="ce212-112">Diese Methode legt den **Format Type** -Member fest.</span><span class="sxs-lookup"><span data-stu-id="ce212-112">This method sets the **formattype** member.</span></span> <span data-ttu-id="ce212-113">Der Formattyp definiert das Layout des Format Blocks.</span><span class="sxs-lookup"><span data-stu-id="ce212-113">The format type defines the layout of the format block.</span></span> <span data-ttu-id="ce212-114">Wenn der Formattyp beispielsweise Format \_ videoinfo ist, sollte der Format Block eine **videoinfoheader** -Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="ce212-114">For example, if the format type is FORMAT\_VideoInfo, the format block should contain a **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="ce212-115">Um den Format Block festzulegen, müssen Sie die [**cmediatype:: SetFormat**](cmediatype-setformat.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ce212-115">To set the format block, call the [**CMediaType::SetFormat**](cmediatype-setformat.md) method.</span></span> <span data-ttu-id="ce212-116">Der Aufrufer ist dafür verantwortlich, sicherzustellen, dass der Format Block mit dem Formattyp übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="ce212-116">The caller is responsible for making sure that the format block matches the format type.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce212-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce212-117">Requirements</span></span>



| <span data-ttu-id="ce212-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce212-118">Requirement</span></span> | <span data-ttu-id="ce212-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ce212-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce212-120">Header</span><span class="sxs-lookup"><span data-stu-id="ce212-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ce212-121"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce212-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="ce212-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ce212-122">Library</span></span><br/> | <dl> <span data-ttu-id="ce212-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ce212-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce212-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce212-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce212-125">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ce212-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 


``
