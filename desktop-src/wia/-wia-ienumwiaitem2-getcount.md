---
description: Gibt die Anzahl von Elementen zurück, die von diesem Enumerator gespeichert werden.
ms.assetid: d374ec81-0bd5-4b5d-8002-e3b53476421a
title: 'IEnumWiaItem2:: GetCount-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.GetCount
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 23c067b8e4da93d678f641890a85e2535b3ca50d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041839"
---
# <a name="ienumwiaitem2getcount-method"></a><span data-ttu-id="41d60-103">IEnumWiaItem2:: GetCount-Methode</span><span class="sxs-lookup"><span data-stu-id="41d60-103">IEnumWiaItem2::GetCount method</span></span>

<span data-ttu-id="41d60-104">Gibt die Anzahl von Elementen zurück, die von diesem Enumerator gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="41d60-104">Returns the number of elements stored by this enumerator.</span></span>

## <a name="syntax"></a><span data-ttu-id="41d60-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="41d60-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *cElt
);
```



## <a name="parameters"></a><span data-ttu-id="41d60-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="41d60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41d60-107">*celt* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="41d60-107">*cElt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41d60-108">Typ: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="41d60-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="41d60-109">Empfängt einen Zeiger auf ein _ \*ulong\*\*-Element, das die Anzahl der Elemente in der-Enumeration empfängt.</span><span class="sxs-lookup"><span data-stu-id="41d60-109">Receives a pointer to a _ *ULONG*\* that receives the number of elements in the enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41d60-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41d60-110">Return value</span></span>

<span data-ttu-id="41d60-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="41d60-111">Type: **HRESULT**</span></span>

<span data-ttu-id="41d60-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="41d60-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="41d60-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="41d60-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="41d60-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41d60-114">Requirements</span></span>



| <span data-ttu-id="41d60-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41d60-115">Requirement</span></span> | <span data-ttu-id="41d60-116">Wert</span><span class="sxs-lookup"><span data-stu-id="41d60-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="41d60-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41d60-117">Minimum supported client</span></span><br/> | <span data-ttu-id="41d60-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41d60-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="41d60-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41d60-119">Minimum supported server</span></span><br/> | <span data-ttu-id="41d60-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41d60-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="41d60-121">Header</span><span class="sxs-lookup"><span data-stu-id="41d60-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="41d60-122"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="41d60-122"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="41d60-123">IDL</span><span class="sxs-lookup"><span data-stu-id="41d60-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41d60-124"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="41d60-124"><dt>Wia.idl</dt></span></span> </dl> |



 

 




