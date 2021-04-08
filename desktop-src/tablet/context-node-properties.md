---
description: Definiert Global Unique Identifier (GUIDs) für die Eigenschaften eines icontextnode.
ms.assetid: 14992253-c384-43c1-9465-e015ea2348db
title: Kontext Knoten Eigenschaften (iaguid. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_CNP_ALIGNMENTLEVEL
- GUID_CNP_ASCENDERS
- GUID_CNP_BASELINE
- GUID_CNP_CONFIDENCELEVEL
- GUID_CNP_CUSTOMRECOGNIZERID
- GUID_CNP_DESCENDERS
- GUID_CNP_MIDLINE
- GUID_CNP_NODEDATA
- GUID_CNP_RECOGNIZEDSTRING
- GUID_CNP_ROTATEDBOUNDINGBOX
- GUID_CNP_SEMANTICTYPE
- GUID_CNP_SHAPENAME
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 8eb1034516c62e2121f835951d1f04db5710d275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861771"
---
# <a name="context-node-properties"></a>Kontext Knoten Eigenschaften

Definiert Global Unique Identifier (GUIDs) für die Eigenschaften eines [**icontextnode**](icontextnode.md).

In der folgenden Tabelle werden die von den einzelnen Konstanten referenzierten Informationen beschrieben.



| Konstante                                                                                                                                                                                                 | BESCHREIBUNG                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_CNP_ALIGNMENTLEVEL"></span><span id="guid_cnp_alignmentlevel"></span><dl> <dt>**GUID \_ CNP \_ alignmentlevel**</dt> </dl>             | Die Ausrichtungs Ebene eines Absatzes.<br/>                                                                                                               |
| <span id="GUID_CNP_ASCENDERS"></span><span id="guid_cnp_ascenders"></span><dl> <dt>**GUID \_ CNP-Vorgänger \_**</dt> </dl>                            | Die Vorgänger eines frei Hand Worts.<br/>                                                                                                                     |
| <span id="GUID_CNP_BASELINE"></span><span id="guid_cnp_baseline"></span><dl> <dt>**GUID \_ CNP- \_ Baseline**</dt> </dl>                               | Die Baseline eines frei Hand Worts.<br/>                                                                                                                      |
| <span id="GUID_CNP_CONFIDENCELEVEL"></span><span id="guid_cnp_confidencelevel"></span><dl> <dt>**GUID \_ CNP \_ conficelevel**</dt> </dl>          | Der Vertrauensgrad in den Erkennungs Ergebnissen.<br/>                                                                                                  |
| <span id="GUID_CNP_CUSTOMRECOGNIZERID"></span><span id="guid_cnp_customrecognizerid"></span><dl> <dt>**GUID \_ CNP \_ customerkenzerid**</dt> </dl> | Der Bezeichner der benutzerdefinierten frei Handerkennung für einen benutzerdefinierten Erkennungs Knoten.<br/>                                                                         |
| <span id="GUID_CNP_DESCENDERS"></span><span id="guid_cnp_descenders"></span><dl> <dt>**GUID \_ CNP-Nachfolger \_**</dt> </dl>                         | Die Nachfolger eines frei Hand Worts.<br/>                                                                                                                    |
| <span id="GUID_CNP_MIDLINE"></span><span id="guid_cnp_midline"></span><dl> <dt>**GUID \_ CNP- \_ Mittellinie**</dt> </dl>                                  | Die Mittellinie eines frei Hand Worts.<br/>                                                                                                                       |
| <span id="GUID_CNP_NODEDATA"></span><span id="guid_cnp_nodedata"></span><dl> <dt>**GUID \_ CNP \_ Node Data**</dt> </dl>                               | Die Bilddaten oder Textdaten eines Bilds oder Textworts.<br/>                                                                                           |
| <span id="GUID_CNP_RECOGNIZEDSTRING"></span><span id="guid_cnp_recognizedstring"></span><dl> <dt>**GUID \_ CNP \_ erkenzedstring**</dt> </dl>       | Die erkannte Zeichenfolge.<br/>                                                                                                                            |
| <span id="GUID_CNP_ROTATEDBOUNDINGBOX"></span><span id="guid_cnp_rotatedboundingbox"></span><dl> <dt>**GUID \_ CNP \_ rotatedboundingbox**</dt> </dl> | Das gedrehte Begrenzungsfeld.<br/>                                                                                                                         |
| <span id="GUID_CNP_SEMANTICTYPE"></span><span id="guid_cnp_semantictype"></span><dl> <dt>**GUID \_ CNP \_ SemanticType**</dt> </dl>                   | Die-Eigenschaft enthält Informationen zu den semantischen Typen, die beim Definieren einer Anmerkung verwendet werden, z. b. ob es sich um eine Legende, einen Kommentar usw. handelt.<br/> |
| <span id="GUID_CNP_SHAPENAME"></span><span id="guid_cnp_shapename"></span><dl> <dt>**GUID \_ CNP \_ Shapename**</dt> </dl>                            | Der Form Name eines frei Handzeichen Knotens.<br/>                                                                                                            |



## <a name="remarks"></a>Bemerkungen

Diese GUIDs werden verwendet, um Eigenschaften zu identifizieren, die von [**iinkanalyzer**](iinkanalyzer.md) für einen [**icontextnode**](icontextnode.md)festgelegt werden können. Die Ink Analyzer legt einige Eigenschafts Daten basierend auf dem Typ des Kontext Knotens fest (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)).

Informationen zum Anzeigen oder festlegen spezifischer Eigenschaften für Analyse Hinweis Knoten finden Sie unter [**Analysis Hint Properties**](analysis-hint-properties.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                           |
| Header<br/>                   | <dl> <dt>Iaguid. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften des Analyse Hinweises](analysis-hint-properties.md)
</dt> <dt>

[Kontext Knoten Typen](context-node-types.md)
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

 

 




