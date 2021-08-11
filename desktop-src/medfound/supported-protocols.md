---
description: Unterstützte Protokolle
ms.assetid: 3c026426-c2b7-4909-9524-9cc0bd45347e
title: Unterstützte Protokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b086b48b73c0412968c00091e6353d134006f45fa9c8b8f229ea3f9e695bf99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238127"
---
# <a name="supported-protocols"></a>Unterstützte Protokolle

Media Foundation unterstützt die folgenden Protokolle:

-   Echtzeitstreamingprotokoll (RTSP)

    RTSP wird hauptsächlich zum Streamen von Medieninhalten verwendet. Sie kann UDP oder TCP als Transportprotokolle verwenden. UDP ist für die Inhaltsübermittlung am effizientesten, da der Bandbreitenaufwand geringer ist als bei TCP-basierten Protokollen. Obwohl das TCP-Protokoll eine zuverlässige Paketübermittlung sicherstellt, eignet sich TCP nicht gut für digitale Medienstreams, bei denen eine effiziente Nutzung der Bandbreite wichtiger ist als gelegentlich verlorene Pakete.

-   Hypertext Transfer-Protokoll (HTTP)

    HTTP verwendet TCP und wird von Webservern verwendet. Das Schema "httpd://" gibt an, dass die Quelle von einem Webserver heruntergeladen werden kann. HTTP wird auch bei Firewalls verwendet, die normalerweise so konfiguriert sind, dass sie HTTP-Anforderungen akzeptieren und in der Regel andere Streamingprotokolle ablehnen.

Die Anwendung kann die protokolle abrufen, die von Media Foundation unterstützt werden, indem sie die [**INTERFACESNetSchemeHandlerConfig-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) verwendet. Hierzu muss die Anwendung zuerst die Anzahl der Protokolle abrufen, indem [**SIE DIE DATEI "PROTOCOLSNetSchemeHandlerConfig::GetNumberOfSupportedProtocols"**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) aufruft und dann den Protokolltyp basierend auf dem Index abrufen, indem [**SIE DIESENETSchemeHandlerConfig::GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype)aufrufen. Diese Methode gibt einen der in der [**MFNETSOURCE \_ PROTOCOL \_ TYPE-Enumeration**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) definierten Werte zurück.

Die Anwendung kann auch die vom Quell resolver unterstützten Schemas abrufen, indem sie die [**MFGetSupportedSchemes-Funktion aufruft.**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes)

## <a name="protocol-rollover"></a>Protokollrollover

Wenn eine Anwendung "mms://" als URL-Schema angibt, führt der Quell resolver einen *Protokollrollovervorgang* aus. In diesem Prozess bestimmt der Quell resolver das beste Protokoll für die Netzwerkquelle, das zum Abrufen des Inhalts verwendet werden soll. In der Regel ist RTSP mit UDP (RTSPU) für Medienpush effizienter als HTTP. Wenn der Inhalt jedoch auf einem Webserver gehostet wird, ist HTTP die bessere Wahl.

Ein Protokollrollover kann auch auftreten, wenn beim Versuch, das im URL-Schema angegebene Protokoll zu verwenden, ein Fehler auftritt. Beispielsweise kann ein Protokoll fehlschlagen, wenn eine Firewall UDP-Pakete blockiert. In diesem Fall wechselt der Quell resolver zu HTTP.

Protokollrollover gilt nicht, wenn das URL-Schema ein bestimmtes Protokoll enthält, z. B. "rtspu://". Außerdem wird kein Rollover ausgeführt, wenn die Authentifizierung fehlschlägt oder der Server einen Grenzwert für Clientverbindungen erreicht hat. Es wird empfohlen, dass Anwendungen das Schema "mms://" angeben und dem Quell resolver erlauben, das beste Protokoll für das Szenario auszuwählen.

In der folgenden Tabelle ist die Rolloverreihenfolge aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Zulässige Schemas</th>
<th>Protokollrolloverreihenfolge</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>mms:// oder rtsp://</td>
<td>Fast Cache aktiviert:<br/>
<ol>
<li>RTSP mit TCP (RTSPT)<br/></li>
<li>RTSP mit UDP (RTSPU)<br/></li>
<li>HTTP-Streaming<br/></li>
<li>HTTP-Download (HTTPD)<br/></li>
</ol>
Fast Cache deaktiviert:<br/>
<ol>
<li>Rtspu<br/></li>
<li>RTSPT<br/></li>
<li>HTTP-Streaming<br/></li>
<li>HTTP-Download<br/></li>
</ol></td>
</tr>
<tr class="even">
<td>rtspu://</td>
<td>Rtspu</td>
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



 

