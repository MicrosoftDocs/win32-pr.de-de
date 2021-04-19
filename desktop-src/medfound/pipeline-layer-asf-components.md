---
description: Im Media Foundations-Pipeline Modell ist eine Medienquelle mit einer Transformation verbunden, die weiter mit einer Medien Senke verbunden ist.
ms.assetid: 55ab3a53-d9fd-438c-998c-8888f99958ce
title: Komponenten der Pipeline Schicht-ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3b6eb2d00404d193e50cebf174210a1c25655e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372915"
---
# <a name="pipeline-layer-asf-components"></a>Komponenten der Pipeline Schicht-ASF

In Media Foundation Pipeline Modell ist eine Medienquelle mit einer Transformation verbunden, die weiter mit einer Medien Senke verbunden ist. Die in der Quelle enthaltenen Daten fließen durch die Transformation und generieren Ausgabemedien Beispiele in der Senke für die Wiedergabe oder Codierung. Abhängig davon, ob die Anwendung ASF-Inhalte wiedergeben oder in eine ASF-Datei codieren möchte, muss die Anwendung die Pipeline anders erstellen.

Die folgenden Themen enthalten Informationen zu den Komponenten der Pipeline Schicht.

-   [ASF-Medienquelle](asf-media-source.md)
-   [Windows Media Encoder](windows-media-encoders.md)
-   [ASF-Medien senken](asf-media-sinks.md)

Die drei Hauptkomponenten einer ASF-Pipeline für die Wiedergabe lauten wie folgt:

-   Die ASF-Medienquelle wird von Media Foundation bereitgestellt, die eine ASF-Datei darstellt.
-   Audioresamplers, Grafik Bild-Resizers usw., (Transformation)
-   Audiodatei und Videorenderer (senken)

Weitere Informationen zum Erstellen einer Wiedergabe Pipeline finden Sie unter [Erstellen von Wiedergabe Topologien](creating-playback-topologies.md).

Die drei Hauptkomponenten einer ASF-Pipeline für die Codierung lauten wie folgt:

-   Medienquelle, die die Daten in einem Format darstellt, das konvertiert werden muss. Diese Komponente kann eine der Standard Medienquellen sein, die von Media Foundation bereitgestellt werden, oder eine benutzerdefinierte Quelle, die die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle verfügbar macht.
-   Windows Media Encoder (Transform), die die Formatkonvertierung durchführen.
-   Von Media Foundation bereitgestellte ASF-Medien senken, die in einer von der Anwendung angegebenen Ausgabedatei ASF-Objekte und Medien Beispiele schreiben.

Die Pipeline wird in einer Topologie dargestellt, und jedes Objekt in der Pipeline wird von einem topologieknoten dargestellt. Sowohl bei der Wiedergabe als auch bei der Codierung werden alle Pipeline Vorgänge von der Medien Sitzung verarbeitet. Eine der Zuständigkeiten der Medien Sitzung besteht darin, sicherzustellen, dass die Pipeline über alle Komponenten verfügt, die zum Generieren der Ausgabe erforderlich sind. Wenn sich z. b. in einer Codierungs Pipeline das Format der Audioquelle von dem Zielformat unterscheidet, fügt die Medien Sitzung zusätzliche Transformations Komponenten wie den Resampler ein, der die entsprechenden Abtastraten Konvertierungen ausführt. Die Datenflusssteuerung durch die Pipeline wird auch von der Medien Sitzung verwaltet. In einem Wiedergabe Szenario, in dem die Medien Sitzung gestartet wird, sendet die Medien Sitzung Beispiele an SAR und EVR, das Sie auf dem Ausgabegerät rendert. Bei der Codierung beginnt das Starten der Medien Sitzung mit dem Codierungs Vorgang. Die Sitzung benachrichtigt die Anwendung asynchron, wenn die Codierung vollständig ist.

Das folgende Thema enthält Schritt-für-Schritt-Anleitungen zum Verwenden der Pipeline Schicht Komponenten zum Erstellen einer Codierungs Topologie. Komponenten zum Lesen und Schreiben von ASF-Dateien.

-   [Tutorial: 1-Pass-Windows-Medien Codierung](tutorial--1-pass-windows-media-encoding.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützung von ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



