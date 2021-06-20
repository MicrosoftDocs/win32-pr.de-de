---
description: Erfahren Sie mehr über die Clientprotokollierung für Microsoft Media Foundation. Die Protokollierung bietet dem Medienserver die Möglichkeit, die Aktivität der Clients nachverfolgungen, die eine Verbindung mit ihm herstellen.
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: Clientprotokollierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d994531ff16466054ca0645a35082a4845e4aa4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409933"
---
# <a name="client-logging-microsoft-media-foundation"></a>Clientprotokollierung (Microsoft Media Foundation)

Die Netzwerkquelle unterstützt die Clientprotokollierung, wodurch der Medienserver die Aktivität der Clients nachverfolgen kann, die eine Verbindung damit herstellen. Clientprotokolle ermöglichen einem Server das Aufzeichnen von Verbindungs-, Rendering- und Streamingstatistiken. Diese Protokolle können von Inhaltsanbietern in verschiedenen Szenarien verwendet werden, z. B. zum Nachverfolgen der Nutzung von Medienservern und Generieren von Abrechnungen oder zur Bereitstellung geeigneter Inhalte in Abhängigkeit von der Geschwindigkeit des Clientnetzwerks.

Eine Protokolldatei enthält mehrere Clientereigniseinträge. Jeder Protokolleintrag enthält eine Reihe von durch Leerzeichen getrennten Feldern. Es gibt zwei Arten von Clientprotokollen: *Rendering* (Wiedergabe) und *Streaming* (Empfangen). Da Inhalte gleichzeitig abgespielt und gestreamt werden können, kann der Client eine Kombination aus beiden Protokolldatentypen senden. In bestimmten Fällen können zwei Protokolleinträge für dieselbe Sitzung vorhanden sein. Wenn beispielsweise Fast Cache aktiviert ist, kann der Client den Empfang des gestreamten Inhalts beenden, bevor er das Rendern abgeschlossen hat. In diesem Fall werden die Streamingprotokolldaten vor den Renderingprotokolldaten gesendet.

Der Client sendet Renderingprotokolldaten an den Server, wenn sich der Client von einem wiedergabebasierten Zustand (Wiedergabe, schnelles Vorwärts- oder Zurücksingen) in einen Nichtwiedergabezustand (Beenden, Anhalten, Ende des Streams und Anfang des Streams) ändert. Wenn Daten für ein Renderingprotokoll übermittelt werden, wird eine Verbindung direkt mit dem Medienserver oder einem konfigurierten Proxyserver hergestellt.

Wenn der Inhalt in einer temporären lokalen Cachedatei auf dem Computer gespeichert wird, auf dem der Client ausgeführt wird, kann der Client eine Datei aus seinem lokalen Cache lesen und die Renderingprotokolldaten übermitteln, um anzugeben, dass der Inhalt abgespielt wurde. In diesem Fall liest der Client eine Datei aus seinem lokalen Cache, der Eintrag des Renderingprotokolls enthält keine Netzwerkstatistiken, und das Protokoll ist auf Cache festgelegt.

Der Client sendet Streamingprotokolldaten an den Server, um anzugeben, wie der Client den Inhalt empfangen hat, aber nicht wie er gerendert wurde. Der Client kann das Streamingprotokoll lange senden, bevor der Client das Rendern des Inhalts abgeschlossen hat.

Dieses Thema enthält keine Informationen zu allen Protokollfeldern. Eine vollständige Referenz finden Sie unter [Windows Media Log Data Structure](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).

## <a name="configuring-log-fields"></a>Konfigurieren von Protokollfeldern

Media Foundation ermöglicht es dem Client, die Netzwerkquelle mithilfe von Eigenschaften zu konfigurieren. Die Anwendung muss die entsprechenden Eigenschaften in einem Eigenschaftenspeicher festlegen und an eine der Quellre konfliktlösermethoden übergeben. Der Quellre resolver erstellt die Netzwerkquelle wie angefordert und öffnet eine Verbindung mit dem Server. Wenn die Verbindung erfolgreich hergestellt wurde, sendet der Client Informationen über sich selbst.

