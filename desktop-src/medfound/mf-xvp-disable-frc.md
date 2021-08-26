---
description: Deaktiviert die Bildfrequenzkonvertierung im Videoprozessor-MFT.
ms.assetid: 98AA7B3A-281C-427D-805E-5C4EE1EFAE21
title: MF_XVP_DISABLE_FRC -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e82c60438a91111ffce6cc80c71fa76231b8e00d85644f4f56f1b496202d62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940330"
---
# <a name="mf_xvp_disable_frc-attribute"></a>MF \_ XVP \_ DISABLE \_ FRC-Attribut

Deaktiviert die Bildfrequenzkonvertierung im [**Videoprozessor-MFT.**](video-processor-mft.md)

## <a name="data-type"></a>Datentyp

**BOOL als** **UINT32 gespeichert**

## <a name="remarks"></a>Hinweise

Wenn dieses Attribut **TRUE ist,** führt der Videoprozessor keine Konvertierung der Bildfrequenz durch. Standardmäßig konvertiert der Videoprozessor die Bildfrequenz in den Ausgabemedientyp.

So legen Sie dieses Attribut fest:

1.  Rufen [**Sie AUF DEM Videoprozessor DIETRANSFORM::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) auf.
2.  Rufen [**Sie DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

Legen Sie das Attribut fest, bevor das Streaming beginnt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




