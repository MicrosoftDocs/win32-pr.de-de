---
title: Konfigurieren von Profilen und anderen Dateieigenschaften (qasf)
description: Konfigurieren von Profilen und anderen Dateieigenschaften (qasf)
ms.assetid: a462fc8b-5a2e-4c93-828d-177d1965b734
keywords:
- Windows Media-Format-SDK, Konfigurieren von Profilen (qasf)
- Windows Media-Format-SDK, Konfigurieren von Dateieigenschaften (qasf)
- Windows Media-Format-SDK, Metadaten (qasf)
- Advanced Systems Format (ASF), Konfigurieren von Profilen (qasf)
- ASF (Advanced Systems Format), Konfigurieren von Profilen (qasf)
- Advanced Systems Format (ASF), Konfigurieren von Dateieigenschaften (qasf)
- ASF (Advanced Systems Format), Konfigurieren von Dateieigenschaften (qasf)
- Advanced Systems Format (ASF), Metadaten (qasf)
- ASF (Advanced Systems Format), Metadaten (qasf)
- Windows Media-Format-SDK, qasf
- Advanced Systems Format (ASF), qasf
- ASF (Advanced Systems Format), qasf
- Metadaten, qasf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebb6afedfa00813e7447e5bcaefe1f251c02575
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473740"
---
# <a name="configuring-profiles-and-other-file-properties-qasf"></a>Konfigurieren von Profilen und anderen Dateieigenschaften (qasf)

In den folgenden Artikeln wird beschrieben, wie verschiedene Aufgaben im Zusammenhang mit der Erstellung von ASF-Dateien durchgeführt werden.

## <a name="creating-a-profile-qasf"></a>Erstellen eines Profils (qasf)

Um ein benutzerdefiniertes Profil zu erstellen, verwenden Sie das Windows Media SDK-SDK direkt, um ein Profil-Manager-Objekt mithilfe der [**wmkreateprofilemanager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) -Funktion zu erstellen. Erstellen Sie als nächstes das Profil, und übergeben Sie es mithilfe der [**iconfigasfwriter:: konfigurifisingprofile**](iconfigasfwriter-configurefilterusingprofile.md) -Methode an den [WM-ASF-Writer](wm-asf-writer-filter.md) . Dies ist die einzige Möglichkeit, den Filter mit einem Profil zu konfigurieren, das die Codecs Windows Media Audio und der Video 9-Serie verwendet. System Profile für frühere Versionen dieser Codecs können mithilfe der [**iconfigasfwriter:: Konfigurations refilterusingprofileguid**](iconfigasfwriter-configurefilterusingprofileguid.md) -Methode hinzugefügt werden.

## <a name="adding-metadata-qasf"></a>Hinzufügen von Metadaten (qasf)

