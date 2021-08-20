---
description: Gibt die Startzeit für eine Topologie relativ zum Start der ersten Topologie in der Sequenz an.
ms.assetid: 1ca3709e-88ea-40ca-8da4-c2259365122b
title: MF_TOPOLOGY_PROJECTSTOP-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ab227f1fdcda99148be3106b2ea724578f30bd9fd83756cd3b9d16f46ef993
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875397"
---
# <a name="mf_topology_projectstop-attribute"></a>MF \_ TOPOLOGY \_ PROJECTSTOP-Attribut

Gibt die Startzeit für eine Topologie relativ zum Start der ersten Topologie in der Sequenz an.

## <a name="data-type"></a>Datentyp

**UINT64**

Als **LONGLONG-Wert** behandeln.

## <a name="remarks"></a>Hinweise

Der Wert wird in Einheiten von 100 Nanosekunden angegeben.

Wenn die Mediensitzung mit dem [**MF SESSION GLOBAL \_ \_ \_ TIME-Attribut**](mf-session-global-time-attribute.md) gleich **TRUE** erstellt wurde, müssen alle Topologien das **MF \_ TOPOLOGY \_ PROJECTSTOP-Attribut** enthalten. Andernfalls dürfen Topologien nicht das **MF \_ TOPOLOGY \_ PROJECTSTOP-Attribut** enthalten. Weitere Informationen finden Sie unter [Sequence Presentation Times](sequence-presentation-times.md).

Dieses Attribut ist ein Wert mit Vorzeichen, obwohl es als **UINT64** gespeichert ist.

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

[Sequenzpräsentationszeiten](sequence-presentation-times.md)
</dt> <dt>

[Topologieattribute](topology-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**\_ \_ MF-TOPOLOGIEPROJEKTSTART**](mf-topology-projectstart-attribute.md)
</dt> </dl>

 

 




