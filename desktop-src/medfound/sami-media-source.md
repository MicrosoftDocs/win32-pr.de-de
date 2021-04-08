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
# <a name="sami-media-source"></a><span data-ttu-id="d1184-103">Sami-Medienquelle</span><span class="sxs-lookup"><span data-stu-id="d1184-103">SAMI Media Source</span></span>

<span data-ttu-id="d1184-104">Der synchronisierte, barrierefreie Medienaustausch (Sami) ist ein Format zum Hinzufügen von Beschriftungen zu digitalen Medien.</span><span class="sxs-lookup"><span data-stu-id="d1184-104">Synchronized Accessible Media Interchange (SAMI) is a format for adding captions to digital media.</span></span> <span data-ttu-id="d1184-105">Die Beschriftungen werden in einer separaten Textdatei mit der Dateinamenerweiterung ". SMI" oder ". Sami" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d1184-105">The captions are stored in a separate text file with the file name extension .smi or .sami.</span></span>

<span data-ttu-id="d1184-106">In Media Foundation werden Sami Caption-Dateien durch die Sami Media-Quelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d1184-106">In Media Foundation, SAMI caption files are supported through the SAMI media source.</span></span> <span data-ttu-id="d1184-107">Verwenden Sie den [quellresolver](source-resolver.md) , um eine Instanz der Sami Media-Quelle aus einer URL oder einem Bytestream zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d1184-107">Use the [Source Resolver](source-resolver.md) to create an instance of the SAMI media source from a URL or byte stream.</span></span> <span data-ttu-id="d1184-108">Media Foundation stellt keine-Komponente bereit, die Sami-Beschriftungen anzeigt.</span><span class="sxs-lookup"><span data-stu-id="d1184-108">Media Foundation does not provide a component that displays SAMI captions.</span></span> <span data-ttu-id="d1184-109">Die Anwendung muss die Beschriftungs Daten interpretieren, die Sie von der Sami-Medienquelle empfängt.</span><span class="sxs-lookup"><span data-stu-id="d1184-109">The application must interpret the caption data that it receives from the SAMI media source.</span></span>

<span data-ttu-id="d1184-110">Im folgenden wird ein Beispiel für eine Sami-Datei gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d1184-110">The following shows an example SAMI file.</span></span>

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

<span data-ttu-id="d1184-111">Das- `<STYLE>` Element enthält Stil Informationen.</span><span class="sxs-lookup"><span data-stu-id="d1184-111">The `<STYLE>` element contains style information.</span></span> <span data-ttu-id="d1184-112">Dieses Beispiel enthält einen Basistyp für `<P>` Elemente, zusammen mit zwei benannten Stilen: "Standard" und "Hilite".</span><span class="sxs-lookup"><span data-stu-id="d1184-112">This example contains a base style for `<P>` elements, along with two named styles, "standard" and "hilite".</span></span> <span data-ttu-id="d1184-113">Die benannten Stile werden zum Ändern des Basistyps verwendet.</span><span class="sxs-lookup"><span data-stu-id="d1184-113">The named styles are used to modify the base style.</span></span> <span data-ttu-id="d1184-114">Beschriftungen werden innerhalb von `<SYNC>` Elementen platziert.</span><span class="sxs-lookup"><span data-stu-id="d1184-114">Captions are placed within `<SYNC>` elements.</span></span> <span data-ttu-id="d1184-115">Das Start-Attribut gibt die Präsentationszeit in Millisekunden für diese Beschriftung an.</span><span class="sxs-lookup"><span data-stu-id="d1184-115">The start attribute gives the presentation time in milliseconds for that caption.</span></span> <span data-ttu-id="d1184-116">Die Beschriftungen in diesem Beispiel werden in zwei Sprachen angegeben, die durch ihre RFC-1766-sprach Tags "en-US" und "fr-FR" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d1184-116">The captions in this example are given in two languages, specified by their RFC-1766 language tags, "en-US" and "fr -FR".</span></span> <span data-ttu-id="d1184-117">Innerhalb der Beschriftungen werden Sprachen anhand ihrer Klassennamen identifiziert. in diesem Fall: "Deutsch." und "frfrcc".</span><span class="sxs-lookup"><span data-stu-id="d1184-117">Within the captions, languages are identified by their class names; in this case, "ENUSCC" and "FRFRCC".</span></span>

