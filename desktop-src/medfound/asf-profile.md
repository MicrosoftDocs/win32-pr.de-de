---
description: In diesem Thema wird beschrieben, wie Sie mit ASF-Profilen in Microsoft Media Foundation.
ms.assetid: 03a0981b-29c3-450d-aa58-bc56a76e6cb6
title: ASF-Profil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d38d5d2c869bd8af61289fa15361d216f686abac4eaa366b3c036f40338d355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035522"
---
# <a name="asf-profile"></a>ASF-Profil

In diesem Thema wird beschrieben, wie Sie mit ASF-Profilen in Microsoft Media Foundation.

Eine ASF-Datei (Advanced Systems Format) enthält einen oder mehrere Streams. Für jeden Stream enthält der ASF-Header einen Streameigenschaftenheader, der den Stream beschreibt. Auf der [WMContainer-Ebene](wmcontainer-asf-components.md) werden die folgenden Objekte verwendet, um die Eigenschaften der ASF-Streams zu festlegen oder zu lesen:

-   *ASF-Profilobjekt:* Beschreibt die Streams und ihre Beziehungen untereinander. Das ASF-Profilobjekt macht die [**IMFASFProfile-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) verfügbar.
-   *Streamkonfigurationsobjekt:* Beschreibt einen Stream. Das Streamkonfigurationsobjekt enthält einen Medientyp, der das Format des Streams beschreibt. Bei Audio- und Videostreams beschreibt der Medientyp genau, wie der Stream konfiguriert ist, und wird von Codecs verwendet, die den Stream codieren oder decodieren. Das Streamkonfigurationsobjekt macht die [**IMFASFStreamConfig-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) verfügbar. Ein gültiges ASF-Profil enthält mindestens ein Streamkonfigurationsobjekt.
-   *Objekt für gegenseitigen* Ausschluss: Beschreibt mehrere Streams, die nicht gleichzeitig gelesen werden sollen. Ein objektseitiger Ausschluss macht die [**IMFASFMutualExclusion-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) verfügbar. Ein ASF-Profil enthält null oder mehr gegenseitige Ausschlussobjekte.

Das folgende Diagramm zeigt die Beziehung zwischen dem ASF-Profil und den im Profil enthaltenen Objekten.

![Strukturdiagramm eines asf-Profilknotens mit untergeordneten Knoten für die Streamkonfiguration der erste verweist auf den Medientyp, die nächsten zwei auf gegenseitigen Ausschluss.](images/asf-components02.png)

Für die Wiedergabe wird das ASF-Profil verwendet, um die Streams zu aufzählen und die Streamformate zu suchen. Für die Codierung wird das ASF-Profil verwendet, um die Streams in der Zieldatei zu konfigurieren.

Das ASF-Profil wird auch zum Konfigurieren der [ASF-Mediensenke verwendet.](asf-media-sinks.md) Für jeden Stream im ASF-Profil erstellt die ASF-Mediensenke eine entsprechende Streamsenke.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                           | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Erstellen eines ASF-Profils](creating-an-asf-profile.md)<br/>                               | Beschreibt, wie ein ASF-Profilobjekt erstellt wird.<br/>          |
| [Erstellen und Konfigurieren von ASF-Streams](creating-and-configuring-asf-streams.md)<br/>     | Beschreibt, wie Einem ASF-Profil Streams hinzugefügt werden.<br/>         |
| [Verwenden des gegenseitigen Ausschlusses für ASF-Streams](using-mutual-exclusion-for-asf-streams.md)<br/> | Beschreibt, wie ASF-Streams gegenseitige Ausschlüsse hinzugefügt werden. <br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medientypen](media-types.md)
</dt> <dt>

[Tutorial: 1-Pass-Windows-Mediencodierung](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[Tutorial: Schreiben einer WMA-Datei mit CBR-Codierung](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> <dt>

[WMContainer-ASF-Komponenten](wmcontainer-asf-components.md)
</dt> </dl>

 

 




