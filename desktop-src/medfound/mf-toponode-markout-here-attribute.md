---
description: Gibt an, ob die Pipeline auf diesem Knoten ein Markierungszeichen anwendet. Markierung ist der Punkt, an dem eine Präsentation endet. Wenn Pipeline Komponenten Daten über den Markierungs Punkt hinaus generieren, werden die Daten nicht gerendert.
ms.assetid: adf2361a-90c7-4650-a486-5c450a41ab54
title: MF_TOPONODE_MARKOUT_HERE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c5dc21f39f45aa04860f3374bead54d260f0821
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349063"
---
# <a name="mf_toponode_markout_here-attribute"></a>MF- \_ Attribut "toponode \_ markout \_ here"

Gibt an, ob die Pipeline auf diesem Knoten ein Markierungszeichen anwendet. Markierung ist der Punkt, an dem eine Präsentation endet. Wenn Pipeline Komponenten Daten über den Markierungs Punkt hinaus generieren, werden die Daten nicht gerendert.

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für alle Knoten Typen.

Wenn dieses Attribut **true** ist, schneidet die Media Foundation Pipeline die Ausgabe Beispiele von diesem Knoten ab, sodass Sie mit der Endzeit der Präsentation verglichen werden. Das topologielader legt dieses Attribut fest, wenn es eine Topologie auflöst. Die meisten Anwendungen müssen dieses Attribut nicht festlegen oder abrufen.

Es wird empfohlen, dass für genau einen Knoten in jeder Verzweigung der Topologie dieses Attribut auf " **true**" festgelegt ist. Eine topologieverzweigung ist als Pfad von einem Quellknoten zu einem Ausgabe Knoten definiert. Innerhalb einer Verzweigung müssen die \_ Attribute "MF toponode \_ markout \_ here" und " [MF \_ toponode \_ Markin \_ here](mf-toponode-markin-here-attribute.md) " für denselben Knoten in der Verzweigung festgelegt werden. Sie können nicht auf verschiedenen Knoten innerhalb desselben branches festgelegt werden.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**Imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**Hier finden Sie ein MF- \_ toponode- \_ Markin \_**](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> </dl>

 

 




