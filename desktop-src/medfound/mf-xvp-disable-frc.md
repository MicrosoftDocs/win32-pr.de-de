---
description: Deaktiviert die Frameraten Konvertierung in der MFT des Video Prozessors.
ms.assetid: 98AA7B3A-281C-427D-805E-5C4EE1EFAE21
title: MF_XVP_DISABLE_FRC-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1922705514c51308138f9f301a3681e598ca6278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959142"
---
# <a name="mf_xvp_disable_frc-attribute"></a>MF \_ xvp \_ - \_ Attribut "FRC deaktivieren"

Deaktiviert die Frameraten Konvertierung in der [**MFT des Video Prozessors**](video-processor-mft.md).

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="remarks"></a>Bemerkungen

Wenn dieses Attribut **true** ist, führt der Videoprozessor keine Frameraten Konvertierung durch. Standardmäßig konvertiert der Videoprozessor die Framerate entsprechend dem Ausgabe Medientyp.

So legen Sie dieses Attribut fest:

1.  Aufrufen von [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) für den Videoprozessor.
2.  Rückrufe [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

Legen Sie das-Attribut vor Beginn des Streamings fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




