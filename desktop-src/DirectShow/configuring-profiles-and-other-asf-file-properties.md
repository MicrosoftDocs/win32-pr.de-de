---
description: Konfigurieren von Profilen und anderen ASF-Dateieigenschaften
ms.assetid: c43df556-9d8a-4010-9ed6-f84d8ac6d9bc
title: Konfigurieren von Profilen und anderen ASF-Dateieigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e26dcbb49cb5ff8309dccafc3f1d8d66397871
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392729"
---
# <a name="configuring-profiles-and-other-asf-file-properties"></a>Konfigurieren von Profilen und anderen ASF-Dateieigenschaften

In den folgenden Artikeln wird beschrieben, wie verschiedene Aufgaben im Zusammenhang mit der Erstellung von ASF-Dateien durchgeführt werden. Einige der in diesem Thema erwähnten Schnittstellen sind in der Dokumentation zum Windows Media-Format SDK dokumentiert.

Erstellen eines Profils

ASF-Profile werden im Windows Media-Format SDK ausführlich erläutert. im wesentlichen beschreiben Sie Attribute einer Windows Media-Format Datei, z. b. Bitrate, Anzahl und Typ von Streams und Komprimierungs Qualität. Der Filter verwendet das Profil, um zu bestimmen, welche Art von Windows Media-Format Datei geschrieben werden soll, wie viele Eingabe Pins Sie einrichten muss und welche Medientypen akzeptiert werden können.

Um ein benutzerdefiniertes Profil zu erstellen, verwenden Sie das Windows Media SDK-SDK direkt, um ein Profil-Manager-Objekt mithilfe der **wmkreateprofilemanager** -Funktion zu erstellen. Erstellen Sie als nächstes das Profil, und übergeben Sie es mithilfe der [**iconfigasfwriter:: konfigurifisingprofile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) -Methode an den [WM-ASF-Writer](wm-asf-writer-filter.md) . Dies ist die einzige Möglichkeit, den Filter mit einem Profil zu konfigurieren, das die Codecs Windows Media Audio und der Video 9-Serie verwendet. System Profile für frühere Versionen dieser Codecs können mithilfe der [**iconfigasfwriter:: Konfigurations refilterusingprofileguid**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid) -Methode hinzugefügt werden.

Sie können das Profil zurücksetzen, während die Eingabe Pins des Filters verbunden sind, solange das neue Profil keine zusätzlichen Eingabe Pins erfordert. Wenn Sie z. b. das Profil aus einem reinen reinen Audioprofil in ein zweidimensionales Audio-und Video Profil ändern, wird nur die audiopin wieder hergestellt, und es wird keine neue PIN für den Videostream erstellt.

Hinzufügen von Metadaten

