---
description: Unterstützte Protokolle
ms.assetid: 3c026426-c2b7-4909-9524-9cc0bd45347e
title: Unterstützte Protokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cc5e47bddec9e00fbb62e853db5a492172da84
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468027"
---
# <a name="supported-protocols"></a>Unterstützte Protokolle

Media Foundation unterstützt die folgenden Protokolle:

-   Real Time Streaming Protocol (RTSP)

    RTSP wird hauptsächlich zum Streamen von Medieninhalten verwendet. UDP oder TCP kann als Transportprotokolle verwendet werden. UDP ist für die Inhaltsbereitstellung am effizientesten, da der Bandbreitenaufwand geringer ist als bei TCP-basierten Protokollen. Obwohl das TCP-Protokoll eine zuverlässige Paketbereitstellung gewährleistet, eignet sich TCP nicht gut für digitale Medienstreams, bei denen eine effiziente Nutzung der Bandbreite wichtiger ist als gelegentlich verlorene Pakete.

-   Hypertext Transfer-Protokoll (HTTP)

    HTTP verwendet TCP und wird von Webservern verwendet. Das Schema "httpd://" gibt an, dass die Quelle von einem Webserver heruntergeladen werden kann. HTTP wird auch bei Firewalls verwendet, die in der Regel so konfiguriert sind, dass sie HTTP-Anforderungen akzeptieren und in der Regel andere Streamingprotokolle ablehnen.

Die Anwendung kann die protokolle, die von Media Foundation, mithilfe der [**BENUTZEROBERFLÄCHENTnetSchemeHandlerConfig-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) erhalten. Hierzu muss die Anwendung zuerst die Anzahl der Protokolle abrufen, indem [**sie DURCH AUFRUFEN VONSTNETSCHEMEHandlerConfig::GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) aufruft, und dann den Protokolltyp basierend auf dem Index abrufen, indem sie DURCH AUFRUFEN [**VONGENETSchemeHandlerConfig::GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype). Diese Methode gibt einen der In der [**MFNETSOURCE \_ PROTOCOL \_ TYPE-Enumeration definierten Werte**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) zurück.

Die Anwendung kann auch die vom Quellre resolver unterstützten Schemas durch Aufrufen der [**MFGetSupportedSchemes-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) erhalten.

## <a name="protocol-rollover"></a>Protokollrollover

Wenn eine Anwendung "mms://" als URL-Schema angibt, führt der Quellre resolver einen *Protokollrollovervorgang* aus. In diesem Prozess bestimmt der Quellre resolver das beste Protokoll, das die Netzwerkquelle zum Abrufen des Inhalts verwenden kann. In der Regel ist RTSP mit UDP (RTSPU) für das Übertragen von Medien effizienter als HTTP. Wenn der Inhalt jedoch auf einem Webserver gehostet wird, ist HTTP die bessere Wahl.

Ein Protokollrollover kann auch auftreten, wenn beim Versuch, das im URL-Schema angegebene Protokoll zu verwenden, ein Fehler auftritt. Beispielsweise kann ein Protokoll fehlschlagen, wenn eine Firewall UDP-Pakete blockiert. In diesem Fall wechselt der Quellre resolver zu HTTP.

Das Protokollrollover gilt nicht, wenn das URL-Schema ein bestimmtes Protokoll enthält, z. B. "rtspu://". Außerdem wird kein Rollover ausgeführt, wenn die Authentifizierung fehlschlägt oder der Server ein Limit von Clientverbindungen erreicht hat. Es wird empfohlen, dass Anwendungen das Schema "mms://" angeben und dem Quellre resolver ermöglichen, das beste Protokoll für das Szenario auszuwählen.

In der folgenden Tabelle ist die Rollover-Reihenfolge aufgeführt.




| Zulässige Schemas | Reihenfolge des Protokollrollovers | 
|-----------------|-------------------------|
| mms:// oder rtsp:// | Fast Cache enabled (Schneller Cache aktiviert):<br /><ol><li>RTSP mit TCP (RTSPT)<br /></li><li>RTSP mit UDP (RTSPU)<br /></li><li>HTTP-Streaming<br /></li><li>HTTP-Download (HTTPD)<br /></li></ol>Schneller Cache deaktiviert:<br /><ol><li>RTSPU<br /></li><li>RTSPT<br /></li><li>HTTP-Streaming<br /></li><li>HTTP-Download<br /></li></ol> | 
| rtspu:// | RTSPU | 
| rtspt:// | RTSPT | 
| https:// | <ol><li>HTTP<br /></li><li>HTTPD<br /></li></ol> | 
| httpd:// | HTTPD | 




 

