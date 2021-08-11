---
description: Identifiziert den Topologieknoten für eine Streamsenke.
ms.assetid: 9aa6ca66-5122-4d05-94b9-32be194e9eb3
title: MF_EVENT_OUTPUT_NODE -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b2cbcbc243c195deb1061417adb6d93271b328fa242b497a7fdb232f5f7695e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244709"
---
# <a name="mf_event_output_node-attribute"></a>MF \_ EVENT \_ OUTPUT \_ NODE-Attribut

Identifiziert den Topologieknoten für eine Streamsenke.

## <a name="data-type"></a>Datentyp

**UINT64**

Als [**TOPOID behandeln.**](topoid.md)

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist ein Knotenbezeichner für einen Ausgabeknoten in der aktuellen Topologie. Um einen Zeiger auf den zugeordneten Knoten zu erhalten, rufen Sie [**DIE TOPOLOGIE::GetNodeByID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) in der Topologie auf.

Dieses Attribut wird mit den folgenden Ereignissen verwendet:

-   [MESessionStreamSinkFormatChanged](mesessionstreamsinkformatchanged.md)
-   [MESinkInvalidated](mesinkinvalidated.md)

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Ereignisattribute](event-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**ATTRIBUTEs::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




