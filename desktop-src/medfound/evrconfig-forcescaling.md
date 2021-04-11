---
description: Zwingt den erweiterten Videorenderer (EVR), das Video in einem Rechteck zu mischen, das kleiner als das Ausgabe Rechteck ist, und skaliert dann das Ergebnis.
ms.assetid: f85c4114-ac94-4deb-a1cf-896209079f8b
title: EVRConfig_ForceScaling-Attribut (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b82b7e017d414e86b8b4332fe5646e4808d4009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041547"
---
# <a name="evrconfig_forcescaling-attribute"></a>Evrconfig- \_ forcescaleing-Attribut

Zwingt den erweiterten Videorenderer (EVR), das Video in einem Rechteck zu mischen, das kleiner als das Ausgabe Rechteck ist, und skaliert dann das Ergebnis.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Dieses Attribut kann in der EVR-Medien Senke festgelegt werden. Zum Festlegen des-Attributs verwenden Sie **QueryInterface** , um die EVR-Medien Senke für die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle abzufragen.

Das Festlegen dieses Attributs hat dieselbe Auswirkung wie das Festlegen des Flags " **MF videorenderprefs \_ forcescaleing** " für den EVR. Eine Beschreibung dieses Flags finden Sie unter [**MF videorenderprefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) .

Die GUID-Konstante für dieses Attribut wird aus "straumiids. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>UUIDs. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[EVR-Attribute](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Video Qualitäts Verwaltung](video-quality-management.md)
</dt> </dl>

 

 




