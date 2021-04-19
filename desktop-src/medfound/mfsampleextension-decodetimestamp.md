---
description: Enthält den decodierungszeit Stempel (DTS) für das Beispiel.
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: MFSampleExtension_DecodeTimestamp-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9676b295eb16e7cb2bb607ef4a5074d24b276d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360134"
---
# <a name="mfsampleextension_decodetimestamp-attribute"></a>MF Sample Extension- \_ decodetimestamp-Attribut

Enthält den decodierungszeit Stempel (DTS) für das Beispiel.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Bemerkungen

Der Wert des-Attributs ist der DTS in 100-Nanosecond-Einheiten. DTS ist in einigen Codierungsstandards definiert, einschließlich MPEG. Der DTS gibt an, wann das codierte Bild decodiert werden soll. Wenn das codierte Video b-Frames enthält, kann sich der DTS von der Präsentationszeit unterscheiden, da B-Bilder im Bitstream außerhalb der temporalen Reihenfolge erscheinen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Beispiel Attribute](sample-attributes.md)
</dt> </dl>

 

 