Rufen Sie zum Hinzufügen von Metadaten zu einer Datei **QueryInterface** von der **ibasefilter** -Schnittstelle auf dem [WM-ASF-Writer](wm-asf-writer-filter.md) auf, um die [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -Schnittstelle abzurufen. Nachdem dem Filter ein Profil zugewiesen wurde, verwenden Sie die **iwmheaderinfo** -Schnittstellen Methoden, um die Metadaten zu schreiben.

## <a name="indexing-a-file-qasf"></a>Indizieren einer Datei (qasf)

Der WM-ASF-Writer erstellt standardmäßig Temporale indizierte Dateien. Verwenden Sie zum Erstellen einer Frame indizierten Datei die [**iconfigasfwriter:: setindexmode**](iconfigasfwriter-setindexmode.md) -Methode, um die gesamte Indizierung zu deaktivieren, und erstellen Sie dann die Datei. Verwenden Sie nach Abschluss des Vorgangs das SDK für den Windows Media-Format, um einen Frame basierten Index für die Datei zu erstellen.

## <a name="performing-two-pass-encoding-qasf"></a>Ausführen Two-Pass Codierung (qasf)

Die zwei-Pass-Codierung wird nur auf Windows Media-Codecs der Version 8 und höher unterstützt. Versetzen Sie den WM-ASF-Writer in den Vorverarbeitungs-Modus, indem Sie [**IConfigAsfWriter2:: SetParam**](iconfigasfwriter2-setparam.md) aufrufen und am \_ configasfwriter \_ param \_ Multipass im *dwparam* -Parameter und **true** im *dwParam1* -Parameter angeben.

Führen Sie dann das Filter Diagramm aus. Wenn alle Vorverarbeitungs Durchläufen abgeschlossen sind (in der Regel wird nur ein Vorverarbeitungs Durchlauf ausgeführt), empfängt die Anwendung ein Ereignis vom Typ " **\_ Preprocess \_ Complete** " vom Filter. Wenn dieses Ereignis empfangen wird, verwenden Sie **imediaseeking:: setpositions** , um den Streamzeiger auf den Anfang zurückzusetzen, und führen Sie das Filter Diagramm erneut aus. Nach dem letzten Durchlauf (in der Regel der zweite Durchlauf) empfängt die Anwendung ein **EC \_ Complete** -Ereignis, um anzugeben, dass der Codierungsprozess abgeschlossen ist. Wenn ein Vorverarbeitungs Durchlauf abgebrochen wird, bevor das Ereignis für das Ereignis " **EC \_ Preprocess \_ Complete** " empfangen wird, rufen Sie [**IConfigAsfWriter2:: resetmultipassstate**](iconfigasfwriter2-resetmultipassstate.md) auf, um den Filter vor dem Versuch einer anderen Vorverarbeitungs Ausführung zurückzusetzen

Es ist nur erforderlich, **iconfigasfwriter:: SetParam**(am \_ configasfwriter \_ param \_ Multipass, **false**) aufzurufen, wenn Sie den Filter vollständig aus dem Vorverarbeitungs Modus setzen möchten.

> [!IMPORTANT]
> Die Anwendung ist dafür verantwortlich, den Vorverarbeitungs Modus basierend auf dem Profil zu aktivieren, das für die Codierung verwendet wird. Für einige Profile ist die zwei-Pass-Codierung erforderlich. Wenn Sie versuchen, eine Datei mit einem solchen Profil zu codieren, und am \_ configasfwriter \_ param \_ Multipass nicht auf **true** festgelegt ist, führt dies zu einem Fehler vom Typ " \_ userabort". Weitere Informationen dazu, wie Sie bestimmen können, ob für ein bestimmtes Profil zwei-Pass-Codierungen erforderlich sind, finden [Sie unter using Two-Pass Encoding](using-two-pass-encoding.md) or [Writing Variable Bitrate Streams](writing-variable-bit-rate-streams.md).

 

## <a name="getting-and-setting-buffer-properties-at-run-time-qasf"></a>Erhalten und Festlegen von Puffer Eigenschaften zur Laufzeit (qasf)

In einigen Szenarien, z. b. Wenn Sie die Tastenkombination beim Schreiben einer Datei erzwingen möchten, muss eine Anwendung möglicherweise Informationen zu einem Windows-Medien Puffer zur Laufzeit erhalten oder festlegen. Die Filter " [WM ASF Reader](wm-asf-reader-filter.md) " und " [WM ASF Writer](wm-asf-writer-filter.md) " unterstützen beide einen Rückrufmechanismus, mit dem eine Anwendung beim Lesen oder Schreiben von Dateien auf die [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) -Schnittstelle auf jedem einzelnen Medien Puffer zugreifen kann. Anwendungen können diese Schnittstelle verwenden, um bestimmte Beispiele als Keyframes oder [*cleanpoints*](wmformat-glossary.md)festzulegen, um SMPTE-Zeit Codes festzulegen, damit-Einstellungen anzugeben oder einen beliebigen Typ privater Daten einem Stream hinzuzufügen.

Verwenden Sie die [**iamwmbufferpass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) -Schnittstelle, um Rückrufe von der PIN zu registrieren, die den Videostream verarbeitet. Wenn die PIN die [**iamwmbufferpasscallback:: notify**](iamwmbufferpasscallback-notify.md) -Methode aufruft, untersuchen Sie die Zeitstempel des Puffers, und rufen Sie ggf. [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) auf, um die " **WM \_ sampleextensionguid \_ outputcleanpoint** "-Eigenschaft für den Puffer auf " **true**" festzulegen.

## <a name="non-square-pixel-support-qasf"></a>Unterstützung von nicht quadratischen Pixeln (qasf)

Der WM-ASF-Writer stellt eine Verbindung mit einem upstreamfilter her, z. b. dem DV-Decoder, der Informationen zum Pixel Seitenverhältnis ausgibt Der WM-ASF-Writer schreibt diese Informationen als Dateneinheiten Erweiterungen für jedes Beispiel in der Datei.

Wenn der WM-ASF-Reader die Pixel-Seitenverhältnis Informationen im Dateiheader oder in den Dateneinheiten Erweiterungen für die Beispiele findet, bietet er einen **VIDEOINFOHEADER2** -Medientyp als erste Wahl in der Ausgabe-PIN. Die Member **dwpictaspectratiox** und **dwpictaspectratioy** der Struktur, die das Seitenverhältnis des Video Rechtecks beschreiben, werden richtig angepasst, um das Pixel Seitenverhältnis zu berücksichtigen.

## <a name="maintaining-interlaced-format"></a>Beibehalten des interschnür Formats

Wenn Sie in einem Fernsehgerät oder einer DV-Kamera Zeilen Sprung Video aufzeichnen, sollten Sie das Originalvideo als unabhängige Felder aufbewahren, wenn Sie davon ausgehen, dass die codierte Datei in einem Fernsehgerät oder einem anderen Zeilen Sprung Gerät wiedergegeben werden soll. (Computer Monitore sind progressiv-Scangeräte.) Wenn Sie ein Video deinstalften und dann für die Wiedergabe in einem Fernsehgerät wiederherstellen, entstehen Datenverluste. In einer ASF-Datei werden Zeilen Sprung-Informationen als Dateneinheiten Erweiterungen gespeichert, die die Anwendung auf die einzelnen Beispiele anwendet, indem die zuvor beschriebene **iamwmbufferpasscallback** -Methode verwendet wird. Führen Sie die folgenden Schritte aus, um eine Datei zu codieren, die die ursprünglichen damit-Einstellungen beibehält:

-   Implementieren Sie eine Klasse, die **iamwmbufferpasscallback** unterstützt, und schreiben Sie eine Benachrichtigungsfunktion, die die damit-Flags für die einzelnen Stichproben festlegt. Diese Funktion wird vom WM-ASF-Writer aufgerufen, bevor die einzelnen Beispiele verarbeitet werden.


```C++
// Set to WM_CT_TOP_FIELD_FIRST if that is your format.
BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
            HRESULT hr = pNSSBuffer3->SetProperty(WM_SampleExtensionGUID_ContentType, (void*) &flag, WM_SampleExtension_ContentType_Size);
           
```



-   Legen Sie die dateneinheits Erweiterungen für das Profil fest, bevor Sie das Profil an den Filter übergeben.


```C++
hr = pWMStreamConfig2->AddDataUnitExtension( WM_SampleExtensionGUID_ContentType, WM_SampleExtension_ContentType_Size, NULL, 0 );
```



-   Nachdem Sie den Filter mit dem Profil konfiguriert haben, rufen Sie die **IWMWriterAdvanced2** -Schnittstelle vom WM-ASF-Writer ab, und rufen Sie **die Methode "** die Methode".

`// Must do this first.`

`hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);`


```C++
  
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



 

 