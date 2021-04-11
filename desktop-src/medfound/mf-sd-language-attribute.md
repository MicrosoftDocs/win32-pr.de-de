---
description: Gibt die Sprache für einen Datenstrom an.
ms.assetid: b64a9554-a560-4212-8964-b68ebbadc046
title: MF_SD_LANGUAGE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad13ec4d7d17e715bd2583e499c686de26c7b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217540"
---
# <a name="mf_sd_language-attribute"></a>MF \_ SD- \_ sprach Attribut

Gibt die Sprache für einen Datenstrom an.

## <a name="data-type"></a>Datentyp

Breitzeichenfolge

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein RFC 1766-kompatibles Sprachtag. Dieses Attribut gilt für streamdeskriptoren.

Eine Medienquelle (oder ein beliebiges Objekt, das einen streamdeskriptor erstellt) kann dieses Attribut festlegen, wenn der Stream eine bestimmte Sprache hat. Anwendungen können dieses Attribut Abfragen, um die Sprache zu erhalten. Wenn das-Attribut nicht festgelegt ist, hat der Stream keine bestimmte Sprache.

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

[**Imfattributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**Imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMF-Deskriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Streamdeskriptorattribute](stream-descriptor-attributes.md)
</dt> </dl>

 

 




