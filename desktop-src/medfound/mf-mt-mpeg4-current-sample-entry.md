---
description: Gibt den aktuellen Eintrag im Beispielbeschreibungsfeld für einen MPEG-4-Medientyp an.
ms.assetid: c8c36abf-6905-4874-a6d2-90dd0725421b
title: MF_MT_MPEG4_CURRENT_SAMPLE_ENTRY -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 660f74c1f9335556b514607cc2100f7ef59a00fba84f6cfe90412b91e1ff500a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877034"
---
# <a name="mf_mt_mpeg4_current_sample_entry-attribute"></a>MF \_ MT \_ MPEG4 CURRENT SAMPLE \_ \_ \_ ENTRY-Attribut

Gibt den aktuellen Eintrag im Beispielbeschreibungsfeld für einen MPEG-4-Medientyp an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**VERERBungstyp**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Hinweise

In einer MP4- oder 3GP-Datei beschreibt das Beispielbeschreibungsfeld die Codierung, die für einen Stream in der Datei verwendet wird. Das Beispielbeschreibungsfeld kann mehrere Einträge enthalten. Dieses Attribut gibt an, welcher Eintrag verwendet werden soll. Der Wert ist ein nullbasierter Index in der Liste.

Derzeit ist der einzige unterstützte Wert 0. Das -Attribut wurde für zukünftige Erweiterbarkeit definiert.

Die MPEG-4-Dateiquelle legt den Wert immer auf 0 fest. Die MP4- und 3GP-Dateisenken ignorieren den Wert dieses Attributs, wenn es vorhanden ist.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server 2008 \[ \| R2-Desktop-Apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> <dt>

[BESCHREIBUNG DES MF \_ MT \_ \_ MPEG4-BEISPIELS \_](mf-mt-mpeg4-sample-description.md)
</dt> </dl>

 

 




