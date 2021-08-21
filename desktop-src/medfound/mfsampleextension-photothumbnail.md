---
description: Enthält die Fotominiaturansicht eines NSAMPSamples.
ms.assetid: 510706A3-92FB-4188-97B9-6E8E0B4B175F
title: MFSampleExtension_PhotoThumbnail -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abb9fe5020428f1cb138b2d085a4715adb15bad3fa517fb4c3a605d60fa1ecc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872430"
---
# <a name="mfsampleextension_photothumbnail-attribute"></a>MFSampleExtension-Attribut \_ "PhotoThumbnail"

Enthält die Miniaturansicht des Fotos einer [**NSAMPSample-Datei.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="data-type"></a>Datentyp

**IUnknown als** **1.01.011111**

Die Miniaturansicht wird mithilfe von **KSPROPERTYSETID \_ ExtendedCameraControl konfiguriert.**

## <a name="remarks"></a>Hinweise

Dieses Attribut wird auf dem [**von**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) MFT0 bereitgestellten 10-00-MFTSample festgelegt und ist die [**IUnknown-Schnittstelle**](/windows/win32/api/unknwn/nn-unknwn-iunknown) des DER Fotominiaturminiatur zugeordneten [**ABERMEDIABuffer-Puffers.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)

Das Format der Fotominiaturansicht kann JPEG (Haupttypbild), NV12 oder ARGB32 sein.

[MFSampleExtension \_ PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md) ist erforderlich, damit Miniaturansichten den Medientyp beschreiben können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Desktop-Apps \| UWP-Apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**DURCHSCHN.Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> </dl>

 

 
