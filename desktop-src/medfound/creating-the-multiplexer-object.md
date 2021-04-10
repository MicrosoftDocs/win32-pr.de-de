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
# <a name="creating-the-multiplexer-object"></a>Erstellen des Multiplexer-Objekts

Der ASF Multiplexer ist ein wmcontainer-Ebenenobjekt, das mit dem [ASF-Datenobjekt](asf-file-structure.md) zusammenarbeitet und einer Anwendung die Möglichkeit bietet, ASF-Datenpakete für Mediendaten Ströme zu generieren.

Das Multiplexer-Objekt macht die [**imfasf Multiplexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) -Schnittstelle verfügbar. Um den Multiplexer zu erstellen, rufen Sie [**mfkreateasfmultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer)auf. Diese Funktion gibt einen Zeiger auf ein leeres-Objekt zurück. Wenn die Anwendung eine neue ASF-Datei schreibt, muss die Anwendung den Multiplexer mit einem ContentInfo-Objekt initialisieren. Dazu muss [**imfasfmultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize)aufgerufen werden. Das angegebene ContentInfo-Objekt stellt das ASF-Header Objekt der neuen Datei dar. Weitere Informationen zum Erstellen und Initialisieren des ContentInfo-Objekts für eine neue Datei finden Sie unter [Initialisieren des ContentInfo-Objekts einer neuen ASF-Datei](initializing-the-contentinfo-object-of-a-new-asf-file.md).

Die [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) -Methode analysiert das ContentInfo-Objekt, um Datenstrom-Konfigurationsinformationen wie die Anzahl der Streams, die Paketgröße und die Vorabversion zu erfassen. Optional benötigt der Multiplexer möglicherweise auch undichte Bucket-Parameter und die Nutz Last Erweiterungseinheiten. Diese Informationen sind erforderlich, um Datenpakete zu generieren, die den im ASF-Header Objekt definierten Anforderungen entsprechen. Die **Initialize** -Methode konfiguriert den Multiplexer basierend auf dem Medientyp und den Konfigurationseinstellungen der Streams. Wenn z. b. ein Stream für Nutz Last Erweiterungen konfiguriert ist (siehe [Erstellen und Konfigurieren von ASF-Streams](creating-and-configuring-asf-streams.md)), dann wird der Multiplexer so konfiguriert, dass diese Werte den generierten Datenpaketen hinzugefügt werden.

Die [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) -Methode ruft auch ein Handle für das anfängliche Datenobjekt ab, das während der Erstellung des ContentInfo-Objekts zum Schreiben erstellt wurde. Während der Generierung von Datenpaketen fügt der Multiplexer dem Datenobjekt Pakete hinzu und aktualisiert sie entsprechend. Nachdem der Multiplexer alle Datenpakete generiert hat, aktualisiert er das angegebene ContentInfo-Objekt, sodass bestimmte Werte (z. b. die Anzahl von Datenpaketen) aktualisiert werden.

Im folgenden Codebeispiel wird gezeigt, wie ein Multiplexer erstellt und mit einem ContentInfo-Objekt initialisiert wird.


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



Die Funktion, die in einer kompletten Anwendung verwendet wird, finden Sie unter [Tutorial: Kopieren von ASF-Streams aus einer Datei in eine andere](tutorial--copying-asf-streams-from-one-file-to-another.md).

## <a name="multiplexer-initialization-and-leaky-bucket-settings"></a>Multiplexer-Initialisierungs-und Leaky-Bucket-Einstellungen

Mit der [**imfasfmultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) -Methode wird der Multiplexer konfiguriert, um den Datenfluss für den Leaky-Bucket zu bestimmen. Um diese Parameter zu konfigurieren, stellen Sie sicher, dass die folgenden Eigenschaftswerte für das angegebene ContentInfo-Objekt festgelegt sind. Weitere Informationen zum Festlegen dieser Eigenschaften finden Sie unter [Festlegen von Eigenschaften im ContentInfo-Objekt](setting-properties-in-the-contentinfo-object.md).

-   [**Mfpkey \_ Asfmediasink \_ autoadjust \_ Bitrate**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) -Eigenschaft: gibt an, ob der Multiplexer die Bitrate automatisch anpassen muss, um den Datenfluss im Leaky-Bucket beizubehalten. Diese Einstellung kann von der Anwendung geändert werden, indem [**imfasfmultiplexer:: setFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) aufgerufen und das Flag für die **Automatische Anpassung der mfasf \_ Multiplexer- \_ \_ Bitrate** übergeben wird.

-   [**Mfpkey \_ Asfmediasink \_ Base \_ sendtime**](mfpkey-asfmediasink-base-sendtime-property.md) -Eigenschaft: die Sendezeit gibt an, wann die Nutzlast innerhalb des Leaky-Bucket freigegeben wird. Sendezeiten müssen gleich oder älter als die Präsentationszeit sein, da die Nutzlast vor der Präsentationszeit Zeit benötigt, um zum Ziel zu gelangen.

    Dieser Eigenschafts Wert ist die erste Sende Zeit. Der Multiplexer verwendet diesen Wert, um die nachfolgenden Sendezeiten zu berechnen, um sicherzustellen, dass die Daten kontinuierlich durch den Bucket fließen. Wenn das Flag für die **\_ \_ Automatische Anpassung \_ von mfasf Multiplexer** für den Multiplexer festgelegt wurde, passt der Multiplexer die Bitrate so an, dass die Nutzlast gesendet wird, wenn das Puffer Fenster fast voll ist. Wenn das Flag nicht festgelegt ist, kann der Multiplexer aufgrund von Bandbreiten Überlauf keine Datenpakete generieren.

Der Multiplexer erhält streamkonfigurationsinformationen aus dem ASF-Profil, das mit dem in der [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) -Methode angegebenen ContentInfo-Objekt verknüpft ist. Die Datenstrom-Konfigurationsinformationen beinhalten Lecks-Bucket-Parameter. Dieser Wert wird vom Multiplexer zum Generieren von Datenpaketen benötigt.

Um die Parameter für den Leaky-Bucket anzugeben, legen Sie die Werte im [**MF \_ asfstreamconfig \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) -Attribut für das Datenstrom-Konfigurationsobjekt fest, das den Datenstrom im Profil darstellt. Um den Wert des Puffer Fensters zu verwenden, der vom Encoder verwendet wird, nennen Sie [**iwmcodecleakybucket:: getbuffersizebits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md). Der tatsächliche Puffer Fenster Wert ist erst bekannt, nachdem der Ausgabe Medientyp des Encoders festgelegt wurde. Weitere Informationen zum Festlegen des Ausgabemedien Typs finden Sie unter [Medientyp Aushandlung für den Encoder](media-type-negotiation-on-the-encoder.md).

> [!Note]  
> Die vom Encoder verwendeten Lecks-Bucket-Werte können sich in dem ContentInfo-Objekt unterscheiden, das von dem zum Erstellen des Multiplexers verwendeten ASF-Profil bereitgestellt wurde.

 

Die [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) -Methode aktualisiert das ContentInfo-Objekt so, dass die korrekten Werte im endgültigen ASF-Header Objekt widergespiegelt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF Multiplexer](asf-multiplexer.md)
</dt> <dt>

[Erstellen neuer ASF-Datenpakete](generating-new-asf-data-packets.md)
</dt> </dl>

 

 
