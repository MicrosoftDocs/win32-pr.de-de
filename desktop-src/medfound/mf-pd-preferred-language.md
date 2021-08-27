---
description: Enthält die bevorzugte RFC 1766-Sprache der Medienquelle.
ms.assetid: 30f99804-6aea-473b-9bbf-e8c715501391
title: MF_PD_PREFERRED_LANGUAGE -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cd01a47002bf3cd9419579786ff37df1fc03af940f54b2d2a2bb859d5b97007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740711"
---
# <a name="mf_pd_preferred_language-attribute"></a>MF \_ PD \_ PREFERRED \_ LANGUAGE-Attribut

Enthält die bevorzugte RFC 1766-Sprache der Medienquelle.

## <a name="data-type"></a>Datentyp

**Wchar**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DEN ATTRIBUTEAttributes::GetString auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::Settring auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)

## <a name="applies-to"></a>Gilt für:

[**BESCHRIFTungDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Hinweise

Das MF \_ PD \_ PREFERRED \_ LANGUAGE-Attribut ist optional. Eine Anwendung kann dieses Attribut für eine Medienquelle (z. B. eine Netzwerkquelle) festlegen, um die bevorzugte Sprache anzugeben.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server 2008 \[ \| R2-Desktop-Apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Präsentationsdeskriptorattribute](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




