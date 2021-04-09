---
description: ASF-Splitter
ms.assetid: 383b1cc6-4a77-4e0e-a766-6213c64b025c
title: ASF-Splitter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f61bcd17a81197106d2f7c43fa1fdc25d9da2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128004"
---
# <a name="asf-splitter"></a>ASF-Splitter

Das ASF- *Splitter* Objekt ist eine wmcontainer-Ebenenkomponente, die das ASF-Datenobjekt einer ASF-Datei (Advanced Systems Format) analysiert. Sie können den Splitter verwenden, um die Datenpakete im Datenobjekt zu lesen und streambeispiele zu generieren. Weitere Informationen zur Struktur einer ASF-Datei finden Sie unter [Struktur der ASF-Datei](asf-file-structure.md).

Der Splitter macht die [**imfasf Splitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) -Schnittstelle verfügbar. Der Splitter analysiert die Pakete der ASF-Daten für die ausgewählten Streams und verpackt Sie in einzelne Beispiel Objekte, die die [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle verfügbar machen. Der Splitter ist eine der Komponenten auf Platt Form Ebene Media Foundation. Die ASF-Medienquelle verwendet den Splitter intern zum Analysieren von ASF-Dateien.

Das folgende Diagramm veranschaulicht die Generierung von Beispielen für eine ASF-Datei über den Splitter.

![Diagramm mit Beispiel Generierung einer ASF-Datei](images/1eb9789c-c586-4f44-b907-b086cf288cc1.gif)

Dieser Abschnitt enthält die folgenden Themen:



| Thema                                                                                                                        | BESCHREIBUNG                                                             |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Erstellen des ASF-Splitter Objekts](creating-the-asf-splitter-object.md)                                                     | So erstellen und initialisieren Sie den Splitter.                              |
| [Konfigurieren des ASF-Splitter Objekts](configuring-the-asf-splitter-object.md)                                               | Konfigurationseinstellungen für den Splitter.                                |
| [Erstellen von streambeispielen aus einem vorhandenen ASF-Datenobjekt](generating-stream-samples-from-an-existing-asf-data-object.md) | Analysieren des ASF-Datenobjekts und Generieren von Beispielcode Beispielen |



 

In der folgenden Tabelle sind die relevanten Datenobjekt Attribute aufgeführt.



| Attribut                                                                                                    | BESCHREIBUNG                                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**MF-,-Paket- \_ \_ \_ Dateieigenschaften \_ Pakete**](mf-pd-asf-fileproperties-packets-attribute.md)                   | Anzahl von Datenpaketen im ASF-Datenobjekt.                                                       |
| [**MF \_ PD \_ ASF \_ File Properties \_ Min. \_ Paket \_ Größe**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | Minimale Größe der Datenpakete in der Datei (in Bytes).                                              |
| [**\_maximal zulässige \_ \_ \_ \_ Paket \_ Größe für MF PD ASF File Properties**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | Maximale Größe der Datenpakete in der Datei (in Bytes)                                               |
| [**Länge der MF- \_ \_ \_ Daten \_ Länge von MF**](mf-pd-asf-data-length-attribute.md)                                         | Größe des ASF-Datenobjekts in Bytes.                                                               |
| [**\_ \_ \_ \_ Start \_ Offset für MF PD-ASF-Daten**](mf-pd-asf-data-start-offset-attribute.md)                            | Offset (in Bytes) zum ersten Datenpaket im ASF-Datenobjekt relativ zum Anfang der Datei. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wmcontainer-ASF-Komponenten](wmcontainer-asf-components.md)
</dt> <dt>

[Tutorial: Lesen einer ASF-Datei](tutorial--reading-an-asf-file.md)
</dt> <dt>

[Unterstützung von ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



