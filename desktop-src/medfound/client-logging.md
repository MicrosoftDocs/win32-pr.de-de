---
description: Client Protokollierung
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: Client Protokollierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3cb03c8026e91acd567358e7004211b7fdde4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214338"
---
# <a name="client-logging-microsoft-media-foundation"></a>Client Protokollierung (Microsoft Media Foundation)

Die Netzwerkquelle unterstützt die Client Protokollierung, die es dem Medienserver ermöglicht, die Aktivität der Clients zu verfolgen, die eine Verbindung mit ihm herstellen. Client Protokolle ermöglichen einem Server das Aufzeichnen von Verbindungs-, Rendering-und streamingstatistiken. Diese Protokolle können von Inhaltsanbietern in verschiedenen Szenarien (z. b.) verwendet werden, um die Nutzung von Medienservern zu verfolgen und eine Abrechnung zu generieren, oder um entsprechend der Geschwindigkeit des Client Netzwerks geeignete Inhalte bereitzustellen.

Eine Protokolldatei enthält mehrere Client Ereignis Einträge. Jeder Protokolleintrag enthält eine Reihe von Feldern, die durch Leerzeichen getrennt sind. Es gibt zwei Arten von Client Protokollen: *Rendering* (Wiedergabe) und *Streaming* (empfangen). Da Inhalte gleichzeitig abgespielt und gestreamt werden können, kann der Client eine Kombination beider Protokolldaten Typen senden. In bestimmten Fällen können für dieselbe Sitzung zwei Protokolleinträge vorhanden sein. Wenn z. b. der schnelle Cache aktiviert ist, kann der Client den gestreamten Inhalt abschließen, bevor er das Rendering abgeschlossen hat. In diesem Fall werden die streamingprotokolllierdaten vor den renderingprotokollierung gesendet.

Der Client sendet renderingprotokolllierungsdaten an den Server, wenn sich der Client von einem beliebigen Wiedergabe Zustand ("Wiedergabe", "schnell vorwärts" oder "Zurückspulen") in einen nicht Wiedergabe-Zustand ändert (beenden, anhalten, Ende des Streams und Anfang des Streams). Wenn Daten für ein renderingprotokoll übermittelt werden, wird eine Verbindung direkt mit dem Medienserver oder einem konfigurierten Proxy Server hergestellt.

Wenn der Inhalt in einer temporären lokalen Cachedatei auf dem Computer gespeichert ist, auf dem der-Client ausgeführt wird, kann der Client eine Datei aus dem lokalen Cache lesen und die renderingprotokolllierdaten übermitteln, um anzugeben, dass der Inhalt wiedergegeben wurde. In diesem Fall liest der Client eine Datei aus dem lokalen Cache, der renderingprotokolleintrag enthält keine Netzwerk Statistiken, und das Protokoll ist auf Cache festgelegt.

Der Client sendet streamingprotokolllierdaten an den Server, um anzugeben, wie der Client den Inhalt empfangen hat, aber nicht, wie er gerendert wurde. Der Client kann das Streamingprotokoll lange senden, bevor der Client das Rendern des Inhalts abgeschlossen hat.

Dieses Thema enthält keine Informationen über alle Protokoll Felder. Eine umfassende Referenz finden Sie unter [Windows Media Log Data Structure](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).

## <a name="configuring-log-fields"></a>Konfigurieren von Protokoll Feldern

Media Foundation ermöglicht es dem Client, die Netzwerkquelle mithilfe von Eigenschaften zu konfigurieren. Die Anwendung muss die entsprechenden Eigenschaften in einem Eigenschafts Speicher festlegen und an eine der Quell Konflikt Löser-Methoden übergeben. Der Quell Löser erstellt die Netzwerkquelle wie angefordert und öffnet eine Verbindung mit dem Server. Wenn die Verbindung erfolgreich hergestellt wurde, sendet der Client Informationen über sich selbst.

