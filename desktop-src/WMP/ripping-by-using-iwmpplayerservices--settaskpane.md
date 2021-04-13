---
title: Ripping unter Verwendung von IWMPPlayerServices setTaskPane
description: Ripping unter Verwendung von IWMPPlayerServices setTaskPane
ms.assetid: 0d3efb0e-e8f5-40e3-abb5-6ad22009a4eb
keywords:
- Windows Media Player, CD-einreißen
- Windows Media Player-Objektmodell, CD-einreißen
- Objektmodell, CD-einreißen
- Windows Media Player ActiveX-Steuerelement, CD-einreißen
- ActiveX-Steuerelement, CD-einreißen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-einreißen
- Windows Media Player Mobile, CD-einreißen
- CD-Ripping, iwmpplayerservices settaskpane-Schnittstelle
- einreißen CDs, iwmpplayerservices settaskpane-Schnittstelle
- Iwmpplayerservices-settaskpane-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb1a09d67f310266ae4818bc0b594fe3b74d128
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104472381"
---
# <a name="ripping-by-using-iwmpplayerservicessettaskpane"></a><span data-ttu-id="283b7-113">Ripping mithilfe von iwmpplayerservices:: settaskpane</span><span class="sxs-lookup"><span data-stu-id="283b7-113">Ripping by Using IWMPPlayerServices::setTaskPane</span></span>

> [!Note]  
> <span data-ttu-id="283b7-114">In diesem Abschnitt wird eine Funktion der Windows Media Player 9-Reihe und der ActiveX-Steuerelemente von Windows Media Player 10 dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="283b7-114">This section documents a feature of the Windows Media Player 9 Series and Windows Media Player 10 ActiveX controls.</span></span> <span data-ttu-id="283b7-115">Es wird empfohlen, die **iwmpcdromrip** -Schnittstelle mit neueren Versionen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="283b7-115">It is recommended that you use the **IWMPCdromRip** interface with later versions.</span></span> <span data-ttu-id="283b7-116">Siehe [iwmpcdromrip-Schnittstelle](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip).</span><span class="sxs-lookup"><span data-stu-id="283b7-116">See [IWMPCdromRip Interface](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip).</span></span>

 

<span data-ttu-id="283b7-117">Sie können das Steuerelement Windows Media Player 9 oder höher verwenden, um CD-Spuren auf den Computer des Benutzers zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="283b7-117">You can use the Windows Media Player 9 Series or later control to copy CD tracks to the user's computer.</span></span> <span data-ttu-id="283b7-118">Dieser Vorgang wird als *einreißen* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="283b7-118">This process is called *ripping*.</span></span> <span data-ttu-id="283b7-119">Zu diesem Zweck müssen Sie das Windows Media Player-Steuerelement in den Remote Modus einbetten.</span><span class="sxs-lookup"><span data-stu-id="283b7-119">To do this, you must embed the Windows Media Player control in remote mode.</span></span> <span data-ttu-id="283b7-120">Weitere Informationen zum Remote Modus finden Sie unter [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).</span><span class="sxs-lookup"><span data-stu-id="283b7-120">For more information about remote mode, see [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).</span></span>

<span data-ttu-id="283b7-121">Um den einreißen-Prozess zu starten, nennen Sie [iwmpplayerservices:: settaskpane](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane), und übergeben Sie den copyfromcd? AutoCopy:*ID* -Wert für den *bstrautaskpane* -Parameter, wobei *ID* der Index des CD-Laufwerks ist, von dem kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="283b7-121">To start the ripping process, call [IWMPPlayerServices::setTaskPane](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane), passing the CopyFromCD?AutoCopy:*id* value for the *bstrTaskPane* parameter, where *id* is the index of the CD drive from which to copy.</span></span> <span data-ttu-id="283b7-122">Dieser Index entspricht dem Index eines **CDROM** -Objekts in der **iwmpcdromcollection** -Schnittstelle oder dem **cdrommediachange** -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="283b7-122">This index corresponds to the index of a **Cdrom** object in the **IWMPCdromCollection** interface or the **CdromMediaChange** event.</span></span>

<span data-ttu-id="283b7-123">Der folgende Beispielcode ist eine Funktion, mit der das einreißen einer CD vom CD-Laufwerk gestartet wird, das durch den Index 0 (null) identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="283b7-123">The following example code is a function that starts the process of ripping a CD from the CD drive identified by index zero.</span></span> <span data-ttu-id="283b7-124">Die-Funktion verwendet die folgende Member-Variable:</span><span class="sxs-lookup"><span data-stu-id="283b7-124">The function uses the following member variable:</span></span>


```C++
CComPtr<IWMPPlayer4>  m_spPlayer;  // Smart pointer to IWMPPlayer4.

```



