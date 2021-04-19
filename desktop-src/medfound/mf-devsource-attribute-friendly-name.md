---
description: Gibt den anzeigen Amen für ein Gerät an.
ms.assetid: 3f6c7faf-2ecd-4510-adc2-252c3619d70f
title: MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab0d2bb3c0e75d547e1249a83261b7c804743ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345147"
---
# <a name="mf_devsource_attribute_friendly_name-attribute"></a>Attribut Anzeige Name für das MF- \_ devsource- \_ Attribut \_ \_

Gibt den anzeigen Amen für ein Gerät an. Der *Anzeige Name* ist eine lesbare Zeichenfolge, die für die Anzeige in einer Benutzeroberfläche geeignet ist.

## <a name="data-type"></a>Datentyp

**WCHAR \** _

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: GetString* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird für die Aktivierungs Objekte festgelegt, die von den folgenden Funktionen zurückgegeben werden:

-   [**MF | atedevicesourceaktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**Mfenumschlag**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

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

 

 




