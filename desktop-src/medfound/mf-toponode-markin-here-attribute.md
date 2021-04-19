---
description: Gibt an, ob die Pipeline auf diesem Knoten ein Markierungszeichen anwendet.
ms.assetid: 406145e8-e00e-460d-b282-85face457605
title: MF_TOPONODE_MARKIN_HERE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa355cc070a7371ff2e294b3ca3ad558a4749b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348463"
---
# <a name="mf_toponode_markin_here-attribute"></a>Attribut "MF \_ toponode \_ Markin this" \_

Gibt an, ob die Pipeline auf diesem Knoten ein Markierungszeichen anwendet. Mark-in ist der Punkt, an dem eine Präsentation beginnt. Wenn Pipeline Komponenten Daten vor dem Markierungs Punkt generieren, werden die Daten nicht gerendert.

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die meisten Anwendungen müssen dieses Attribut nicht verwenden. Das Attribut wird bei Bedarf automatisch von der [Medien Sitzung](media-session.md) festgelegt.

 

Dieses Attribut gilt für alle Knoten Typen. Wenn das Attribut **true** ist, schneidet die Media Foundation Pipeline die Ausgabe Beispiele von diesem Knoten ab, sodass Sie mit der Startzeit der Präsentation identisch sind. Das topologielader legt dieses Attribut fest, wenn es eine Topologie auflöst.

Es wird empfohlen, dass für genau einen Knoten in jeder Verzweigung der Topologie dieses Attribut auf " **true**" festgelegt ist. Eine topologieverzweigung ist als Pfad von einem Quellknoten zu einem Ausgabe Knoten definiert. Innerhalb einer Verzweigung müssen die Attribute " [MF \_ toponode \_ markout \_ here](mf-toponode-markout-here-attribute.md) " und "MF \_ toponode \_ Markin \_ here" für denselben Knoten in der Verzweigung festgelegt werden. Sie können nicht auf verschiedenen Knoten innerhalb desselben branches festgelegt werden.

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

[**MF \_ toponode \_ markout \_ hier**](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> </dl>

 

 




