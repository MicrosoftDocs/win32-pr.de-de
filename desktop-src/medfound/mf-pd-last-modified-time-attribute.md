---
description: Gibt an, wann eine Präsentation zuletzt geändert wurde.
ms.assetid: 12990de2-7656-4781-943b-c46f42a0e38d
title: MF_PD_LAST_MODIFIED_TIME-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f97bf47cff32834b694f36cbd4c9062e06f2d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960091"
---
# <a name="mf_pd_last_modified_time-attribute"></a>\_Zeit Attribut für die \_ Letzte \_ Änderung \_ der MF-PD

Gibt an, wann eine Präsentation zuletzt geändert wurde.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Bemerkungen

Medienquellen können dieses Attribut für einen Präsentations Deskriptor festlegen. Der Wert des-Attributs ist eine **FILETIME** -Struktur, die in der Windows SDK dokumentiert ist.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Präsentations deskriptorattribute](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




