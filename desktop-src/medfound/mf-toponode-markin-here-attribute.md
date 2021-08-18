---
description: Gibt an, ob die Pipeline mark-in auf diesen Knoten angewendet.
ms.assetid: 406145e8-e00e-460d-b282-85face457605
title: MF_TOPONODE_MARKIN_HERE -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c105dae6792e995e281309d2b693b78a0ec01e67c4412dc6d62056df09ebe9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874877"
---
# <a name="mf_toponode_markin_here-attribute"></a>MF \_ TOPONODE \_ MARKIN \_ HERE-Attribut

Gibt an, ob die Pipeline mark-in auf diesen Knoten angewendet. Mark-In ist der Punkt, an dem eine Präsentation beginnt. Wenn Pipelinekomponenten Daten vor dem Mark-In-Punkt generieren, werden die Daten nicht gerendert.

## <a name="data-type"></a>Datentyp

**UINT32**

Als boolescher Wert behandeln.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die meisten Anwendungen müssen dieses Attribut nicht verwenden. Die [Mediensitzung](media-session.md) legt dieses Attribut bei Bedarf automatisch fest.

 

Dieses Attribut gilt für alle Knotentypen. Wenn das Attribut **TRUE ist,** entfernt Media Foundation Pipeline die Ausgabebeispiele von diesem Knoten so, dass sie mit der Startzeit für die Präsentation übereinstimmen. Das Topologielader legt dieses Attribut fest, wenn es eine Topologie auflöset.

Es wird empfohlen, dass für genau einen Knoten in jedem Branch der Topologie dieses Attribut auf TRUE festgelegt **ist.** Ein Topologiezweig wird als Pfad von einem Quellknoten zu einem Ausgabeknoten definiert. Innerhalb einer Verzweigung müssen die [Attribute MF \_ TOPONODE \_ MARKOUT \_ HERE](mf-toponode-markout-here-attribute.md) und MF TOPONODE MARKIN HERE auf demselben Knoten \_ in der \_ \_ Verzweigung festgelegt werden. Sie können nicht auf verschiedenen Knoten innerhalb desselben Branchs festgelegt werden.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEs::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**TOPOLOGIENode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**MF \_ TOPONODE \_ MARKOUT \_ HIER**](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> </dl>

 

 




