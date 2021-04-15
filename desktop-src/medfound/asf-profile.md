---
description: In diesem Thema wird beschrieben, wie Sie in Microsoft Media Foundation mit ASF-Profilen arbeiten.
ms.assetid: 03a0981b-29c3-450d-aa58-bc56a76e6cb6
title: ASF-Profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616670e7de68fd73c168c474544fc6236f1586e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524659"
---
# <a name="asf-profile"></a>ASF-Profil

In diesem Thema wird beschrieben, wie Sie in Microsoft Media Foundation mit ASF-Profilen arbeiten.

Eine ASF-Datei (Advanced Systems Format) enthält mindestens einen Stream. Für jeden Stream enthält der ASF-Header einen Stream Properties-Header, der den Datenstrom beschreibt. Auf der [wmcontainer](wmcontainer-asf-components.md) -Ebene werden die folgenden Objekte verwendet, um die Eigenschaften der ASF-Streams festzulegen oder zu lesen:

-   *ASF-Profil* Objekt: Beschreibt die Streams und ihre Beziehungen untereinander. Das ASF-Profil Objekt macht die [**imfasf profile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) -Schnittstelle verfügbar.
-   *Stream Configuration* Object: Beschreibt einen Stream. Das Datenstrom-Konfigurationsobjekt enthält einen Medientyp, der das Format des Streams beschreibt. Für Audiodaten und Videostreams beschreibt der Medientyp genau, wie der Stream konfiguriert ist, und wird von Codecs verwendet, die den Datenstrom codieren oder decodieren. Das Datenstrom-Konfigurationsobjekt macht die [**imfasf streamconfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) -Schnittstelle verfügbar. Ein gültiges ASF-Profil enthält mindestens ein Datenstrom-Konfigurationsobjekt.
-   *Gegenseitiges Ausschluss* Objekt: Beschreibt mehrere Datenströme, die nicht gleichzeitig gelesen werden sollen. Ein gegenseitiges Ausschluss Objekt macht die [**imfassmutualexclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) -Schnittstelle verfügbar. Ein ASF-Profil enthält keine oder mehrere gegenseitige Ausschluss Objekte.

Das folgende Diagramm zeigt die Beziehung zwischen dem ASF-Profil und den Objekten, die im Profil enthalten sind.

![Strukturdiagramm eines Knoten vom Typ "ASF-Profil" mit untergeordneten Datenstrom Konfigurations Knoten; der erste Punkt zeigt den Medientyp, die nächsten zwei für den gegenseitigen Ausschluss.](images/asf-components02.png)

Zur Wiedergabe wird das ASF-Profil zum Auflisten der Streams und zum Suchen der Streamformate verwendet. Bei der Codierung wird das ASF-Profil zum Konfigurieren der Streams in der Zieldatei verwendet.

Das ASF-Profil wird auch zum Konfigurieren der [ASF-Medien Senke](asf-media-sinks.md)verwendet. Für jeden Datenstrom im ASF-Profil erstellt die ASF-Medien Senke eine entsprechende streamsenke.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                           | BESCHREIBUNG                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Erstellen eines ASF-Profils](creating-an-asf-profile.md)<br/>                               | Beschreibt, wie ein ASF-Profil Objekt erstellt wird.<br/>          |
| [Erstellen und Konfigurieren von ASF-Streams](creating-and-configuring-asf-streams.md)<br/>     | Beschreibt, wie Datenströme einem ASF-Profil hinzugefügt werden.<br/>         |
| [Verwenden des gegenseitigen Ausschlusses für ASF-Streams](using-mutual-exclusion-for-asf-streams.md)<br/> | Beschreibt das Hinzufügen von gegenseitigen Ausschlüssen zu ASF-Streams. <br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medientypen](media-types.md)
</dt> <dt>

[Tutorial: 1-Pass-Windows-Medien Codierung](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[Tutorial: Schreiben einer WMA-Datei mithilfe der CBR-Codierung](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> <dt>

[Wmcontainer-ASF-Komponenten](wmcontainer-asf-components.md)
</dt> </dl>

 

 




