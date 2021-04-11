---
description: Legt einen Rückruf fest, der während der Quell Auflösung die PMP-Medien Sitzung erstellt.
ms.assetid: 7277C5E0-BB91-4EEA-9529-64E66D179CDC
title: MFPKEY_PMP_Creation_Callback-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b18e04a15e035a9e4dc04a4039ce230342031a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215502"
---
# <a name="mfpkey_pmp_creation_callback-property"></a><span data-ttu-id="d03d7-103">Rückruf Eigenschaft für mfpkey \_ PMP- \_ Erstellung \_</span><span class="sxs-lookup"><span data-stu-id="d03d7-103">MFPKEY\_PMP\_Creation\_Callback property</span></span>

<span data-ttu-id="d03d7-104">Legt einen Rückruf fest, der während der Quell Auflösung die [PMP-Medien Sitzung](pmp-media-session.md) erstellt.</span><span class="sxs-lookup"><span data-stu-id="d03d7-104">Sets a callback that creates the [PMP Media Session](pmp-media-session.md) during source resolution.</span></span>



<span data-ttu-id="d03d7-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d03d7-105">Data type</span></span>

<span data-ttu-id="d03d7-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="d03d7-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="d03d7-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="d03d7-107">PROPVARIANT member</span></span>

<span data-ttu-id="d03d7-108">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="d03d7-108">\**IUnknown\** _</span></span>

<span data-ttu-id="d03d7-109">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="d03d7-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="d03d7-110">_ *punkVal*\*</span><span class="sxs-lookup"><span data-stu-id="d03d7-110">_ *punkVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="d03d7-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d03d7-111">Remarks</span></span>

<span data-ttu-id="d03d7-112">Für einige geschützte Inhalte ist möglicherweise die Verwendung dieser Eigenschaft erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d03d7-112">Some protected content might require the use of this property.</span></span> <span data-ttu-id="d03d7-113">Wenn dies der Fall ist, tritt bei der Quell Auflösung ein Fehler auf, und der Fehlercode **MF \_ E \_ \_ erfordert \_ PMP- \_ Erstellungs \_ Rückruf**.</span><span class="sxs-lookup"><span data-stu-id="d03d7-113">If so, the source resolution process fails with the error code **MF\_E\_RESOLUTION\_REQUIRES\_PMP\_CREATION\_CALLBACK**.</span></span>

<span data-ttu-id="d03d7-114">Gehen Sie folgendermaßen vor, um diese Eigenschaft zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d03d7-114">To use this property, do the following.</span></span>

1.  <span data-ttu-id="d03d7-115">Rufen Sie [**pscreatememorypropertystore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) auf, um einen Eigenschafts Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d03d7-115">Call [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create a property store.</span></span>
2.  <span data-ttu-id="d03d7-116">Implementieren Sie die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Rückruf Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d03d7-116">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) callback interface.</span></span>
3.  <span data-ttu-id="d03d7-117">Legen Sie die \_ Eigenschaft Rückruf für mfpkey PMP- \_ Erstellung \_ für den Eigenschaften Speicher fest.</span><span class="sxs-lookup"><span data-stu-id="d03d7-117">Set the MFPKEY\_PMP\_Creation\_Callback property on the property store.</span></span> <span data-ttu-id="d03d7-118">Der Wert ist ein Zeiger auf die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Implementierung.</span><span class="sxs-lookup"><span data-stu-id="d03d7-118">The value is a pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) implementation.</span></span>
4.  <span data-ttu-id="d03d7-119">Aufrufen von [**imfsourceresolver:: beginkreateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span><span class="sxs-lookup"><span data-stu-id="d03d7-119">Call [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span></span> <span data-ttu-id="d03d7-120">Übergeben Sie einen Zeiger auf den Eigenschaften Speicher im *prequiterparameter* .</span><span class="sxs-lookup"><span data-stu-id="d03d7-120">Pass in a pointer to the property store in the *pProps* parameter.</span></span>

<span data-ttu-id="d03d7-121">Führen Sie in der [**imfasynccallback:: Aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) -Methode Ihrer Rückruf Schnittstelle die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="d03d7-121">In the [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method of your callback interface, do the following.</span></span>

1.  <span data-ttu-id="d03d7-122">Rufen Sie [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) auf, um die [PMP-Medien Sitzung](pmp-media-session.md)zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d03d7-122">Call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the [PMP Media Session](pmp-media-session.md).</span></span>
2.  <span data-ttu-id="d03d7-123">Aufrufen von [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) in der PMP-Medien Sitzung an einen Zeiger auf die [**imfpmphost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d03d7-123">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the PMP Media Session to a pointer to the [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) interface.</span></span>
3.  <span data-ttu-id="d03d7-124">Rufen Sie [**imfasynkresult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) für das Result-Objekt auf, das im *pasynkresult* -Parameter von [**imfasynccallback:: Aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d03d7-124">Call [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) on the result object that is passed in the *pAsyncResult* parameter of [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="d03d7-125">Fragen Sie den zurückgegebenen [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger für die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="d03d7-125">Query the returned [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer for the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
4.  <span data-ttu-id="d03d7-126">Nennen Sie [**mfputworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) mit den folgenden Parametern:</span><span class="sxs-lookup"><span data-stu-id="d03d7-126">Call [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) with the following parameters:</span></span>
    -   <span data-ttu-id="d03d7-127">*dwqueue*: **mfasync- \_ Rückruf \_ Warteschlangen \_ Standard**</span><span class="sxs-lookup"><span data-stu-id="d03d7-127">*dwQueue*: **MFASYNC\_CALLBACK\_QUEUE\_STANDARD**</span></span>
    -   <span data-ttu-id="d03d7-128">*pCallback*: der [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Zeiger, der in Schritt 3 abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="d03d7-128">*pCallback*: The [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) pointer obtained in step 3.</span></span>
    -   <span data-ttu-id="d03d7-129">*pState*: der [**imfpmphost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) -Zeiger, der in Schritt 2 abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="d03d7-129">*pState*: The [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) pointer obtained in step 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="d03d7-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d03d7-130">Requirements</span></span>



| <span data-ttu-id="d03d7-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d03d7-131">Requirement</span></span> | <span data-ttu-id="d03d7-132">Wert</span><span class="sxs-lookup"><span data-stu-id="d03d7-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d03d7-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d03d7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d03d7-134">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="d03d7-134">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="d03d7-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d03d7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d03d7-136">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="d03d7-136">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="d03d7-137">Header</span><span class="sxs-lookup"><span data-stu-id="d03d7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="d03d7-138"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d03d7-138"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d03d7-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d03d7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d03d7-140">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d03d7-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d03d7-141">PMP-Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="d03d7-141">PMP Media Session</span></span>](pmp-media-session.md)
</dt> <dt>

[<span data-ttu-id="d03d7-142">Geschützter Medien Pfad</span><span class="sxs-lookup"><span data-stu-id="d03d7-142">Protected Media Path</span></span>](protected-media-path.md)
</dt> <dt>

[<span data-ttu-id="d03d7-143">Quellresolver</span><span class="sxs-lookup"><span data-stu-id="d03d7-143">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 
