---
title: XTYP_ADVDATA Transaktion (Ddeml. h)
description: Informiert den Client, dass sich der Wert des Datenelements geändert hat. Dynamischer Datenaustausch die DDE-Client Rückruffunktion (DDE Callback) empfängt diese Transaktion, nachdem eine Empfehlung-Schleife mit einem Server eingerichtet wurde.
ms.assetid: c6e61785-b98c-4ffa-9d23-339e1c66cb4d
keywords:
- XTYP_ADVDATA Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_ADVDATA
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8359e34388d185200b5f30c4554e138cc1f6b94a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338120"
---
# <a name="xtyp_advdata-transaction"></a><span data-ttu-id="0a92d-105">\_Xttyadvdata-Transaktion</span><span class="sxs-lookup"><span data-stu-id="0a92d-105">XTYP\_ADVDATA transaction</span></span>

<span data-ttu-id="0a92d-106">Informiert den Client, dass sich der Wert des Datenelements geändert hat.</span><span class="sxs-lookup"><span data-stu-id="0a92d-106">Informs the client that the value of the data item has changed.</span></span> <span data-ttu-id="0a92d-107">Dynamischer Datenaustausch die DDE-Client Rückruffunktion ( [*DDE Callback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt diese Transaktion, nachdem eine Empfehlung-Schleife mit einem Server eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="0a92d-107">The Dynamic Data Exchange (DDE) client callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction after establishing an advise loop with a server.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_ADVDATA            (0x0010 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="0a92d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a92d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a92d-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="0a92d-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="0a92d-110">Der Transaktionstyp:</span><span class="sxs-lookup"><span data-stu-id="0a92d-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="0a92d-111">*UF*</span><span class="sxs-lookup"><span data-stu-id="0a92d-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="0a92d-112">Das Format Atom der vom Server gesendeten Daten.</span><span class="sxs-lookup"><span data-stu-id="0a92d-112">The format atom of the data sent from the server.</span></span>

</dd> <dt>

<span data-ttu-id="0a92d-113">*has*</span><span class="sxs-lookup"><span data-stu-id="0a92d-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="0a92d-114">Ein Handle für die Konversation.</span><span class="sxs-lookup"><span data-stu-id="0a92d-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="0a92d-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="0a92d-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="0a92d-116">Ein Handle für den Themen Namen.</span><span class="sxs-lookup"><span data-stu-id="0a92d-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="0a92d-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="0a92d-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="0a92d-118">Ein Handle für den Elementnamen.</span><span class="sxs-lookup"><span data-stu-id="0a92d-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="0a92d-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="0a92d-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="0a92d-120">Ein Handle für die Daten, die dem Themen Namen und dem Elementnamen paar zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0a92d-120">A handle to the data associated with the topic name and item name pair.</span></span> <span data-ttu-id="0a92d-121">Dieser Parameter ist **null** , wenn der Client das **xtypf \_ NODATA** -Flag angegeben hat, als er die Empfehlung-Schleife angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="0a92d-121">This parameter is **NULL** if the client specified the **XTYPF\_NODATA** flag when it requested the advise loop.</span></span>

</dd> <dt>

<span data-ttu-id="0a92d-122">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="0a92d-122">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="0a92d-123">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0a92d-123">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0a92d-124">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="0a92d-124">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="0a92d-125">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0a92d-125">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a92d-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a92d-126">Return value</span></span>

<span data-ttu-id="0a92d-127">Eine DDE-Rückruffunktion sollte **DDE \_ fakk** zurückgeben, wenn Sie diese Transaktion verarbeitet, **DDE \_ fausgelastet** , wenn Sie für die Verarbeitung dieser Transaktion zu stark ausgelastet ist, oder **DDE \_ fnotverarbeitete** , wenn Sie diese Transaktion ablehnt.</span><span class="sxs-lookup"><span data-stu-id="0a92d-127">A DDE callback function should return **DDE\_FACK** if it processes this transaction, **DDE\_FBUSY** if it is too busy to process this transaction, or **DDE\_FNOTPROCESSED** if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a92d-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a92d-128">Remarks</span></span>

<span data-ttu-id="0a92d-129">Eine Anwendung darf das Daten handle, das während dieser Transaktion abgerufen wurde, nicht freigeben.</span><span class="sxs-lookup"><span data-stu-id="0a92d-129">An application must not free the data handle obtained during this transaction.</span></span> <span data-ttu-id="0a92d-130">Eine Anwendung muss jedoch die Daten kopieren, die dem Daten Handle zugeordnet sind, wenn die Anwendung die Daten verarbeiten muss, nachdem die Rückruffunktion zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="0a92d-130">An application must, however, copy the data associated with the data handle if the application must process the data after the callback function returns.</span></span> <span data-ttu-id="0a92d-131">Eine Anwendung kann die [**DDE GetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) -Funktion verwenden, um die Daten zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="0a92d-131">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a92d-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a92d-132">Requirements</span></span>



| <span data-ttu-id="0a92d-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a92d-133">Requirement</span></span> | <span data-ttu-id="0a92d-134">Wert</span><span class="sxs-lookup"><span data-stu-id="0a92d-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a92d-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a92d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0a92d-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a92d-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0a92d-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a92d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0a92d-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a92d-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="0a92d-139">Header</span><span class="sxs-lookup"><span data-stu-id="0a92d-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a92d-140"><dt>Ddeml. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a92d-140"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a92d-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a92d-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="0a92d-142">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="0a92d-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0a92d-143">**DDE clienttransaction**</span><span class="sxs-lookup"><span data-stu-id="0a92d-143">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="0a92d-144">**DDE GetData**</span><span class="sxs-lookup"><span data-stu-id="0a92d-144">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

[<span data-ttu-id="0a92d-145">**DDE postadvise**</span><span class="sxs-lookup"><span data-stu-id="0a92d-145">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="0a92d-146">**Licher**</span><span class="sxs-lookup"><span data-stu-id="0a92d-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0a92d-147">dynamischer Datenaustausch-Verwaltungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0a92d-147">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

