---
description: Erfahren Sie mehr über die Clientprotokollierung für Microsoft Media Foundation. Die Protokollierung bietet dem Medienserver die Möglichkeit, die Aktivität der Clients nachzuverfolgen, die eine Verbindung damit herstellen.
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: Clientprotokollierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3874c413f61b3495dc7e67f082a83e789a7a1357
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483086"
---
# <a name="client-logging-microsoft-media-foundation"></a>Clientprotokollierung (Microsoft Media Foundation)

Die Netzwerkquelle unterstützt die Clientprotokollierung, die dem Medienserver die Möglichkeit bietet, die Aktivität der Clients nachzuverfolgen, die eine Verbindung damit herstellen. Clientprotokolle ermöglichen es einem Server, Verbindungs-, Rendering- und Streamingstatistiken aufzuzeichnen. Diese Protokolle können von Inhaltsanbietern in verschiedenen Szenarien verwendet werden, z. B. zum Nachverfolgen der Nutzung des Medienservers und zum Generieren von Abrechnungen oder zum Bereitstellen von Inhalten in geeigneter Qualität, abhängig von der Geschwindigkeit des Clientnetzwerks.

Eine Protokolldatei enthält mehrere Clientereigniseinträge. Jeder Protokolleintrag enthält eine Reihe von Durch Leerzeichen getrennten Feldern. Es gibt zwei Arten von Clientprotokollen: *Rendering* (Wiedergabe) und *Streaming* (Empfangen). Da Inhalt gleichzeitig wiedergegeben und gestreamt werden kann, kann der Client eine Kombination aus beiden Protokolldatentypen senden. In bestimmten Fällen können zwei Protokolleinträge für dieselbe Sitzung vorhanden sein. Wenn z. B. Fast Cache aktiviert ist, kann der Client den Empfang des gestreamten Inhalts beenden, bevor er mit dem Rendern fertig ist. In diesem Fall werden die Streamingprotokolldaten vor den Renderingprotokolldaten gesendet.

Der Client sendet Renderingprotokolldaten an den Server, wenn sich der Client von einem Wiedergabezustand (Wiedergabe, Schnellervorlauf oder Zurückspulen) in einen Nicht-Wiedergabezustand (Beenden, Anhalten, Ende des Streams und Anfang des Streams) ändert. Wenn Daten für ein Renderingprotokoll übermittelt werden, wird eine direkte Verbindung mit dem Medienserver oder einem konfigurierten Proxyserver hergestellt.

Wenn der Inhalt in einer temporären lokalen Cachedatei auf dem Computer gespeichert wird, auf dem der Client ausgeführt wird, kann der Client eine Datei aus dem lokalen Cache lesen und die Renderingprotokolldaten übermitteln, um anzugeben, dass der Inhalt wiedergegeben wurde. In diesem Fall liest der Client eine Datei aus dem lokalen Cache, der Renderingprotokolleintrag enthält keine Netzwerkstatistiken, und das Protokoll ist auf Cache festgelegt.

Der Client sendet Streamingprotokolldaten an den Server, um anzugeben, wie der Client den Inhalt empfangen hat, aber nicht, wie er gerendert wurde. Der Client kann das Streamingprotokoll senden, lange bevor der Client das Rendern des Inhalts abgeschlossen hat.

Dieses Thema enthält keine Informationen zu allen Protokollfeldern. Eine vollständige Referenz finden Sie unter [Windows Media Log Data Structure](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).

## <a name="configuring-log-fields"></a>Konfigurieren von Protokollfeldern

Media Foundation ermöglicht es dem Client, die Netzwerkquelle mithilfe von Eigenschaften zu konfigurieren. Die Anwendung muss die entsprechenden Eigenschaften in einem Eigenschaftenspeicher festlegen und an eine der Quell resolver-Methoden übergeben. Der Quell resolver erstellt die Netzwerkquelle wie angefordert und öffnet eine Verbindung mit dem Server. Wenn die Verbindung erfolgreich hergestellt wurde, sendet der Client Informationen über sich selbst.

In der folgenden Tabelle werden die Protokollfelder und die entsprechenden Eigenschaften beschrieben, die eine Anwendung über den Quell resolver festlegen kann. Diese Informationen ändern sich während der Sitzung nicht.