## <a name="retrieving-the-current-protocol"></a>Abrufen des aktuellen Protokolls

Nach einem Protokollrollovervorgang verwendet die Netzwerkquelle möglicherweise ein anderes Protokoll als das, das von der Anwendung im URL-Schema angegeben wird. Das Protokollrolloverergebnis ist für die Anwendung verfügbar, nachdem die Netzwerkquelle die Verbindung mit dem Medienserver hergestellt hat.

Um das Protokoll und den Transport abzurufen, die zum Abrufen des Inhalts verwendet werden, kann die Anwendung die Eigenschaftswerte für die [MFNETSOURCE \_ PROTOCOL-Eigenschaft](mfnetsource-protocol-property.md) und die [MFNETSOURCE \_ TRANSPORT-Eigenschaft](mfnetsource-transport-property.md) eines **IPropertyStore-Objekts** aus der Netzwerkquelle abrufen.

Der folgende Code zeigt, wie sie diese Werte abrufen.


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



Im vorherigen Beispielcode ruft **IPropertyStore::GetValue** den MFNETSOURCE \_ PROTOCOL-Wert ab, der ein Member der [**MFNETSOURCE \_ PROTOCOL \_ TYPE-Enumeration**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) ist. Bei MFNETSOURCE \_ TRANSPORT ist der Wert ein Member der [**MFNETSOURCE \_ TRANSPORT \_ TYPE-Enumeration.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type)

Alternativ kann die Anwendung die gleichen Werte mithilfe des MFNETSOURCE \_ STATISTICS \_ SERVICE-Diensts abrufen. Um diesen Dienst zu verwenden, kann die Anwendung die [**MFGetService-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) aufrufen, um den Eigenschaftenspeicher aus der Netzwerkquelle abzurufen. Dieser Eigenschaftenspeicher enthält Netzwerkstatistiken in der [MFNETSOURCE \_ STATISTICS-Eigenschaft.](mfnetsource-statistics-property.md) Protokoll- und Transportwerte können durch Angabe der \_ MFNETSOURCE-PROTOKOLL-ID und der \_ MFNETSOURCE-TRANSPORT-ID abgerufen \_ \_ werden, die in der [**MFNETSOURCE \_ STATISTICS \_ IDS-Enumeration**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) definiert sind. Der folgende Code zeigt, wie Sie die Protokoll- und Transportwerte mithilfe des MFNETSOURCE \_ STATISTICS \_ SERVICE-Diensts abrufen.


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

Die Anwendung kann die Netzwerkquelle so konfigurieren, dass bestimmte Protokolle während des Rollovervorgangs übersprungen werden. Zu diesem Zweck werden Netzwerkquelleigenschaften verwendet, um bestimmte Protokolle zu deaktivieren. Die folgende Tabelle zeigt die Eigenschaften und protokolle, die sie steuern.



| Eigenschaft                                                                    | BESCHREIBUNG                                 |
|-----------------------------------------------------------------------------|---------------------------------------------|
| [MFNETSOURCE \_ ENABLE \_ HTTP](mfnetsource-enable-http-property.md)           | Aktiviert oder deaktiviert HTTP und HTTPD.         |
| [MFNETSOURCE \_ ENABLE \_ RTSP](mfnetsource-enable-rtsp-property.md)           | Aktiviert oder deaktiviert RTSPU und RTSPT.        |
| [MFNETSOURCE \_ ENABLE \_ TCP](mfnetsource-enable-tcp-property.md)             | Aktiviert oder deaktiviert RTSPT.                  |
| [MFNETSOURCE \_ ENABLE \_ UDP](mfnetsource-enable-udp-property.md)             | Aktiviert oder deaktiviert RTSPU.                  |
| [MFNETSOURCE– \_ DOWNLOAD AKTIVIEREN \_](mfnetsource-enable-download-property.md)   | Aktiviert oder deaktiviert HTTPD.                  |
| [MFNETSOURCE \_ ENABLE \_ STREAMING](mfnetsource-enable-streaming-property.md) | Aktiviert oder deaktiviert RTSPU, RTSPT und HTTP. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




