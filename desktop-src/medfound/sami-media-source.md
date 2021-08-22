---
description: Synchronized Accessible Media Interchange (SAMI) ist ein Format zum Hinzufügen von Untertiteln zu digitalen Medien.
ms.assetid: 007c8181-089e-4e56-a31d-9d1942f90b07
title: SAMI-Medienquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7567f7479b6f8d0d2439f89dbf3e6cf273fc7dcae31590ddf9b51a4d66a6940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034818"
---
# <a name="sami-media-source"></a>SAMI-Medienquelle

Synchronized Accessible Media Interchange (SAMI) ist ein Format zum Hinzufügen von Untertiteln zu digitalen Medien. Die Untertitel werden in einer separaten Textdatei mit der Dateierweiterung .smi oder .sami gespeichert.

In Media Foundation werden SAMI-Untertiteldateien über die SAMI-Medienquelle unterstützt. Verwenden Sie den [Quelllöser,](source-resolver.md) um eine Instanz der SAMI-Medienquelle aus einer URL oder einem Bytestream zu erstellen. Media Foundation stellt keine Komponente bereit, die SAMI-Untertitel anzeigt. Die Anwendung muss die Beschriftungsdaten interpretieren, die sie von der SAMI-Medienquelle empfängt.

Das folgende Beispiel zeigt eine SAMI-Beispieldatei.

``` syntax
<SAMI>
<HEAD>
    <STYLE TYPE="text/css">
    <!--
    P {
        font-family: Arial;
        background: #000000;
        text-align: center;
        }

#standard {Name: Standard; color: #FFFFFF; font-size: 14pt; } 
#hilite {Name: Youth; color: greenyellow; font-size: 18pt;}

    .ENUSCC { Name: English; lang: EN-US-CC; }
    .FRFRCC { Name: French; lang: fr-FR; } 

    -->
    </STYLE>
</HEAD>
<BODY>
    <SYNC Start="0">
        <P Class="ENUSCC">The <I>first</I> caption.</P>
        <P Class="FRFRCC">Un</P>
    </SYNC>
    <SYNC Start="3000">
        <P Class="ENUSCC">The <I>second</I> caption.</P>
        <P Class="FRFRCC">Deux</P>
    </SYNC>
    <SYNC Start="5000">
        <P Class="ENUSCC">The <I>third</I> caption.</P>
        <P Class="FRFRCC">Trois</P>
    </SYNC>
</BODY>
</SAMI>
```

Das `<STYLE>` -Element enthält Stilinformationen. Dieses Beispiel enthält einen Basisstil für `<P>` Elemente zusammen mit zwei benannten Stilen, "standard" und "hilite". Die benannten Stile werden verwendet, um den Basisstil zu ändern. Beschriftungen werden in `<SYNC>` -Elementen platziert. Das Startattribut gibt die Präsentationszeit für diese Beschriftung in Millisekunden an. Die Beschriftungen in diesem Beispiel werden in zwei Sprachen angegeben, die durch die RFC-1766-Sprachtags "en-US" und "fr -FR" angegeben werden. Innerhalb der Beschriftungen werden Sprachen anhand ihrer Klassennamen identifiziert. in diesem Fall "ENUSCC" und "FRFRCC".

Die SAMI-Medienquelle erstellt einen Medienstream für jede Sprache. Standardmäßig wird der erste Stream ausgewählt, und die restlichen Streams werden deaktiviert. Die Anwendung kann die Datenstromauswahl ändern, indem [**SIE DIE AUFRUFEPRESENTATIONDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) und [**DIE ZusammenstellungDescriptor::D eselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream)aufrufen. Jeder Streamdeskriptor enthält die folgenden Attribute.



| attribute                                                       | Beschreibung                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| [**MF \_ SD \_ LANGUAGE**](mf-sd-language-attribute.md)            | Sprachtag, wie durch das `lang` -Attribut angegeben.  |
| [**MF \_ SD \_ SAMI \_ LANGUAGE**](mf-sd-sami-language-attribute.md) | Sprachname, wie durch das `Name` -Attribut angegeben. |



 

