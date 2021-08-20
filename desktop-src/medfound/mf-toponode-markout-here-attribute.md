---
description: Gibt an, ob die Pipeline mark-out auf diesen Knoten anwendet. Mark-out ist der Punkt, an dem eine Präsentation endet. Wenn Pipelinekomponenten Daten über den Mark-Out-Punkt hinaus generieren, werden die Daten nicht gerendert.
ms.assetid: adf2361a-90c7-4650-a486-5c450a41ab54
title: MF_TOPONODE_MARKOUT_HERE-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d7196fd9f0ccc342672b609ce32d922d091a3f962ef9dd8e9dcdd4077c34a87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117691121"
---
# <a name="mf_toponode_markout_here-attribute"></a>MF \_ TOPONODE \_ MARKOUT \_ HERE-Attribut

Gibt an, ob die Pipeline mark-out auf diesen Knoten anwendet. Mark-out ist der Punkt, an dem eine Präsentation endet. Wenn Pipelinekomponenten Daten über den Mark-Out-Punkt hinaus generieren, werden die Daten nicht gerendert.

## <a name="data-type"></a>Datentyp

**UINT32**

Als boolescher Wert behandeln.

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für alle Knotentypen.

Wenn dieses Attribut **TRUE** ist, entfernt die Media Foundation Pipeline die Ausgabebeispiele von diesem Knoten entsprechend der Beendigungszeit für die Präsentation. Das Topologieladeprogramm legt dieses Attribut beim Auflösen einer Topologie fest. Die meisten Anwendungen müssen dieses Attribut nicht festlegen oder abrufen.

Es wird empfohlen, dass für genau einen Knoten in jedem Branch der Topologie dieses Attribut auf TRUE festgelegt **ist.** Ein Topologiezweig wird als Pfad von einem Quellknoten zu einem Ausgabeknoten definiert. Innerhalb eines Branchs müssen die Attribute MF \_ TOPONODE \_ MARKOUT \_ HERE und MF [ \_ TOPONODE \_ MARKIN \_ HERE](mf-toponode-markin-here-attribute.md) auf demselben Knoten im Branch festgelegt werden. Sie können nicht auf verschiedenen Knoten innerhalb desselben Branchs festgelegt werden.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**DENKattribute::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**TOPOLOGYNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**MF \_ TOPONODE \_ MARKIN \_ HIER**](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> </dl>

 

 