In der folgenden Tabelle werden die Protokoll Felder und die entsprechenden Eigenschaften beschrieben, die von einer Anwendung über den quellresolver festgelegt werden können. Diese Informationen werden während der Sitzung nicht geändert.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Protokollierungs Feld</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>c-playerid</td>
<td>Eindeutige Identifikation des Players. Diese Informationen werden am Anfang der Verbindung gesendet. In der Regel handelt es sich hierbei um eine GUID des Clients. Der Client kann diese Informationen in der <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> -Eigenschaft an den-Server senden.<br/> Diese Informationen werden vom Client am Anfang der Verbindung an den Server gesendet.<br/> Beispiel Wert: &quot; {c579d042-CECC-11d1-BB31-00a0c9603954}&quot;<br/></td>
</tr>
<tr class="even">
<td>c-Playerversion</td>
<td>Die Versionsnummer des Players, der am Anfang der Verbindung gesendet wird. Der Client kann diese Informationen in der <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> -Eigenschaft an den-Server senden.<br/> Diese Informationen werden vom Client am Anfang der Verbindung an den Server gesendet.<br/></td>
</tr>
<tr class="odd">
<td>CS (Benutzer-Agent)</td>
<td>Der Browsertyp, der verwendet wird, wenn der Player in einen Browser eingebettet wurde. Dieser Wert kann vom Client in der <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> -Eigenschaft festgelegt werden.<br/> Wenn der Spieler nicht eingebettet war, verweist dieses Feld auf den Benutzer-Agent des Clients, der das Protokoll generiert hat. In diesem Fall muss der Client die <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> -Eigenschaft festlegen.<br/> Diese Informationen werden vom Client am Anfang der Verbindung an den Server gesendet.<br/> Beispiel Wert: &quot; Mozilla/4.0 _ (kompatibel; _MSIE_4.01; _Windows_98)&quot;<br/></td>
</tr>
<tr class="even">
<td>CS (Referer)</td>
<td>Die URL der Webseite, in die der Player eingebettet wurde (wenn Sie eingebettet wurde). Der Client kann diese Informationen in der <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> -Eigenschaft an den-Server senden.<br/> Diese Informationen werden vom Client am Ende der Verbindung an den Server gesendet.<br/> Beispiel Wert: &quot; https://www.example.microsoft.com&quot ;<br/></td>
</tr>
<tr class="odd">
<td>c-hostexe</td>
<td>Für Player-Protokolleinträge das Host Programm (. exe), das ausgeführt wurde. Beispielsweise eine Webseite in einem Browser, ein Microsoft Visual Basic Applet oder ein eigenständiger Player. Der Client kann diese Informationen in der <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> -Eigenschaft an den-Server senden.<br/> Diese Informationen werden vom Client am Ende der Verbindung an den Server gesendet.<br/> Beispielwerte:<br/>
<ul>
<li>&quot;iexplore.exe&quot;</li>
<li>&quot;myplayer.exe&quot;</li>
</ul></td>
</tr>
<tr class="even">
<td>c-hostexever</td>
<td>Die Versionsnummer des Host Programms (. exe). Der Client kann diese Informationen in der <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> -Eigenschaft an den-Server senden.<br/> Diese Informationen werden vom Client am Ende der Verbindung an den Server gesendet.<br/></td>
</tr>
</tbody>
</table>



 

Das folgende Codebeispiel zeigt, wie eine Client Anwendung die Netzwerkquelle konfiguriert. In diesem Beispiel wird das Protokollfeld "c-hostexe" festgelegt.


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



## <a name="retrieving-network-statistics"></a>Netzwerk Statistiken werden abgerufen.

Wenn die Anwendung eine der Quell Konflikt Löser-Methoden aufruft, wird die Netzwerkquelle erstellt, die im Eigenschaften Speicher angegebenen Eigenschaften festgelegt und eine Sitzung mit dem Medienserver geöffnet. Zusätzlich zu den konfigurierbaren Informationen, die im vorherigen Abschnitt beschrieben wurden, werden zusätzliche Daten zwischen dem Server und dem Client am Anfang der Sitzung, während des Streamings und beim Schließen der Sitzung übertragen.

