---
description: Definiert Werte, die die Eigenschaften eines Erkennungswechsels angeben. Die Anwendungsprogrammierschnittstelle (Application Programming Interface, API) von Tablet PC verwendet GUIDs (Globally Unique Identifiers), um Paketeigenschaften zu identifizieren, bei denen es sich in Automation um konstante Zeichenfolgen handelt.
ms.assetid: 2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8
title: RecognitionProperty-Konstanten (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd18aeae50e0ae08337dd89a494292a7accbb389e6d02f0b990035fbf9644879
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856421"
---
# <a name="recognitionproperty-constants"></a>RecognitionProperty-Konstanten

Definiert Werte, die die Eigenschaften eines Erkennungswechsels angeben. Die Anwendungsprogrammierschnittstelle (Application Programming Interface, API) von Tablet PC verwendet GUIDs (Globally Unique Identifiers), um Paketeigenschaften zu identifizieren, bei denen es sich in Automation um konstante Zeichenfolgen handelt.

In der folgenden Tabelle sind die verfügbaren Felder für die Erkennung alternativer Eigenschaften mit global eindeutigem Bezeichner (Globally Unique Identifier, GUID) aufgeführt. Verwenden Sie diese GUIDs für den Zugriff auf Eigenschaften eines [**IInkRecognitionAlternate-Objekts,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) indem Sie die [**GetPropertyValue-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue) aufrufen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstantenname</th>
<th style="text-align: left;">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINENUMBER_________"></span><span id="___________inkrecognitionproperty_linenumber_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong></dt> </dl></td>
<td style="text-align: left;">Die GUID, die die Eigenschaft für die Zeilennummer des <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate-Objekts identifiziert.</strong></a> <br/> LineNumber gibt die Alternativen mit einer bestimmten Zeilennummer an.<br/>
<blockquote>
[!Note]<br />
Dieses Feld wird für die Erkennen ostasiatischer Zeichen nicht unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_SEGMENTATION_________"></span><span id="___________inkrecognitionproperty_segmentation_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong></dt> </dl></td>
<td style="text-align: left;">Die GUID, die die Eigenschaft für die Segmentierung des <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate-Objekts identifiziert.</strong></a> <br/> Segmentierung gibt das grundlegende Ink-Fragment oder die Basiseinheit an, das bzw. die die Erkennung verwendet, um ein Erkennungsergebnis zu erzeugen.<br/>
<blockquote>
[!Note]<br />
Nicht implementiert.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_HOTPOINT_________"></span><span id="___________inkrecognitionproperty_hotpoint_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong></dt> </dl></td>
<td style="text-align: left;">Die GUID, die die Eigenschaft für den Erkennungs-Hot Point des <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate-Objekts identifiziert.</strong></a> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT_________"></span><span id="___________inkrecognitionproperty_maximumstrokecount_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong></dt> </dl></td>
<td style="text-align: left;">Die GUID, die die Eigenschaft für die maximale Strichanzahl des Erkennungsergebnis für das <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate-Objekt identifiziert.</strong></a> <br/>
<blockquote>
[!Note]<br />
Nicht implementiert.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_POINTSPERINCH_________"></span><span id="___________inkrecognitionproperty_pointsperinch_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong></dt> </dl></td>
<td style="text-align: left;">Die GUID, die die Eigenschaft für die Punkt-pro-Zoll-Metrik des <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate-Objekts</strong></a> identifiziert. <br/>
<blockquote>
[!Note]<br />
Nicht implementiert.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_CONFIDENCELEVEL_________"></span><span id="___________inkrecognitionproperty_confidencelevel_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong></dt> </dl></td>
<td style="text-align: left;">Die GUID, die die Eigenschaft für die Vertrauensebene identifiziert, über die die Erkennung im Erkennungsergebnis verfügt.<br/>
<blockquote>
[!Note]<br />
Die Konfidenzauswertung ist nur für USA Englisch und alle Gestenerkennungen in Microsoft Windows XP Tablet PC Edition und Windows Vista verfügbar. Methoden, die die Vertrauenseigenschaft für alle anderen Recognizer bereitstellen, geben E_NOTIMPL.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINEMETRICS_________"></span><span id="___________inkrecognitionproperty_linemetrics_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong></dt> </dl></td>
<td style="text-align: left;">Die GUID, die die -Eigenschaft für die Zeilenmetriken des <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate-Objekts</strong></a> identifiziert. Dies ist die Zeile, für die Metriken abgerufen werden. <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Hinweise

In C++ können Sie auf diese Konstanten in der Headerdatei Msinkaut.h zugreifen, die sich im Verzeichnis : Programme <systemdrive> \\ Microsoft \\ SDKs Windows \\ \\ v6.0 \\ Include befindet, wenn Sie das SDK am Standardspeicherort installiert haben.

> [!Note]  
> In C++ sind diese Konstanten WCHARs, nicht BSTRs. Konvertieren Sie sie vor der Verwendung in BSTRs. Weitere Informationen zum BSTR-Datentyp finden Sie unter [Verwenden der COM-Bibliothek](using-the-com-library.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AlternatesWithConstantPropertyValues-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues)
</dt> <dt>

[**ConfidenceAlternates-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidencealternates)
</dt> <dt>

[**LineAlternates-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates)
</dt> <dt>

[**IInkRecognitionAlternates-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates)
</dt> </dl>

 

 




