---
description: Identifiziert den topologieknoten für eine streamsenke.
ms.assetid: 9aa6ca66-5122-4d05-94b9-32be194e9eb3
title: MF_EVENT_OUTPUT_NODE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c484ea55841f4057bf0855dd51b90db951acb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354600"
---
# <a name="mf_event_output_node-attribute"></a>\_Attribut für \_ Ausgabe \_ Knoten des MF-Ereignisses

Identifiziert den topologieknoten für eine streamsenke.

## <a name="data-type"></a>Datentyp

**UINT64**

Als [**topoid**](topoid.md)behandeln.

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein Knoten Bezeichner für einen Ausgabe Knoten in der aktuellen Topologie. Um einen Zeiger auf den zugeordneten Knoten abzurufen, nennen Sie [**imftopology:: getNodeById**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) für die Topologie.

Dieses Attribut wird mit den folgenden Ereignissen verwendet:

-   [Mesessionstreamsinkformatchanged](mesessionstreamsinkformatchanged.md)
-   [Mesinkinvalidieren](mesinkinvalidated.md)

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Ereignisattribute](event-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**Imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