## <a name="retrieving-the-current-protocol"></a>Abrufen des aktuellen Protokolls

Nach einem Protokollrollovervorgang verwendet die Netzwerkquelle möglicherweise ein anderes Protokoll als das, das von der Anwendung im URL-Schema angegeben wurde. Das Protokollrolloverergebnis ist für die Anwendung verfügbar, nachdem die Netzwerkquelle die Verbindung mit dem Medienserver hergestellt hat.

Um das Protokoll und den Transport abzurufen, die zum Abrufen des Inhalts verwendet werden, kann die Anwendung die Eigenschaftswerte für die [MFNETSOURCE \_ PROTOCOL-Eigenschaft](mfnetsource-protocol-property.md) und die [MFNETSOURCE \_ TRANSPORT-Eigenschaft](mfnetsource-transport-property.md) eines **IPropertyStore-Objekts** aus der Netzwerkquelle abrufen.

Der folgende Code zeigt, wie diese Werte erhalten werden.


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



Im vorherigen Beispielcode ruft **IPropertyStore::GetValue** den MFNETSOURCE PROTOCOL-Wert ab, der ein Member der \_ [**MFNETSOURCE \_ PROTOCOL \_ TYPE-Enumeration**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) ist. Für MFNETSOURCE \_ TRANSPORT ist der Wert ein Member der [**MFNETSOURCE \_ TRANSPORT \_ TYPE-Enumeration.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type)

Alternativ kann die Anwendung die gleichen Werte mithilfe des Diensts MFNETSOURCE \_ STATISTICS \_ SERVICE erhalten. Um diesen Dienst zu verwenden, kann die Anwendung die [**MFGetService-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) aufrufen, um den Eigenschaftenspeicher aus der Netzwerkquelle zu erhalten. Dieser Eigenschaftenspeicher enthält Netzwerkstatistiken in der [MFNETSOURCE \_ STATISTICS-Eigenschaft.](mfnetsource-statistics-property.md) Protokoll- und Transportwerte können durch Angabe der MFNETSOURCE-PROTOKOLL-ID und \_ \_ der MFNETSOURCE-TRANSPORT-ID abgerufen werden, die in der \_ \_ [**MFNETSOURCE \_ STATISTICS \_ IDS-Enumeration definiert**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) sind. Der folgende Code zeigt, wie Sie die Protokoll- und Transportwerte mithilfe des MFNETSOURCE \_ STATISTICS \_ SERVICE-Diensts erhalten.


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

Die Anwendung kann die Netzwerkquelle so konfigurieren, dass bestimmte Protokolle während des Rolloverprozesses übersprungen werden. Zu diesem Grund werden Netzwerkquelleneigenschaften verwendet, um bestimmte Protokolle zu deaktivieren. Die folgende Tabelle zeigt die Eigenschaften und die Protokolle, die sie steuern.



| Eigenschaft                                                                    | BESCHREIBUNG                                 |
|-----------------------------------------------------------------------------|---------------------------------------------|
| [MFNETSOURCE: \_ HTTP \_ AKTIVIEREN](mfnetsource-enable-http-property.md)           | Aktiviert oder deaktiviert HTTP und HTTPD.         |
| [MFNETSOURCE \_ ENABLE \_ RTSP](mfnetsource-enable-rtsp-property.md)           | Aktiviert oder deaktiviert RTSPU und RTSPT.        |
| [MFNETSOURCE AKTIVIEREN \_ VON \_ TCP](mfnetsource-enable-tcp-property.md)             | Aktiviert oder deaktiviert RTSPT.                  |
| [MFNETSOURCE: \_ \_ UDP AKTIVIEREN](mfnetsource-enable-udp-property.md)             | Aktiviert oder deaktiviert RTSPU.                  |
| [MFNETSOURCE: \_ DOWNLOAD \_ AKTIVIEREN](mfnetsource-enable-download-property.md)   | Aktiviert oder deaktiviert HTTPD.                  |
| [MFNETSOURCE: \_ STREAMING \_ AKTIVIEREN](mfnetsource-enable-streaming-property.md) | Aktiviert oder deaktiviert RTSPU, RTSPT und HTTP. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