Die Anwendung kann Netzwerk Statistiken mithilfe des Dienst Bezeichners für den **mfnetsource- \_ Statistik \_ Dienst** abrufen. Um diesen Dienst zu verwenden, kann die Anwendung die [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) -Funktion aufrufen, um den Eigenschaften Speicher zu erhalten, der Netzwerk Statistiken in der [**mfnetsource- \_ Statistik**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) Eigenschaft enthält. Bestimmte Werte können abgerufen werden, indem der entsprechende Bezeichner bereitgestellt wird, der in der **mfnetsource \_ Statistics \_ IDs** -Enumeration definiert ist.

Im folgenden Codebeispiel wird gezeigt, wie der-Dienst verwendet wird, um die Anzahl der vom Client empfangenen Pakete zu erhalten.


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



In der folgenden Liste werden einige der in [**MF-Quell \_ Statistik- \_ IDs**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids)definierten Netzwerk Statistik-IDs beschrieben.



| Netzwerk Statistik Bezeichner              | BESCHREIBUNG                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MF-Quell- \_ ID avgbandwidthbit/s \_**       | Die durchschnittliche Bandbreite (in Bits pro Sekunde), an der der Client mit dem Server verbunden war. Der Wert wird über die gesamte Dauer der Verbindung berechnet.                                                              |
| **MF-Quell- \_ bufferingcount- \_ ID**        | Gibt an, wie oft der Client während der Wiedergabe des Streams gepuffert hat.                                                                                                                                                              |
| **MF-Quell- \_ ID (bytesempfangene) \_**         | Anzahl von Bytes, die vom Client vom Server empfangen wurden. Der Wert umfasst keinen Aufwand, der vom Netzwerk Stapel hinzugefügt wird. Derselbe Inhalt, der mithilfe verschiedener Protokolle gestreamt wird, kann zu unterschiedlichen Werten führen. |
| **MF NetSource \_ linkbandwidth- \_ ID**         | Maximale verfügbare Bandbreite des Clients in Bits pro Sekunde.                                                                                                                                                              |
| **MF NetSource- \_ lostpakete- \_ ID**           | Die Anzahl der vom Server gesendeten Pakete, die während der Übertragung verloren gegangen sind und nie vom Client abgespielt wurden. Der Wert enthält keine TCP-oder UDP-Pakete.                                                                          |
| **mfnetsource- \_ recvpakete- \_ ID**           | Anzahl der vom Server empfangenen Pakete. der Wert enthält keine TCP-oder UDP-Pakete.                                                                                                                                  |
| **MF-Quell \_ Wiederherstellungstyp- \_ ID** | Im Netzwerk verlorene Pakete, die auf der Client Ebene repariert und wieder hergestellt wurden. Dieser Wert enthält keine TCP-oder UDP-Pakete.                                                                                          |
| **MF-Quell- \_ ID resendsangeforderten \_ ID**      | Die Anzahl der Anforderungen, die vom Client zum Empfangen neuer Pakete gesendet wurden. Dieser Wert enthält keine TCP-oder UDP-Pakete.                                                                                                          |
| **ID des MF-Quell \_ Wiederherstellung. \_**      | Anzahl der wiederhergestellten Pakete, weil Sie über UDP erneut gesendet wurden. Dieser Wert enthält keine TCP-oder UDP-Pakete. Dieses Feld enthält eine NULL, es sei denn, der Client verwendet UDP Resend.                                        |
| **MF-Quell- \_ bufferprogress- \_ ID**        | Der Prozentsatz des bei der Pufferung gefüllten Broadcasts-Puffers.                                                                                                                                                              |
| **MF-Quell \_ Protokoll- \_ ID**              | Protokoll, das für den Zugriff auf den Stream verwendet wird. Dies kann sich von dem vom Client angeforderten Protokoll unterscheiden.                                                                                                                             |
| **MF-Quell- \_ Transport- \_ ID**             | Transport Protokoll, das zum Übermitteln des Streams verwendet wird. Dabei muss es sich entweder um UDP oder TCP handeln.                                                                                                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Netzwerk Quell Features](network-source-features.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

