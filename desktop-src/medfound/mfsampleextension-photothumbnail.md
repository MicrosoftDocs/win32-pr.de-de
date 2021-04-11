---
description: Enthält die Foto Miniaturansicht eines IMF Sample.
ms.assetid: 510706A3-92FB-4188-97B9-6E8E0B4B175F
title: MFSampleExtension_PhotoThumbnail-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cbdb6f79b1b1ee187677a7f1a7a7792acb10fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131116"
---
# <a name="mfsampleextension_photothumbnail-attribute"></a>MF SampleExtension- \_ photominiatur-Attribut

Enthält die Foto Miniaturansicht eines [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).

## <a name="data-type"></a>Datentyp

**IUnknown** als **imfmediabuffer** gespeichert

Die Miniaturansicht wird mithilfe von " **ksproperty\tid \_ extendedcameracontrol**" konfiguriert.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird für das [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) festgelegt, das von MFT0 bereitgestellt wird, und ist die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle des [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) , der der Foto Miniaturansicht zugeordnet ist.

Das Format der Foto Miniaturansicht kann JPEG (Major Type Image), NV12 oder ARGB32 sein.

[Mfsampleextension \_ photothumbnailmediatype](mfsampleextension-photothumbnailmediatype.md) ist für Miniaturansichten erforderlich, um den Medientyp zu beschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> </dl>

 

 
