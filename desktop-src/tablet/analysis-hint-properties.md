---
description: 'Definiert Global Unique Identifier (GUIDs) für Eigenschaften eines Analyse Hinweis Knotens (siehe icontextnode:: GetType).'
ms.assetid: 8300c792-a741-49de-a03b-f4840ea5d647
title: Eigenschaften des Analysis-Hinweises (iaguid. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AHP_ALLOWPARTIALDICTIONARYTERMS
- GUID_AHP_ANALYSISHINTNAME
- GUID_AHP_COERCETOFACTOID
- GUID_AHP_ENABLEDUNICODECHARACTERRANGES
- GUID_AHP_FACTOID
- GUID_AHP_GUIDE
- GUID_AHP_PREFIXTEXT
- GUID_AHP_SUFFIXTEXT
- GUID_AHP_TOPINKBREAKSONLY
- GUID_AHP_WORDLIST
- GUID_AHP_WORDMODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 8a7a25cfa94bb7f2354418ded2b35e3137364901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958638"
---
# <a name="analysis-hint-properties"></a>Eigenschaften des Analyse Hinweises

Definiert Global Unique Identifier (GUIDs) für Eigenschaften eines Analyse Hinweis Knotens (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)).

In der folgenden Tabelle werden die von den einzelnen Konstanten referenzierten Informationen beschrieben.



| Konstante                                                                                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AHP_ALLOWPARTIALDICTIONARYTERMS"></span><span id="guid_ahp_allowpartialdictionaryterms"></span><dl> <dt>**GUID \_ AHP \_ allowpartialdiktattionaryterms**</dt> </dl>       | Gibt an, ob partielle Wörterbuch Begriffe in einem Analyse Hinweis zulässig sind.<br/>                                                                              |
| <span id="GUID_AHP_ANALYSISHINTNAME"></span><span id="guid_ahp_analysishintname"></span><dl> <dt>**GUID \_ AHP \_ analysishintname**</dt> </dl>                                        | Der Name eines Analyse Hinweises.<br/>                                                                                                                  |
| <span id="GUID_AHP_COERCETOFACTOID"></span><span id="guid_ahp_coercetofactoid"></span><dl> <dt>**GUID \_ AHP \_ coercetofaktoid**</dt> </dl>                                           | Gibt an, ob der Ink Analyzer seine Analyse von frei Hand Eingaben innerhalb des Hinweis Bereichs auf das Faktoid beschränkt.<br/>                                          |
| <span id="GUID_AHP_ENABLEDUNICODECHARACTERRANGES"></span><span id="guid_ahp_enabledunicodecharacterranges"></span><dl> <dt>**GUID \_ AHP \_ enabledunicode~ terranges**</dt> </dl> | Der-Hinweis enthält ein Zeichen Array, das den eingeschränkten Satz von unterstützter Unicode-Zeichensätze darstellt, die von diesem InkRecognizer unterstützt werden.<br/> |
| <span id="GUID_AHP_FACTOID"></span><span id="guid_ahp_factoid"></span><dl> <dt>**GUID- \_ AHP- \_ Faktoid**</dt> </dl>                                                                   | Die Faktoid eines Analyse Hinweises.<br/>                                                                                                               |
| <span id="GUID_AHP_GUIDE"></span><span id="guid_ahp_guide"></span><dl> <dt>**GUID- \_ AHP- \_ Leitfaden**</dt> </dl>                                                                         | Die [**inkanalysiserkenzerguide**](inkanalysisrecognizerguide.md) -Struktur, die den Leitfaden für einen Analyse Hinweis darstellt.<br/>                 |
| <span id="GUID_AHP_PREFIXTEXT"></span><span id="guid_ahp_prefixtext"></span><dl> <dt>**GUID \_ AHP \_ PrefixText**</dt> </dl>                                                          | Der Präfix Text eines Analyse Hinweises.<br/>                                                                                                           |
| <span id="GUID_AHP_SUFFIXTEXT"></span><span id="guid_ahp_suffixtext"></span><dl> <dt>**GUID- \_ AHP- \_ SuffixText**</dt> </dl>                                                          | Der Suffixtext eines Analyse Hinweises.<br/>                                                                                                           |
| <span id="GUID_AHP_TOPINKBREAKSONLY"></span><span id="guid_ahp_topinkbreaksonly"></span><dl> <dt>**GUID \_ AHP \_ TopInkBreaksOnly**</dt> </dl>                                        | Gibt an, ob die mehrere Segmentationen in den frei Hand Erkennungs Ergebnissen deaktiviert sind.<br/>                                                                |
| <span id="GUID_AHP_WORDLIST"></span><span id="guid_ahp_wordlist"></span><dl> <dt>**GUID- \_ AHP- \_ WordList**</dt> </dl>                                                                | Das Zeichen folgen Array, das die Wortliste für einen Analyse Hinweis darstellt.<br/>                                                                       |
| <span id="GUID_AHP_WORDMODE"></span><span id="guid_ahp_wordmode"></span><dl> <dt>**GUID- \_ AHP- \_ wordmode**</dt> </dl>                                                                | Gibt an, ob die frei Hand Analyseergebnisse von einzelnen Wörtern für einen Analyse Hinweis auf Ergebnisse mit mehreren Wörtern priorisiert.<br/>                                      |



## <a name="remarks"></a>Bemerkungen

Diese GUIDs werden verwendet, um Eigenschaften zu identifizieren, die von [**iinkanalyzer**](iinkanalyzer.md) für einen Kontext Knoten des Analyse Hinweises festgelegt werden können (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)).

Informationen zum Anzeigen oder Festlegen von Eigenschaften eines [**icontextnode**](icontextnode.md) im Allgemeinen finden Sie unter [Kontext Knoten Eigenschaften](context-node-properties.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                           |
| Header<br/>                   | <dl> <dt>Iaguid. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kontext Knoten Eigenschaften](context-node-properties.md)
</dt> <dt>

[Kontext Knoten Typen](context-node-types.md)
</dt> <dt>

[**Iinkanalyzer:: feateanalysishint-Methode**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**Iinkanalyzer:: getanalysishintsbyname-Methode**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[**Icontextnode:: ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**Icontextnode:: GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**Icontextnode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**Icontextnode:: loadpropertiesdata**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**Icontextnode:: RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**Icontextnode:: savepropertiesdata**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




