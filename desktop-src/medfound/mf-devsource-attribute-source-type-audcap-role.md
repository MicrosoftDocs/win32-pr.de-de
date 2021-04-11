---
description: Gibt die Geräte Rolle für ein audioerfassungs-Gerät an.
ms.assetid: 4f2885b6-c771-4577-880d-5feea671432e
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148ae6697151698eef58d3c0148de3ed81822a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041960"
---
# <a name="mf_devsource_attribute_source_type_audcap_role-attribute"></a>MF \_ devsource \_ - \_ Attribut \_ Quelltyp ( \_ audcap- \_ Rollen Attribut)

Gibt die Geräte Rolle für ein audioerfassungs-Gerät an.

## <a name="data-type"></a>Datentyp

**Erole** als **UInt32** gespeichert

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Der **erole-Enumerationstyp** ist in der Dokumentation zur kernton-API dokumentiert.

Der Wert des-Attributs gibt eine Geräte Rolle an. Dieses Attribut wird mit den folgenden Funktionen verwendet.

Dieses Attribut kann als Eingabe für die Funktionen [**mfkreatedevicesource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) und [**mfkreatedevicesourceaktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) verwendet werden. Wenn das-Attribut angegeben wird, erstellt die Funktion eine Medienquelle, die das standardaudioerfassungs-Gerät für die angegebene Geräte Rolle verwendet.

Dieses Attribut kann auch als Eingabe für die [**mfenumschlag**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) -Funktion verwendet werden. Wenn das-Attribut angegeben wird, ist die-Enumeration auf die angegebene Geräte Rolle beschränkt. Außerdem enthält jedes Aktivierungs Objekt, das von der **mfenenumervicesources** -Funktion zurückgegeben wird, dieses Attribut. Das-Attribut wird dann intern vom Aktivierungs Objekt verwendet, wenn es die Medienquelle erstellt.

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

[Audio-/Videoaufzeichnung](audio-video-capture.md)
</dt> <dt>

[Geräte Attribute erfassen](capture-device-attributes.md)
</dt> </dl>

 

 




