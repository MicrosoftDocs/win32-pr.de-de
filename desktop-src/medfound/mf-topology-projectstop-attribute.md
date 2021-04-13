---
description: Gibt die Startzeit für eine Topologie relativ zum Anfang der ersten Topologie in der Sequenz an.
ms.assetid: 1ca3709e-88ea-40ca-8da4-c2259365122b
title: MF_TOPOLOGY_PROJECTSTOP-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5730791440131cd9efdbbb94ce15a598051f1e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528232"
---
# <a name="mf_topology_projectstop-attribute"></a>Das MF- \_ topologieprojectstoppattribut \_

Gibt die Startzeit für eine Topologie relativ zum Anfang der ersten Topologie in der Sequenz an.

## <a name="data-type"></a>Datentyp

**UINT64**

Als **Longlong** -Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Der Wert wird in Einheiten von 100 Nanosekunden angegeben.

Wenn die Medien Sitzung mit dem [**\_ \_ globalen \_ time**](mf-session-global-time-attribute.md) -Attribut der MF-Sitzung gleich **true** erstellt wurde, müssen alle Topologien das Projekt für die **MF- \_ Topologie \_ projectstoppt** enthalten. Andernfalls dürfen Topologien nicht das Projekt für die **MF- \_ Topologie \_ projectstoppt** enthalten. Weitere Informationen finden Sie unter [Sequenz Präsentations Zeiten](sequence-presentation-times.md).

Dieses Attribut ist ein Wert mit Vorzeichen, obwohl er als **UINT64** gespeichert wird.

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

[Sequenz Präsentations Zeiten](sequence-presentation-times.md)
</dt> <dt>

[Topologieattribute](topology-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**Imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**MF- \_ Topologie \_ ProjectStart**](mf-topology-projectstart-attribute.md)
</dt> </dl>

 

 




