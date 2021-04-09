---
description: Der Media Foundation DV-Video Decoder ist eine Media Foundation Transformation, die das DV-Video decodiert.
ms.assetid: 97e5ba52-92fc-49e4-9c22-6f61bfda2003
title: DV-Video Decoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed277c3e4dd1aaa031d4dcf4694c7c3051fe37ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749257"
---
# <a name="dv-video-decoder"></a>DV-Video Decoder

Der Media Foundation DV-Video Decoder ist eine [Media Foundation Transformation](media-foundation-transforms.md) , die das DV-Video decodiert.

Der DV-Video Decoder unterstützt die folgenden Eingabetypen:



| Subtype                 | BESCHREIBUNG                  |
|-------------------------|------------------------------|
| **MF-Format ( \_ DVC)**  | DVC/DV-Video                 |
| **MF-Format ( \_ dvhd)** | HD-dvcr (1125-60 oder 1250-50) |
| **MF-Format ( \_ DVSD)** | SDL-dvcr (525-60 oder 625-50)  |
| **MF-Format \_ dvsl** | SD-dvcr (525-60 oder 625-50)   |



 

Es unterstützt einen einzelnen Ausgabetyp:



| Subtype             | BESCHREIBUNG |
|---------------------|-------------|
| MF-Format \_ im YUY2 | Im YUY2-Video  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                |
| DLL<br/>                      | <dl> <dt>Mfdvdec.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Video Medientypen](video-media-types.md)
</dt> </dl>

 

 




