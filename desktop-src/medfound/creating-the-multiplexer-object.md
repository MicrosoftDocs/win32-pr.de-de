---
description: Erstellen des Multiplexer-Objekts
ms.assetid: a5adc40c-abb4-4012-b6f2-eb871eaed7b9
title: Erstellen des Multiplexer-Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aedf314a63e9475342a7a2091e1d8531bc5bb2839f8c53ae71fa760cdd58b32e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942940"
---
# <a name="creating-the-multiplexer-object"></a>Erstellen des Multiplexer-Objekts

Der ASF-Multiplexer ist ein WMContainer-Ebenenobjekt, das mit dem [ASF-Datenobjekt](asf-file-structure.md) funktioniert und einer Anwendung die Möglichkeit bietet, ASF-Datenpakete für Medienstreams zu generieren.

Das multiplexer-Objekt macht die [**IMFASFMultiplexer-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) verfügbar. Um den Multiplexer zu erstellen, rufen [**Sie MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer)auf. Diese Funktion gibt einen Zeiger auf ein leeres Objekt zurück. Wenn die Anwendung eine neue ASF-Datei schreibt, muss die Anwendung den Multiplexer mit einem ContentInfo-Objekt initialisieren. Rufen Sie hierzu [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize)auf. Das angegebene ContentInfo-Objekt stellt das ASF-Headerobjekt der neuen Datei dar. Informationen zum Erstellen und Initialisieren des ContentInfo-Objekts für eine neue Datei finden Sie unter [Initialisieren des ContentInfo-Objekts einer neuen ASF-Datei.](initializing-the-contentinfo-object-of-a-new-asf-file.md)

Die [**Initialize-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) analysiert das ContentInfo-Objekt, um Datenstromkonfigurationsinformationen wie die Anzahl der Datenströme, die Paketgröße und den Vorabroll zu erfassen. Optional benötigt der Multiplexer möglicherweise auch leaky bucket-Parameter und die Nutzlasterweiterungseinheiten. Diese Informationen sind erforderlich, um Datenpakete zu generieren, die den im ASF-Headerobjekt definierten Anforderungen entsprechen. Die **Initialize-Methode** konfiguriert den Multiplexer basierend auf dem Medientyp und den Konfigurationseinstellungen der Streams. Wenn ein Stream beispielsweise so konfiguriert ist, dass er Nutzlasterweiterungen aufweist (siehe [Erstellen und Konfigurieren von ASF Streams](creating-and-configuring-asf-streams.md)), und dann wird der Multiplexer so konfiguriert, dass diese Werte den generierten Datenpaketen hinzugefügt werden.

Die [**Initialize-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) ruft auch ein Handle für das anfängliche Datenobjekt ab, das während der Erstellung des ContentInfo-Objekts zum Schreiben erstellt wurde. Während der Generierung von Datenpaketen fügt der Multiplexer dem Datenobjekt Pakete hinzu und aktualisiert es entsprechend. Nachdem der Multiplexer alle Datenpakete generiert hat, aktualisiert er das angegebene ContentInfo-Objekt, sodass bestimmte Werte, z. B. die Anzahl der Datenpakete, aktualisiert werden.

Das folgende Codebeispiel zeigt, wie Sie einen Multiplexer erstellen und mit einem ContentInfo-Objekt initialisieren.


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



Informationen zur Verwendung dieser Funktion in einer vollständigen Anwendung finden Sie unter [Tutorial: Kopieren von ASF-Streams aus einer Datei in eine andere](tutorial--copying-asf-streams-from-one-file-to-another.md).

## <a name="multiplexer-initialization-and-leaky-bucket-settings"></a>Multiplexer Initialization and Leaky Bucket Einstellungen

Mit der [**IMFASFMultiplexer::Initialize-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) wird der Multiplexer so konfiguriert, dass der Datenfluss des bucket-Datenverlusts bestimmt wird. Stellen Sie zum Konfigurieren dieser Parameter sicher, dass die folgenden Eigenschaftswerte für das angegebene ContentInfo-Objekt festgelegt sind. Informationen zum Festlegen dieser Eigenschaften finden Sie unter [Festlegen von Eigenschaften im ContentInfo-Objekt.](setting-properties-in-the-contentinfo-object.md)

-   [**MFPKEY \_ ASFMEDIASINK \_ AUTOADJUST \_ BITRATE-Eigenschaft:**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) Gibt an, ob der Multiplexer die Bitrate automatisch anpassen muss, um den Datenfluss im Bucket "Leaky" beizubehalten. Diese Einstellung kann von der Anwendung geändert werden, indem [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) aufgerufen und das **MFASF \_ MULTIPLEXER \_ AUTOADJUST \_ BITRATE-Flag** übergeben wird.

-   [**MFPKEY \_ ASFMEDIASINK \_ BASE \_ SENDTIME-Eigenschaft:**](mfpkey-asfmediasink-base-sendtime-property.md) Die Sendezeit gibt an, wann die Nutzlast im bucket leaky freigegeben wird. Sendezeiten müssen gleich oder früher als die Präsentationszeit sein, da die Nutzlast vor der Präsentationszeit Zeit zum Erreichen des Ziels haben muss.

    Dieser Eigenschaftswert ist die erste Sendezeit. Der Multiplexer verwendet diesen Wert, um die nachfolgenden Sendezeiten zu berechnen, um sicherzustellen, dass Daten kontinuierlich durch den Bucket fließen. Wenn das **MFASF \_ MULTIPLEXER \_ AUTOADJUST \_ BITRATE-Flag** für den Multiplexer festgelegt wurde, passt der Multiplexer die Bitrate so an, dass die Nutzlast gesendet wird, wenn das Pufferfenster fast voll ist. Wenn das Flag nicht festgelegt ist, kann der Multiplexer aufgrund eines Bandbreitenüberlaufs keine Datenpakete generieren.

Der Multiplexer ruft Datenstromkonfigurationsinformationen aus dem ASF-Profil ab, das dem ContentInfo-Objekt zugeordnet ist, das in der [**Initialize-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) angegeben ist. Die Datenstromkonfigurationsinformationen enthalten leaky bucket-Parameter. Dieser Wert wird vom Multiplexer benötigt, um Datenpakete zu generieren.

Um die Leaky-Bucketparameter anzugeben, legen Sie die Werte im [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1-Attribut**](mf-asfstreamconfig-leakybucket1-attribute.md) für das Streamkonfigurationsobjekt fest, das den Stream im Profil darstellt. Um den Pufferfensterwert zu verwenden, der vom Encoder verwendet wird, rufen [**Sie IWMCodecLeakyBucket::GetBufferSizeBits auf.**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) Der tatsächliche Pufferfensterwert ist erst nach dem Festlegen des Ausgabemedientyps des Encoders bekannt. Informationen zum Festlegen des Ausgabemedientyps finden Sie unter [Medientypaushandlung auf dem Encoder.](media-type-negotiation-on-the-encoder.md)

> [!Note]  
> Die vom Encoder verwendeten leaky-Bucketwerte können sich im ContentInfo-Objekt unterscheiden, das vom ASF-Profil bereitgestellt wurde, das zum Erstellen des Multiplexers verwendet wurde.

 

Die [**Initialize-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) aktualisiert das ContentInfo-Objekt, sodass die richtigen Werte im endgültigen ASF-Headerobjekt widergespiegelt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF Multiplexer](asf-multiplexer.md)
</dt> <dt>

[Generieren neuer ASF-Datenpakete](generating-new-asf-data-packets.md)
</dt> </dl>

 

 
