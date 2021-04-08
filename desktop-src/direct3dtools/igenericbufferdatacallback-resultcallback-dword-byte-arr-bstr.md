---
description: Ein Rückruf, der den Host über generische Puffer Informationen benachrichtigt, die von der assocaas-Anforderung zurückgegeben werden.
MS-HAID: vspixengine.IGenericBufferDataCallback\_ResultCallback\_DWORD\_BYTE\_arr\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Igenericbufferdatacallback:: resultCallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5627A93E-8BE8-4413-BFB4-724AF2DDFEB6
api_name:
- IGenericBufferDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: be2d6aa7cd5e844cd5d1297c16de2ebb21c939a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747152"
---
# <a name="span-idvspixengineigenericbufferdatacallback_resultcallback_dword_byte_arr_bstrspanigenericbufferdatacallbackresultcallback-method"></a><span data-ttu-id="41a6b-103"><span id="vspixengine.igenericbufferdatacallback_resultcallback_dword_byte_arr_bstr"></span>Igenericbufferdatacallback:: resultCallback-Methode</span><span class="sxs-lookup"><span data-stu-id="41a6b-103"><span id="vspixengine.igenericbufferdatacallback_resultcallback_dword_byte_arr_bstr"></span>IGenericBufferDataCallback::ResultCallback method</span></span>

<span data-ttu-id="41a6b-104">Ein Rückruf, der den Host über generische Puffer Informationen benachrichtigt, die von der assocaas-Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="41a6b-104">A callback that notifies the host of generic buffer information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="41a6b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="41a6b-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD   size,
   BYTE [] count0_buffer,
   BSTR    type
);
```

## <a name="parameters"></a><span data-ttu-id="41a6b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="41a6b-106">Parameters</span></span>

<span data-ttu-id="41a6b-107">*Größe* </span><span class="sxs-lookup"><span data-stu-id="41a6b-107">*size* </span></span>  
<span data-ttu-id="41a6b-108">Die Größe des Puffer Inhalts in Bytes.</span><span class="sxs-lookup"><span data-stu-id="41a6b-108">The size of the buffer contents in bytes.</span></span>

<span data-ttu-id="41a6b-109">*count0- \_ Puffer* </span><span class="sxs-lookup"><span data-stu-id="41a6b-109">*count0\_buffer* </span></span>  
<span data-ttu-id="41a6b-110">Der Pufferinhalt.</span><span class="sxs-lookup"><span data-stu-id="41a6b-110">The buffer contents.</span></span> <span data-ttu-id="41a6b-111">In den meisten Fällen handelt es sich um XML-Daten.</span><span class="sxs-lookup"><span data-stu-id="41a6b-111">In most cases this is XML data.</span></span>

<span data-ttu-id="41a6b-112">*Typ* </span><span class="sxs-lookup"><span data-stu-id="41a6b-112">*type* </span></span>  
<span data-ttu-id="41a6b-113">Eine com-Zeichenfolge, die den Typ des im Puffer zurückgegebenen Inhalts angibt.</span><span class="sxs-lookup"><span data-stu-id="41a6b-113">A COM string that indicates the type of content returned in the buffer.</span></span>

## <a name="return-value"></a><span data-ttu-id="41a6b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41a6b-114">Return value</span></span>

<span data-ttu-id="41a6b-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="41a6b-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="41a6b-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="41a6b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="41a6b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41a6b-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="41a6b-118">Header</span><span class="sxs-lookup"><span data-stu-id="41a6b-118">Header</span></span></p></td><td><span data-ttu-id="41a6b-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="41a6b-119">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="41a6b-120"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41a6b-120"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="41a6b-121">**Igenericbufferdatacallback**</span><span class="sxs-lookup"><span data-stu-id="41a6b-121">**IGenericBufferDataCallback**</span></span>](/windows/desktop/direct3dtools/igenericbufferdatacallback)

 

 
