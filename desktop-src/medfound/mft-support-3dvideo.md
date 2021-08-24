---
description: Gibt an, ob eine Media Foundation-Transformation (MFT) 3D-Stereoaufzeichnungsvideo unterstützt.
ms.assetid: DE96FD14-5C7E-4560-99AC-B1EBDA1EBB2B
title: MFT_SUPPORT_3DVIDEO-Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da60bac92d1274f9d9a6624e247fc24d122ec26eabc103ad2d43477ae8f6b64b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776990"
---
# <a name="mft_support_3dvideo-attribute"></a>MFT \_ SUPPORT \_ 3DVIDEO-Attribut

Gibt an, ob eine Media Foundation-Transformation (MFT) 3D-Stereoaufzeichnungsvideo unterstützt.

## <a name="data-type"></a>Datentyp

**BOOL** als **UINT32** gespeichert

## <a name="remarks"></a>Hinweise

Um dieses Attribut abzufragen, rufen [**Sie ÜBERTRANSFORM::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) auf, um den globalen Attributspeicher des MFT abzurufen. Wenn **GetAttributes** erfolgreich ist, rufen Sie [**DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Der Standardwert dieses Attributs ist **FALSE.** Behandeln Sie dieses Attribut als schreibgeschützt. Ändern Sie den Wert nicht. Der MFT ignoriert alle Änderungen am Wert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




