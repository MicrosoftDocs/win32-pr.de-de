---
description: Legt das Renderzielformat für die Medien-Engine fest.
ms.assetid: 70FFDD44-9FDE-4D86-AD65-60019AC4A2BC
title: MF_MEDIA_ENGINE_VIDEO_OUTPUT_FORMAT-Attribut (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaa0dab3c3ea1c9ce23d767458df0b68a9b3c787f80ca1af786061536343a356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973729"
---
# <a name="mf_media_engine_video_output_format-attribute"></a>MF \_ MEDIA ENGINE VIDEO OUTPUT \_ \_ \_ \_ FORMAT-Attribut

Legt das Renderzielformat für die Medien-Engine fest.

## <a name="data-type"></a>Datentyp

**DXGI \_ ALS** **UINT32** gespeichertes FORMAT

## <a name="remarks"></a>Hinweise

Legen Sie dieses Attribut fest, wenn Sie die Medien-Engine im Frameservermodus erstellen. Weitere Informationen finden Sie unter [**ÜBERMEDIAMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance). Der Wert des Attributs ist ein [DXGI \_ FORMAT-Wert.](../direct3d9/d3dformat.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
