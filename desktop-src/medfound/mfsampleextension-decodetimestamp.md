---
description: Enthält den Decodierungszeitstempel (DTS) für das Beispiel.
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: MFSampleExtension_DecodeTimestamp -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0d72ea69f487efe24148fa8ce60ad05eb7a124673f02a78e70c67f604a51bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241481"
---
# <a name="mfsampleextension_decodetimestamp-attribute"></a>MFSampleExtension \_ DecodeTimestamp-Attribut

Enthält den Decodierungszeitstempel (DTS) für das Beispiel.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Hinweise

Der Wert des Attributs ist der DTS in Einheiten von 100 Nanosekunden. Der DTS ist in einigen Codierungsstandards definiert, einschließlich MPEG. Der DTS gibt an, wann das codierte Bild decodiert werden soll. Wenn das codierte Video B-Frames enthält, kann sich der DTS von der Präsentationszeit unterscheiden, da B-Bilder nicht in temporaler Reihenfolge im Bitstream angezeigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Beispielattribute](sample-attributes.md)
</dt> </dl>

 

 