| Protokollierungsfeld | BESCHREIBUNG | 
|---------------|-------------|
| c-playerid | Eindeutige Identifikation des Spielers. Diese Informationen werden am Anfang der Verbindung gesendet. In der Regel ist dies eine GUID des Clients. Der Client kann diese Informationen an den Server in der <a href="mfnetsource-playerid-property.md"><strong>eigenschaft MFNETSOURCE_PLAYERID</strong></a> senden.<br /> Der Client sendet diese Informationen am Anfang der Verbindung an den Server.<br /> Beispielwert: "{c579d042-cecc-11d1-bb31-00a0c9603954}"<br /> | 
| c-playerversion | Die Versionsnummer des Players, der am Anfang der Verbindung gesendet wird. Der Client kann diese Informationen an den Server in der <a href="mfnetsource-playerversion-property.md"><strong>eigenschaft MFNETSOURCE_PLAYERVERSION</strong></a> senden.<br /> Der Client sendet diese Informationen am Anfang der Verbindung an den Server.<br /> | 
| cs(User-Agent) | Browsertyp, der verwendet wird, wenn der Player in einen Browser eingebettet wurde. Dieser Wert kann vom Client in der <a href="mfnetsource-browseruseragent-property.md"><strong>eigenschaft MFNETSOURCE_BROWSERUSERAGENT</strong></a> festgelegt werden.<br /> Wenn der Player nicht eingebettet wurde, bezieht sich dieses Feld auf den Benutzer-Agent des Clients, der das Protokoll generiert hat. In diesem Fall muss der Client die <a href="mfnetsource-playeruseragent-property.md"><strong>eigenschaft MFNETSOURCE_PLAYERUSERAGENT</strong></a> festlegen.<br /> Der Client sendet diese Informationen am Anfang der Verbindung an den Server.<br /> Beispielwert: "Mozilla/4.0_(compatible;_MSIE_4.01;_Windows_98)"<br /> | 
| cs(Referer) | URL der Webseite, auf die der Player eingebettet wurde (sofern eingebettet). Der Client kann diese Informationen an den Server in der <a href="mfnetsource-browserwebpage-property.md"><strong>eigenschaft MFNETSOURCE_BROWSERWEBPAGE</strong></a> senden.<br /> Der Client sendet diese Informationen am Ende der Verbindung an den Server.<br /> Beispielwert: " https://www.example.microsoft.com "<br /> | 
| c-hostexe | Bei Playerprotokolleinträgen das Hostprogramm (.exe), das ausgeführt wurde. Beispielsweise eine Webseite in einem Browser, ein Microsoft Visual Basic Applet oder ein eigenständiger Player. Der Client kann diese Informationen an den Server in der <a href="mfnetsource-hostexe-property.md"><strong>eigenschaft MFNETSOURCE_HOSTEXE</strong></a> senden.<br /> Der Client sendet diese Informationen am Ende der Verbindung an den Server.<br /> Beispielwerte:<br /><ul><li>"iexplore.exe"</li><li>"myplayer.exe"</li></ul> | 
| c-hostexever | Versionsnummer des Hostprogramms (.exe). Der Client kann diese Informationen an den Server in der <a href="mfnetsource-hostversion-property.md"><strong>eigenschaft MFNETSOURCE_HOSTVERSION</strong></a> senden.<br /> Der Client sendet diese Informationen am Ende der Verbindung an den Server.<br /> | 




 

Das folgende Codebeispiel zeigt, wie eine Clientanwendung die Netzwerkquelle konfiguriert. In diesem Beispiel wird das Protokollfeld "c-hostexe" festgelegt.


```C++
// Creates a media source from a URL.
//
// This example demonstrates how to set the MFNETSOURCE_HOSTEXE
// configuration property on the network source.

HRESULT CreateMediaSourceWithLogParams(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_HOSTEXE;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_LPWSTR;
        var.pwszVal = L"MyPlayer.exe";

        hr = pConfig->SetValue(key, var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    return hr;
}
```



## <a name="retrieving-network-statistics"></a>Abrufen von Netzwerkstatistiken

Wenn die Anwendung eine der Quell resolver-Methoden aufruft, erstellt sie die Netzwerkquelle, legt die im Eigenschaftenspeicher angegebenen Eigenschaften fest und öffnet eine Sitzung mit dem Medienserver. Zusätzlich zu den im vorherigen Abschnitt beschriebenen konfigurierbaren Informationen werden am Anfang der Sitzung, während des Streamings und beim Schließen der Sitzung zusätzliche Daten zwischen dem Server und dem Client übertragen.

