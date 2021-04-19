---
description: Gibt an, ob der Bildstream in einer Video Erfassungs Quelle unabhängig vom Videostream ist.
ms.assetid: DC4ED612-593B-40BF-BB42-946149042D1F
title: MF_DEVICESTREAM_INDEPENDENT_IMAGE_STREAM-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 174e62a1bdd178ad2d8dce7fab5bf9ce3104d834
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353196"
---
# <a name="mf_devicestream_independent_image_stream-attribute"></a>Das MF- \_ Attribut "devicestream \_ Independent \_ Image \_ Stream"

Gibt an, ob der Bildstream in einer Video Erfassungs Quelle unabhängig vom Videostream ist.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="remarks"></a>Bemerkungen

Einige USB-Videokameras machen einen Stream verfügbar, der weiterhin Bilder erzeugt. In einigen Kameras gibt der Bildstream einfach den nächsten Frame aus dem Videostream zurück. In anderen Kameras funktioniert der Bildstream unabhängig vom Videostream. Wenn die Kamera über einen unabhängigen Bildstream verfügt, legt die Medienquelle für das Erfassungsgerät dieses Attribut für den Bildstream auf **true** fest.

Gehen Sie folgendermaßen vor, um dieses Attribut zu erhalten:

1.  Fragen Sie die Medienquelle für die [**imfmediasourceex**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) -Schnittstelle ab.
2.  Aufrufen von [**imfmediasourceex:: getstreamattributs**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) , um einen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger für den Stream zu erhalten.
3.  Zum Abrufen des Attributs muss [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) aufgerufen werden.

Dieses Attribut gilt nur, wenn das MF-Attribut " [ \_ devicestream \_ Image \_ Stream](mf-devicestream-image-stream.md) " den Wert **true** hat.

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

 

 




