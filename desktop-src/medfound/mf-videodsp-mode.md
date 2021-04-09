---
description: Legt den Verarbeitungsmodus der Videostabilisierung MFT fest.
ms.assetid: 0D49892A-8628-4F2B-B41B-51160A19DC9B
title: MF_VIDEODSP_MODE-Attribut (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88383e6bdd197e4912c660657eefa6b9e812fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130128"
---
# <a name="mf_videodsp_mode-attribute"></a>MF \_ videodsp \_ mode-Attribut

Legt den Verarbeitungsmodus der [**Videostabilisierung MFT**](video-stabilization-mft.md)fest.

## <a name="data-type"></a>Datentyp

**MF videodspmode** gespeichert als **UIINT32**

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein [**MF videodspmode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) -Enumerationswert. Dieses Attribut kann verwendet werden, um die Bildstabilisierung zu aktivieren oder zu deaktivieren, und kann für jedes Ausgabe Beispiel aktualisiert werden.

So legen Sie dieses Attribut fest:

1.  Aufrufen von [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) auf der Video Stabilisierungs-MFT, um einen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger zu erhalten.
2.  Zum Festlegen des-Attributs wird [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Videostabilisierung-MFT**](video-stabilization-mft.md)
</dt> </dl>

 

 




