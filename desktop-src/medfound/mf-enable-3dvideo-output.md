---
description: Gibt an, wie eine Media Foundation Transformation (MFT) einen Videodaten Strom mit 3D-Stereotyp ausgeben soll.
ms.assetid: AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39
title: MF_ENABLE_3DVIDEO_OUTPUT-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0123a574ec74ed4aa9fa0aea3b2cabecbb29da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863591"
---
# <a name="mf_enable_3dvideo_output-attribute"></a>MF \_ \_ -Attribut "3dvideo-Ausgabe" aktivieren \_

Gibt an, wie eine Media Foundation Transformation (MFT) einen Videodaten Strom mit 3D-Stereotyp ausgeben soll.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Der Wert des-Attributs ist ein Member der [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) -Enumeration.

Dieses Attribut ist nur gültig, wenn die MFT-Eigenschaft für das [ \_ \_ 3dvideo-Attribut der MFT-Unterstützung](mft-support-3dvideo.md) **true** zurückgibt

Zum Abrufen oder Festlegen dieses Attributs müssen Sie [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) aufrufen, um den globalen Attribut Speicher des MFT abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