<span data-ttu-id="283b7-125">Der folgende Code zeigt den Text der-Funktion:</span><span class="sxs-lookup"><span data-stu-id="283b7-125">The following code shows the body of the function:</span></span>


```C++
HRESULT CMyApp::StartRip()
{
    CComPtr<IWMPPlayerApplication>  spPlayerApp;
    CComPtr<IWMPPlayerServices>     spPlayerServices;
    CComBSTR bstrParam;  // Contains the parameter string.

    ATLASSERT(m_spPlayer.p);

    HRESULT hr = m_spPlayer->QueryInterface(&spPlayerServices);

    if(SUCCEEDED(hr))
    {
        // Create the parameter string.
        hr = bstrParam.Append(_T("CopyFromCD?AutoCopy:0"));
    }

    if(SUCCEEDED(hr))
    {
        // Rip the CD in drive 0.
        hr = spPlayerServices->setTaskPane(bstrParam);
    }

    return hr;
}

```



<span data-ttu-id="283b7-126">Anzeigen des Status für den Benutzer</span><span class="sxs-lookup"><span data-stu-id="283b7-126">Displaying Status to the User</span></span>

<span data-ttu-id="283b7-127">Beim Kopieren von einer CD können Sie eine Zeichenfolge abrufen, die Statusinformationen zum Kopiervorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="283b7-127">When copying from a CD, you can retrieve a string containing status information about the copy operation.</span></span> <span data-ttu-id="283b7-128">Zu diesem Zweck müssen Sie zuerst eine Wiedergabeliste mit Medien Elementen abrufen, die die CD-Spuren darstellen, indem Sie [iwmpcdrom:: get \_ Wiedergabeliste](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="283b7-128">To do this, you must first retrieve a playlist containing media items that represent the CD tracks by calling [IWMPCdrom::get\_playlist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist).</span></span> <span data-ttu-id="283b7-129">Wie im vorherigen Beispiel funktioniert der folgende Beispielcode mit dem CD-Laufwerks Index 0 (null).</span><span class="sxs-lookup"><span data-stu-id="283b7-129">Like the previous example, the following example code works with CD drive index zero.</span></span> <span data-ttu-id="283b7-130">Die abgerufene Wiedergabeliste wird in der folgenden Member-Variablen gespeichert:</span><span class="sxs-lookup"><span data-stu-id="283b7-130">It stores the retrieved playlist in the following member variable:</span></span>


```C++
CComPtr<IWMPPlaylist>  m_spCDPlaylist;

```



<span data-ttu-id="283b7-131">Der folgende Code zeigt den Text der-Funktion:</span><span class="sxs-lookup"><span data-stu-id="283b7-131">The following code shows the body of the function:</span></span>


```C++
HRESULT CMyApp::GetCDPlaylist()
{
    HRESULT hr = S_OK;

    // Release any existing playlist instance.
    m_spCDPlaylist.Release();

    CComPtr<IWMPCdromCollection> spCDDrives;
    CComPtr<IWMPCdrom>  spDrive;
    long lCount = 0;  // Count of CD drives.

    ATLASSERT(m_spPlayer);

    hr = m_spPlayer->get_cdromCollection(&spCDDrives);

    // Test to make sure there is at least one drive.
    if(SUCCEEDED(hr))
    {
        hr = spCDDrives->get_count(&lCount);
    }

    if(SUCCEEDED(hr) && lCount < 1)
    {
        MessageBox(_T("No CD drive detected"), 
                   _T("CD Rip Error"), MB_OK);
        hr = NS_E_CD_READ_ERROR;
    }

    if(SUCCEEDED(hr))
    {
        // Retrieve the first drive.
        hr = spCDDrives->item(0, &spDrive);
    }
    
    if(SUCCEEDED(hr))
    {
        // Get the playlist.
        hr = spDrive->get_playlist(&m_spCDPlaylist);
    }
   
    return hr;
}

```



<span data-ttu-id="283b7-132">Behandeln Sie als nächstes das [iwmpevents:: mediachange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="283b7-132">Next, handle the [IWMPEvents::MediaChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) event.</span></span> <span data-ttu-id="283b7-133">Dieses Ereignis tritt auf, wenn ein CD-Track ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="283b7-133">This event occurs when a CD track is being ripped.</span></span> <span data-ttu-id="283b7-134">Der an den Ereignishandler weiter gegebene **IDispatch** -Zeiger verweist auf die **iwmpmedia** -Schnittstelle für den CD-Track. Rufen Sie **QueryInterface** über **IDispatch** auf, um den Zeiger auf **iwmpmedia** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="283b7-134">The **IDispatch** pointer passed to the event handler points to the **IWMPMedia** interface for the CD track. Call **QueryInterface** through **IDispatch** to retrieve the pointer to **IWMPMedia**.</span></span>

<span data-ttu-id="283b7-135">Um zu ermitteln, welcher CD-Track gerade geritten wird, vergleichen Sie den **iwmpmedia** -Zeiger aus dem Ereignis mit den Medien Elementen in der CD-Wiedergabeliste, indem Sie [iwmpmedia:: get \_ isidentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="283b7-135">To detect which CD track is being ripped, compare the **IWMPMedia** pointer from the event to the media items in the CD playlist by calling [IWMPMedia::get\_isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical).</span></span>

<span data-ttu-id="283b7-136">Nennen Sie [iwmpmedia:: getiteminfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo), und übergeben Sie die Zeichenfolge "Status" als Elementname.</span><span class="sxs-lookup"><span data-stu-id="283b7-136">Call [IWMPMedia::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo), passing the string "Status" as the item name.</span></span> <span data-ttu-id="283b7-137">Der **Status** ist ein temporäres Attribut, das von Windows Media Player auf Medien Elementen festgelegt wird, während Sie von der CD gerissen werden. Er ist nicht in der Bibliothek verfügbar.</span><span class="sxs-lookup"><span data-stu-id="283b7-137">**Status** is a temporary attribute set by Windows Media Player on media items while they are being ripped from CD; it is not available from the library.</span></span>

<span data-ttu-id="283b7-138">Der folgende Beispielcode zeigt einen **mediachange** -Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="283b7-138">The following example code shows a **MediaChange** event handler.</span></span>


```C++
void CMyApp::MediaChange(IDispatch * Item)
{
    // Test whether the CD playlist exists.
    if(!m_spCDPlaylist)
    {
        return;
    }

    // Declare and initialize variables.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = S_OK;
    VARIANT_BOOL vbIdentical = VARIANT_FALSE;
    CComBSTR bstrVal;
    CComBSTR bstrName;
    long lCount = 0;  

    // Create the attribute value string.
    hr = bstrName.Append(_T("Status"));

    if(SUCCEEDED(hr))
    { 
        // Retrieve the IWMPMedia pointer from IDispatch.
        hr = Item->QueryInterface(__uuidof(IWMPMedia),(void**)&spMedia);
    }

    if(SUCCEEDED(hr))
    {
        // Get the value of the Status attribute.
        hr = spMedia->getItemInfo(bstrName, &bstrVal);
    }

    if(SUCCEEDED(hr))
    {
        // If the attribute is empty, set a failure code
        // to simply exit the function.
        if(bstrVal.Length() == 0)
        {
            hr = E_PENDING;
        }
    }
      
    if(SUCCEEDED(hr))
    {
        // Retrieve the count of items in the CD playlist.
        hr = m_spCDPlaylist->get_count(&lCount);
    }

    if(lCount < 1)
    {
        // Exit if the playlist is empty.
        hr = E_PENDING;
    }    

    if(SUCCEEDED(hr) && spMedia)
    {
        // Iterate through the playlist.
        // Compare the media item that raised the event
        // to each CD track. This detects which track
        // has a new status.
        for(long i = 0; i < lCount; i++)
        {
            CComPtr<IWMPMedia> spTrack;

            // Retrieve the CD track as a media object.
            hr = m_spCDPlaylist->get_item(i, &spTrack);

            if(SUCCEEDED(hr))
            {
                // Do the comparison.
                hr = spMedia->get_isIdentical(spTrack, &vbIdentical);
            }

            if(SUCCEEDED(hr) && VARIANT_TRUE == vbIdentical)
            {
                 // spTrack represents a track with changed status.
                 // bstrVal contains a status string. For example:
                 // "Ripping (10%)"
                 //
                 // TODO: Retrieve metadata about the track, and then
                 // display the status to the user.
            }
        }
    }

    return;
}

```



## <a name="related-topics"></a><span data-ttu-id="283b7-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="283b7-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="283b7-140">**Iwmpcdrom-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="283b7-140">**IWMPCdrom Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[<span data-ttu-id="283b7-141">**Iwmpcdromcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="283b7-141">**IWMPCdromCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[<span data-ttu-id="283b7-142">**Iwmpevents-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="283b7-142">**IWMPEvents Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> <dt>

[<span data-ttu-id="283b7-143">**Iwmpmedia-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="283b7-143">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="283b7-144">**Iwmpplayerservices-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="283b7-144">**IWMPPlayerServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
</dt> <dt>

[<span data-ttu-id="283b7-145">**Iwmpwiedergabe-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="283b7-145">**IWMPPlaylist Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[<span data-ttu-id="283b7-146">**Player-Steuerelement Handbuch**</span><span class="sxs-lookup"><span data-stu-id="283b7-146">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> <dt>

[<span data-ttu-id="283b7-147">**Ripping mithilfe der iwmpcdromrip-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="283b7-147">**Ripping by Using the IWMPCdromRip Interface**</span></span>](ripping-by-using-the-iwmpcdromrip-interface.md)
</dt> </dl>

 

 




