---
description: Gibt an, ob ein Encoder in der transcodieren-Topologie enthalten sein muss.
ms.assetid: 73f23aed-d1b9-4821-b1ca-0a07f02b6913
title: MF_TRANSCODE_DONOT_INSERT_ENCODER-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92d3f8fc5dabfd3e4c55c6242ba9b8f52b6f5c2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348234"
---
# <a name="mf_transcode_donot_insert_encoder-attribute"></a>MF- \_ transcode- \_ Attribut zum Einfügen von \_ \_ Encodern

Gibt an, ob ein Encoder in der transcodieren-Topologie enthalten sein muss.

Die [**MF-atetranscodetopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) -Funktion überprüft dieses Attribut beim Aufbau der Topologie. Wenn dieses Attribut nicht festgelegt ist, wird ein Encoder in die transcodieren-Topologie eingefügt.

## <a name="data-type"></a>Datentyp

**UINT32**



| Wert                                                                        | Bedeutung                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Ein Encoder wird in die transcodieren-Topologie eingefügt.<br/>                                                      |
| <dl> <dt>1</dt> </dl> | Ein Encoder ist nicht in der transcodieren-Topologie enthalten. Der Quellknoten ist mit dem Ausgabe Knoten verbunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> </dl>

 

 




