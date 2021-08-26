---
description: Gibt an, wie Media Foundation -Transformation (MFT) einen 3D-Stereoaufzeichnungsvideostream ausgibt.
ms.assetid: AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39
title: MF_ENABLE_3DVIDEO_OUTPUT -Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed361ef53d628e0970ffa35f9920750c9d3b0f7efbe81a0ef8759e8ba00a45ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013170"
---
# <a name="mf_enable_3dvideo_output-attribute"></a>MF \_ ENABLE \_ 3DVIDEO \_ OUTPUT-Attribut

Gibt an, wie Media Foundation -Transformation (MFT) einen 3D-Stereoaufzeichnungsvideostream ausgibt.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Der Wert des Attributs ist ein Member der [**MF3DVideoOutputType-Enumeration.**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype)

Dieses Attribut gilt nur, wenn MFT **TRUE für** das [MFT SUPPORT \_ \_ 3DVIDEO-Attribut zurückgibt.](mft-support-3dvideo.md)

Um dieses Attribut zu erhalten oder zu festlegen, rufen [**Sie DIETRANSFORM::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) auf, um den globalen Attributspeicher des MFT zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




