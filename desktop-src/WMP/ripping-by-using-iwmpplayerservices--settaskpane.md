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
# <a name="ripping-by-using-iwmpplayerservicessettaskpane"></a>Ripping mithilfe von iwmpplayerservices:: settaskpane

> [!Note]  
> In diesem Abschnitt wird eine Funktion der Windows Media Player 9-Reihe und der ActiveX-Steuerelemente von Windows Media Player 10 dokumentiert. Es wird empfohlen, die **iwmpcdromrip** -Schnittstelle mit neueren Versionen zu verwenden. Siehe [iwmpcdromrip-Schnittstelle](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip).

 

Sie können das Steuerelement Windows Media Player 9 oder höher verwenden, um CD-Spuren auf den Computer des Benutzers zu kopieren. Dieser Vorgang wird als *einreißen* bezeichnet. Zu diesem Zweck müssen Sie das Windows Media Player-Steuerelement in den Remote Modus einbetten. Weitere Informationen zum Remote Modus finden Sie unter [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).

Um den einreißen-Prozess zu starten, nennen Sie [iwmpplayerservices:: settaskpane](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane), und übergeben Sie den copyfromcd? AutoCopy:*ID* -Wert für den *bstrautaskpane* -Parameter, wobei *ID* der Index des CD-Laufwerks ist, von dem kopiert werden soll. Dieser Index entspricht dem Index eines **CDROM** -Objekts in der **iwmpcdromcollection** -Schnittstelle oder dem **cdrommediachange** -Ereignis.

Der folgende Beispielcode ist eine Funktion, mit der das einreißen einer CD vom CD-Laufwerk gestartet wird, das durch den Index 0 (null) identifiziert wird. Die-Funktion verwendet die folgende Member-Variable:


```C++
CComPtr<IWMPPlayer4>  m_spPlayer;  // Smart pointer to IWMPPlayer4.

```



Der folgende Code zeigt den Text der-Funktion:


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



Anzeigen des Status für den Benutzer

Beim Kopieren von einer CD können Sie eine Zeichenfolge abrufen, die Statusinformationen zum Kopiervorgang enthält. Zu diesem Zweck müssen Sie zuerst eine Wiedergabeliste mit Medien Elementen abrufen, die die CD-Spuren darstellen, indem Sie [iwmpcdrom:: get \_ Wiedergabeliste](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist)aufrufen. Wie im vorherigen Beispiel funktioniert der folgende Beispielcode mit dem CD-Laufwerks Index 0 (null). Die abgerufene Wiedergabeliste wird in der folgenden Member-Variablen gespeichert:


```C++
CComPtr<IWMPPlaylist>  m_spCDPlaylist;

```



Der folgende Code zeigt den Text der-Funktion:


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



Behandeln Sie als nächstes das [iwmpevents:: mediachange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) -Ereignis. Dieses Ereignis tritt auf, wenn ein CD-Track ausgeführt wird. Der an den Ereignishandler weiter gegebene **IDispatch** -Zeiger verweist auf die **iwmpmedia** -Schnittstelle für den CD-Track. Rufen Sie **QueryInterface** über **IDispatch** auf, um den Zeiger auf **iwmpmedia** abzurufen.

Um zu ermitteln, welcher CD-Track gerade geritten wird, vergleichen Sie den **iwmpmedia** -Zeiger aus dem Ereignis mit den Medien Elementen in der CD-Wiedergabeliste, indem Sie [iwmpmedia:: get \_ isidentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical)aufrufen.

Nennen Sie [iwmpmedia:: getiteminfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo), und übergeben Sie die Zeichenfolge "Status" als Elementname. Der **Status** ist ein temporäres Attribut, das von Windows Media Player auf Medien Elementen festgelegt wird, während Sie von der CD gerissen werden. Er ist nicht in der Bibliothek verfügbar.

Der folgende Beispielcode zeigt einen **mediachange** -Ereignishandler.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmpcdrom-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[**Iwmpcdromcollection-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[**Iwmpevents-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> <dt>

[**Iwmpmedia-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**Iwmpplayerservices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
</dt> <dt>

[**Iwmpwiedergabe-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Player-Steuerelement Handbuch**](player-control-guide.md)
</dt> <dt>

[**Ripping mithilfe der iwmpcdromrip-Schnittstelle**](ripping-by-using-the-iwmpcdromrip-interface.md)
</dt> </dl>

 

 




