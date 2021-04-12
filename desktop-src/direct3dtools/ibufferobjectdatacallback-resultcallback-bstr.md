---
description: Ein Rückruf, der den Host über Puffer Informationen benachrichtigt, die von der assocaas-Anforderung in eine Datei geschrieben wurden.
MS-HAID: vspixengine.IBufferObjectDataCallback\_ResultCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ibufferobjectdatacallback:: resultCallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8083FDF-0A56-4777-8EFD-66F77AD195EA
api_name:
- IBufferObjectDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 41a5017171fee8476033e3c38d050bc38b1642a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392874"
---
# <a name="span-idvspixengineibufferobjectdatacallback_resultcallback_bstrspanibufferobjectdatacallbackresultcallback-method"></a><span data-ttu-id="84c3c-103"><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>Ibufferobjectdatacallback:: resultCallback-Methode</span><span class="sxs-lookup"><span data-stu-id="84c3c-103"><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>IBufferObjectDataCallback::ResultCallback method</span></span>

<span data-ttu-id="84c3c-104">Ein Rückruf, der den Host über Puffer Informationen benachrichtigt, die von der assocaas-Anforderung in eine Datei geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="84c3c-104">A callback that notifies the host of buffer information written to a file by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="84c3c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="84c3c-105">Syntax</span></span>

```C++
HRESULT ResultCallback(
   BSTR File
);
```

## <a name="parameters"></a><span data-ttu-id="84c3c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="84c3c-106">Parameters</span></span>

<span data-ttu-id="84c3c-107">*Datei* Eine com-Zeichenfolge, die den Pfadnamen der Datei enthält, in die Ergebnisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="84c3c-107">*File* A COM string that contains the pathname of the file where results are written.</span></span>

## <a name="return-value"></a><span data-ttu-id="84c3c-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84c3c-108">Return value</span></span>

<span data-ttu-id="84c3c-109">Wenn diese Methode erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="84c3c-109">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="84c3c-110">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="84c3c-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="84c3c-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84c3c-111">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="84c3c-112">Header</span><span class="sxs-lookup"><span data-stu-id="84c3c-112">Header</span></span></p></td><td><span data-ttu-id="84c3c-113">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="84c3c-113">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="84c3c-114"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84c3c-114"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="84c3c-115">**Ibufferobjectdatacallback**</span><span class="sxs-lookup"><span data-stu-id="84c3c-115">**IBufferObjectDataCallback**</span></span>](/windows/desktop/direct3dtools/ibufferobjectdatacallback)

 

 
