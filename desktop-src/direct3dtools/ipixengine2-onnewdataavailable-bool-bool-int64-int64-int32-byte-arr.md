---
description: Anforderungen, um anzugeben, dass das Grafik Protokoll neue Daten enthält.
MS-HAID: vspixengine.IPixEngine2\_OnNewDataAvailable\_BOOL\_BOOL\_INT64\_INT64\_INT32\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine2:: onnewdataavailable-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B99FC54C-9395-4B14-93D5-B6408D655DC3
api_name:
- IPixEngine2.OnNewDataAvailable
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3de880153eec5b41849167f3a87a3f77f31aeffd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521528"
---
# <a name="span-idvspixengineipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arrspanipixengine2onnewdataavailable-method"></a><span data-ttu-id="aea2d-103"><span id="vspixengine.ipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arr"></span>IPixEngine2:: onnewdataavailable-Methode</span><span class="sxs-lookup"><span data-stu-id="aea2d-103"><span id="vspixengine.ipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arr"></span>IPixEngine2::OnNewDataAvailable method</span></span>

<span data-ttu-id="aea2d-104">Anforderungen, um anzugeben, dass das Grafik Protokoll neue Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="aea2d-104">Requests to indicate that the graphics log has new data inside of it.</span></span>

## <a name="syntax"></a><span data-ttu-id="aea2d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aea2d-105">Syntax</span></span>


```C++
HRESULT OnNewDataAvailable(
   BOOL    fSessionEnd,
   BOOL    fUnloadCurFrame,
   INT64   i64FilePositionStart,
   INT64   i64FilePositionEnd,
   INT32   iObjectTableDataSize,
   BYTE [] count4_pObjectTableData
);
```

## <a name="parameters"></a><span data-ttu-id="aea2d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aea2d-106">Parameters</span></span>

<span data-ttu-id="aea2d-107">*fsessionend* </span><span class="sxs-lookup"><span data-stu-id="aea2d-107">*fSessionEnd* </span></span>  
<span data-ttu-id="aea2d-108">true, wenn die Sitzung beendet wurde, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="aea2d-108">true if the session has ended, otherwise false.</span></span>

<span data-ttu-id="aea2d-109">*funloadcurrframe* </span><span class="sxs-lookup"><span data-stu-id="aea2d-109">*fUnloadCurFrame* </span></span>  
<span data-ttu-id="aea2d-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="aea2d-110">Not used.</span></span>

<span data-ttu-id="aea2d-111">*i64FilePositionStart* </span><span class="sxs-lookup"><span data-stu-id="aea2d-111">*i64FilePositionStart* </span></span>  
<span data-ttu-id="aea2d-112">Die Dateiposition in Bytes, an der die neuen Daten beginnen.</span><span class="sxs-lookup"><span data-stu-id="aea2d-112">The file position, in bytes, at which the new data begins.</span></span>

<span data-ttu-id="aea2d-113">*i64FilePositionEnd* </span><span class="sxs-lookup"><span data-stu-id="aea2d-113">*i64FilePositionEnd* </span></span>  
<span data-ttu-id="aea2d-114">Die Dateiposition in Bytes, an der die neuen Daten enden.</span><span class="sxs-lookup"><span data-stu-id="aea2d-114">The file position, in bytes, at which the new data ends.</span></span>

<span data-ttu-id="aea2d-115">*iobjecttabledatasize* </span><span class="sxs-lookup"><span data-stu-id="aea2d-115">*iObjectTableDataSize* </span></span>  
<span data-ttu-id="aea2d-116">Die Anzahl von Bytes, die in count4 \_ pobjecttabledata enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="aea2d-116">The number of bytes contained in count4\_pObjectTableData.</span></span>

<span data-ttu-id="aea2d-117">*count4 \_ pobjecttabledata* </span><span class="sxs-lookup"><span data-stu-id="aea2d-117">*count4\_pObjectTableData* </span></span>  
<span data-ttu-id="aea2d-118">Ein-Puffer, der Daten für die Objekttabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="aea2d-118">An buffer containing data for the object table.</span></span>

## <a name="return-value"></a><span data-ttu-id="aea2d-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aea2d-119">Return value</span></span>

<span data-ttu-id="aea2d-120">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="aea2d-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aea2d-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aea2d-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="aea2d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aea2d-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="aea2d-123">Header</span><span class="sxs-lookup"><span data-stu-id="aea2d-123">Header</span></span></p></td><td><span data-ttu-id="aea2d-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="aea2d-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="aea2d-125"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aea2d-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="aea2d-126">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="aea2d-126">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
