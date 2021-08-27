---
description: Implementieren Sie Unterstützung für die Medientypaushandlung als Teil des Schreibens eines Transformationsfilters. Der Medientyp beschreibt das Format der Daten.
ms.assetid: b2b5dafc-d38d-4ec3-a390-55229495b4f9
title: 'Schritt 3: Medientypaushandlung unterstützen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1558d5b1a7fd9db41fef7e5a9818d93c306f4f15f42099d4cb88f66b34725660
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051470"
---
# <a name="step-3-support-media-type-negotiation"></a>Schritt 3: Medientypaushandlung unterstützen

Dies ist Schritt 3 des Tutorials Schreiben von [Transformationsfiltern.](writing-transform-filters.md)

Wenn zwei Pins eine Verbindung herstellen, müssen sie sich auf einen Medientyp für die Verbindung einigen. Der Medientyp beschreibt das Format der Daten. Ohne den Medientyp kann ein Filter eine Art von Daten liefern, nur um einen anderen Filter als etwas anderes behandeln zu lassen.

Der grundlegende Mechanismus zum Aushandeln von Medientypen ist die [**IPin::ReceiveConnection-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) Der Ausgabepin ruft diese Methode auf dem Eingabepin mit einem vorgeschlagenen Medientyp auf. Der Eingabepin akzeptiert die Verbindung oder lehnt sie ab. Wenn die Verbindung abgelehnt wird, kann der Ausgabepin einen anderen Medientyp ausprobieren. Wenn keine geeigneten Typen gefunden werden, schlägt die Verbindung fehl. Optional kann der Eingabepin über die [**IPin::EnumMediaTypes-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) eine Liste von Typen ankündigen, die er bevorzugt. Der Ausgabepin kann diese Liste verwenden, wenn er Medientypen vorschlägt, obwohl dies nicht der Grund ist.

Die **CTransformFilter-Klasse** implementiert wie folgt ein allgemeines Framework für diesen Prozess:

-   Der Eingabepin hat keine bevorzugten Medientypen. Es basiert vollständig auf dem Upstreamfilter, um den Medientyp vorzuschlagen. Für Videodaten ist dies sinnvoll, da der Medientyp die Bildgröße und die Bildfrequenz enthält. In der Regel müssen diese Informationen von einem Upstreamquellfilter oder Parserfilter bereitgestellt werden. Bei Audiodaten ist der Satz möglicher Formate kleiner, sodass es für den Eingabepin praktisch sein kann, einige bevorzugte Typen anzubieten. In diesem Fall überschreiben [**Sie CBasePin::GetMediaType**](cbasepin-getmediatype.md) auf dem Eingabepin.
-   Wenn der Upstreamfilter einen Medientyp vorschlägt, ruft der Eingabepin die [**CTransformFilter::CheckInputType-Methode**](ctransformfilter-checkinputtype.md) auf, die den Typ akzeptiert oder ablehnt.
-   Der Ausgabepin stellt nur dann eine Verbindung her, wenn der Eingabepin zuerst verbunden ist. Dieses Verhalten ist typisch für Transformationsfilter. In den meisten Fällen muss der Filter den Eingabetyp bestimmen, bevor er den Ausgabetyp festlegen kann.
-   Wenn der Ausgabepin eine Verbindung herstellt, verfügt er über eine Liste von Medientypen, die er dem Downstreamfilter vorschlägt. Sie ruft die [**CTransformFilter::GetMediaType-Methode**](ctransformfilter-getmediatype.md) auf, um diese Liste zu generieren. Der Ausgabepin testet auch alle Medientypen, die der Downstreamfilter vorschlägt.
-   Um zu überprüfen, ob ein bestimmter Ausgabetyp mit dem Eingabetyp kompatibel ist, ruft der Ausgabepin die [**CTransformFilter::CheckTransform-Methode**](ctransformfilter-checktransform.md) auf.

Die drei zuvor aufgeführten **CTransformFilter-Methoden** sind reine virtuelle Methoden, sodass ihre abgeleitete Klasse sie implementieren muss. Keine dieser Methoden gehört zu einer COM-Schnittstelle. sie sind einfach Teil der Implementierung, die von den Basisklassen bereitgestellt wird.

In den folgenden Abschnitten werden die einzelnen Methoden ausführlicher beschrieben:

-   [Schritt 3A: Implementieren der CheckInputType-Methode](step-3a--implement-the-checkinputtype-method.md)
-   [Schritt 3B: Implementieren der GetMediaType-Methode](step-3b--implement-the-getmediatype-method.md)
-   [Schritt 3C: Implementieren der CheckTransform-Methode](step-3c--implement-the-checktransform-method.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[So Verbinden Filter](how-filters-connect.md)
</dt> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



