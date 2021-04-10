---
title: Konfigurieren von Datei Übertragungsdaten strömen
description: Konfigurieren von Datei Übertragungsdaten strömen
ms.assetid: faed54ae-9e80-492a-9602-e726bdb3b54a
keywords:
- Streams, Konfigurieren von Datei Übertragungsdaten strömen
- Codecs, Konfigurieren von Datei Übertragungsdaten strömen
- Datei Übertragungsdaten Ströme
- Streams, Dateneinheiten Erweiterungen
- Codecs, Dateneinheiten Erweiterungen
- dateneinheits Erweiterungen, Datei Übertragungsdaten Ströme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75fac7d2270da82f1f9e82ed9123611ae608dd3c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038593"
---
# <a name="configuring-file-transfer-streams"></a>Konfigurieren von Datei Übertragungsdaten strömen

Für Datei Übertragungs Datenströme sind keine speziellen Einstellungen in der [**WM \_ - \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur erforderlich. Sie benötigen eine Erweiterung für Dateneinheiten, um jedem Beispiel einen Dateinamen zuzuordnen. Um einen Namen mit Datei Übertragungs Beispielen zu senden, müssen Sie ein dateneinheits-Erweiterungssystem für den Stream implementieren.

Führen Sie die folgenden Schritte aus, um eine Dateneinheiten Erweiterung für den Stream festzulegen:

1.  Abrufen eines Zeigers auf die [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) -Schnittstelle des Stream-Konfigurations Objekts durch Aufrufen von **iwmstreamconfig:: QueryInterface**.
2.  Fügen Sie eine dateneinheits Erweiterung für den Stream hinzu, indem Sie [**IWMStreamConfig2:: adddataunitextension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) wie folgt aufrufen:
    ```C++
    hr = pStreamConfig2->AddDataUnitExtension(CLSID_WMTPropertyFileName,
                                              -1, NULL, 0);
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Konfiguration für alle Streams**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Konfigurieren beliebiger Streamtypen**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Dateistreams**](file-streams.md)
</dt> </dl>

 

 