In der folgenden Tabelle werden die Protokollfelder und die entsprechenden Eigenschaften beschrieben, die eine Anwendung über den Quellre resolver festlegen kann. Diese Informationen ändern sich während der Sitzung nicht.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Protokollierungsfeld</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>c-playerid</td>
<td>Eindeutige Identifikation des Players. Diese Informationen werden am Anfang der Verbindung gesendet. In der Regel ist dies eine GUID des Clients. Der Client kann diese Informationen an den Server in der <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> senden.<br/> Der Client sendet diese Informationen am Anfang der Verbindung an den Server.<br/> Beispielwert: &quot; {c579d042-cecc-11d1-bb31-00a0c9603954}&quot;<br/></td>
</tr>
<tr class="even">
<td>c-playerversion</td>
<td>Die Versionsnummer des Players, der am Anfang der Verbindung gesendet wird. Der Client kann diese Informationen an den Server in der MFNETSOURCE_PLAYERVERSION <a href="mfnetsource-playerversion-property.md"><strong>senden.</strong></a><br/> Der Client sendet diese Informationen am Anfang der Verbindung an den Server.<br/></td>
</tr>
<tr class="odd">
<td>cs(User-Agent)</td>
<td>Browsertyp, der verwendet wird, wenn der Player in einen Browser eingebettet wurde. Dieser Wert kann vom Client in der Eigenschaft MFNETSOURCE_BROWSERUSERAGENT <a href="mfnetsource-browseruseragent-property.md"><strong>werden.</strong></a><br/> Wenn der Player nicht eingebettet wurde, bezieht sich dieses Feld auf den Benutzer-Agent des Clients, der das Protokoll generiert hat. In diesem Fall muss der Client die eigenschaft <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> festlegen.<br/> Der Client sendet diese Informationen am Anfang der Verbindung an den Server.<br/> Beispielwert: &quot; Mozilla/4.0_(compatible;_MSIE_4.01;_Windows_98)&quot;<br/></td>
</tr>
<tr class="even">
<td>cs(Referer)</td>
<td>URL der Webseite, in die der Player eingebettet wurde (wenn er eingebettet wurde). Der Client kann diese Informationen an den Server in der eigenschaft <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> senden.<br/> Der Client sendet diese Informationen am Ende der Verbindung an den Server.<br/> Beispielwert: &quot; https://www.example.microsoft.com&quot ;<br/></td>
</tr>
<tr class="odd">
<td>c-hostexe</td>
<td>Bei Playerprotokolleinträgen wird das Hostprogramm (.exe), das ausgeführt wurde. Beispielsweise eine Webseite in einem Browser, ein Microsoft Visual Basic Applet oder ein eigenständiger Player. Der Client kann diese Informationen an den Server in der <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> senden.<br/> Der Client sendet diese Informationen am Ende der Verbindung an den Server.<br/> Beispielwerte:<br/>
<ul>
<li>&quot;iexplore.exe&quot;</li>
<li>&quot;myplayer.exe&quot;</li>
</ul></td>
</tr>
<tr class="even">
<td>c-hostexever</td>
<td>Versionsnummer des Hostprogramms (.exe) Der Client kann diese Informationen an den Server in der <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> senden.<br/> Der Client sendet diese Informationen am Ende der Verbindung an den Server.<br/></td>
</tr>
</tbody>
</table>



 

Das folgende Codebeispiel zeigt, wie eine Clientanwendung die Netzwerkquelle konfiguriert. In diesem Beispiel wird das Protokollfeld "c-hostexe" definiert.


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

Wenn die Anwendung eine der Quellre resolvermethoden aufruft, erstellt sie die Netzwerkquelle, legt die im Eigenschaftenspeicher angegebenen Eigenschaften fest und öffnet eine Sitzung mit dem Medienserver. Zusätzlich zu den im vorherigen Abschnitt beschriebenen konfigurierbaren Informationen werden zu Beginn der Sitzung, während des Streamings und beim Schließen der Sitzung zusätzliche Daten zwischen dem Server und dem Client übertragen.

