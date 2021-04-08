---
description: Gibt an, ob ein Stream in einer Video Erfassungs Quelle ein Bild Datenstrom ist.
ms.assetid: 52251A45-3603-41C7-A869-7F6319BD337F
title: MF_DEVICESTREAM_IMAGE_STREAM-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 382ce587574d6ec46509a460dfb964e23dd416d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752448"
---
# <a name="mf_devicestream_image_stream-attribute"></a>MF- \_ devicestream \_ Image-Daten \_ Strom Attribut

Gibt an, ob ein Stream in einer Video Erfassungs Quelle ein Bild Datenstrom ist.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="remarks"></a>Bemerkungen

Einige Videokameras machen einen noch Bild Datenstrom verfügbar, der hochauflösende Bilder erzeugt. Der Bildstream erzeugt möglicherweise unkomprimierte Bilder oder JPEG-Bilder. Wenn die Kamera über einen Bildstream verfügt, legt die Medienquelle für das Erfassungsgerät dieses Attribut für den Bildstream auf **true** fest.

Gehen Sie folgendermaßen vor, um dieses Attribut zu erhalten:

1.  Fragen Sie die Medienquelle für die [**imfmediasourceex**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) -Schnittstelle ab.
2.  Aufrufen von [**imfmediasourceex:: getstreamattributs**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) , um einen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger für den Stream zu erhalten.
3.  Zum Abrufen des Attributs muss [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) aufgerufen werden.

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

 

 




