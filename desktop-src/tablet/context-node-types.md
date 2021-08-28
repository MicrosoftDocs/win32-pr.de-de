---
description: Diese Konstanten definieren Werte, die den Typ von IContextNode-Objekten angeben.
ms.assetid: 333db79e-f503-4545-84fd-7c1a39a96728
title: Kontextknotentypen (Iaguid.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_CNT_ANALYSISHINT
- GUID_CNT_CUSTOMRECOGNIZER
- GUID_CNT_IMAGE
- GUID_CNT_INKBULLET
- GUID_CNT_INKDRAWING
- GUID_CNT_INKWORD
- GUID_CNT_LINE
- GUID_CNT_OBJECT
- GUID_CNT_PARAGRAPH
- GUID_CNT_ROOT
- GUID_CNT_TEXTWORD
- GUID_CNT_UNCLASSIFIEDINKNODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 2bb2064cc72b398d290fa78606b31bd37208535e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473886"
---
# <a name="context-node-types"></a>Kontextknotentypen

Diese Konstanten definieren Werte, die den Typ von [**IContextNode-Objekten**](icontextnode.md) angeben.




| Konstante/Wert | BESCHREIBUNG | 
|----------------|-------------|
| <span id="GUID_CNT_ANALYSISHINT"></span><span id="guid_cnt_analysishint"></span><dl><dt><strong>GUID_CNT_ANALYSISHINT</strong></dt><dt>(AnalysisHint)</dt></dl> | Stellt einen Knoten dar, der zusätzliche Kontextinformationen für einen Bereich enthält, den <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> zur Verbesserung seiner Analyse verwendet.<br /> | 
| <span id="GUID_CNT_CUSTOMRECOGNIZER"></span><span id="guid_cnt_customrecognizer"></span><dl><dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt><dt>(CustomRecognizer)</dt></dl> | Stellt einen Knoten dar, der für einen einzelnen Erkennungsvorgang verwendet wird.<br /> Alle Striche und Knoten innerhalb eines benutzerdefinierten Erkennungsknotens werden von einem unabhängigen Erkennungsvorgang erkannt und nicht vom <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>analysiert.<br /> Ein benutzerdefinierter Erkennungsknoten muss das direkte untergeordnete Element des Stammknotens des Ink-Analysetools sein.<br /> Ein benutzerdefinierter Erkennungsknoten kann die folgenden Typen von untergeordneten Elementen enthalten:<br /><ul><li>Eine beliebige Anzahl von UnclassifiedInk-Knoten.</li><li>Eine beliebige Anzahl von Objektknoten.</li><li>Eine beliebige Anzahl von Linienknoten.</li><li>Eine beliebige Anzahl von InkWord-Knoten.</li><li>Eine beliebige Anzahl von Knoten mit einem unbekannten GUID-Wert.</li></ul> | 
| <span id="GUID_CNT_IMAGE"></span><span id="guid_cnt_image"></span><dl><dt><strong>GUID_CNT_IMAGE</strong></dt><dt>(Abbildung)</dt></dl> | Stellt einen Knoten für einen zweidimensionalen Bereich dar, in dem alle Nicht-Ink-Bilder im Dokument vorhanden sein können.<br /> <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> erzeugt keine Imageknoten. Verwenden Sie <a href="icontextnode-createsubnode.md"><strong>IContextNode::CreateSubNode,</strong></a> um der Kontextknotenstruktur einen Imageknoten hinzuzufügen. <strong>Der IInkAnalyzer</strong> verwendet dann die vom Imageknoten definierten Bereiche, um zu bestimmen, ob freihand ein Freihandbild das Nicht-Freihandbild kommentiert.<br /> Ein Imageknoten darf keine untergeordneten Elemente enthalten.<br /> | 
| <span id="GUID_CNT_INKBULLET"></span><span id="guid_cnt_inkbullet"></span><dl><dt><strong>GUID_CNT_INKBULLET</strong></dt><dt>(InkBullet)</dt></dl> | InkBullet ContextNodeType stellt eine Auflistung von Strichen dar, die einen Aufzählungszeichen in einer Aufzählung bilden.<br /> Ein ContextNode vom Typ InkBullet darf keine untergeordneten Elemente aufweisen. Es kann nur ein untergeordnetes Element eines Paragraph ContextNode sein. Nur ein InkBullet kann in einem einzelnen Paragraph ContextNode angezeigt werden.<br /> | 
| <span id="GUID_CNT_INKDRAWING"></span><span id="guid_cnt_inkdrawing"></span><dl><dt><strong>GUID_CNT_INKDRAWING</strong></dt><dt>(InkDrawing)</dt></dl> | Stellt einen Knoten für eine Auflistung von Strichen dar, die eine Zeichnung bilden.<br /> Zeichnungen sind Striche, die als Formen oder abstrakte Striche bestimmt werden. Es handelt sich im Allgemeinen um Striche, die nicht als Schreiben von Strichen klassifiziert sind.<br /> Ein Ink-Zeichnungsknoten darf keine untergeordneten Elemente enthalten.<br /> | 
| <span id="GUID_CNT_INKWORD"></span><span id="guid_cnt_inkword"></span><dl><dt><strong>GUID_CNT_INKWORD</strong></dt><dt>(InkWord)</dt></dl> | Stellt einen Knoten für eine Auflistung von Strichen dar, die eine logische Gruppierung bilden, um ein erkennbares Wort zu bilden.<br /> Ein Ink-Wortknoten darf keine untergeordneten Elemente enthalten.<br /> | 
| <span id="GUID_CNT_LINE"></span><span id="guid_cnt_line"></span><dl><dt><strong>GUID_CNT_LINE</strong></dt><dt>(Zeile)</dt></dl> | Stellt einen Knoten für eine Wortzeile dar.<br /> Ein Linienknoten kann die folgenden Typen von untergeordneten Elementen enthalten:<br /><ul><li>Eine beliebige Anzahl von Ink-Wortknoten.</li><li>Eine beliebige Anzahl von Textwortknoten.</li><li>Eine beliebige Anzahl von Knoten mit einem unbekannten <strong>GUID-Wert.</strong></li></ul> | 
| <span id="GUID_CNT_OBJECT"></span><span id="guid_cnt_object"></span><dl><dt><strong>GUID_CNT_OBJECT</strong></dt><dt>(Objekt)</dt></dl> | Stellt einen Knoten für ein Objekt dar, das von einer benutzerdefinierten Objekterkennung zurückgegeben wird.<br /> Ein Objektknoten darf keine untergeordneten Elemente enthalten.<br /> Nur benutzerdefinierte Erkennungsknoten können Objektknoten enthalten.<br /> | 
| <span id="GUID_CNT_PARAGRAPH"></span><span id="guid_cnt_paragraph"></span><dl><dt><strong>GUID_CNT_PARAGRAPH</strong></dt><dt>(Absatz)</dt></dl> | Stellt einen Knoten für eine Auflistung von Knoten dar, die eine logische Gruppierung von Zeilen bilden.<br /> Die genaue Definition eines Absatzes wird durch die analysierenden Engines bestimmt. Im Allgemeinen enthält ein Absatz Zeilengruppen, die zusammenfließen würden, wenn die Größe des Felds, das die Zeilen enthält, geändert würde.<br /> Ein Absatzknoten kann die folgenden Typen von untergeordneten Elementen enthalten:<br /><ul><li>Eine beliebige Anzahl von Ink-Aufzählungsknoten.</li><li>Eine beliebige Anzahl von Zeilenknoten.</li><li>Eine beliebige Anzahl von Knoten mit einem unbekannten <strong>GUID-Wert.</strong></li></ul> | 
| <span id="GUID_CNT_ROOT"></span><span id="guid_cnt_root"></span><dl><dt><strong>GUID_CNT_ROOT</strong></dt><dt>(Root)</dt></dl> | Stellt einen Knoten für den obersten Knoten einer Knotenstruktur dar, der die Ergebnisse der Ink-Analyse beschreibt.<br /> Stammknoten werden im Allgemeinen von der <a href="iinkanalyzer-getrootnode.md"><strong>IInkAnalyzer::GetRootNode-Methode</strong></a> abgerufen.<br /> Ein Stammknoten kann die folgenden Typen von untergeordneten Elementen enthalten:<br /><ul><li>Eine beliebige Anzahl von Analysehinweisknoten.</li><li>Eine beliebige Anzahl von benutzerdefinierten Erkennungsknoten.</li><li>Eine beliebige Anzahl von Imageknoten.</li><li>Eine beliebige Anzahl von Ink-Zeichnungsknoten.</li><li>Eine beliebige Anzahl von Schreibbereichsknoten.</li><li>Eine beliebige Anzahl von nicht klassifizierten Ink-Knoten.</li><li>Eine beliebige Anzahl von Knoten mit einem unbekannten <strong>GUID-Wert.</strong></li></ul> | 
| <span id="GUID_CNT_TEXTWORD"></span><span id="guid_cnt_textword"></span><dl><dt><strong>GUID_CNT_TEXTWORD</strong></dt><dt>(TextWord)</dt></dl> | Stellt einen Knoten für den zweidimensionalen Bereich dar, in dem beliebiger Nicht-Ink-Text im Dokument vorhanden sein kann.<br /> <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> erzeugt keine Textwortknoten. Verwenden Sie <a href="icontextnode-createsubnode.md"><strong>IContextNode::CreateSubNode,</strong></a> um der Kontextknotenstruktur einen Textwortknoten hinzuzufügen. <strong>Der IInkAnalyzer</strong> verwendet dann die bereiche, die vom Textwortknoten definiert werden, um zu bestimmen, ob Freihandnoten den Nicht-Freihandtext kommentieren.<br /> Zukünftige Erkennungen können den durch einen Textwortknoten definierten Bereich verwenden, um zu bestimmen, ob eine Ink-Struktur das Nicht-Ink-Wort kommentiert.<br /> Ein Textwortknoten darf keine untergeordneten Elemente enthalten.<br /> | 
| <span id="GUID_CNT_UNCLASSIFIEDINKNODE"></span><span id="guid_cnt_unclassifiedinknode"></span><dl><dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt><dt>(UnclassifiedInk)</dt></dl> | Stellt einen Knoten für Striche dar, die noch nicht klassifiziert oder erkannt wurden.<br /> Ein nicht klassifizierter Ink-Knoten darf keine untergeordneten Elemente enthalten.<br /> | 




## <a name="remarks"></a>Hinweise

Weitere Informationen zu den verschiedenen Kontextknotentypen finden Sie unter Übersicht über die [Ink-Analyse.](ink-analysis-overview.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                           |
| Header<br/>                   | <dl> <dt>Iaguid.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IContextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**IContextNode::CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[**IContextNode::GetType**](icontextnode-gettype.md)
</dt> <dt>

[**IInkAnalyzer::CreateAnalysisHint-Methode**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer::CreateCustomRecognizer-Methode**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesOfType-Methode**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesOfTypeForStrokes-Methode**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesOfTypeInSubTree-Methode**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




