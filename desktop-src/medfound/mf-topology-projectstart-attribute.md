---
description: Gibt die Beendigungszeit für eine Topologie relativ zum Start der ersten Topologie in der Sequenz an.
ms.assetid: 7669f97e-87ad-4a64-a2a5-62b8ce450d80
title: MF_TOPOLOGY_PROJECTSTART-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f295f68b3ac94bf29fa4607eb2b5ba00ea8eab19774bcaa0af150ef6d3fbe1f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875407"
---
# <a name="mf_topology_projectstart-attribute"></a>MF \_ TOPOLOGY \_ PROJECTSTART-Attribut

Gibt die Beendigungszeit für eine Topologie relativ zum Start der ersten Topologie in der Sequenz an.

## <a name="data-type"></a>Datentyp

**UINT64**

Als **LONGLONG-Wert** behandeln.

## <a name="remarks"></a>Hinweise

Der Wert wird in Einheiten von 100 Nanosekunden angegeben.

Wenn die Mediensitzung mit dem [**MF SESSION GLOBAL \_ \_ \_ TIME-Attribut**](mf-session-global-time-attribute.md) gleich **TRUE** erstellt wurde, müssen alle Topologien das **MF \_ TOPOLOGY \_ PROJECTSTART-Attribut** enthalten. Andernfalls dürfen Topologien nicht das **MF \_ TOPOLOGY \_ PROJECTSTART-Attribut** enthalten. Weitere Informationen finden Sie unter [Sequence Presentation Times](sequence-presentation-times.md).

Dieses Attribut ist ein Wert mit Vorzeichen, obwohl es als **UINT64** gespeichert ist.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Sequenzpräsentationszeiten](sequence-presentation-times.md)
</dt> <dt>

[Topologieattribute](topology-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**\_ \_ MF-TOPOLOGIEPROJEKTETOP**](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




