---
description: Gibt an, ob sich ein Stream mit anderen Streams desselben Typs gegenseitig ausschließt.
ms.assetid: 00a426ae-297c-4fcb-8132-d9c538bc9f1a
title: MF_SD_MUTUALLY_EXCLUSIVE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e3604eb9424bb646766f57261f745c57e18f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352402"
---
# <a name="mf_sd_mutually_exclusive-attribute"></a>\_ \_ Gegenseitig \_ Ausschließendes MF-Attribut

Gibt an, ob sich ein Stream mit anderen Streams desselben Typs gegenseitig ausschließt.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**IMF-Deskriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a>Bemerkungen

Wenn dieses Attribut **true** (ungleich null) ist, schließt sich der Stream mit anderen Streams desselben Typs, z. b. Audiodaten oder Videos, innerhalb derselben Präsentation gegenseitig aus. Wenn eine AVI-Datei z. b. mehrere Audiostreams enthält, werden Sie als gegenseitig ausschließende Datenströme gekennzeichnet, da jeweils nur ein Audiostream abgespielt werden soll.

Der Standardwert ist **FALSE**.

> [!Note]  
> Dieses Attribut wird nicht für ASF-Dateien (Advanced Systems Format) verwendet, die eine anspruchsvollere Methode zur Darstellung von gegenseitigen Ausschlusskriterien aufweisen. Weitere Informationen finden Sie unter [**imfasf mutualexclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion).

 

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Streamdeskriptorattribute](stream-descriptor-attributes.md)
</dt> </dl>

 

 




