---
title: Schreiben von Dateien auf das Gerät
description: Schreiben von Dateien auf das Gerät
ms.assetid: 66eaed16-032b-4ac0-a768-aded80f10255
keywords:
- Windows Media Device Manager, Schreiben von Dateien auf Geräte
- Device Manager, Schreiben von Dateien auf Geräte
- Programmier Handbuch, Schreiben von Dateien auf Geräte
- Desktop Anwendungen, Schreiben von Dateien auf Geräte
- Erstellen von Windows Media Device Manager-Anwendungen, Schreiben von Dateien auf Geräte
- Schreiben von Dateien auf Geräte, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d8b5234cc275eed1b4aa344c16a2b927b8122d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515501"
---
# <a name="writing-files-to-the-device"></a>Schreiben von Dateien auf das Gerät

Vor dem Senden einer Datei an ein Gerät muss Ihre Anwendung herausfinden, welche Typen von Dateien und Formaten das Gerät verarbeiten kann. so kann die Anwendung bestimmen, ob die Datei vor dem Senden oder unverändert gesendet werden soll oder nicht.

In den folgenden Schritten wird gezeigt, wie eine vorhandene Datei an das Gerät gesendet wird. Informationen zum Erstellen einer neuen Datei auf dem Gerät, z. b. eine Wiedergabeliste, finden Sie unter [Erstellen einer Wiedergabeliste auf dem Gerät](creating-a-playlist-on-the-device.md).

1.  Hiermit wird das Format der Datei, die Sie an das Gerät senden möchten, angezeigt. Weitere Informationen finden Sie unter Ermitteln [eines Datei Formats](discovering-a-files-format.md).
2.  Wenn das Gerät für die Wiedergabe der Datei vorgesehen ist,
    -   Fragen Sie die Datei nach den Formatfunktionen ab. Weitere Informationen finden Sie unter Ermitteln der [Geräte Formatierungsfunktionen](discovering-device-format-capabilities.md).
    -   Suchen Sie ein akzeptables Format, das von der Anwendung aus der ursprünglichen Datei erstellt werden kann.
    -   Wenn die Datei transcodiert werden muss, transcodieren Sie Sie.
3.  Suchen Sie nach einem übergeordneten Speicher für das neue-Objekt. Windows Media Device Manager bietet keine Möglichkeit, den Standard Speicherort für bestimmte Dateitypen (Video-oder Audiodateien, WMV oder BMP, einen "Favoriten"-Ordner usw.) zu ermitteln. Sie müssen daher jedes Gerät untersuchen, um herauszufinden, wo das neue Objekt am besten gespeichert wird. (Andere Anwendungen erzwingen eine bestimmte Ordnerstruktur, z. b. Windows Media Player erstellt Alben, Wiedergabelisten und Musik Ordner, in denen der Ordner "Music" eine "Künstlerin" und "Albumname"-Struktur enthält. Aus diesem Grund und da einige Geräte möglicherweise nicht mit einer anderen Software als Windows Media Player getestet wurden, sollten Sie beachten, dass die Platzierung von Wiedergabelisten-oder Album Objekten in einem anderen Ordner als den Wiedergabelisten oder Alben manchmal zu nicht funktionierenden Objekten auf einigen Geräten führen kann.)
4.  Wenn der Zielspeicher [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3)unterstützt, erstellen Sie eine neue Metadatenschnittstelle durch Aufrufen von [**IWMDMStorage3:: CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject). Legen Sie Metadaten für eine [**iwmdmmetadata**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) -Schnittstelle fest. Weitere Informationen finden Sie unter [Festlegen von Metadaten für eine Datei](setting-metadata-on-a-file.md). Die einzigen erforderlichen Metadaten sind g \_ wszwmdmformatcode (ein [**WMDM- \_ Formatcode**](wmdm-formatcode.md) -Wert, der den Inhalt beschreibt), aber die weiteren Metadaten, die Sie bereitstellen können, desto effizienter wird die Übertragung für den Dienstanbieter.
5.  Senden Sie die Datei mithilfe der [**Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)-, [**Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)-oder [**Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) -Methode an das Gerät. **Insert3** ermöglicht das Einschließen der Metadaten auf das Gerät als Teil der-Methode. Weitere Informationen finden Sie unter [Senden der Datei an das Gerät](sending-the-file-to-the-device.md).

Der Code, der jeden dieser Schritte demonstriert, wird auf den verknüpften Themenseiten bereitgestellt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen einer Windows Media Device Manager-Anwendung**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




