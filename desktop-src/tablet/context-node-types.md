---
description: Diese Konstanten definieren Werte, die den Typ von icontextnode-Objekten angeben.
ms.assetid: 333db79e-f503-4545-84fd-7c1a39a96728
title: Kontext Knoten Typen (iaguid. h)
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
ms.openlocfilehash: 918b7cf818ebcedc98f45bff7c41ee66ad4d1592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127816"
---
# <a name="context-node-types"></a>Kontext Knoten Typen

Diese Konstanten definieren Werte, die den Typ von [**icontextnode**](icontextnode.md) -Objekten angeben.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante/Wert</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_ANALYSISHINT"></span><span id="guid_cnt_analysishint"></span><dl> <dt><strong>GUID_CNT_ANALYSISHINT</strong></dt> <dt>(AnalysisHint)</dt> </dl></td>
<td style="text-align: left;">Stellt einen Knoten dar, der zusätzliche Kontextinformationen für einen Bereich enthält, den der <a href="iinkanalyzer.md"><strong>iinkanalyzer</strong></a> verwendet, um die Analyse zu verbessern.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_CUSTOMRECOGNIZER"></span><span id="guid_cnt_customrecognizer"></span><dl> <dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt> <dt>(customerkenzer)</dt> </dl></td>
<td style="text-align: left;">Stellt einen Knoten dar, der für einen einzelnen Erkennungs Vorgang verwendet wird.<br/> Alle Striche und Knoten, die sich in einem benutzerdefinierten Erkennungs Knoten befinden, werden von einem unabhängigen Erkennungs Vorgang erkannt und nicht von <a href="iinkanalyzer.md"><strong>iinkanalyzer</strong></a>analysiert.<br/> Ein benutzerdefinierter Erkennungs Knoten muss das direkt untergeordnete Element des Stamm Knotens von Ink Analyzer sein.<br/> Ein benutzerdefinierter Erkennungs Knoten kann die folgenden Typen von untergeordneten Elementen enthalten:<br/>
<ul>
<li>Eine beliebige Anzahl von unclassimeedink-Knoten.</li>
<li>Eine beliebige Anzahl von Objekt Knoten.</li>
<li>Eine beliebige Anzahl von Zeilen Knoten.</li>
<li>Beliebig viele inkWord-Knoten.</li>
<li>Eine beliebige Anzahl von Knoten mit einem unbekannten GUID-Wert.</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_IMAGE"></span><span id="guid_cnt_image"></span><dl> <dt><strong>GUID_CNT_IMAGE</strong></dt> <dt>(Bild)</dt> </dl></td>
<td style="text-align: left;">Stellt einen Knoten für einen zweidimensionalen Bereich dar, in dem alle Non-Ink-Bilder im Dokument vorhanden sein können.<br/> Der <a href="iinkanalyzer.md"><strong>iinkanalyzer</strong></a> erzeugt keine Bild Knoten. Verwenden Sie <a href="icontextnode-createsubnode.md"><strong>icontextnode:: kreatesubnode</strong></a> , um der Kontext Knoten Struktur einen Bild Knoten hinzuzufügen. Der <strong>iinkanalyzer</strong> verwendet dann die vom Knoten Image definierten Bereiche, um zu bestimmen, ob frei Hand Eingaben das nicht-frei Hand Bild kommentieren.<br/> Ein Bild Knoten darf keine untergeordneten Elemente aufweisen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKBULLET"></span><span id="guid_cnt_inkbullet"></span><dl> <dt><strong>GUID_CNT_INKBULLET</strong></dt> <dt>(InkBullet)</dt> </dl></td>
<td style="text-align: left;">Der InkBullet ContextNodeType stellt eine Auflistung von Strichen dar, die ein Aufzählungs Zeichen in einer Aufzählung bilden.<br/> Ein ContextNode des Typs "InkBullet" kann keine untergeordneten Elemente aufweisen. Es kann nur ein untergeordnetes Element eines Absatz-ContextNode sein. Nur eine InkBullet kann in einem einzelnen Absatz ContextNode angezeigt werden.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_INKDRAWING"></span><span id="guid_cnt_inkdrawing"></span><dl> <dt><strong>GUID_CNT_INKDRAWING</strong></dt> <dt>(InkDrawing)</dt> </dl></td>
<td style="text-align: left;">Stellt einen Knoten für eine Auflistung von Strichen dar, die eine Zeichnung bilden.<br/> Zeichnungen sind Striche, die als Formen oder abstrakte Skizzen bestimmt werden. Dabei handelt es sich im Allgemeinen um alle Striche, die nicht als Schreibvorgänge klassifiziert werden.<br/> Ein Ink-Zeichnungs Knoten darf keine untergeordneten Elemente aufweisen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKWORD"></span><span id="guid_cnt_inkword"></span><dl> <dt><strong>GUID_CNT_INKWORD</strong></dt> <dt>(InkWord)</dt> </dl></td>
<td style="text-align: left;">Stellt einen Knoten für eine Auflistung von Strichen dar, die eine logische Gruppierung zum bilden eines erkennbaren Worts bilden.<br/> Ein Ink Word-Knoten darf keine untergeordneten Elemente enthalten.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_LINE"></span><span id="guid_cnt_line"></span><dl> <dt><strong>GUID_CNT_LINE</strong></dt> <dt>(Zeile)</dt> </dl></td>
<td style="text-align: left;">Stellt einen Knoten für eine Zeile von Wörtern dar.<br/> Ein Zeilen Knoten kann die folgenden Typen von untergeordneten Elementen enthalten:<br/>
<ul>
<li>Beliebig viele frei Hand Wort Knoten.</li>
<li>Eine beliebige Anzahl von Text Word-Knoten.</li>
<li>Eine beliebige Anzahl von Knoten mit einem unbekannten <strong>GUID</strong> -Wert.</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_OBJECT"></span><span id="guid_cnt_object"></span><dl> <dt><strong>GUID_CNT_OBJECT</strong></dt> <dt>(Objekt)</dt> </dl></td>
<td style="text-align: left;">Stellt einen Knoten für ein Objekt dar, das von einem &quot; benutzerdefinierten Objekterkennungsmodul zurückgegeben wird &quot; .<br/> Ein Objekt Knoten kann keine untergeordneten Elemente enthalten.<br/> Nur benutzerdefinierte Erkennungs Knoten können Objekt Knoten enthalten.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_PARAGRAPH"></span><span id="guid_cnt_paragraph"></span><dl> <dt><strong>GUID_CNT_PARAGRAPH</strong></dt> <dt>(Absatz)</dt> </dl></td>
<td style="text-align: left;">Stellt einen Knoten für eine Auflistung von Knoten dar, die eine logische Gruppierung von Zeilen bilden.<br/> Die genaue Definition eines Absatzes wird von den analysierten Engines bestimmt. Im Allgemeinen enthält ein Absatz Gruppen von Zeilen, die sich wiederholen, wenn das Feld, das die Zeilen enthält, geändert wurde.<br/> Ein Absatz Knoten kann die folgenden Typen von untergeordneten Elementen enthalten:<br/>
<ul>
<li>Beliebig viele Freihand-Aufzählungs Knoten.</li>
<li>Eine beliebige Anzahl von Zeilen Knoten.</li>
<li>Eine beliebige Anzahl von Knoten mit einem unbekannten <strong>GUID</strong> -Wert.</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_ROOT"></span><span id="guid_cnt_root"></span><dl> <dt><strong>GUID_CNT_ROOT</strong></dt> <dt>(root)</dt> </dl></td>
<td style="text-align: left;">Stellt einen Knoten für den obersten Knoten einer Struktur von Knoten dar, die die Ergebnisse der frei Hand Analyse beschreiben.<br/> Stamm Knoten werden in der Regel von der <a href="iinkanalyzer-getrootnode.md"><strong>Methoden Methode iinkanalyzer:: GetRootNode</strong></a> abgerufen.<br/> Ein Stamm Knoten kann die folgenden Typen von untergeordneten Elementen enthalten:<br/>
<ul>
<li>Eine beliebige Anzahl von Analyse Hinweis Knoten.</li>
<li>Eine beliebige Anzahl von benutzerdefinierten Erkennungs Knoten.</li>
<li>Beliebig viele Bild Knoten.</li>
<li>Eine beliebige Anzahl von frei Hand Zeichnungs Knoten.</li>
<li>Eine beliebige Anzahl von Schreib Regions Knoten.</li>
<li>Eine beliebige Anzahl von nicht klassifizierten frei Hand Knoten.</li>
<li>Eine beliebige Anzahl von Knoten mit einem unbekannten <strong>GUID</strong> -Wert.</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_TEXTWORD"></span><span id="guid_cnt_textword"></span><dl> <dt><strong>GUID_CNT_TEXTWORD</strong></dt> <dt>(textword)</dt> </dl></td>
<td style="text-align: left;">Stellt einen Knoten für den zweidimensionalen Bereich dar, in dem ein nicht frei Hand Text im Dokument vorhanden sein kann.<br/> Der <a href="iinkanalyzer.md"><strong>iinkanalyzer</strong></a> erzeugt keine Text Wort Knoten. Verwenden Sie <a href="icontextnode-createsubnode.md"><strong>icontextnode:: kreatesubnode</strong></a> , um der Kontext Knoten Struktur einen Text Wort Knoten hinzuzufügen. Der <strong>iinkanalyzer</strong> verwendet dann die vom Text Word-Knoten definierten Regionen, um zu bestimmen, ob frei Hand Eingaben den nicht frei Hand Text kommentieren.<br/> Zukünftige erkenungen können die von einem Text Word-Knoten definierte Region verwenden, um zu bestimmen, ob frei Hand Eingaben das nicht frei Hand Wort kommentieren.<br/> Ein Text Word-Knoten darf keine untergeordneten Elemente aufweisen.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_UNCLASSIFIEDINKNODE"></span><span id="guid_cnt_unclassifiedinknode"></span><dl> <dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt> <dt>(unclassimeedink)</dt> </dl></td>
<td style="text-align: left;">Stellt einen Knoten für alle Striche dar, die noch nicht klassifiziert oder erkannt wurden.<br/> Ein nicht klassifizierter Ink-Knoten darf keine untergeordneten Elemente aufweisen.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu den verschiedenen Kontext Knoten Typen finden Sie unter [Übersicht](ink-analysis-overview.md)über die Ink-Analyse.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                           |
| Header<br/>                   | <dl> <dt>Iaguid. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontextnode:: kreatepartiallypopulatedsubnode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**Icontextnode:: "kreatesubnode"**](icontextnode-createsubnode.md)
</dt> <dt>

[**Icontextnode:: GetType**](icontextnode-gettype.md)
</dt> <dt>

[**Iinkanalyzer:: feateanalysishint-Methode**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**Iinkanalyzer:: kreatecustomerkenzer-Methode**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[**Iinkanalyzer:: findnodesoft ype-Methode**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**Iinkanalyzer:: findnodesoft ypeer forstrokes-Methode**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**Iinkanalyzer:: findnodesoft ypeinsubtree-Methode**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