Die Anwendung kann Netzwerkstatistiken mithilfe des Dienstbezeichners **MFNETSOURCE \_ STATISTICS \_ SERVICE** abrufen. Um diesen Dienst zu verwenden, kann die Anwendung die [**MFGetService-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) aufrufen, um den Eigenschaftenspeicher abzurufen, der Netzwerkstatistiken in der [**MFNETSOURCE \_ STATISTICS-Eigenschaft**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) enthält. Bestimmte Werte können abgerufen werden, indem der entsprechende Bezeichner angegeben wird, der in der **MFNETSOURCE \_ STATISTICS \_ IDS-Enumeration** definiert ist.

Das folgende Codebeispiel zeigt, wie der Dienst verwendet wird, um die Anzahl der vom Client empfangenen Pakete abzurufen.


```C++
HRESULT GetPacketsReceived(IMFMediaSession *pSession, DWORD *pcPackets)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    // Get the number of packets received by the client.

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_RECVPACKETS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pcPackets = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
    return hr;
}
```



In der folgenden Liste werden einige der Netzwerkstatistikbezeichner beschrieben, die in [**MFNETSOURCE STATISTICS IDS definiert \_ \_ sind.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids)



| Netzwerkstatistikbezeichner              | BESCHREIBUNG                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFNETSOURCE \_ AVGBANDWIDTHBPS \_ ID**       | Durchschnittliche Bandbreite (in Bits pro Sekunde), mit der der Client mit dem Server verbunden war. Der Wert wird über die gesamte Dauer der Verbindung berechnet.                                                              |
| **MFNETSOURCE \_ BUFFERINGCOUNT \_ ID**        | Gibt an, wie oft der Client beim Wiedergeben des Streams gepuffert hat.                                                                                                                                                              |
| **MFNETSOURCE \_ BYTESRECEIVED \_ ID**         | Anzahl der vom Client vom Server empfangenen Bytes. Der Wert enthält keinen Mehraufwand, der vom Netzwerkstapel hinzugefügt wird. Derselbe Inhalt, der mithilfe verschiedener Protokolle gestreamt wird, kann zu unterschiedlichen Werten führen. |
| **MFNETSOURCE \_ \_ LINKBANDWIDTH-ID**         | Maximal verfügbare Bandbreite des Clients in Bits pro Sekunde.                                                                                                                                                              |
| **MFNETSOURCE \_ \_ LOSTPACKETS-ID**           | Anzahl der vom Server gesendeten Pakete, die während der Übertragung verloren gegangen sind und nie vom Client wiedergegeben wurden. Der Wert enthält keine TCP- oder UDP-Pakete.                                                                          |
| **MFNETSOURCE \_ \_ RECVPACKETS-ID**           | Anzahl der vom Server empfangenen Pakete Der Wert enthält keine TCP- oder UDP-Pakete.                                                                                                                                  |
| **MFNETSOURCE \_ RECOVEREDBYECCPACKETS-ID \_** | Pakete, die im Netzwerk verloren gegangen sind und auf Clientebene repariert und wiederhergestellt wurden. Dieser Wert enthält keine TCP- oder UDP-Pakete.                                                                                          |
| **MFNETSOURCE \_ RESENDSREQUESTED \_ ID**      | Die Anzahl der Anforderungen, die vom Client zum Empfangen neuer Pakete gesendet werden. Dieser Wert enthält keine TCP- oder UDP-Pakete.                                                                                                          |
| **MFNETSOURCE \_ RECOVEREDPACKETS \_ ID**      | Anzahl der Pakete, die wiederhergestellt wurden, weil sie über UDP erneut gesendet wurden. Dieser Wert enthält keine TCP- oder UDP-Pakete. Dieses Feld enthält eine 0 (null), es sei denn, der Client verwendet das erneute Senden von UDP.                                        |
| **MFNETSOURCE \_ BUFFERPROGRESS \_ ID**        | Der Prozentsatz des während der Pufferung gefüllten Playoutpuffers.                                                                                                                                                              |
| **\_MFNETSOURCE-PROTOKOLL-ID \_**              | Protokoll, das für den Zugriff auf den Stream verwendet wird. Dies kann sich vom vom Client angeforderten Protokoll unterscheiden.                                                                                                                             |
| **\_MFNETSOURCE-TRANSPORT-ID \_**             | Transportprotokoll, das zum Übermitteln des Streams verwendet wird. Dies muss entweder UDP oder TCP sein.                                                                                                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Netzwerkquellfeatures](network-source-features.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

