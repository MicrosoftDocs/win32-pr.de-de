---
description: Gibt an, ob ein Deinterlacing-Videoframe aus dem oberen Feld oder dem unteren Feld abgeleitet wurde.
ms.assetid: 3710ab94-afb3-44d3-a680-b4a716810ec1
title: MFSampleExtension_DerivedFromTopField-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f90a67edf0b08337748bc118b0aa4ff024ec0ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349137"
---
# <a name="mfsampleextension_derivedfromtopfield-attribute"></a>MF SampleExtension \_ derivedfromtopfield-Attribut

Gibt an, ob ein Deinterlacing-Videoframe aus dem oberen Feld oder dem unteren Feld abgeleitet wurde. Dieses Attribut gilt für Medien Beispiele.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist nur für Deinterlacing-Beispiele gültig. Legen Sie dieses Attribut fest, wenn der Frame durch Interpolation eines der Felder deinstaliert wurde.

Wenn der Wert **true** ist, wurde das untere Feld aus dem oberen Feld interpoliert. Wenn der Wert **false** ist, wurde das obere Feld aus dem unteren Feld interpoliert.

Wenn das-Attribut nicht festgelegt ist, wurde der Frame nicht deinstalterlacing. Der Frame ist entweder ein echter progressiver Frame, oder es handelt sich um einen verschachtelten Frame.

Dieses Attribut dient nur zu Informationszwecken. Ein Software-Deinterlacer konnte dieses Attribut festlegen. Wenn dieses Attribut festgelegt ist, gibt es einen Hinweis, dass Sie das ursprüngliche Feld wiederherstellen können, indem Sie die interpoliert-Scan Zeilen ablegen. Wenn das Attribut z. b. **true** ist, können Sie das ursprüngliche obere Feld Wiederherstellen, indem Sie das interpoliert untere Feld ablegen.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Beispiel Attribute](sample-attributes.md)
</dt> <dt>

[Medien Beispiele](media-samples.md)
</dt> <dt>

[Video-Interlacing](video-interlacing.md)
</dt> </dl>

 

 




