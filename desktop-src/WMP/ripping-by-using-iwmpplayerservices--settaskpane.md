---
title: Ripping unter Verwendung von IWMPPlayerServices setTaskPane
description: Ripping unter Verwendung von IWMPPlayerServices setTaskPane
ms.assetid: 0d3efb0e-e8f5-40e3-abb5-6ad22009a4eb
keywords:
- Windows Media Player, CD-Umarbeitung
- Windows Media Player-Objektmodell, CD-Platte
- Objektmodell, CD-Endering
- Windows Media Player ActiveX-Steuerelement, CD-Platte
- ActiveX-Steuerelement, CD-Platte
- Windows Media Player Mobile ActiveX-Steuerelement, CD-Platte
- Windows Media Player Mobil, CD-Platte
- CD-Sperre,IWMPPlayerServices setTaskPane-Schnittstelle
- CDs, IWMPPlayerServices setTaskPane-Schnittstelle
- IWMPPlayerServices setTaskPane-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2abf53d29284b5da629598e6f23d6dcae78c69c60c23ba07f30445d5252845e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569833"
---
# <a name="ripping-by-using-iwmpplayerservicessettaskpane"></a>Erfolgt mit IWMPPlayerServices::setTaskPane

> [!Note]  
> In diesem Abschnitt wird ein Feature der Windows Media Player 9-Serie und Windows Media Player 10 ActiveX-Steuerelementen beschrieben. Es wird empfohlen, die **IWMPC csvRip-Schnittstelle** mit späteren Versionen zu verwenden. Weitere Informationen finden Sie unter [IWMPC csvRip-Schnittstelle.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)

 

Sie können das Windows Media Player 9-Serie oder höher verwenden, um CD-Spuren auf den Computer des Benutzers zu kopieren. Dieser Prozess wird als *"verfälschend"* bezeichnet. Hierzu müssen Sie das Windows Media Player-Steuerelement in den Remotemodus einbetten. Weitere Informationen zum Remotemodus finden Sie unter [Remoting des Windows Media Player Control](remoting-the-windows-media-player-control.md).

Rufen Sie zum Starten des Vorgangs [IWMPPlayerServices::setTaskPane](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane)auf, und übergeben Sie copyFromCD? AutoCopy:*ID-Wert* für den *bstrTaskPane-Parameter,* wobei *id* der Index des CD-Laufwerks ist, aus dem kopiert werden soll. Dieser Index entspricht dem Index eines **Credo-Objekts** in der **IWMPCcollectionCollection-Schnittstelle** oder dem **CmediaMediaChange-Ereignis.**

Der folgende Beispielcode ist eine Funktion, die den Prozess der Löschung einer CD aus dem CD-Laufwerk startet, das durch Index 0 (null) identifiziert wird. Die Funktion verwendet die folgende Membervariable:


```C++
CComPtr<IWMPPlayer4>  m_spPlayer;  // Smart pointer to IWMPPlayer4.

```



Der folgende Code zeigt den Text der Funktion:


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

Beim Kopieren von einer CD können Sie eine Zeichenfolge mit Statusinformationen zum Kopiervorgang abrufen. Hierzu müssen Sie zunächst eine Wiedergabeliste mit Medienelementen abrufen, die die CD-Spuren darstellen, indem [Sie IWMPCmost::get \_ playlist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist)aufrufen. Wie im vorherigen Beispiel funktioniert der folgende Beispielcode mit dem CD-Laufwerkindex 0 (null). Die abgerufene Wiedergabeliste wird in der folgenden Membervariablen gespeichert:


```C++
CComPtr<IWMPPlaylist>  m_spCDPlaylist;

```



Der folgende Code zeigt den Text der Funktion:


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



Behandeln Sie als Nächstes das [IWMPEvents::MediaChange-Ereignis.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) Dieses Ereignis tritt auf, wenn eine CD-Spur ausfällt. Der an den Ereignishandler übergebene **IDispatch-Zeiger** zeigt auf die **IWMPMedia-Schnittstelle** für die CD-Spur. Rufen Sie **QueryInterface** über **IDispatch** auf, um den Zeiger auf **IWMPMedia** abzurufen.

Vergleichen Sie den **IWMPMedia-Zeiger** aus dem -Ereignis mit den Medienelementen in der CD-Wiedergabeliste, indem Sie [IWMPMedia::get \_ isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical)aufrufen, um zu ermitteln, welche CD-Spur überschrieben wird.

Rufen Sie [IWMPMedia::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)auf, und übergeben Sie die Zeichenfolge "Status" als Elementnamen. **Status** ist ein temporäres Attribut, das von Windows Media Player auf Medienelementen festgelegt wird, während sie von CD übertragen werden. sie ist nicht in der Bibliothek verfügbar.

Der folgende Beispielcode  zeigt einen MediaChange-Ereignishandler.


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

[**IWMPCaku-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[**IWMPCcollectionCollection-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[**IWMPEvents-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> <dt>

[**IWMPMedia-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**IWMPPlayerServices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Leitfaden zum Playersteuerelement**](player-control-guide.md)
</dt> <dt>

[**Umleiten mithilfe der IWMPC opcRip-Schnittstelle**](ripping-by-using-the-iwmpcdromrip-interface.md)
</dt> </dl>

 

 




