---
description: AVI-Splitter Filter
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: AVI-Splitter Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61b9a60c4c42aafa875c166ae08ccdf337793c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125318"
---
# <a name="avi-splitter-filter"></a>AVI-Splitter Filter

Der avi-Splitter Filter wird für die Wiedergabe von AVI-Dateien verwendet. Sie akzeptiert Daten im AVI-Format und teilt Sie zur weiteren Verarbeitung und/oder zum Rendering in die zugehörigen Datenströme auf.



|                                          |                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Iammediacontent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ipersistmediapropertybag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)                        |
| Eingabe-PIN-Medientypen                    | MediaType \_ Stream, mediasubtype \_ AVI                                                                                                                                |
| PIN-Eingabeschnittstellen                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                    |
| Ausgabe-PIN-Medientypen                   | Üblicherweise **mediaType- \_ Video** oder **mediaType \_ -Audiodatei**. Der genaue Typ hängt vom Inhalt der Datei ab, davon, ob die Datei komprimiert ist und welcher Codec verwendet wurde. |
| PIN-Schnittstellen                    | [**Imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)    |
| CLSID Filtern                             | CLSID- \_ avisplitter                                                                                                                                                  |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite.                                                                                                                                                   |
| Ausführbare Datei                               | quartz.dll                                                                                                                                                          |
| [Verdienst](merit.md)                       | Verdienst \_ Normal                                                                                                                                                       |
| [Filter Kategorie](filter-categories.md) | CLSID \_ legacyamfiltercategory                                                                                                                                       |



 

## <a name="remarks"></a>Bemerkungen

Dieser Filter ist in der Regel mit dem asynchronen [Datei Quell](file-source--async--filter.md) Filter in der eingabepin verbunden. Es kann eine Verbindung mit jedem Filter herstellen, dessen Ausgabepin [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) unterstützt und den richtigen Medientyp für die Eingabe-PIN des avi-Splitter Filters anbietet.

Die Ausgabe Pins für den avi-Splitter unterstützen die IPropertyBag:: Read-Methode zum Lesen von Eigenschaften aus einzelnen Streams. Derzeit ist die folgende Eigenschaft definiert.



| Eigenschaft | BESCHREIBUNG                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| name     | Gibt den Namen des Streams zurück, der aus dem Block `'strn'` in der AVI-Datei entnommen wurde. Wenn dieser Block nicht vorhanden ist, gibt die Read-Methode E \_ invalidArg zurück. |



 

Die IPropertyBag:: Write-Methode gibt "E Fail" zurück \_ . Der [AVI MUX](avi-mux-filter.md) -Filter unterstützt IPropertyBag:: Write zum Speichern von streameigenschaften in einer AVI-Datei.

Der avi-Splitter gestattet es nicht, dass Downstream-Filter Ihre eigene Zuweisung verwenden.

Die interanhaltedauer in der Datei bestimmt, wie viel Arbeitsspeicher der avi-Splitter für deren Verarbeitung zuweist. Eine Datei, die in einem Sekunde verschachtelt ist, benötigt viel mehr Arbeitsspeicher als eine Datei, deren Interleave-Dauer auf einen oder zwei Frames festgelegt ist. Auf modernen Computern ist dies in der Regel kein Problem, es sei denn, Sie führen mehrere Instanzen des avi-Splitter gleichzeitig aus.

### <a name="seeking"></a>Diejenigen

Wenn die Datei einen Videostream enthält, unterstützt der avi-Splitter das Suchen nach Frame Nummer. Um Frame basierte Suche zu aktivieren, rufen Sie [**imediaseeking:: settimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) im [Filter Graph-Manager](filter-graph-manager.md) mit dem Wert **Zeit \_ Format \_ Rahmen** auf.

Wenn die Datei einen Audiodatenstrom enthält, unterstützt der avi-Splitter das Suchen nach Stichproben Nummer. Zum Aktivieren der Beispiel basierten Suche wenden Sie [**settimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) im Filter Graph-Manager mit dem **\_ \_ Beispiel Wert Zeitformat** an.

In beiden Fällen muss die Ausgabe-PIN für diesen Datenstrom mit einem rendererfilter verbunden werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



