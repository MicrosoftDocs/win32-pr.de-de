---
description: Unterstützte Protokolle
ms.assetid: 3c026426-c2b7-4909-9524-9cc0bd45347e
title: Unterstützte Protokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e618f47a1ffc4a81c36e48407b93da54d7d532f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753840"
---
# <a name="supported-protocols"></a>Unterstützte Protokolle

Media Foundation unterstützt die folgenden Protokolle:

-   Real-Time Streaming Protocol (RTSP)

    RTSP wird hauptsächlich zum Streamen von Medieninhalten verwendet. Sie kann UDP oder TCP als Transportprotokolle verwenden. UDP ist die effizienteste für die Inhalts Übermittlung, da der Bandbreiten Aufwand kleiner ist als bei TCP-basierten Protokollen. Obwohl das TCP-Protokoll eine zuverlässige Paket Bereitstellung gewährleistet, eignet sich TCP nicht gut für digitale Medienströme, bei denen die effiziente Nutzung der Bandbreite wichtiger als gelegentliche verlorene Pakete ist.

-   Hypertext Transfer-Protokoll (HTTP)

    HTTP verwendet TCP und wird von Webservern verwendet. Das Schema "httpd://" gibt an, dass die Quelle von einem Webserver heruntergeladen werden kann. Http wird auch bei Firewalls verwendet, die in der Regel so konfiguriert werden, dass HTTP-Anforderungen akzeptiert werden, und die in der Regel andere Streamingprotokolle ablehnen.

Die Anwendung kann die Protokolle, die von Media Foundation unterstützt werden, mithilfe der [**imvnetschemehandlerconfig**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) -Schnittstelle erhalten. Hierzu muss die Anwendung zunächst die Anzahl der Protokolle abrufen, indem Sie [**imfnetschemehandlerconfig:: getnumofsupportedprotokolls**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) aufrufen und dann den Protokolltyp basierend auf dem Index abrufen, indem Sie [**imfnetschemehandlerconfig:: getsupportedprotocoltype**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype)aufrufen. Diese Methode gibt einen der Werte zurück, die in der Enumeration des [**msnetsource- \_ Protokoll \_ Typs**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) definiert sind.

Die Anwendung kann auch die vom quellresolver unterstützten Schemas abrufen, indem Sie die Funktion [**mfgetsupportedschemas**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) aufruft.

## <a name="protocol-rollover"></a>Protokollrollover

Wenn eine Anwendung "MMS://" als URL-Schema angibt, führt der Quell Konflikt Löser einen *protokollrollovervorgang* aus. In diesem Prozess bestimmt der quellresolver das beste Protokoll, das die Netzwerkquelle zum erhalten des Inhalts verwendet. In der Regel ist RTSP mit UDP (RTSPU) für das Streaming von Medien effizienter als http. Wenn der Inhalt jedoch auf einem Webserver gehostet wird, ist http eine bessere Wahl.

Ein Protokollrollover kann auch auftreten, wenn der Versuch, das im URL-Schema angegebene Protokoll zu verwenden, fehlschlägt. Beispielsweise kann ein Protokoll fehlschlagen, wenn UDP-Pakete von einer Firewall blockiert werden. In diesem Fall wechselt der quellresolver zu http.

Der Protokollrollover trifft nicht zu, wenn das URL-Schema ein bestimmtes Protokoll enthält, z. b. "rtspu://". Außerdem wird der Rollover nicht ausgeführt, wenn die Authentifizierung fehlschlägt oder der Server ein Limit von Clientverbindungen erreicht hat. Es wird empfohlen, dass Anwendungen das Schema "MMS://" angeben und zulassen, dass der quellresolver das beste Protokoll für das Szenario auswählt.

In der folgenden Tabelle ist die rolloverreihenfolge aufgelistet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Zulässige Schemas</th>
<th>Protokollrollover-Reihenfolge</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>MMS://oder RTSP://</td>
<td>Schneller Cache aktiviert:<br/>
<ol>
<li>RTSP mit TCP (RTSPT)<br/></li>
<li>RTSP mit UDP (RTSPU)<br/></li>
<li>HTTP-Streaming<br/></li>
<li>HTTP-Download (httpd)<br/></li>
</ol>
Schneller Cache deaktiviert:<br/>
<ol>
<li>RTSPU<br/></li>
<li>RTSPT<br/></li>
<li>HTTP-Streaming<br/></li>
<li>HTTP-Download<br/></li>
</ol></td>
</tr>
<tr class="even">
<td>rtspu://</td>
<td>RTSPU</td>
</tr>
<tr class="odd">
<td>rtspt://</td>
<td>RTSPT</td>
</tr>
<tr class="even">
<td>https://</td>
<td><ol>
<li>HTTP<br/></li>
<li>HTTPD<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>httpd://</td>
<td>HTTPD</td>
</tr>
</tbody>
</table>



 

## <a name="retrieving-the-current-protocol"></a>Das aktuelle Protokoll wird abgerufen.

