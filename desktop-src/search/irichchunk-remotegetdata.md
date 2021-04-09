---
description: Ruft die PROPVARIANT-und Eingabe Zeichenfolge ab, die einen Datenblock darstellt. Das Aufrufen dieser Methode entspricht dem Aufrufen von GetData.
ms.assetid: 78846D1D-923F-4FEA-8BF2-B16BB1B21BB3
title: 'Irichchunk:: remotegetdata-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRichChunk.RemoteGetData
api_type:
- COM
api_location: ''
ms.openlocfilehash: 002c85b189a3994b70795c05228ae5331c610284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128505"
---
# <a name="irichchunkremotegetdata-method"></a><span data-ttu-id="a36aa-104">Irichchunk:: remotegetdata-Methode</span><span class="sxs-lookup"><span data-stu-id="a36aa-104">IRichChunk::RemoteGetData method</span></span>

<span data-ttu-id="a36aa-105">Ruft die [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -und Eingabe Zeichenfolge ab, die einen Datenblock darstellt.</span><span class="sxs-lookup"><span data-stu-id="a36aa-105">Retrieves the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) and input string that represents a chunk of data.</span></span> <span data-ttu-id="a36aa-106">Das Aufrufen dieser Methode entspricht dem Aufrufen von [**GetData**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata).</span><span class="sxs-lookup"><span data-stu-id="a36aa-106">Calling this method is the same as calling [**GetData**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata).</span></span>

## <a name="syntax"></a><span data-ttu-id="a36aa-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a36aa-107">Syntax</span></span>


```C++
HRESULT RemoteGetData(
  [out] ULONG       *pFirstPos,
  [out] ULONG       *pLength,
  [out] LPWSTR      *ppsz,
  [out] PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="a36aa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a36aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a36aa-109">*Pfirsich Torys* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a36aa-109">*pFirstPos* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a36aa-110">Empfängt die null basierte Anfangsposition des Bereichs.</span><span class="sxs-lookup"><span data-stu-id="a36aa-110">Receives the zero-based starting position of the range.</span></span> <span data-ttu-id="a36aa-111">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="a36aa-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a36aa-112">*pLength* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a36aa-112">*pLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a36aa-113">Empfängt die Länge des Bereichs.</span><span class="sxs-lookup"><span data-stu-id="a36aa-113">Receives the length of the range.</span></span> <span data-ttu-id="a36aa-114">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="a36aa-114">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a36aa-115">*ppsz* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a36aa-115">*ppsz* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a36aa-116">Empfängt den zugeordneten Unicode-Zeichen folgen Wert oder **null** , wenn er nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a36aa-116">Receives the associated Unicode string value, or **NULL** if not available.</span></span>

</dd> <dt>

<span data-ttu-id="a36aa-117">*pValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a36aa-117">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a36aa-118">Empfängt den zugeordneten [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Wert oder **VT \_ empty** , wenn nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a36aa-118">Receives the associated [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value, or **VT\_EMPTY** if not available.</span></span> <span data-ttu-id="a36aa-119">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="a36aa-119">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a36aa-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a36aa-120">Return value</span></span>

<span data-ttu-id="a36aa-121">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a36aa-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a36aa-122">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a36aa-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="a36aa-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a36aa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a36aa-124">**Irichchunk**</span><span class="sxs-lookup"><span data-stu-id="a36aa-124">**IRichChunk**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk)
</dt> </dl>

 

 
