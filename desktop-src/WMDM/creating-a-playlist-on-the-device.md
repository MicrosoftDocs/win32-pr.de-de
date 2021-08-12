---
title: Erstellen einer Wiedergabeliste auf dem Gerät
description: Erstellen einer Wiedergabeliste auf dem Gerät
ms.assetid: 9f803e1a-ff33-443a-9448-e8c875d77e51
keywords:
- Windows Medien Geräte-Manager, Wiedergabelisten
- Geräte-Manager, Wiedergabelisten
- Programmierhandbuch, Wiedergabelisten
- Desktopanwendungen, Wiedergabelisten
- Erstellen von Windows Media Geräte-Manager-Anwendungen, Wiedergabelisten
- Abstrakte Wiedergabelisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a61d45c234f1cdbe03a713e4d10568fa45c83bdd90227b815c85b0f544d2a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585863"
---
# <a name="creating-a-playlist-on-the-device"></a>Erstellen einer Wiedergabeliste auf dem Gerät

Das Windows Media Geräte-Manager SDK bietet einer MTP-Anwendung die Möglichkeit, eine Wiedergabeliste auf einem Gerät zu erstellen. Diese Art von Wiedergabeliste wird als *abstrakte* Wiedergabeliste bezeichnet, da die auf dem Gerät erstellte Datei keine Mediendaten, sondern nur Metadaten enthält, die die Links zu Mediendateien in der Wiedergabeliste enthalten.

Andere abstrakte Elemente, die auf dem Gerät erstellt werden können, sind Alben (im Wesentlichen Wiedergabelisten mit zusätzlichen Eigenschaften wie Coverart), Kontakte und Nachrichten.

**So erstellen Sie eine Wiedergabeliste**

1.  Abrufen einer [**IWMDMDevice3-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) zum Zielgerät.
2.  Rufen Sie [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) auf, um die \_ g wszWMDMFormatsSupported-Eigenschaft abzurufen.
3.  Wenn keine Wiedergabelistenformate unterstützt werden, lassen Sie das Senden von Wiedergabelisten an das Gerät nicht zu, und überspringen Sie die folgenden Schritte. Wählen Sie andernfalls den vom Gerät unterstützten Formatcode aus, der dem beabsichtigten Objekttyp am besten entspricht. Die generischen Formatcodes WMDM \_ FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST und WMDM \_ FORMATCODE \_ ABSTRACTAUDIOLAYLIST werden am häufigsten unterstützt.
4.  Rufen Sie eine [**IWMDMStorage3-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) für den Speicher (stamm oder ordner) ab, in dem Sie das Objekt erstellen möchten. Einige Geräte funktionieren am besten, wenn sich das Wiedergabelistenobjekt in einem Ordner der obersten Ebene namens "Playlists" befindet.
5.  Erstellen Sie mit [**IWMDMStorage3::CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject)ein leeres Metadatenobjekt.
6.  Rufen Sie mithilfe der **IWMDMMetaData-Schnittstelle** aus dem vorherigen Schritt [**IWMDMMetaData::AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) auf, um den Speichermetadateneigenschaften den ausgewählten Formatcode (aus Schritt 3) hinzuzufügen.
7.  Rufen Sie die [**IWMDMStorageControl3-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) von der **IWMDMStorage3-Schnittstelle** ab.
8.  Rufen Sie [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) auf, um eine neue Wiedergabelistendatei in den ausgewählten Speicher einzufügen. Diese Datei enthält die Metadaten, die durch die **IWMDMMetaData-Schnittstelle** dargestellt werden, die Sie in Schritt 5 erstellt und an **Insert3** übergeben haben. Die -Methode gibt eine **IWMDMStorage-Schnittstelle** für die Wiedergabelistendatei zurück. Sie können die [**IWMDMStorage4-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) abfragen.
9.  Rufen Sie [**IWMDMStorage4::SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) auf, um Verweise auf die **IWMDMStorage-Schnittstellen** der Mediendateien in der Wiedergabeliste zu erstellen.

Beispielcode finden Sie in der \_ Funktion OnCreatePlaylist in der [Beispieldesktopanwendung](sample-desktop-application.md).

> [!Note]  
> Der von Microsoft bereitgestellte MTP-Dienstanbieter ermöglicht einer Anwendung das Festlegen von Verweisen in Metadaten. Um Wiedergabelisten zu implementieren, muss Ihre Anwendung mit einem MTP-Gerät kommunizieren oder einen benutzerdefinierten Dienstanbieter verwenden, der abstrakte Objekte verarbeiten kann. Der CE-Dienstanbieter verarbeitet Wiedergabelisten- und Albumobjekte.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schreiben von Dateien auf das Gerät**](writing-files-to-the-device.md)
</dt> </dl>

 

 




