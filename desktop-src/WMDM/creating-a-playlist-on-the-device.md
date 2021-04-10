---
title: Erstellen einer Wiedergabeliste auf dem Gerät
description: Erstellen einer Wiedergabeliste auf dem Gerät
ms.assetid: 9f803e1a-ff33-443a-9448-e8c875d77e51
keywords:
- Windows Media Device Manager, Wiedergabelisten
- Device Manager, Wiedergabelisten
- Programmier Handbuch, Wiedergabelisten
- Desktop Anwendungen, Wiedergabelisten
- Erstellen von Windows Media Device Manager-Anwendungen, Wiedergabelisten
- abstrakte Wiedergabelisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c287cc406b795db07fde3f10103822dea32185a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309772"
---
# <a name="creating-a-playlist-on-the-device"></a>Erstellen einer Wiedergabeliste auf dem Gerät

Das Windows Media Device Manager SDK bietet die Möglichkeit, dass eine MTP-Anwendung eine Wiedergabeliste auf einem Gerät erstellt. Diese Art von Wiedergabeliste wird als *abstrakte* Wiedergabeliste bezeichnet, da die Datei, die auf dem Gerät erstellt wird, keine Mediendaten enthält, sondern nur Metadaten, die die Links zu Mediendateien in der Wiedergabeliste enthalten.

Andere abstrakte Elemente, die auf dem Gerät erstellt werden können, umfassen Alben (im wesentlichen Wiedergabelisten mit zusätzlichen Eigenschaften wie z. b. Cover Art), Kontakte und Nachrichten.

**So erstellen Sie eine Wiedergabeliste**

1.  Beschaffen einer [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) -Schnittstelle für das Zielgerät.
2.  Rufen Sie [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) auf, um die Eigenschaft "g \_ wszwmdmformatssupported" zu erhalten.
3.  Wenn keine Wiedergabelisten Formate unterstützt werden, lassen Sie das Senden von Wiedergabelisten an das Gerät nicht zu und überspringen Sie die folgenden Schritte. Wählen Sie andernfalls den Geräte gestützten Formatierungs Code aus, der dem gewünschten Objekttyp am ehesten entspricht. Die allgemeinen Codes "WMDM \_ Formatcode \_ abstractaudiovideoplaylist" und "WMDM \_ Formatcode \_ abstractaudiolaylist" werden am häufigsten unterstützt.
4.  Rufen Sie eine [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) -Schnittstelle für den Speicher (das Stammverzeichnis oder einen Ordner) ab, in dem Sie das Objekt erstellen möchten. Einige Geräte funktionieren am besten, wenn das Wiedergabelisten Objekt in einem Ordner der obersten Ebene mit dem Namen "Playlists" platziert wird.
5.  Erstellen Sie ein leeres Metadatenobjekt mithilfe von [**IWMDMStorage3:: CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).
6.  Wenn Sie die im vorherigen Schritt abzurufende **iwmdmmetadata** -Schnittstelle verwenden, nennen Sie [**iwmdmmetadata:: AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) , um den ausgewählten Format Code (aus Schritt 3) den speichermetadateneigenschaften hinzuzufügen.
7.  Abrufen der [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) -Schnittstelle von der **IWMDMStorage3** -Schnittstelle.
8.  Ruft [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) auf, um eine neue Wiedergabelisten Datei in den ausgewählten Speicher einzufügen. Diese Datei enthält die Metadaten, die von der in Schritt 5 erstellten **iwmdmmetadata** -Schnittstelle dargestellt und an **Insert3** übergeben werden. Die-Methode gibt eine **iwmdmstorage** -Schnittstelle für die Wiedergabelisten Datei zurück. Sie können die [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) -Schnittstelle Abfragen.
9.  Rufen Sie [**IWMDMStorage4:: setreferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) auf, um Verweise auf die **iwmdmstorage** -Schnittstellen der Mediendateien in der Wiedergabeliste zu erstellen.

Beispielcode finden Sie in der \_ onkreatewiedergabe-Funktion in der [Beispiel-Desktop Anwendung](sample-desktop-application.md).

> [!Note]  
> Der von Microsoft bereitgestellte MTP-Dienstanbieter ermöglicht es einer Anwendung, Verweise in Metadaten festzulegen. Zum Implementieren von Wiedergabelisten muss Ihre Anwendung mit einem MTP-Gerät kommunizieren, oder es muss ein benutzerdefinierter Dienstanbieter verwendet werden, der abstrakte Objekte verarbeiten kann. Der CE-Dienstanbieter verarbeitet Wiedergabelisten-und Album Objekte.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schreiben von Dateien auf das Gerät**](writing-files-to-the-device.md)
</dt> </dl>

 

 




