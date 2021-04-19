---
title: TF_IAS_ Konstanten (msctf. h)
description: Die TF \_ IAS \_ \ Konstanten werden in Methoden verwendet, die Text oder eingebettete Objekte an einer Auswahl-oder Einfügemarke einfügen.
ms.assetid: adc5c539-fdb1-4829-ad17-2f54ec179c47
topic_type:
- apiref
api_name:
- TF_IAS_NOQUERY
- TF_IAS_QUERYONLY
- TF_IAS_NO_DEFAULT_COMPOSITION
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a025e295d80ac9a58625c221c4b4c224233fbb26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339151"
---
# <a name="tf_ias_-constants"></a><span data-ttu-id="d4bd5-103">TF \_ IAS- \_ \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="d4bd5-103">TF\_IAS\_\* Constants</span></span>

<span data-ttu-id="d4bd5-104">Die TF \_ IAS- \_ \* Konstanten werden als bitfeldflags in Methoden verwendet, die Text oder eingebettete Objekte an einer Auswahl-oder Einfügemarke einfügen.</span><span class="sxs-lookup"><span data-stu-id="d4bd5-104">The TF\_IAS\_\* constants are used as bitfield flags in methods that insert text or embedded objects at a selection or insertion point.</span></span>



| <span data-ttu-id="d4bd5-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="d4bd5-105">Constant/value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="d4bd5-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4bd5-106">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_IAS_NOQUERY"></span><span id="tf_ias_noquery"></span><dl> <span data-ttu-id="d4bd5-107"><dt>**Tf \_ IAS \_ noquery**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="d4bd5-107"><dt>**TF\_IAS\_NOQUERY**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                                       | <span data-ttu-id="d4bd5-108">Der Text wird eingefügt, und der Bereichs Zeiger wird beim Beenden auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d4bd5-108">Text is inserted and the range pointer is set to **NULL** upon exit.</span></span> <span data-ttu-id="d4bd5-109">Kann nicht mit dem TF \_ IAS- \_ Flag queryonly kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="d4bd5-109">Cannot be combined with the TF\_IAS\_QUERYONLY flag.</span></span><br/>       |
| <span id="TF_IAS_QUERYONLY"></span><span id="tf_ias_queryonly"></span><dl> <span data-ttu-id="d4bd5-110"><dt>**Tf \_ IAS- \_ queryonly**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="d4bd5-110"><dt>**TF\_IAS\_QUERYONLY**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                                 | <span data-ttu-id="d4bd5-111">Führen Sie den Einfügevorgang nicht aus.</span><span class="sxs-lookup"><span data-stu-id="d4bd5-111">Do not perform the insert.</span></span> <span data-ttu-id="d4bd5-112">Für den Aufrufer muss nur der Bereichs Zeiger festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d4bd5-112">Caller only requires the range pointer to be set.</span></span> <span data-ttu-id="d4bd5-113">Kann nicht mit dem TF \_ IAS \_ noquery-Flag kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="d4bd5-113">Cannot be combined with the TF\_IAS\_NOQUERY flag.</span></span><br/> |
| <span id="TF_IAS_NO_DEFAULT_COMPOSITION"></span><span id="tf_ias_no_default_composition"></span><dl> <span data-ttu-id="d4bd5-114"><dt>**Tf \_ IAS \_ keine \_ Standard \_ Komposition**</dt> <dt>(0x80000000)</dt></span><span class="sxs-lookup"><span data-stu-id="d4bd5-114"><dt>**TF\_IAS\_NO\_DEFAULT\_COMPOSITION**</dt> <dt>( 0x80000000 )</dt></span></span> </dl> | <span data-ttu-id="d4bd5-115">TSF erstellt keine Standard Komposition, wenn eine Komposition erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d4bd5-115">TSF will not create a default composition if a composition is required.</span></span> <span data-ttu-id="d4bd5-116">Der Aufrufer muss eine Komposition für den Bereich starten.</span><span class="sxs-lookup"><span data-stu-id="d4bd5-116">Caller must start a composition over the range.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="d4bd5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4bd5-117">Requirements</span></span>



| <span data-ttu-id="d4bd5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4bd5-118">Requirement</span></span> | <span data-ttu-id="d4bd5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d4bd5-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d4bd5-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4bd5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d4bd5-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4bd5-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d4bd5-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4bd5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d4bd5-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4bd5-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d4bd5-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="d4bd5-124">Redistributable</span></span><br/>          | <span data-ttu-id="d4bd5-125">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d4bd5-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="d4bd5-126">Header</span><span class="sxs-lookup"><span data-stu-id="d4bd5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4bd5-127"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4bd5-127"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4bd5-128">IDL</span><span class="sxs-lookup"><span data-stu-id="d4bd5-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d4bd5-129"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d4bd5-129"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4bd5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4bd5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4bd5-131">ITextStoreACP:: insertembedentdatselection</span><span class="sxs-lookup"><span data-stu-id="d4bd5-131">ITextStoreACP::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="d4bd5-132">ITextStoreACP:: inserttextatselection</span><span class="sxs-lookup"><span data-stu-id="d4bd5-132">ITextStoreACP::InsertTextAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-inserttextatselection)
</dt> <dt>

[<span data-ttu-id="d4bd5-133">Itextstoreanchor:: insertembedentdatselection</span><span class="sxs-lookup"><span data-stu-id="d4bd5-133">ITextStoreAnchor::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="d4bd5-134">Itextstoreanchor:: inserttextatselection</span><span class="sxs-lookup"><span data-stu-id="d4bd5-134">ITextStoreAnchor::InsertTextAtSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-inserttextatselection)
</dt> <dt>

[<span data-ttu-id="d4bd5-135">Itfinsertatselection:: insertembedentdatselection</span><span class="sxs-lookup"><span data-stu-id="d4bd5-135">ITfInsertAtSelection::InsertEmbeddedAtSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-insertembeddedatselection)
</dt> <dt>

[<span data-ttu-id="d4bd5-136">Itfinsertatselection:: inserttextatselection</span><span class="sxs-lookup"><span data-stu-id="d4bd5-136">ITfInsertAtSelection::InsertTextAtSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-inserttextatselection)
</dt> </dl>

 

 