Die Anwendung kann Netzwerkstatistiken mithilfe des **Dienstbezeichners MFNETSOURCE \_ STATISTICS \_ SERVICE** abrufen. Um diesen Dienst zu verwenden, kann die Anwendung die [**MFGetService-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) aufrufen, um den Eigenschaftenspeicher zu erhalten, der Netzwerkstatistiken in der [**MFNETSOURCE \_ STATISTICS-Eigenschaft**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) enthält. Bestimmte Werte können abgerufen werden, indem der entsprechende Bezeichner angegeben wird, der in der **MFNETSOURCE \_ STATISTICS \_ IDS-Enumeration definiert** ist.

Das folgende Codebeispiel zeigt, wie sie den Dienst verwenden, um die Anzahl der vom Client empfangenen Pakete zu erhalten.


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



In der folgenden Liste werden einige der in [**MFNETSOURCE STATISTICS IDS definierten Netzwerkstatistikbezeichner \_ \_ beschrieben.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids)



| Netzwerkstatistikbezeichner              | Beschreibung                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFNETSOURCE-ID \_ "AVGBANDWIDTHBPS" \_**       | Durchschnittliche Bandbreite (in Bits pro Sekunde), bei der der Client mit dem Server verbunden war. Der Wert wird für die gesamte Dauer der Verbindung berechnet.                                                              |
| **MFNETSOURCE \_ \_ BUFFERINGCOUNT-ID**        | Gibt an, wie oft der Client während der Wiedergabe des Streams gepuffert hat.                                                                                                                                                              |
| **MFNETSOURCE \_ BYTESRECEIVED \_ ID**         | Anzahl der vom Client vom Server empfangenen Bytes. Der Wert enthält keinen Mehraufwand, der durch den Netzwerkstapel hinzugefügt wird. Derselbe Inhalt, der mit verschiedenen Protokollen gestreamt wird, kann zu unterschiedlichen Werten führen. |
| **\_MFNETSOURCE-LINKBANDWIDTH-ID \_**         | Maximale verfügbare Bandbreite des Clients in Bits pro Sekunde.                                                                                                                                                              |
| **MFNETSOURCE \_ LOSTPACKETS-ID \_**           | Anzahl von Paketen, die vom Server gesendet wurden, aber während der Übertragung verloren gegangen sind und nie vom Client abgespielt wurden. Der Wert enthält keine TCP- oder UDP-Pakete.                                                                          |
| **MFNETSOURCE \_ RECVPACKETS-ID \_**           | Anzahl der vom Server empfangenen Pakete Der Wert enthält keine TCP- oder UDP-Pakete.                                                                                                                                  |
| **MFNETSOURCE \_ RECOVEREDBYECCPACKETS-ID \_** | Verlorene Pakete im Netzwerk, die auf Clientebene repariert und wiederhergestellt wurden. Dieser Wert enthält keine TCP- oder UDP-Pakete.                                                                                          |
| **MFNETSOURCE \_ RESENDSREQUESTED \_ ID**      | Die Anzahl der Anforderungen, die vom Client zum Empfangen neuer Pakete gesendet werden. Dieser Wert enthält keine TCP- oder UDP-Pakete.                                                                                                          |
| **MFNETSOURCE \_ RECOVEREDPACKETS \_ ID**      | Anzahl der Pakete, die wiederhergestellt wurden, weil sie über UDP erneut gesendet wurden. Dieser Wert enthält keine TCP- oder UDP-Pakete. Dieses Feld enthält eine Null, es sei denn, der Client verwendet UDP erneut.                                        |
| **MFNETSOURCE \_ \_ BUFFERPROGRESS-ID**        | Der Prozentsatz des während der Pufferung gefüllten Playoutpuffers.                                                                                                                                                              |
| **\_MFNETSOURCE-PROTOKOLL-ID \_**              | Protokoll, das für den Zugriff auf den Stream verwendet wird. Dies kann sich vom vom Client angeforderten Protokoll unterscheiden.                                                                                                                             |
| **\_MFNETSOURCE-TRANSPORT-ID \_**             | Transportprotokoll, das zum Übermitteln des Streams verwendet wird. Dies muss entweder UDP oder TCP sein.                                                                                                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Netzwerkquellfeatures](network-source-features.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