<span data-ttu-id="d1184-118">Die Sami Media-Quelle erstellt einen Mediendaten Strom für jede Sprache.</span><span class="sxs-lookup"><span data-stu-id="d1184-118">The SAMI media source creates one media stream for each language.</span></span> <span data-ttu-id="d1184-119">Standardmäßig ist der erste Stream ausgewählt, und die verbleibenden Datenströme werden deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d1184-119">By default, the first stream is selected and the remaining streams are deselected.</span></span> <span data-ttu-id="d1184-120">Die Anwendung kann die Datenstrom Auswahl ändern, indem [**imfpresentationdescriptor:: selectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) und [**imfpresentationdescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d1184-120">The application can change the stream selection by calling [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) and [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span></span> <span data-ttu-id="d1184-121">Jeder Datenstrom Deskriptor enthält die folgenden Attribute.</span><span class="sxs-lookup"><span data-stu-id="d1184-121">Each stream descriptor contains the following attributes.</span></span>



| <span data-ttu-id="d1184-122">Attribut</span><span class="sxs-lookup"><span data-stu-id="d1184-122">Attribute</span></span>                                                       | <span data-ttu-id="d1184-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d1184-123">Description</span></span>                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="d1184-124">**MF \_ SD- \_ Sprache**</span><span class="sxs-lookup"><span data-stu-id="d1184-124">**MF\_SD\_LANGUAGE**</span></span>](mf-sd-language-attribute.md)            | <span data-ttu-id="d1184-125">Das Sprachtag, wie durch das- `lang` Attribut angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1184-125">Language tag, as given by the `lang` attribute.</span></span>  |
| [<span data-ttu-id="d1184-126">**MF, \_ SD, \_ Samisch \_**</span><span class="sxs-lookup"><span data-stu-id="d1184-126">**MF\_SD\_SAMI\_LANGUAGE**</span></span>](mf-sd-sami-language-attribute.md) | <span data-ttu-id="d1184-127">Der Name der Sprache, wie vom- `Name` Attribut angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1184-127">Language name, as given by the `Name` attribute.</span></span> |



 

<span data-ttu-id="d1184-128">Jeder Stream weist den folgenden Medientyp auf:</span><span class="sxs-lookup"><span data-stu-id="d1184-128">Each stream has the following media type:</span></span>



