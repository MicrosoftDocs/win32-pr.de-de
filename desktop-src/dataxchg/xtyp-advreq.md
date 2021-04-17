---
title: XTYP_ADVREQ Transaktion (Ddeml. h)
description: Mit der xtipp- \_ advreq-Transaktion wird dem Server mitgeteilt, dass eine Benachrichtigungs Transaktion für den angegebenen Themen Namen und das angegebene Elementnamen paar aussteht und dass die Daten, die dem Themen Namen und dem Elementnamen paar entsprechen, geändert wurden.
ms.assetid: 9bd43e61-cbd6-4d53-bab3-90e85819b16b
keywords:
- XTYP_ADVREQ Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_ADVREQ
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2884e838268342ab10c556c6ae3cfc8349ed5d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391974"
---
# <a name="xtyp_advreq-transaction"></a><span data-ttu-id="8e07a-104">XYP- \_ advreq-Transaktion</span><span class="sxs-lookup"><span data-stu-id="8e07a-104">XTYP\_ADVREQ transaction</span></span>

<span data-ttu-id="8e07a-105">Mit der **xtipp- \_ advreq** -Transaktion wird dem Server mitgeteilt, dass eine Benachrichtigungs Transaktion für den angegebenen Themen Namen und das angegebene Elementnamen paar aussteht und dass die Daten, die dem Themen Namen und dem Elementnamen paar entsprechen, geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="8e07a-105">The **XTYP\_ADVREQ** transaction informs the server that an advise transaction is outstanding on the specified topic name and item name pair and that data corresponding to the topic name and item name pair has changed.</span></span> <span data-ttu-id="8e07a-106">Das System sendet diese Transaktion an die dynamischer Datenaustausch (DDE)-Rückruffunktion [*ddecallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), nachdem der Server die [**ddepostadvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) -Funktion aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="8e07a-106">The system sends this transaction to the Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), after the server calls the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ADVREQ             (0x0020 | XCLASS_DATA | XTYPF_NOBLOCK )
```



## <a name="parameters"></a><span data-ttu-id="8e07a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e07a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e07a-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="8e07a-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="8e07a-109">Der Transaktionstyp:</span><span class="sxs-lookup"><span data-stu-id="8e07a-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="8e07a-110">*UF*</span><span class="sxs-lookup"><span data-stu-id="8e07a-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="8e07a-111">Das Format, in dem die Daten an den Client übermittelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8e07a-111">The format in which the data should be submitted to the client.</span></span>

</dd> <dt>

<span data-ttu-id="8e07a-112">*has*</span><span class="sxs-lookup"><span data-stu-id="8e07a-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="8e07a-113">Ein Handle für die Konversation.</span><span class="sxs-lookup"><span data-stu-id="8e07a-113">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="8e07a-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="8e07a-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="8e07a-115">Ein Handle für den Themen Namen.</span><span class="sxs-lookup"><span data-stu-id="8e07a-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="8e07a-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="8e07a-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="8e07a-117">Ein Handle für den Elementnamen, der geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="8e07a-117">A handle to the item name that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="8e07a-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="8e07a-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="8e07a-119">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e07a-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="8e07a-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="8e07a-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="8e07a-121">Die Anzahl der **xD \_ advreq** -Transaktionen im nieder wertigen Wort, die im Kontext des aktuellen Aufrufens der [**ddepostadvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) -Funktion für dasselbe Thema, Element und denselben Format Namen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="8e07a-121">The count, in the low-order word, of **XTYP\_ADVREQ** transactions that remain to be processed on the same topic, item, and format name set within the context of the current call to the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function.</span></span> <span data-ttu-id="8e07a-122">Der Zählerwert ist 0 (null), wenn die aktuelle **xD- \_ advreq** -Transaktion der letzte ist.</span><span class="sxs-lookup"><span data-stu-id="8e07a-122">The count is zero if the current **XTYP\_ADVREQ** transaction is the last one.</span></span> <span data-ttu-id="8e07a-123">Ein Server kann diese Anzahl verwenden, um zu bestimmen, ob ein **hdata \_** -Daten Handle für die Empfehlung erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e07a-123">A server can use this count to determine whether to create an **HDATA\_APPOWNED** data handle to the advise data.</span></span>

<span data-ttu-id="8e07a-124">Das nieder wertige Wort wird auf **cadv \_ lateack** festgelegt, wenn die Ddeml die **xD- \_ advreq** -Transaktion aufgrund einer Nachricht, die eine späte Bestätigung durchläuft, von \_ einem Client, der vom Server entfernt wird, ausgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="8e07a-124">The low-order word is set to **CADV\_LATEACK** if the DDEML issued the **XTYP\_ADVREQ** transaction because of a late-arriving DDE\_ACK message from a client being outrun by the server.</span></span>

<span data-ttu-id="8e07a-125">Das höchst wertige Wort wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e07a-125">The high-order word is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8e07a-126">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="8e07a-126">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="8e07a-127">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e07a-127">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e07a-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e07a-128">Return value</span></span>

<span data-ttu-id="8e07a-129">Der Server sollte zuerst die [**ddecreatedatahandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) -Funktion aufrufen, um ein Daten Handle zu erstellen, das die geänderten Daten identifiziert und dann das Handle zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8e07a-129">The server should first call the [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) function to create a data handle that identifies the changed data and then return the handle.</span></span> <span data-ttu-id="8e07a-130">Der Server sollte **null** zurückgeben, wenn die Transaktion nicht abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="8e07a-130">The server should return **NULL** if it is unable to complete the transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e07a-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e07a-131">Remarks</span></span>

<span data-ttu-id="8e07a-132">Ein Server kann diesen Transaktionstyp nicht blockieren. der Rückgabecode des **CBR- \_ Blocks** wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8e07a-132">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e07a-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e07a-133">Requirements</span></span>



| <span data-ttu-id="8e07a-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e07a-134">Requirement</span></span> | <span data-ttu-id="8e07a-135">Wert</span><span class="sxs-lookup"><span data-stu-id="8e07a-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e07a-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e07a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8e07a-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e07a-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8e07a-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e07a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8e07a-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e07a-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="8e07a-140">Header</span><span class="sxs-lookup"><span data-stu-id="8e07a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e07a-141"><dt>Ddeml. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e07a-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e07a-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e07a-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="8e07a-143">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="8e07a-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8e07a-144">**Ddecreatedatahandle**</span><span class="sxs-lookup"><span data-stu-id="8e07a-144">**DdeCreateDataHandle**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[<span data-ttu-id="8e07a-145">**DDEInitialize**</span><span class="sxs-lookup"><span data-stu-id="8e07a-145">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="8e07a-146">**DDE postadvise**</span><span class="sxs-lookup"><span data-stu-id="8e07a-146">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="8e07a-147">**Licher**</span><span class="sxs-lookup"><span data-stu-id="8e07a-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8e07a-148">dynamischer Datenaustausch-Verwaltungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8e07a-148">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