Jeder Stream weist den folgenden Medientyp auf:



| attribute                                                                            | Wert                 |
|--------------------------------------------------------------------------------------|-----------------------|
| [**MF \_ \_ MT-HAUPTTYP \_**](mf-mt-major-type-attribute.md)                            | **MFMediaType \_ SAMI** |
| [**MF \_ \_ MT– ALLE \_ BEISPIELE \_ UNABHÄNGIG**](mf-mt-all-samples-independent-attribute.md) | **TRUE**              |



 

Die SAMI-Quelle übermittelt jede Beschriftung in einem separaten Medienbeispiel. Der Beispielzeitstempel und die Dauer werden vom `<SYNC>` -Element abgeleitet. Der im Beispiel enthaltene Medienpuffer enthält die Beschriftung als ASCII-Text. Der Beschriftungsstil wird als Inlineattribut in die Beschriftung `STYLE` eingebettet. Wenn Sie beispielsweise die vorherige SAMI-Datei verwenden und den englischsprachigen Datenstrom mit den Standardformaten verwenden, enthält der erste Medienpuffer die folgenden Daten. (Die Zeilenumbrüche können sich von den hier gezeigten unterscheiden.)

``` syntax
<P STYLE="
    font-family: Arial;
    background: #000000;
    text-align: center;
    Name: English; lang: EN-US-CC;  
    Name: Standard; color: #FFFFFF; 
    font-size: 14pt; ">The<I>first</I> caption.
```

## <a name="sami-styles"></a>SAMI-Stile

Um den aktuellen Stil zu ändern, verwenden Sie die [**INTERFACESSAMIStyle-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) Diese Schnittstelle wird abgerufen, indem [**SIE AUFGETService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) für die SAMI-Medienquelle aufrufen. (Wenn Sie die SAMI-Medienquelle mit der Mediensitzung verwenden, rufen **Sie GetService** in der Mediensitzung auf.) Der Dienstbezeichner ist **MF \_ SAMI \_ SERVICE.**

Im folgenden Beispiel wird der aktuelle SAMI-Stil festgelegt, der durch index angegeben wird.


```C++
HRESULT SetSAMIStyleByIndex(IMFMediaSource *pSource, DWORD index)
{
    IMFSAMIStyle *pSami = NULL;

    DWORD cStyles;
    PROPVARIANT varStyles;

    HRESULT hr = MFGetService(pSource, MF_SAMI_SERVICE, IID_PPV_ARGS(&pSami));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSami->GetStyleCount(&cStyles);
    if (FAILED(hr))
    {
        goto done;
    }

    if (index >= cStyles)
    {
        hr = E_INVALIDARG;
        goto done;
    }

    hr = pSami->GetStyles(&varStyles);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSami->SetSelectedStyle(varStyles.calpwstr.pElems[index]);

done:
    PropVariantClear(&varStyles);
    SafeRelease(&pSami);
    return hr;
}
```



In diesem Beispiel werden die folgenden Methoden für die SAMI-Medienquelle aufrufen:

-   [**STYLESSAMIStyle::GetStyleCount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) ruft die Anzahl der Stile ab.
-   [**STYLESSAMIStyle::GetStyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) ruft eine Liste der Formatnamen ab, die in einem **PROPVARIANT** gespeichert sind.
-   [**STYLESSAMIStyle::SetSelectedStyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) legt einen Stil nach Namen fest.

Die Liste der Stilnamen wird auch im Präsentationsdeskriptor im [**MF \_ PD \_ SAMI \_ STYLELIST-Attribut**](mf-pd-sami-stylelist-attribute.md) gespeichert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medienquellen und -senken](media-sources-and-sinks.md)
</dt> <dt>

[Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