Nach einem protokollrollovervorgang verwendet die Netzwerkquelle möglicherweise ein anderes Protokoll als das, das von der Anwendung im URL-Schema angegeben wird. Das Ergebnis des Protokollrollovers steht der Anwendung zur Verfügung, nachdem die Netzwerkquelle die Verbindung mit dem Medienserver hergestellt hat.

Zum Abrufen des Protokolls und des Transports, die zum Abrufen des Inhalts verwendet werden, kann die Anwendung die Eigenschaftswerte für die [mfnetsource- \_ Protokoll](mfnetsource-protocol-property.md) Eigenschaft und die [mfnetsource- \_ Transport](mfnetsource-transport-property.md) Eigenschaft eines **IPropertyStore** -Objekts aus der Netzwerkquelle abrufen.

Der folgende Code zeigt, wie Sie diese Werte erhalten.


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    PROPVARIANT var;
    PropVariantInit(&var);

// Get the property store from the network source.
// The network source is created by the source resolver. Not shown.
    if (SUCCEEDED(hr))
    {
        hr = pNetworkSource->QueryInterface 
                (__uuidof(IPropertyStore), 
                (void**)&pProp);
    }
    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the MFNETSOURCE_PROTOCOL property value.
        key.fmtid = MFNETSOURCE_PROTOCOL;
        hr = pProp->GetValue (key, &var);

        // Get the MFNETSOURCE_TRANSPORT property value.
        key.fmtid = MFNETSOURCE_TRANSPORT;
        key.pid = 0;
        hr = pProp->GetValue (key, &var);

    }
```



Im vorherigen Beispielcode ruft **IPropertyStore:: GetValue** den mfnetsource- \_ Protokoll Wert ab, der ein Member der [**mfnetsource- \_ \_ Protokolltyp**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) -Enumeration ist. Für den mfnetsource- \_ Transport ist der Wert ein Member der [**mfnetsource \_ - \_ Transporttyp**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) -Enumeration.

Alternativ kann die Anwendung dieselben Werte mithilfe des MF-Quell \_ Statistik \_ Dienst-Dienstanbieter erhalten. Um diesen Dienst zu verwenden, kann die Anwendung die [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) -Funktion aufrufen, um den Eigenschaften Speicher aus der Netzwerkquelle abzurufen. Dieser Eigenschaften Speicher enthält Netzwerk Statistiken in der Eigenschaft " [MF-Quell \_ Statistik](mfnetsource-statistics-property.md) ". Protokoll-und Transport Werte können abgerufen werden, indem die mfnetsource \_ -Protokoll- \_ ID und mfnetsource-Transport-ID – angegeben werden, \_ \_ die in der Enumeration der [**mfnetsource- \_ Statistik- \_ IDs**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) Der folgende Code zeigt, wie Sie die Protokoll-und Transport Werte mithilfe des mfnetsource- \_ Statistik \_ Dienst Dienstanbieter erhalten.


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    HRESULT hr = S_OK;

    hr = MFGetService(
        pMediaSource, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_IPropertyStore, 
        (void**) & pProp); 

    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the property value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_PROTOCOL_ID;
        hr = pProp->GetValue (key, &var);

        // Get the transport value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_TRANSPORT_ID;
        hr = pProp->GetValue (key, &var);

    }
```



## <a name="enabling-and-disabling-protocols"></a>Aktivieren und Deaktivieren von Protokollen

Die Anwendung kann die Netzwerkquelle so konfigurieren, dass bestimmte Protokolle während des rolloverprozesses übersprungen werden. Zu diesem Zweck werden die Eigenschaften von Netzwerk Quellen verwendet, um bestimmte Protokolle zu deaktivieren. In der folgenden Tabelle werden die Eigenschaften und die von Ihnen kontrollierten Protokolle angezeigt.



| Eigenschaft                                                                    | BESCHREIBUNG                                 |
|-----------------------------------------------------------------------------|---------------------------------------------|
| [MF NetSource \_ \_ http aktivieren](mfnetsource-enable-http-property.md)           | Aktiviert oder deaktiviert http und httpd.         |
| [MF NetSource \_ , \_ RTSP aktivieren](mfnetsource-enable-rtsp-property.md)           | Aktiviert oder deaktiviert RTSPU und RTSPT.        |
| [MF NetSource \_ \_ TCP aktivieren](mfnetsource-enable-tcp-property.md)             | Aktiviert oder deaktiviert RTSPT.                  |
| [MF NetSource \_ Aktivieren von \_ UDP](mfnetsource-enable-udp-property.md)             | Aktiviert oder deaktiviert RTSPU.                  |
| [MF-Quell \_ \_ Download aktivieren](mfnetsource-enable-download-property.md)   | Aktiviert oder deaktiviert httpd.                  |
| [MF-Quelle \_ Aktivieren des \_ Streamings](mfnetsource-enable-streaming-property.md) | Aktiviert oder deaktiviert RTSPU, RTSPT und http. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




