---
title: XTYP_XACT_COMPLETE Transaktion (Ddeml. h)
description: Eine dynamischer Datenaustausch (DDE)-Client Rückruffunktion (DDE Callback) empfängt die vollständige xD- \_ \_ Transaktion, wenn eine asynchrone Transaktion, die durch einen-Aufrufs der DDE clienttransaction-Funktion initiiert wurde, abgeschlossen wurde.
ms.assetid: d34a6fab-0e3c-44fe-b25f-7011228fe261
keywords:
- XTYP_XACT_COMPLETE Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_XACT_COMPLETE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03a81869270a771836c4dd5c1a6b300f148ea13d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338717"
---
# <a name="xtyp_xact_complete-transaction"></a><span data-ttu-id="7db3e-104">\_Xttxact- \_ Transaktion abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="7db3e-104">XTYP\_XACT\_COMPLETE transaction</span></span>

<span data-ttu-id="7db3e-105">Eine dynamischer Datenaustausch (DDE)-Client Rückruffunktion ( [*DDE Callback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt die **\_ \_ vollständige xD** -Transaktion, wenn eine asynchrone Transaktion, die durch einen-Aufrufs der [**DDE clienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) -Funktion initiiert wurde, abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="7db3e-105">A Dynamic Data Exchange (DDE) client callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_XACT\_COMPLETE** transaction when an asynchronous transaction, initiated by a call to the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function, has completed.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_XACT_COMPLETE      (0x0080 | XCLASS_NOTIFICATION  )
```



## <a name="parameters"></a><span data-ttu-id="7db3e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7db3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7db3e-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="7db3e-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="7db3e-108">Der Transaktionstyp:</span><span class="sxs-lookup"><span data-stu-id="7db3e-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="7db3e-109">*UF*</span><span class="sxs-lookup"><span data-stu-id="7db3e-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="7db3e-110">Das Format der Daten, die der abgeschlossenen Transaktion (falls zutreffend) zugeordnet sind, oder **null** , wenn während der Transaktion keine Daten ausgetauscht wurden.</span><span class="sxs-lookup"><span data-stu-id="7db3e-110">The format of the data associated with the completed transaction (if applicable) or **NULL** if no data was exchanged during the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="7db3e-111">*has*</span><span class="sxs-lookup"><span data-stu-id="7db3e-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="7db3e-112">Ein Handle für die Konversation.</span><span class="sxs-lookup"><span data-stu-id="7db3e-112">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="7db3e-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="7db3e-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="7db3e-114">Ein Handle für den Themen Namen, der an der abgeschlossenen Transaktion beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="7db3e-114">A handle to the topic name involved in the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="7db3e-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="7db3e-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="7db3e-116">Ein Handle für den Elementnamen, der an der abgeschlossenen Transaktion beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="7db3e-116">A handle to the item name involved in the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="7db3e-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="7db3e-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="7db3e-118">Ein Handle für die Daten, die an der abgeschlossenen Transaktion beteiligt sind, falls zutreffend.</span><span class="sxs-lookup"><span data-stu-id="7db3e-118">A handle to the data involved in the completed transaction, if applicable.</span></span> <span data-ttu-id="7db3e-119">Wenn die Transaktion erfolgreich war, aber keine Daten umfasste, ist dieser Parameter **true**.</span><span class="sxs-lookup"><span data-stu-id="7db3e-119">If the transaction was successful but involved no data, this parameter is **TRUE**.</span></span> <span data-ttu-id="7db3e-120">Dieser Parameter ist **null** , wenn die Transaktion nicht erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="7db3e-120">This parameter is **NULL** if the transaction was unsuccessful.</span></span>

</dd> <dt>

<span data-ttu-id="7db3e-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="7db3e-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="7db3e-122">Der Transaktions Bezeichner der abgeschlossenen Transaktion.</span><span class="sxs-lookup"><span data-stu-id="7db3e-122">The transaction identifier of the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="7db3e-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="7db3e-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="7db3e-124">Alle anwendbaren **DDE \_** -Statusflags im unteren Wort.</span><span class="sxs-lookup"><span data-stu-id="7db3e-124">Any applicable **DDE\_** status flags in the low word.</span></span> <span data-ttu-id="7db3e-125">Dieser Parameter bietet Unterstützung für Anwendungen, die von **DDE \_ appstatus** Bits abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="7db3e-125">This parameter provides support for applications dependent on **DDE\_APPSTATUS** bits.</span></span> <span data-ttu-id="7db3e-126">Es wird empfohlen, dass Anwendungen diese Bits nicht mehr verwenden, da Sie möglicherweise in zukünftigen Versionen der Ddeml nicht mehr unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7db3e-126">It is recommended that applications no longer use these bits   they may not be supported in future versions of the DDEML.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7db3e-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7db3e-127">Remarks</span></span>

<span data-ttu-id="7db3e-128">Eine Anwendung darf das Daten handle, das während dieser Transaktion abgerufen wurde, nicht freigeben.</span><span class="sxs-lookup"><span data-stu-id="7db3e-128">An application must not free the data handle obtained during this transaction.</span></span> <span data-ttu-id="7db3e-129">Eine Anwendung muss jedoch die Daten kopieren, die dem Daten Handle zugeordnet sind, wenn die Anwendung die Daten verarbeiten muss, nachdem die Rückruffunktion zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="7db3e-129">An application must, however, copy the data associated with the data handle if the application must process the data after the callback function returns.</span></span> <span data-ttu-id="7db3e-130">Eine Anwendung kann die [**DDE GetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) -Funktion verwenden, um die Daten zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="7db3e-130">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

## <a name="requirements"></a><span data-ttu-id="7db3e-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7db3e-131">Requirements</span></span>



| <span data-ttu-id="7db3e-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7db3e-132">Requirement</span></span> | <span data-ttu-id="7db3e-133">Wert</span><span class="sxs-lookup"><span data-stu-id="7db3e-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7db3e-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7db3e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7db3e-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7db3e-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7db3e-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7db3e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7db3e-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7db3e-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="7db3e-138">Header</span><span class="sxs-lookup"><span data-stu-id="7db3e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7db3e-139"><dt>Ddeml. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7db3e-139"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7db3e-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7db3e-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="7db3e-141">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="7db3e-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7db3e-142">**DDE clienttransaction**</span><span class="sxs-lookup"><span data-stu-id="7db3e-142">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="7db3e-143">**DDE GetData**</span><span class="sxs-lookup"><span data-stu-id="7db3e-143">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

<span data-ttu-id="7db3e-144">**Licher**</span><span class="sxs-lookup"><span data-stu-id="7db3e-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7db3e-145">dynamischer Datenaustausch-Verwaltungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7db3e-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

