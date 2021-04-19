---
title: TF_ES_ Konstanten (msctf. h)
description: Die folgenden Konstanten werden von der ITF Context requesteditsession-Methode verwendet.
ms.assetid: 5498329f-3302-4f66-bdec-cab7db0cdc0e
topic_type:
- apiref
api_name:
- TF_ES_ASYNCDONTCARE
- TF_ES_SYNC
- TF_ES_READ
- TF_ES_READWRITE
- TF_ES_ASYNC
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ed96adc1d6f6d66671e91f7a70bce856663e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345918"
---
# <a name="tf_es_-constants"></a><span data-ttu-id="bffcd-103">TF \_ es- \_ \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="bffcd-103">TF\_ES\_\* Constants</span></span>

<span data-ttu-id="bffcd-104">Die folgenden Konstanten werden von der [ITF context:: requesteditsession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="bffcd-104">The following are constants used by the [ITfContext::RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession) method.</span></span>



| <span data-ttu-id="bffcd-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="bffcd-105">Constant/value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="bffcd-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bffcd-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                             |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_ES_ASYNCDONTCARE"></span><span id="tf_es_asyncdontcare"></span><dl> <span data-ttu-id="bffcd-107"><dt>**Tf \_ ES \_ asyncdontcare**</dt> <dt>(0)</dt></span><span class="sxs-lookup"><span data-stu-id="bffcd-107"><dt>**TF\_ES\_ASYNCDONTCARE**</dt> <dt>( 0 )</dt></span></span> </dl> | <span data-ttu-id="bffcd-108">Die Bearbeitungs Sitzung kann nach dem Ermessen des Vorgesetzten synchron oder asynchron erfolgen.</span><span class="sxs-lookup"><span data-stu-id="bffcd-108">The edit session can occur synchronously or asynchronously, at the discretion of the manager.</span></span> <span data-ttu-id="bffcd-109">Der Manager versucht, eine synchrone Bearbeitungs Sitzung zu planen, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="bffcd-109">The manager will attempt to schedule a synchronous edit session for improved performance.</span></span> <span data-ttu-id="bffcd-110">Dieser Wert kann nicht mit den TF \_ es- \_ Werten "Async" oder "TF \_ es Sync" kombiniert werden \_ .</span><span class="sxs-lookup"><span data-stu-id="bffcd-110">This value cannot be combined with the TF\_ES\_ASYNC or TF\_ES\_SYNC values.</span></span><br/>                                                                         |
| <span id="TF_ES_SYNC"></span><span id="tf_es_sync"></span><dl> <span data-ttu-id="bffcd-111"><dt>**Tf \_ ES \_ Sync**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="bffcd-111"><dt>**TF\_ES\_SYNC**</dt> <dt>( 0x1 )</dt></span></span> </dl>                          | <span data-ttu-id="bffcd-112">Die Bearbeitungs Sitzung muss synchron sein, oder die Anforderung schlägt fehl (mit tf \_ E \_ synchron).</span><span class="sxs-lookup"><span data-stu-id="bffcd-112">The edit session must be synchronous or the request will fail (with TF\_E\_SYNCHRONOUS).</span></span> <span data-ttu-id="bffcd-113">Dieses Flag sollte nur in dokumentierten Situationen verwendet werden (z. b. bei der Tastatureingabe), bei denen es erwartungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="bffcd-113">This flag should only be used in documented situations (such as keystroke handling) where it can be expected to succeed.</span></span> <span data-ttu-id="bffcd-114">Andernfalls schlägt der-Vorgang wahrscheinlich fehl.</span><span class="sxs-lookup"><span data-stu-id="bffcd-114">Otherwise the call will likely fail.</span></span> <span data-ttu-id="bffcd-115">Dieser Wert kann nicht mit den \_ Async-Werten von tf es \_ asyncdontcare oder TF es kombiniert werden \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="bffcd-115">This value cannot be combined with the TF\_ES\_ASYNCDONTCARE or TF\_ES\_ASYNC values.</span></span><br/> |
| <span id="TF_ES_READ"></span><span id="tf_es_read"></span><dl> <span data-ttu-id="bffcd-116"><dt>**Tf \_ \_Lese**</dt> Vorgänge <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="bffcd-116"><dt>**TF\_ES\_READ**</dt> <dt>( 0x2 )</dt></span></span> </dl>                          | <span data-ttu-id="bffcd-117">Fordert schreibgeschützten Zugriff auf den Kontext an.</span><span class="sxs-lookup"><span data-stu-id="bffcd-117">Requests read-only access to the context.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="TF_ES_READWRITE"></span><span id="tf_es_readwrite"></span><dl> <span data-ttu-id="bffcd-118"><dt>**Tf \_ ES- \_ Lesevorgang**</dt> <dt>(0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="bffcd-118"><dt>**TF\_ES\_READWRITE**</dt> <dt>( 0x6 )</dt></span></span> </dl>           | <span data-ttu-id="bffcd-119">Fordert den Lese-/Schreibzugriff auf den Kontext an.</span><span class="sxs-lookup"><span data-stu-id="bffcd-119">Requests read/write access to the context.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span id="TF_ES_ASYNC"></span><span id="tf_es_async"></span><dl> <span data-ttu-id="bffcd-120"><dt>**Tf \_ ES \_ Async**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="bffcd-120"><dt>**TF\_ES\_ASYNC**</dt> <dt>( 0x8 )</dt></span></span> </dl>                       | <span data-ttu-id="bffcd-121">Die Bearbeitungs Sitzung muss asynchron sein, oder die Anforderung kann nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bffcd-121">The edit session must be asynchronous or the request will fail.</span></span> <span data-ttu-id="bffcd-122">Dieser Wert kann nicht mit den TF \_ es \_ asyncdontcare-oder TF \_ es- \_ Synchronisierungs Werten kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="bffcd-122">This value cannot be combined with the TF\_ES\_ASYNCDONTCARE or TF\_ES\_SYNC values.</span></span><br/>                                                                                                                                                                                         |



## <a name="requirements"></a><span data-ttu-id="bffcd-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bffcd-123">Requirements</span></span>



| <span data-ttu-id="bffcd-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bffcd-124">Requirement</span></span> | <span data-ttu-id="bffcd-125">Wert</span><span class="sxs-lookup"><span data-stu-id="bffcd-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bffcd-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bffcd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bffcd-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bffcd-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bffcd-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bffcd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bffcd-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bffcd-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bffcd-130">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="bffcd-130">Redistributable</span></span><br/>          | <span data-ttu-id="bffcd-131">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bffcd-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="bffcd-132">Header</span><span class="sxs-lookup"><span data-stu-id="bffcd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bffcd-133"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="bffcd-133"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="bffcd-134">IDL</span><span class="sxs-lookup"><span data-stu-id="bffcd-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bffcd-135"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bffcd-135"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bffcd-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bffcd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bffcd-137">ITF context:: requestedizession</span><span class="sxs-lookup"><span data-stu-id="bffcd-137">ITfContext::RequestEditSession</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession)
</dt> </dl>

 

 





