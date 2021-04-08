---
description: Der synchronisierte, barrierefreie Medienaustausch (Sami) ist ein Format zum Hinzufügen von Beschriftungen zu digitalen Medien.
ms.assetid: 007c8181-089e-4e56-a31d-9d1942f90b07
title: Sami-Medienquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9340b51815b130cb41061478358b2ab9dcf68f60
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104050698"
---
# <a name="sami-media-source"></a>Sami-Medienquelle

Der synchronisierte, barrierefreie Medienaustausch (Sami) ist ein Format zum Hinzufügen von Beschriftungen zu digitalen Medien. Die Beschriftungen werden in einer separaten Textdatei mit der Dateinamenerweiterung ". SMI" oder ". Sami" gespeichert.

In Media Foundation werden Sami Caption-Dateien durch die Sami Media-Quelle unterstützt. Verwenden Sie den [quellresolver](source-resolver.md) , um eine Instanz der Sami Media-Quelle aus einer URL oder einem Bytestream zu erstellen. Media Foundation stellt keine-Komponente bereit, die Sami-Beschriftungen anzeigt. Die Anwendung muss die Beschriftungs Daten interpretieren, die Sie von der Sami-Medienquelle empfängt.

Im folgenden wird ein Beispiel für eine Sami-Datei gezeigt.

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

Das- `<STYLE>` Element enthält Stil Informationen. Dieses Beispiel enthält einen Basistyp für `<P>` Elemente, zusammen mit zwei benannten Stilen: "Standard" und "Hilite". Die benannten Stile werden zum Ändern des Basistyps verwendet. Beschriftungen werden innerhalb von `<SYNC>` Elementen platziert. Das Start-Attribut gibt die Präsentationszeit in Millisekunden für diese Beschriftung an. Die Beschriftungen in diesem Beispiel werden in zwei Sprachen angegeben, die durch ihre RFC-1766-sprach Tags "en-US" und "fr-FR" angegeben werden. Innerhalb der Beschriftungen werden Sprachen anhand ihrer Klassennamen identifiziert. in diesem Fall: "Deutsch." und "frfrcc".

Die Sami Media-Quelle erstellt einen Mediendaten Strom für jede Sprache. Standardmäßig ist der erste Stream ausgewählt, und die verbleibenden Datenströme werden deaktiviert. Die Anwendung kann die Datenstrom Auswahl ändern, indem [**imfpresentationdescriptor:: selectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) und [**imfpresentationdescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream)aufgerufen werden. Jeder Datenstrom Deskriptor enthält die folgenden Attribute.



| Attribut                                                       | BESCHREIBUNG                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| [**MF \_ SD- \_ Sprache**](mf-sd-language-attribute.md)            | Das Sprachtag, wie durch das- `lang` Attribut angegeben.  |
| [**MF, \_ SD, \_ Samisch \_**](mf-sd-sami-language-attribute.md) | Der Name der Sprache, wie vom- `Name` Attribut angegeben. |



 

Jeder Stream weist den folgenden Medientyp auf:



| Attribut                                                                            | Wert                 |
|--------------------------------------------------------------------------------------|-----------------------|
| [**Haupt-Typ des MF- \_ MT \_ \_**](mf-mt-major-type-attribute.md)                            | **MF MediaType \_ Sami** |
| [**\_ \_ alle \_ Beispiele \_ unabhängig von MF**](mf-mt-all-samples-independent-attribute.md) | **TRUE**              |



 

Die Sami-Quelle übermittelt jede Beschriftung in einem separaten Medien Beispiel. Der Beispiel Zeitstempel und die Dauer werden vom- `<SYNC>` Element abgeleitet. Der im Beispiel enthaltene Medien Puffer enthält die Beschriftung als ASCII-Text. Der Beschriftungs Stil ist in die Beschriftung als Inline `STYLE` Attribut eingebettet. Wenn z. b. die vorherige samische Datei und der englischsprachige Stream mit den Standardformaten verwendet werden, enthält der erste Medien Puffer die folgenden Daten. (Die Zeilenumbrüche können sich von den hier gezeigten unterscheiden.)

``` syntax
<P STYLE="
    font-family: Arial;
    background: #000000;
    text-align: center;
    Name: English; lang: EN-US-CC;  
    Name: Standard; color: #FFFFFF; 
    font-size: 14pt; ">The<I>first</I> caption.
```

## <a name="sami-styles"></a>Sami-Stile

Um den aktuellen Stil zu ändern, verwenden Sie die [**imfsamistyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) -Schnittstelle. Diese Schnittstelle wird durch Aufrufen von [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) in der Sami Media-Quelle abgerufen. (Wenn Sie die Sami Media-Quelle mit der Medien Sitzung verwenden, müssen Sie **GetService** für die Medien Sitzung aufrufen.) Der Dienst Bezeichner ist der **MF- \_ Sami- \_ Dienst**.

Im folgenden Beispiel wird der aktuelle Sami-Stil festgelegt, der durch den Index angegeben wird.


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



In diesem Beispiel werden die folgenden Methoden für die Sami Media-Quelle aufgerufen:

-   [**IMF-mistyle:: getstylecount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) Ruft die Anzahl der Stile ab.
-   [**Imbsamistyle:: getStyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) Ruft eine Liste der in einem **PROPVARIANT** gespeicherten Stilnamen ab.
-   [**Imamsamistyle:: setselectedstyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) legt einen Stil anhand des namensfest.

Die Liste der stylenames wird auch auf dem Präsentations Deskriptor im [**MF PD-Attribut \_ " \_ Sami \_ stylelist**](mf-pd-sami-stylelist-attribute.md) " gespeichert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medienquellen und senken](media-sources-and-sinks.md)
</dt> <dt>

[Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



