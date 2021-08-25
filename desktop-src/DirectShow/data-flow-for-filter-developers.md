---
description: Data Flow für Filterentwickler
ms.assetid: cc7378c8-e268-4caa-98eb-6dc9c3b5bcad
title: Data Flow für Filterentwickler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77ced9507856d7a6b8aea2acaea86c20b393b8d937ab4427bf522596a29ba690
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749370"
---
# <a name="data-flow-for-filter-developers"></a>Data Flow für Filterentwickler

In diesem Abschnitt wird ausführlich beschrieben, wie Daten durch das Filterdiagramm bewegt werden. Der Schwerpunkt liegt auf dem lokalen Speichertransport mithilfe der [**IMemInputPin-**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) oder [**IAsyncReader-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) Es richtet sich an Entwickler, die eigene benutzerdefinierte Filter schreiben. Eine allgemeine Einführung in die Verarbeitung des Datenflusses durch Microsoft DirectShow finden Sie unter [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).

Viele Daten werden durch ein Filterdiagramm bewegt. Sie fällt ungefähr in zwei Kategorien: Mediendaten und Steuerungsdaten. Im Allgemeinen werden Mediendaten nachgelagert und steuern, dass Daten vorgelagert werden. Mediendaten umfassen die Videoframes, Audiobeispiele, MPEG-Pakete usw., aus denen ein Stream besteht, aber auch Leerungsbefehle, End-of-Stream-Benachrichtigungen und andere Daten, die mit dem Stream übertragen werden. Steuerungsdaten sind nicht Teil des Medienstreams. Beispiele für Steuerungsdaten sind Qualitätskontrollanforderungen und Suchbefehle.

Dieser Abschnitt enthält die folgenden Artikel.

-   [Bereitstellen von Beispielen](delivering-samples.md)
-   [Verarbeiten von Daten](processing-data.md)
-   [End-of-Stream-Benachrichtigungen](end-of-stream-notifications.md)
-   [Neue Segmente](new-segments.md)
-   [Spülung](flushing.md)
-   [Suchen](seeking.md)
-   [Dynamische Formatänderungen](dynamic-format-changes.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Qualitätskontrollverwaltung](quality-control-management.md)
</dt> <dt>

[Threads und kritische Abschnitte](threads-and-critical-sections.md)
</dt> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



