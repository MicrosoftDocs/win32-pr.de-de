---
description: Definiert Werte, die die Eigenschaften einer Erkennungs Alternative angeben. Die Tablet PC-API (Application Programming Interface) verwendet Global Unique Bezeichner (GUIDs), um Paket Eigenschaften zu identifizieren, die in Automation Konstante Zeichen folgen sind.
ms.assetid: 2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8
title: Erkentionproperty-Konstanten (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62971276b6348af3d8ac971851d70b03f7b003c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348638"
---
# <a name="recognitionproperty-constants"></a>Erkentionproperty-Konstanten

Definiert Werte, die die Eigenschaften einer Erkennungs Alternative angeben. Die Tablet PC-API (Application Programming Interface) verwendet Global Unique Bezeichner (GUIDs), um Paket Eigenschaften zu identifizieren, die in Automation Konstante Zeichen folgen sind.

In der folgenden Tabelle sind die verfügbaren Eigenschaften der alternativen Erkennungs Eigenschaft Globally Unique Identifier (GUID) aufgelistet. Verwenden Sie diese GUIDs, um auf Eigenschaften eines [**iinkrecognitionalternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) -Objekts zuzugreifen, indem Sie die [**GetPropertyValue**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue) -Methode aufrufen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstantenname</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINENUMBER_________"></span><span id="___________inkrecognitionproperty_linenumber_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong></dt> </dl></td>
<td style="text-align: left;">Der GUID, der die Eigenschaft für die Zeilennummer des <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>iinkrecognitionalternate</strong></a> -Objekts identifiziert. <br/> LineNumber gibt die Alternativen zu einer bestimmten Zeilennummer an.<br/>
<blockquote>
[!Note]<br />
Dieses Feld wird für Erkennungs Modul von ostasiatischen Zeichen nicht unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_SEGMENTATION_________"></span><span id="___________inkrecognitionproperty_segmentation_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong></dt> </dl></td>
<td style="text-align: left;">Der GUID, der die Eigenschaft für die Segmentierung des <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>iinkrecognitionalternate</strong></a> -Objekts identifiziert. <br/> Segmentierung gibt das grundlegende Freihand Fragment oder die Einheit an, die die Erkennung verwendet, um ein Erkennungs Ergebnis zu erhalten.<br/>
<blockquote>
[!Note]<br />
Nicht implementiert.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_HOTPOINT_________"></span><span id="___________inkrecognitionproperty_hotpoint_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong></dt> </dl></td>
<td style="text-align: left;">Der GUID, der die Eigenschaft für den Erkennungs-Hot Point des <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>iinkrecognitionalternate</strong></a> -Objekts identifiziert. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT_________"></span><span id="___________inkrecognitionproperty_maximumstrokecount_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong></dt> </dl></td>
<td style="text-align: left;">Die GUID, die die Eigenschaft für die maximale Anzahl der Striche des Erkennungs Ergebnisses für das <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>iinkrecognitionalternate</strong></a> -Objekt identifiziert. <br/>
<blockquote>
[!Note]<br />
Nicht implementiert.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_POINTSPERINCH_________"></span><span id="___________inkrecognitionproperty_pointsperinch_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong></dt> </dl></td>
<td style="text-align: left;">Die GUID, die die Eigenschaft für die Metrik "Punkte pro Zoll" des <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>iinkrecognitionalternate</strong></a> -Objekts identifiziert. <br/>
<blockquote>
[!Note]<br />
Nicht implementiert.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_CONFIDENCELEVEL_________"></span><span id="___________inkrecognitionproperty_confidencelevel_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong></dt> </dl></td>
<td style="text-align: left;">Die GUID, die die Eigenschaft für die Vertrauens Ebene identifiziert, die die Erkennung im Erkennungs Ergebnis aufweist.<br/>
<blockquote>
[!Note]<br />
Die vertrauensbewertung ist nur für USA Englisch und alle Gesten Erkennungs Tools in Microsoft Windows XP Tablet PC Edition und Windows Vista verfügbar. Methoden, die die Eigenschaft Vertrauen für alle anderen Erkennungs Modul bereitstellen E_NOTIMPL zurückgeben.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINEMETRICS_________"></span><span id="___________inkrecognitionproperty_linemetrics_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong></dt> </dl></td>
<td style="text-align: left;">Die GUID, die die Eigenschaft für die linienmetriken des <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>iinkrecognitionalternate</strong></a> -Objekts identifiziert, d. h. die Zeile, für die Metriken abgerufen werden sollen. <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

In C++ können Sie auf diese Konstanten in der Header Datei "msink AUT. h" zugreifen, die sich im <systemdrive> \\ Verzeichnis "Programme \\ Microsoft SDKs \\ Windows \\ v 6.0 include" befindet, \\ Wenn Sie das SDK am Standard Speicherort installiert haben.

> [!Note]  
> In C++ sind diese Konstanten WCHARs, nicht bstrins. Konvertieren Sie diese vor der Verwendung in bstraus. Weitere Informationen zum BSTR-Datentyp finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Alternativen Methode (Alternativen withconstantpropertyvalues-Methode)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues)
</dt> <dt>

[**Conficealternativen-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidencealternates)
</dt> <dt>

[**Linealternativen (Eigenschaft)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates)
</dt> <dt>

[**Iinkrecognitionalternativen-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates)
</dt> </dl>

 

 




