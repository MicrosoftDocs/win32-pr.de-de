---
description: Gibt die Drehung eines Videoframes in richtung gegen den Uhrzeigersinn an.
ms.assetid: 7C0911A6-6D7C-4510-891F-A6F56CE1EC2B
title: MF_MT_VIDEO_ROTATION -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf3d909b29757a02d46cc842b30f04bfb0463d6f734eecb74bfb957fa206fb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876700"
---
# <a name="mf_mt_video_rotation-attribute"></a>MF \_ MT \_ VIDEO \_ ROTATION-Attribut

Gibt die Drehung eines Videoframes in richtung gegen den Uhrzeigersinn an.

## <a name="data-type"></a>Datentyp

Als **UINT32** **gespeichertes MFVideoRotationFormat**

## <a name="remarks"></a>Hinweise

Videos von einem Gerätegerät, z. B. einem Mobiltelefon, werden häufig um 90, 180 oder 270 Grad gedreht. Wenn die Kamera die Ausrichtung als Metadaten in der Videodatei speichert, kann das Bild zum Zeitpunkt der Wiedergabe angepasst werden.

Wenn dieses Attribut auf **MFVideoRotationFormat \_ 90** festgelegt ist, bedeutet dies, dass der Inhalt gegen den Uhrzeigersinn um 90 Grad gedreht wurde. Wenn der Inhalt im Uhrzeigersinn um 90 Grad gedreht würde, wäre der Attributwert **MFVideoRotationFormat \_ 270.**

Die unterstützten Werte für dieses Attribut werden im [**MFVideoRotationFormat aufzählt.**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat)

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientypen](media-types.md)
</dt> </dl>

 

 




