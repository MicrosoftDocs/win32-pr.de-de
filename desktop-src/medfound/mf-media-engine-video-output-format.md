---
description: Legt das Renderziel-Format für die Medien-Engine fest.
ms.assetid: 70FFDD44-9FDE-4D86-AD65-60019AC4A2BC
title: MF_MEDIA_ENGINE_VIDEO_OUTPUT_FORMAT-Attribut (MF mediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 004025da1ad5258e5b04a3afba4a359f50f7444c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761385"
---
# <a name="mf_media_engine_video_output_format-attribute"></a>Format Attribut der MF- \_ Medien-Engine- \_ \_ Video \_ Ausgabe \_

Legt das Renderziel-Format für die Medien-Engine fest.

## <a name="data-type"></a>Datentyp

**DXGI \_** Als **UInt32** gespeicherter Format

## <a name="remarks"></a>Bemerkungen

Legen Sie dieses Attribut fest, wenn Sie die Medien-Engine im Frame Server Modus erstellen. Weitere Informationen finden Sie unter [**IMF mediaengineclassfactory:: forateinstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance). Der Wert des-Attributs ist ein [DXGI- \_ Format](../direct3d9/d3dformat.md) Wert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>MF mediaengine. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