Fragen Sie zum Hinzufügen von Metadaten zu einer Datei den [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter für die **iwmheaderinfo** -Schnittstelle ab. Nachdem dem Filter ein Profil zugewiesen wurde, verwenden Sie die **iwmheaderinfo** -Schnittstellen Methoden, um die Metadaten zu schreiben.

Indizieren einer Datei

Der WM-ASF-Writer erstellt standardmäßig Temporale indizierte Dateien. Verwenden Sie zum Erstellen einer Frame indizierten Datei die [**iconfigasfwriter:: setindexmode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) -Methode, um die gesamte Indizierung zu deaktivieren, und erstellen Sie dann die Datei. Verwenden Sie nach Abschluss des Vorgangs das SDK für den Windows Media-Format, um einen Frame basierten Index für die Datei zu erstellen.

Two-Pass Codierung

Die zwei-Pass-Codierung wird nur auf Windows Media-Codecs der Version 8 und höher unterstützt. Versetzen Sie den WM-ASF-Writer in den Vorverarbeitungs-Modus, indem Sie [**IConfigAsfWriter2:: SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) aufrufen und am \_ configasfwriter \_ param \_ Multipass im *dwparam* -Parameter und **true** im *dwParam1* -Parameter angeben.

Führen Sie dann das Filter Diagramm aus. Wenn alle Vorverarbeitungs Durchläufen abgeschlossen sind (in der Regel wird nur ein Vorverarbeitungs Durchlauf ausgeführt), empfängt die Anwendung ein Ereignis vom Typ " [**\_ Preprocess \_ Complete**](ec-preprocess-complete.md) " vom Filter. Wenn dieses Ereignis empfangen wird, verwenden Sie [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) , um den Streamzeiger auf den Anfang zurückzusetzen, und führen Sie das Filter Diagramm erneut aus. Nach dem letzten Durchlauf (in der Regel der zweite Durchlauf) empfängt die Anwendung ein [**EC \_ Complete**](ec-complete.md) -Ereignis, um anzugeben, dass der Codierungsprozess abgeschlossen ist. Wenn ein Vorverarbeitungs Durchlauf abgebrochen wird, bevor das Ereignis für das Ereignis " **EC \_ Preprocess \_ Complete** " empfangen wird, rufen Sie [**IConfigAsfWriter2:: resetmultipassstate**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) auf, um den Filter vor dem Versuch einer anderen Vorverarbeitungs Ausführung zurückzusetzen

Es ist nur erforderlich, den Parameter "am \_ configasfwriter \_ param Multipass" auf "false" festzulegen \_ , wenn Sie den Filter vollständig aus dem Vorverarbeitungs Modus setzen möchten. 

> [!IMPORTANT]
> Es ist Aufgabe der Anwendung, den Vorverarbeitungs Modus basierend auf dem Profil zu aktivieren, das für die Codierung verwendet wird. Für einige Profile ist die zwei-Pass-Codierung erforderlich. Wenn Sie versuchen, eine Datei mit einem solchen Profil zu codieren, und am \_ configasfwriter \_ param \_ Multipass nicht auf **true** festgelegt ist, führt dies zu einem Fehler vom Typ " [**\_ userabort**](ec-userabort.md) ". Weitere Informationen finden Sie in der Dokumentation zum Windows Media-Format SDK.

 

Erhalten und Festlegen von Puffer Eigenschaften zur Laufzeit

In einigen Szenarien, z. b. Wenn Sie die Tastenkombination beim Schreiben einer Datei erzwingen möchten, muss eine Anwendung möglicherweise Informationen zu einem Windows-Medien Puffer zur Laufzeit erhalten oder festlegen. Die Filter " [WM ASF Reader](wm-asf-reader-filter.md) " und " [WM ASF Writer](wm-asf-writer-filter.md) " unterstützen beide einen Rückrufmechanismus, mit dem eine Anwendung beim Lesen oder Schreiben von Dateien auf die **INSSBuffer3** -Schnittstelle auf jedem einzelnen Medien Puffer zugreifen kann. Anwendungen können diese Schnittstelle verwenden, um bestimmte Beispiele als Keyframes festzulegen, SMPTE-Zeit Codes festzulegen, damit-Einstellungen anzugeben oder einen beliebigen Typ privater Daten einem Stream hinzuzufügen.

Verwenden Sie die [**iamwmbufferpass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) -Schnittstelle, um Rückrufe von der PIN zu registrieren, die den Videostream verarbeitet. Mit der PIN wird die [**iamwmbufferpasscallback:: notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) -Methode für jeden Puffer aufgerufen.

Nicht quadratische Pixel

Der WM-ASF-Writer stellt eine Verbindung mit einem upstreamfilter her, z. b. dem DV-Decoder, der Informationen zum Pixel Seitenverhältnis ausgibt Der WM-ASF-Writer schreibt diese Informationen als Dateneinheiten Erweiterungen für jedes Beispiel in der Datei.

Wenn der WM-ASF-Reader Pixel-Seitenverhältnis Informationen im Dateiheader oder in Dateneinheiten Erweiterungen für die Beispiele findet, bietet er ein [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Format als erste Wahl in der Ausgabe-PIN. Die Member **dwpictaspectratiox** und **dwpictaspectratioy** der Struktur, die das Seitenverhältnis des Video Rechtecks beschreiben, werden richtig angepasst, um das Pixel Seitenverhältnis zu berücksichtigen.

Beibehalten des interschnür Formats

Wenn Sie in einem Fernsehgerät oder einer DV-Kamera Zeilen Sprung Video aufzeichnen, sollten Sie das Originalvideo als unabhängige Felder aufbewahren, wenn Sie davon ausgehen, dass die codierte Datei in einem Fernsehgerät oder einem anderen Zeilen Sprung Gerät wiedergegeben werden soll. (Computer Monitore sind progressiv-Scangeräte.) Wenn Sie ein Video deinstalften und dann für die Wiedergabe in einem Fernsehgerät wiederherstellen, entstehen Datenverluste. In einer ASF-Datei werden Zeilen Sprung-Informationen als Dateneinheiten Erweiterungen gespeichert, die die Anwendung auf die einzelnen Beispiele anwendet, indem die zuvor beschriebene [**iamwmbufferpasscallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) -Methode verwendet wird. Führen Sie die folgenden Schritte aus, um eine Datei zu codieren, die die ursprünglichen damit-Einstellungen beibehält:

1.  Implementieren Sie eine Klasse, die **iamwmbufferpasscallback** unterstützt, und schreiben Sie eine Benachrichtigungsfunktion, die die damit-Flags für die einzelnen Stichproben festlegt. Diese Funktion wird vom WM-ASF-Writer aufgerufen, bevor die einzelnen Beispiele verarbeitet werden.
    ```C++
    // Set to WM_CT_TOP_FIELD_FIRST if that is your format.
    BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
    HRESULT hr = S_OK;

    hr = pNSSBuffer3->SetProperty(
        WM_SampleExtensionGUID_ContentType, 
        (void*) &flag, 
        WM_SampleExtension_ContentType_Size
        );         
    ```

    

2.  Legen Sie die dateneinheits Erweiterungen für das Profil fest, bevor Sie das Profil an den Filter übergeben.
    ```C++
    hr = pWMStreamConfig2->AddDataUnitExtension(
        WM_SampleExtensionGUID_ContentType, 
        WM_SampleExtension_ContentType_Size, 
        NULL, 
        0 
        );
    ```

    

3.  Nachdem Sie den Filter mit dem Profil konfiguriert haben, rufen Sie die **IWMWriterAdvanced2** -Schnittstelle vom WM-ASF-Writer ab, und rufen Sie **die Methode "** die Methode".

    ``

    ``

    ```C++
    // Must do this first.
    hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);
      
    CComPtr<IServiceProvider> pProvider;
    CComPtr<IWMWriterAdvanced2> pWMWA2;

    hr = pConfigAsfWriter2->QueryInterface( __uuidof(IServiceProvider),
                                             (void**)&pProvider);
    if (SUCCEEDED(hr))
    {
        hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
            IID_IWMWriterAdvanced2,
            (void**)&pWMWA2);
    }

    BOOL pValue = TRUE;

    // Set the first parameter to your actual input number.
    hr = pWMWA2->SetInputSetting(0, g_wszInterlacedCoding,
        WMT_TYPE_BOOL, (BYTE*) &pValue, sizeof(WMT_TYPE_BOOL));
                
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von ASF-Dateien in DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



