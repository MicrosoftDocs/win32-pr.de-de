---
description: Eine Rückruffunktion, die verwendet wird, um den Host von Objekt Tabellen Informationen zu benachrichtigen.
MS-HAID: vspixengine.IObjectTableCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iobjecttablecallback:: resultCallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AAD02864-AE08-406B-A0E9-2228DC9A73E7
api_name:
- IObjectTableCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 66247dddbf0926b420faa998461393397a4717b7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747393"
---
# <a name="span-idvspixengineiobjecttablecallback_resultcallback_dword_dword_dword_variant_arrspaniobjecttablecallbackresultcallback-method"></a><span data-ttu-id="9acf6-103"><span id="vspixengine.iobjecttablecallback_resultcallback_dword_dword_dword_variant_arr"></span>Iobjecttablecallback:: resultCallback-Methode</span><span class="sxs-lookup"><span data-stu-id="9acf6-103"><span id="vspixengine.iobjecttablecallback_resultcallback_dword_dword_dword_variant_arr"></span>IObjectTableCallback::ResultCallback method</span></span>

<span data-ttu-id="9acf6-104">Eine Rückruffunktion, die verwendet wird, um den Host von Objekt Tabellen Informationen zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="9acf6-104">A callback function used to notify the host of object table information.</span></span>

## <a name="syntax"></a><span data-ttu-id="9acf6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9acf6-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD      numElements,
   DWORD      numRows,
   DWORD      numColumns,
   VARIANT [] count0_pRowData
);
```

## <a name="parameters"></a><span data-ttu-id="9acf6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9acf6-106">Parameters</span></span>

<span data-ttu-id="9acf6-107">*numElements* </span><span class="sxs-lookup"><span data-stu-id="9acf6-107">*numElements* </span></span>  
<span data-ttu-id="9acf6-108">Die Gesamtanzahl der Felder in allen Spalten aller-Objekte.</span><span class="sxs-lookup"><span data-stu-id="9acf6-108">The total number of fields in all columns of all objects.</span></span>

<span data-ttu-id="9acf6-109">*numRows* </span><span class="sxs-lookup"><span data-stu-id="9acf6-109">*numRows* </span></span>  
<span data-ttu-id="9acf6-110">Die Anzahl der Objekte, die übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="9acf6-110">The number of objects being transferred.</span></span>

<span data-ttu-id="9acf6-111">*NumColumns* </span><span class="sxs-lookup"><span data-stu-id="9acf6-111">*numColumns* </span></span>  
<span data-ttu-id="9acf6-112">Die Anzahl der Spalten (Felder) der Informationen, die für jedes Objekt übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="9acf6-112">The number of columns (fields) of information being transferred for each object.</span></span>

<span data-ttu-id="9acf6-113">*count0 \_ prowdata* </span><span class="sxs-lookup"><span data-stu-id="9acf6-113">*count0\_pRowData* </span></span>  
<span data-ttu-id="9acf6-114">Informationen zu den Objekten ein-Element für jedes Feld der einzelnen-Objekte.</span><span class="sxs-lookup"><span data-stu-id="9acf6-114">Information about the objects; one item for each field of each object.</span></span>

## <a name="return-value"></a><span data-ttu-id="9acf6-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9acf6-115">Return value</span></span>

<span data-ttu-id="9acf6-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="9acf6-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9acf6-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9acf6-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9acf6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9acf6-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9acf6-119">Header</span><span class="sxs-lookup"><span data-stu-id="9acf6-119">Header</span></span></p></td><td><span data-ttu-id="9acf6-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="9acf6-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9acf6-121"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9acf6-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9acf6-122">**Iobjecttablecallback**</span><span class="sxs-lookup"><span data-stu-id="9acf6-122">**IObjectTableCallback**</span></span>](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 
