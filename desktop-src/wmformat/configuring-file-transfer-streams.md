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
# <a name="configuring-file-transfer-streams"></a><span data-ttu-id="dc3d6-109">Konfigurieren von Datei Übertragungsdaten strömen</span><span class="sxs-lookup"><span data-stu-id="dc3d6-109">Configuring File Transfer Streams</span></span>

<span data-ttu-id="dc3d6-110">Für Datei Übertragungs Datenströme sind keine speziellen Einstellungen in der [**WM \_ - \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-110">File transfer streams do not require any special settings in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="dc3d6-111">Sie benötigen eine Erweiterung für Dateneinheiten, um jedem Beispiel einen Dateinamen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-111">They do require a data unit extension to associate a file name with each sample.</span></span> <span data-ttu-id="dc3d6-112">Um einen Namen mit Datei Übertragungs Beispielen zu senden, müssen Sie ein dateneinheits-Erweiterungssystem für den Stream implementieren.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-112">To send a name with file transfer samples, you must implement a data unit extension system for the stream.</span></span>

<span data-ttu-id="dc3d6-113">Führen Sie die folgenden Schritte aus, um eine Dateneinheiten Erweiterung für den Stream festzulegen:</span><span class="sxs-lookup"><span data-stu-id="dc3d6-113">To set a data unit extension for the stream, perform the following steps:</span></span>

1.  <span data-ttu-id="dc3d6-114">Abrufen eines Zeigers auf die [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) -Schnittstelle des Stream-Konfigurations Objekts durch Aufrufen von **iwmstreamconfig:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-114">Obtain a pointer to the [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
2.  <span data-ttu-id="dc3d6-115">Fügen Sie eine dateneinheits Erweiterung für den Stream hinzu, indem Sie [**IWMStreamConfig2:: adddataunitextension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) wie folgt aufrufen:</span><span class="sxs-lookup"><span data-stu-id="dc3d6-115">Add a data unit extension for the stream by calling [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) as follows:</span></span>
    ```C++
    hr = pStreamConfig2->AddDataUnitExtension(CLSID_WMTPropertyFileName,
                                              -1, NULL, 0);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="dc3d6-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dc3d6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc3d6-117">**Allgemeine Konfiguration für alle Streams**</span><span class="sxs-lookup"><span data-stu-id="dc3d6-117">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="dc3d6-118">**Konfigurieren beliebiger Streamtypen**</span><span class="sxs-lookup"><span data-stu-id="dc3d6-118">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="dc3d6-119">**Dateistreams**</span><span class="sxs-lookup"><span data-stu-id="dc3d6-119">**File Streams**</span></span>](file-streams.md)
</dt> </dl>

 

 




