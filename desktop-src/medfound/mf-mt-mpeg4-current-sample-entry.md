---
description: Gibt den aktuellen Eintrag im Feld für die Beispiel Beschreibung für einen MPEG-4-Medientyp an.
ms.assetid: c8c36abf-6905-4874-a6d2-90dd0725421b
title: MF_MT_MPEG4_CURRENT_SAMPLE_ENTRY-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c1f2a43eef1a520a49f5cfbb889f13149fa249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362608"
---
# <a name="mf_mt_mpeg4_current_sample_entry-attribute"></a>"MF \_ MT \_ MPEG4 \_ Current \_ Sample Entry \_ "-Attribut

Gibt den aktuellen Eintrag im Feld für die Beispiel Beschreibung für einen MPEG-4-Medientyp an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Bemerkungen

In einer MP4-oder 3GP-Datei beschreibt das Feld Beispiel Beschreibung die Codierung, die für einen Datenstrom in der Datei verwendet wird. Das Feld für die Beispiel Beschreibung kann mehrere Einträge enthalten. Dieses Attribut gibt an, welcher Eintrag verwendet werden soll. Der Wert ist ein NULL basierter Index in der Liste.

Derzeit ist der einzige unterstützte Wert 0. Das-Attribut wurde für die spätere Erweiterbarkeit definiert.

Die MPEG-4-Datei Quelle legt den Wert immer auf 0 fest. Die MP4-und 3GP-Datei senken ignorieren den Wert dieses Attributs, wenn dieser vorhanden ist.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> <dt>

[\_ \_ \_ Beispiel Beschreibung für MF MT MPEG4 \_](mf-mt-mpeg4-sample-description.md)
</dt> </dl>

 

 




