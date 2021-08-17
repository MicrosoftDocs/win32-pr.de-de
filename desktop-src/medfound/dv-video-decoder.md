---
description: Der Media Foundation DV-Videodecoder ist eine Media Foundation Transform, die DV-Videos decodiert.
ms.assetid: 97e5ba52-92fc-49e4-9c22-6f61bfda2003
title: DV-Videodecoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd91cf325d9ba715d75aae884e29665d05d449ca39f01c195f9b13e2e1f8c1fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118064093"
---
# <a name="dv-video-decoder"></a>DV-Videodecoder

Der Media Foundation DV-Videodecoder ist eine [Media Foundation Transform,](media-foundation-transforms.md) die DV-Videos decodiert.

Der DV-Videodecoder unterstützt die folgenden Eingabetypen:



| Subtype                 | Beschreibung                  |
|-------------------------|------------------------------|
| **MFVideoFormat \_ DVC**  | DVC/DV-Video                 |
| **MFVideoFormat \_ DVHD** | HD-DVCR (1125-60 oder 1250-50) |
| **MFVideoFormat \_ DVSD** | SDL-DVCR (525-60 oder 625-50)  |
| **MFVideoFormat \_ DVSL** | SD-DVCR (525-60 oder 625-50)   |



 

Es wird ein einzelner Ausgabetyp unterstützt:



| Subtype             | Beschreibung |
|---------------------|-------------|
| MFVideoFormat \_ YUY2 | YUY2-Video  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                |
| DLL<br/>                      | <dl> <dt>Mfdvdec.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Videomedientypen](video-media-types.md)
</dt> </dl>

 

 