| <span data-ttu-id="d1184-129">Attribut</span><span class="sxs-lookup"><span data-stu-id="d1184-129">Attribute</span></span>                                                                            | <span data-ttu-id="d1184-130">Wert</span><span class="sxs-lookup"><span data-stu-id="d1184-130">Value</span></span>                 |
|--------------------------------------------------------------------------------------|-----------------------|
| [<span data-ttu-id="d1184-131">**Haupt-Typ des MF- \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d1184-131">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                            | <span data-ttu-id="d1184-132">**MF MediaType \_ Sami**</span><span class="sxs-lookup"><span data-stu-id="d1184-132">**MFMediaType\_SAMI**</span></span> |
| [<span data-ttu-id="d1184-133">**\_ \_ alle \_ Beispiele \_ unabhängig von MF**</span><span class="sxs-lookup"><span data-stu-id="d1184-133">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md) | <span data-ttu-id="d1184-134">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="d1184-134">**TRUE**</span></span>              |



 

<span data-ttu-id="d1184-135">Die Sami-Quelle übermittelt jede Beschriftung in einem separaten Medien Beispiel.</span><span class="sxs-lookup"><span data-stu-id="d1184-135">The SAMI source delivers each caption in a separate media sample.</span></span> <span data-ttu-id="d1184-136">Der Beispiel Zeitstempel und die Dauer werden vom- `<SYNC>` Element abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d1184-136">The sample time stamp and duration are derived from the `<SYNC>` element.</span></span> <span data-ttu-id="d1184-137">Der im Beispiel enthaltene Medien Puffer enthält die Beschriftung als ASCII-Text.</span><span class="sxs-lookup"><span data-stu-id="d1184-137">The media buffer contained in the sample holds the caption as ASCII text.</span></span> <span data-ttu-id="d1184-138">Der Beschriftungs Stil ist in die Beschriftung als Inline `STYLE` Attribut eingebettet.</span><span class="sxs-lookup"><span data-stu-id="d1184-138">The caption style is embedded in the caption as an inline `STYLE` attribute.</span></span> <span data-ttu-id="d1184-139">Wenn z. b. die vorherige samische Datei und der englischsprachige Stream mit den Standardformaten verwendet werden, enthält der erste Medien Puffer die folgenden Daten.</span><span class="sxs-lookup"><span data-stu-id="d1184-139">For example, given the previous SAMI file, and using the English-language stream with the default styles, the first media buffer would contain the following data.</span></span> <span data-ttu-id="d1184-140">(Die Zeilenumbrüche können sich von den hier gezeigten unterscheiden.)</span><span class="sxs-lookup"><span data-stu-id="d1184-140">(The line breaks might differ from what is shown here.)</span></span>

``` syntax
<P STYLE="
    font-family: Arial;
    background: #000000;
    text-align: center;
    Name: English; lang: EN-US-CC;  
    Name: Standard; color: #FFFFFF; 
    font-size: 14pt; ">The<I>first</I> caption.
```

## <a name="sami-styles"></a><span data-ttu-id="d1184-141">Sami-Stile</span><span class="sxs-lookup"><span data-stu-id="d1184-141">SAMI Styles</span></span>

<span data-ttu-id="d1184-142">Um den aktuellen Stil zu ändern, verwenden Sie die [**imfsamistyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d1184-142">To change the current style, use the [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) interface.</span></span> <span data-ttu-id="d1184-143">Diese Schnittstelle wird durch Aufrufen von [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) in der Sami Media-Quelle abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d1184-143">This interface is obtained by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the SAMI media source.</span></span> <span data-ttu-id="d1184-144">(Wenn Sie die Sami Media-Quelle mit der Medien Sitzung verwenden, müssen Sie **GetService** für die Medien Sitzung aufrufen.) Der Dienst Bezeichner ist der **MF- \_ Sami- \_ Dienst**.</span><span class="sxs-lookup"><span data-stu-id="d1184-144">(If you are using the SAMI media source with the Media Session, call **GetService** on the Media Session.) The service identifier is **MF\_SAMI\_SERVICE**.</span></span>

<span data-ttu-id="d1184-145">Im folgenden Beispiel wird der aktuelle Sami-Stil festgelegt, der durch den Index angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d1184-145">The following example sets the current SAMI style, specified by index.</span></span>


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



<span data-ttu-id="d1184-146">In diesem Beispiel werden die folgenden Methoden für die Sami Media-Quelle aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="d1184-146">This example calls the following methods on the SAMI media source:</span></span>

-   <span data-ttu-id="d1184-147">[**IMF-mistyle:: getstylecount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) Ruft die Anzahl der Stile ab.</span><span class="sxs-lookup"><span data-stu-id="d1184-147">[**IMFSAMIStyle::GetStyleCount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) gets the number of styles.</span></span>
-   <span data-ttu-id="d1184-148">[**Imbsamistyle:: getStyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) Ruft eine Liste der in einem **PROPVARIANT** gespeicherten Stilnamen ab.</span><span class="sxs-lookup"><span data-stu-id="d1184-148">[**IMFSAMIStyle::GetStyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) gets a list of the style names, stored in a **PROPVARIANT**.</span></span>
-   <span data-ttu-id="d1184-149">[**Imamsamistyle:: setselectedstyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) legt einen Stil anhand des namensfest.</span><span class="sxs-lookup"><span data-stu-id="d1184-149">[**IMFSAMIStyle::SetSelectedStyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) sets a style by name.</span></span>

<span data-ttu-id="d1184-150">Die Liste der stylenames wird auch auf dem Präsentations Deskriptor im [**MF PD-Attribut \_ " \_ Sami \_ stylelist**](mf-pd-sami-stylelist-attribute.md) " gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d1184-150">The list of style names is also stored on the presentation descriptor, in the [**MF\_PD\_SAMI\_STYLELIST**](mf-pd-sami-stylelist-attribute.md) attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1184-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d1184-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1184-152">Medienquellen und senken</span><span class="sxs-lookup"><span data-stu-id="d1184-152">Media Sources and Sinks</span></span>](media-sources-and-sinks.md)
</dt> <dt>

[<span data-ttu-id="d1184-153">Unterstützte Medienformate in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d1184-153">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



