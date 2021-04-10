---
description: Erstellen des Multiplexer-Objekts
ms.assetid: a5adc40c-abb4-4012-b6f2-eb871eaed7b9
title: Erstellen des Multiplexer-Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28dd7933bdd7c3a8587c96cb490c4e4122ecc04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214331"
---
# <a name="creating-the-multiplexer-object"></a><span data-ttu-id="3b5cf-103">Erstellen des Multiplexer-Objekts</span><span class="sxs-lookup"><span data-stu-id="3b5cf-103">Creating the Multiplexer Object</span></span>

<span data-ttu-id="3b5cf-104">Der ASF Multiplexer ist ein wmcontainer-Ebenenobjekt, das mit dem [ASF-Datenobjekt](asf-file-structure.md) zusammenarbeitet und einer Anwendung die Möglichkeit bietet, ASF-Datenpakete für Mediendaten Ströme zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-104">The ASF multiplexer is a WMContainer layer object that works with the [ASF Data Object](asf-file-structure.md) and gives an application the ability to generate ASF data packets for media streams.</span></span>

<span data-ttu-id="3b5cf-105">Das Multiplexer-Objekt macht die [**imfasf Multiplexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-105">The multiplexer object exposes the [**IMFASFMultiplexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) interface.</span></span> <span data-ttu-id="3b5cf-106">Um den Multiplexer zu erstellen, rufen Sie [**mfkreateasfmultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer)auf.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-106">To create the multiplexer, call [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer).</span></span> <span data-ttu-id="3b5cf-107">Diese Funktion gibt einen Zeiger auf ein leeres-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-107">This function returns a pointer to an empty object.</span></span> <span data-ttu-id="3b5cf-108">Wenn die Anwendung eine neue ASF-Datei schreibt, muss die Anwendung den Multiplexer mit einem ContentInfo-Objekt initialisieren.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-108">If the application is writing a new ASF file, the application must initialize the multiplexer with a ContentInfo object.</span></span> <span data-ttu-id="3b5cf-109">Dazu muss [**imfasfmultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-109">To do this, call [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize).</span></span> <span data-ttu-id="3b5cf-110">Das angegebene ContentInfo-Objekt stellt das ASF-Header Objekt der neuen Datei dar.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-110">The specified ContentInfo object represents the ASF Header Object of the new file.</span></span> <span data-ttu-id="3b5cf-111">Weitere Informationen zum Erstellen und Initialisieren des ContentInfo-Objekts für eine neue Datei finden Sie unter [Initialisieren des ContentInfo-Objekts einer neuen ASF-Datei](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="3b5cf-111">For information about creating and initializing the ContentInfo object for a new file, see [Initializing the ContentInfo Object of a New ASF File](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span></span>

<span data-ttu-id="3b5cf-112">Die [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) -Methode analysiert das ContentInfo-Objekt, um Datenstrom-Konfigurationsinformationen wie die Anzahl der Streams, die Paketgröße und die Vorabversion zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-112">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method parses the ContentInfo object to collect stream configuration information such as the number of streams, packet size, preroll.</span></span> <span data-ttu-id="3b5cf-113">Optional benötigt der Multiplexer möglicherweise auch undichte Bucket-Parameter und die Nutz Last Erweiterungseinheiten.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-113">Optionally, the multiplexer might also need leaky bucket parameters, and the payload extension units.</span></span> <span data-ttu-id="3b5cf-114">Diese Informationen sind erforderlich, um Datenpakete zu generieren, die den im ASF-Header Objekt definierten Anforderungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-114">This information is required in order to generate data packets that match the requirements defined in the ASF Header Object.</span></span> <span data-ttu-id="3b5cf-115">Die **Initialize** -Methode konfiguriert den Multiplexer basierend auf dem Medientyp und den Konfigurationseinstellungen der Streams.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-115">The **Initialize** method configures the multiplexer based on the media type and configuration settings of the streams.</span></span> <span data-ttu-id="3b5cf-116">Wenn z. b. ein Stream für Nutz Last Erweiterungen konfiguriert ist (siehe [Erstellen und Konfigurieren von ASF-Streams](creating-and-configuring-asf-streams.md)), dann wird der Multiplexer so konfiguriert, dass diese Werte den generierten Datenpaketen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-116">For example, if a stream is configured to have payload extensions (see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md)), and then the multiplexer is configured to add those values to the generated data packets.</span></span>

<span data-ttu-id="3b5cf-117">Die [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) -Methode ruft auch ein Handle für das anfängliche Datenobjekt ab, das während der Erstellung des ContentInfo-Objekts zum Schreiben erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-117">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method also gets a handle to the initial data object that was created during the creation of the ContentInfo object for writing.</span></span> <span data-ttu-id="3b5cf-118">Während der Generierung von Datenpaketen fügt der Multiplexer dem Datenobjekt Pakete hinzu und aktualisiert sie entsprechend.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-118">During data packet generation, the multiplexer adds packets to the data object and updates it appropriately.</span></span> <span data-ttu-id="3b5cf-119">Nachdem der Multiplexer alle Datenpakete generiert hat, aktualisiert er das angegebene ContentInfo-Objekt, sodass bestimmte Werte (z. b. die Anzahl von Datenpaketen) aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-119">After the multiplexer generates all the data packets, it updates the supplied ContentInfo object so that certain values, such as number of data packets, are updated.</span></span>

<span data-ttu-id="3b5cf-120">Im folgenden Codebeispiel wird gezeigt, wie ein Multiplexer erstellt und mit einem ContentInfo-Objekt initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-120">The following code example shows how to create a multiplexer and initialize it with a ContentInfo object.</span></span>


```C++
//-------------------------------------------------------------------
// CreateOutputGenerators
//
// Creates the ASF mux and the ASF Content Info object for the 
// output file.
//-------------------------------------------------------------------

HRESULT CreateOutputGenerators(
    IMFASFProfile *pProfile, 
    IMFASFContentInfo **ppContentInfo, 
    IMFASFMultiplexer **ppMux
    )
{
    IMFASFContentInfo *pContentInfo = NULL;
    IMFASFMultiplexer *pMux = NULL;

    // Use the ASF profile to create the ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);

    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->SetProfile(pProfile);
    }

    // Create the ASF Multiplexer object.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFMultiplexer(&pMux);
    }
    
    // Initialize it using the new ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Initialize(pContentInfo);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();

        *ppMux = pMux;
        (*ppMux)->AddRef();
    }

    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);

    return hr;
}
```



<span data-ttu-id="3b5cf-121">Die Funktion, die in einer kompletten Anwendung verwendet wird, finden Sie unter [Tutorial: Kopieren von ASF-Streams aus einer Datei in eine andere](tutorial--copying-asf-streams-from-one-file-to-another.md).</span><span class="sxs-lookup"><span data-stu-id="3b5cf-121">To see this function used in a complete application, see [Tutorial: Copying ASF Streams from One File to Another](tutorial--copying-asf-streams-from-one-file-to-another.md).</span></span>

## <a name="multiplexer-initialization-and-leaky-bucket-settings"></a><span data-ttu-id="3b5cf-122">Multiplexer-Initialisierungs-und Leaky-Bucket-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="3b5cf-122">Multiplexer Initialization and Leaky Bucket Settings</span></span>

<span data-ttu-id="3b5cf-123">Mit der [**imfasfmultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) -Methode wird der Multiplexer konfiguriert, um den Datenfluss für den Leaky-Bucket zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-123">The [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method configures the multiplexer to determine the leaky bucket data flow.</span></span> <span data-ttu-id="3b5cf-124">Um diese Parameter zu konfigurieren, stellen Sie sicher, dass die folgenden Eigenschaftswerte für das angegebene ContentInfo-Objekt festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-124">To configure these parameters, make sure that the following property values are set on the specified ContentInfo object.</span></span> <span data-ttu-id="3b5cf-125">Weitere Informationen zum Festlegen dieser Eigenschaften finden Sie unter [Festlegen von Eigenschaften im ContentInfo-Objekt](setting-properties-in-the-contentinfo-object.md).</span><span class="sxs-lookup"><span data-stu-id="3b5cf-125">For information about setting these properties, see [Setting Properties in the ContentInfo Object](setting-properties-in-the-contentinfo-object.md).</span></span>

-   <span data-ttu-id="3b5cf-126">[**Mfpkey \_ Asfmediasink \_ autoadjust \_ Bitrate**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) -Eigenschaft: gibt an, ob der Multiplexer die Bitrate automatisch anpassen muss, um den Datenfluss im Leaky-Bucket beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-126">[**MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) property: This indicates whether the multiplexer needs to adjust the bit rate automatically, to maintain the data flow in the leaky bucket.</span></span> <span data-ttu-id="3b5cf-127">Diese Einstellung kann von der Anwendung geändert werden, indem [**imfasfmultiplexer:: setFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) aufgerufen und das Flag für die **Automatische Anpassung der mfasf \_ Multiplexer- \_ \_ Bitrate** übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-127">This setting can be changed by the application by calling [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) and passing the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag.</span></span>

-   <span data-ttu-id="3b5cf-128">[**Mfpkey \_ Asfmediasink \_ Base \_ sendtime**](mfpkey-asfmediasink-base-sendtime-property.md) -Eigenschaft: die Sendezeit gibt an, wann die Nutzlast innerhalb des Leaky-Bucket freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-128">[**MFPKEY\_ASFMEDIASINK\_BASE\_SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md) property: The send time indicates when the payload inside the leaky bucket will be released.</span></span> <span data-ttu-id="3b5cf-129">Sendezeiten müssen gleich oder älter als die Präsentationszeit sein, da die Nutzlast vor der Präsentationszeit Zeit benötigt, um zum Ziel zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-129">Send times must be equal to or earlier than the presentation time because the payload must have time to get to the destination before the presentation time.</span></span>

    <span data-ttu-id="3b5cf-130">Dieser Eigenschafts Wert ist die erste Sende Zeit.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-130">This property value is the first send time.</span></span> <span data-ttu-id="3b5cf-131">Der Multiplexer verwendet diesen Wert, um die nachfolgenden Sendezeiten zu berechnen, um sicherzustellen, dass die Daten kontinuierlich durch den Bucket fließen.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-131">The multiplexer uses this value to calculate the subsequent send times to ensure that data flows through the bucket steadily.</span></span> <span data-ttu-id="3b5cf-132">Wenn das Flag für die **\_ \_ Automatische Anpassung \_ von mfasf Multiplexer** für den Multiplexer festgelegt wurde, passt der Multiplexer die Bitrate so an, dass die Nutzlast gesendet wird, wenn das Puffer Fenster fast voll ist.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-132">If the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag has been set on the multiplexer, the multiplexer will adjust the bit rate so that the payload is sent out when the buffer window is close to being full.</span></span> <span data-ttu-id="3b5cf-133">Wenn das Flag nicht festgelegt ist, kann der Multiplexer aufgrund von Bandbreiten Überlauf keine Datenpakete generieren.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-133">If the flag is not set, the multiplexer fails to generate data packets due to bandwidth overrun.</span></span>

<span data-ttu-id="3b5cf-134">Der Multiplexer erhält streamkonfigurationsinformationen aus dem ASF-Profil, das mit dem in der [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) -Methode angegebenen ContentInfo-Objekt verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-134">The multiplexer obtains stream configuration information from the ASF profile associated with the ContentInfo object specified in the [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method.</span></span> <span data-ttu-id="3b5cf-135">Die Datenstrom-Konfigurationsinformationen beinhalten Lecks-Bucket-Parameter.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-135">The stream configuration information includes leaky bucket parameters.</span></span> <span data-ttu-id="3b5cf-136">Dieser Wert wird vom Multiplexer zum Generieren von Datenpaketen benötigt.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-136">This value is required by the multiplexer to generate data packets.</span></span>

<span data-ttu-id="3b5cf-137">Um die Parameter für den Leaky-Bucket anzugeben, legen Sie die Werte im [**MF \_ asfstreamconfig \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) -Attribut für das Datenstrom-Konfigurationsobjekt fest, das den Datenstrom im Profil darstellt.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-137">To specify the leaky bucket parameters, set the values in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute on the stream configuration object that represents the stream in the profile.</span></span> <span data-ttu-id="3b5cf-138">Um den Wert des Puffer Fensters zu verwenden, der vom Encoder verwendet wird, nennen Sie [**iwmcodecleakybucket:: getbuffersizebits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span><span class="sxs-lookup"><span data-stu-id="3b5cf-138">To use the buffer window value, which is used by the encoder, call [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span></span> <span data-ttu-id="3b5cf-139">Der tatsächliche Puffer Fenster Wert ist erst bekannt, nachdem der Ausgabe Medientyp des Encoders festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-139">The actual buffer window value is known only after setting the output media type of the encoder.</span></span> <span data-ttu-id="3b5cf-140">Weitere Informationen zum Festlegen des Ausgabemedien Typs finden Sie unter [Medientyp Aushandlung für den Encoder](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="3b5cf-140">For information about setting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

> [!Note]  
> <span data-ttu-id="3b5cf-141">Die vom Encoder verwendeten Lecks-Bucket-Werte können sich in dem ContentInfo-Objekt unterscheiden, das von dem zum Erstellen des Multiplexers verwendeten ASF-Profil bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-141">The leaky bucket values used by the encoder might be different in the ContentInfo object that was provided by the ASF Profile that was used to create the multiplexer.</span></span>

 

<span data-ttu-id="3b5cf-142">Die [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) -Methode aktualisiert das ContentInfo-Objekt so, dass die korrekten Werte im endgültigen ASF-Header Objekt widergespiegelt werden.</span><span class="sxs-lookup"><span data-stu-id="3b5cf-142">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method updates the ContentInfo object so that the correct values are reflected in the final ASF Header Object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b5cf-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3b5cf-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b5cf-144">ASF Multiplexer</span><span class="sxs-lookup"><span data-stu-id="3b5cf-144">ASF Multiplexer</span></span>](asf-multiplexer.md)
</dt> <dt>

[<span data-ttu-id="3b5cf-145">Erstellen neuer ASF-Datenpakete</span><span class="sxs-lookup"><span data-stu-id="3b5cf-145">Generating New ASF Data Packets</span></span>](generating-new-asf-data-packets.md)
</dt> </dl>

 

 
