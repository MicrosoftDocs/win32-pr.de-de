---
title: Konfigurieren von Streams
description: Konfigurieren von Streams
ms.assetid: faed54ae-9e80-492a-9602-e726bdb3b54a
keywords:
- Streams,Konfigurieren von Dateiübertragungsstreams
- Codecs,Konfigurieren von Dateiübertragungsstreams
- Dateiübertragungsstreams
- Streams, Dateneinheitenerweiterungen
- Codecs, Dateneinheitserweiterungen
- Dateneinheitenerweiterungen, Datenübertragungsdatenströme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0be95c9760a02275e223f56785149f6867d4aaf2462d07d158991b3cd21c01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849063"
---
# <a name="configuring-file-transfer-streams"></a>Konfigurieren von Streams

Dateiübertragungsstreams erfordern keine besonderen Einstellungen in der [**WM \_ MEDIA \_ TYPE-Struktur.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Sie erfordern eine Dateneinheitserweiterung, um jedem Beispiel einen Dateinamen zuzuordnen. Um einen Namen mit Dateiübertragungsbeispielen zu senden, müssen Sie ein Dateneinheiterweiterungssystem für den Stream implementieren.

Führen Sie die folgenden Schritte aus, um eine Dateneinheitenerweiterung für den Stream festzulegen:

1.  Rufen Sie einen Zeiger auf die [**IWMStreamConfig2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) des Streamkonfigurationsobjekts ab, indem **Sie IWMStreamConfig::QueryInterface** aufrufen.
2.  Fügen Sie eine Dateneinheitenerweiterung für den Stream hinzu, indem [**Sie IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) wie folgt aufrufen:
    ```C++
    hr = pStreamConfig2->AddDataUnitExtension(CLSID_WMTPropertyFileName,
                                              -1, NULL, 0);
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Configuration Common to All Streams**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Konfigurieren beliebiger Streamtypen**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Datei-Streams**](file-streams.md)
</dt> </dl>

 

 




