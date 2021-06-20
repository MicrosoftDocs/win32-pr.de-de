---
description: Implementieren Sie Unterstützung für die Medientypaushandlung als Teil des Schreibens eines Transformationsfilters. Der Medientyp beschreibt das Format der Daten.
ms.assetid: b2b5dafc-d38d-4ec3-a390-55229495b4f9
title: 'Schritt 3: Medientypaushandlung unterstützen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a23784e70330f751325fc5f780463d5a3904d20
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410043"
---
# <a name="step-3-support-media-type-negotiation"></a>Schritt 3: Medientypaushandlung unterstützen

Dies ist Schritt 3 des Tutorials [Schreiben von Transformationsfiltern](writing-transform-filters.md).

Wenn zwei Stecknadeln verbunden sind, müssen sie sich auf einen Medientyp für die Verbindung einigen. Der Medientyp beschreibt das Format der Daten. Ohne den Medientyp kann ein Filter eine Art von Daten liefern, nur um einen anderen Filter als etwas anderes behandeln zu lassen.

Der grundlegende Mechanismus zum Aushandeln von Medientypen ist die [**IPin::ReceiveConnection-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) Der Ausgabepin ruft diese Methode auf dem Eingabepin mit einem vorgeschlagenen Medientyp auf. Der Eingabepin akzeptiert die Verbindung oder lehnt sie ab. Wenn die Verbindung abgelehnt wird, kann der Ausgabepin einen anderen Medientyp ausprobieren. Wenn keine geeigneten Typen gefunden werden, schlägt die Verbindung fehl. Optional kann der Eingabepin über die [**IPin::EnumMediaTypes-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) eine Liste der bevorzugten Typen anordnen. Der Ausgabepin kann diese Liste verwenden, wenn medientypen vorgeschlagen werden, obwohl dies nicht der Fall ist.

Die **CTransformFilter-Klasse** implementiert wie folgt ein allgemeines Framework für diesen Prozess:

-   Der Eingabepin hat keine bevorzugten Medientypen. Es basiert vollständig auf dem Upstreamfilter, um den Medientyp vorzuschlagen. Für Videodaten ist dies sinnvoll, da der Medientyp die Bildgröße und die Bildfrequenz enthält. In der Regel müssen diese Informationen von einem Upstreamquellenfilter oder Parserfilter bereitgestellt werden. Im Fall von Audiodaten ist der Satz möglicher Formate kleiner, daher kann es für den Eingabepin praktisch sein, einige bevorzugte Typen zu bieten. Überschreiben Sie in diesem Fall [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) für den Eingabepin.
-   Wenn der Upstreamfilter einen Medientyp vorschlägt, ruft der Eingabepin die [**CTransformFilter::CheckInputType-Methode**](ctransformfilter-checkinputtype.md) auf, die den Typ akzeptiert oder ablehnt.
-   Der Ausgabepin wird nur verbunden, wenn der Eingabepin zuerst verbunden ist. Dieses Verhalten ist typisch für Transformationsfilter. In den meisten Fällen muss der Filter den Eingabetyp bestimmen, bevor er den Ausgabetyp festlegen kann.
-   Wenn der Ausgabepin eine Verbindung hergestellt hat, verfügt er über eine Liste von Medientypen, die er dem Downstreamfilter vorschlägt. Sie ruft die [**CTransformFilter::GetMediaType-Methode**](ctransformfilter-getmediatype.md) auf, um diese Liste zu generieren. Der Ausgabepin versucht auch alle Medientypen, die vom Downstreamfilter vorgeschlagen werden.
-   Um zu überprüfen, ob ein bestimmter Ausgabetyp mit dem Eingabetyp kompatibel ist, ruft der Ausgabepin die [**CTransformFilter::CheckTransform-Methode**](ctransformfilter-checktransform.md) auf.

Die drei **zuvor aufgeführten CTransformFilter-Methoden** sind reine virtuelle Methoden, sodass Ihre abgeleitete Klasse sie implementieren muss. Keine dieser Methoden gehört zu einer COM-Schnittstelle. sie sind einfach Teil der Implementierung, die von den Basisklassen bereitgestellt wird.

In den folgenden Abschnitten wird jede Methode ausführlicher beschrieben:

-   [Schritt 3A. Implementieren der CheckInputType-Methode](step-3a--implement-the-checkinputtype-method.md)
-   [Schritt 3B. Implementieren der GetMediaType-Methode](step-3b--implement-the-getmediatype-method.md)
-   [Schritt 3C. Implementieren der CheckTransform-Methode](step-3c--implement-the-checktransform-method.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Herstellen einer Verbindung mit Filtern](how-filters-connect.md)
</dt> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



